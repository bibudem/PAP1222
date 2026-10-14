# Administrer le dépôt

*Guide destiné à l'administrateur du dépôt. Les consignes pour les équipes sont
dans le [README](README.md), celles de l'enseignant dans le
[guide de l'enseignant](GUIDE_ENSEIGNANT.md).*

Ce document décrit chaque fichier du dépôt, les réglages GitHub dont la chaîne
dépend, et les opérations à faire en début et en fin de session. Il existe pour
que le montage survive à la personne qui l'a mis en place.

> Le dépôt est public. N'écrivez ici ni mot de passe, ni secret, ni
> renseignement personnel.

---

## Vue d'ensemble

```
equipes.yml ──────────────┬──► Déployer le gabarit ──► equipes/equipe-NN/strategie_recherche.md
.github/gabarit/…  ───────┘        (sur demande)                     │
                                                                     │ l'équipe rédige sur sa branch
                                                                     ▼
                                                            pull request (la remise)
                                                                     │
                     contrôle « verification » ◄─────────────────────┤ à chaque commit
                     (renseignements personnels)                     │
                                                                     │ review de l'enseignant
                                                                     ▼
                                                              merge dans main
                                                                     │
equipes.yml ─────────────────────────────────────────► Production des PDF
(titre, cours, auteurs, licence)                                     │
                                                                     ▼
                                                    release « documents-finaux »
```

---

## Inventaire des fichiers

### À la racine

| Fichier | Rôle | Qui le modifie |
|---|---|---|
| `README.md` | Consignes pour les équipes : consentement, droit de refus, marche à suivre, règles, lexique. C'est la page d'accueil du dépôt. | L'administrateur |
| `GUIDE_ENSEIGNANT.md` | Consignes de correction pour l'enseignant : filtres, *review*, suggestions, fusion, récupération des PDF. | L'administrateur |
| `GUIDE_ADMINISTRATEUR.md` | Ce document. | L'administrateur |
| `GRILLE_CORRECTION.md` | Les douze critères d'évaluation du cours, avec leurs échelles et des questions de lecture. Se copie dans une *review*. | L'administrateur, à la demande de l'enseignant |
| `CORRESPONDANCE_GABARIT.md` | Explique le passage du classeur Excel au gabarit et les choix de conception. Contient les points encore à décider. | L'administrateur |
| `equipes.yml` | **Source unique de vérité.** Titre, cours, session, licence, mode de signature et liste des équipes avec leurs membres. Alimente les deux workflows. | L'administrateur seulement |
| `LICENSE` | Texte officiel de la licence CC BY 4.0, en anglais. | Personne |
| `equipes/equipe-NN/strategie_recherche.md` | Le fichier de travail de chaque équipe. Créé par le workflow « Déployer le gabarit ». | L'équipe, par sa *pull request* |

### Dans `.github/`

| Fichier | Rôle | Qui le modifie |
|---|---|---|
| `gabarit/strategie_recherche.md` | Le gabarit vierge copié dans chaque dossier d'équipe. Contient les consignes en commentaires HTML. | L'administrateur |
| `pull_request_template.md` | Le formulaire de remise, prérempli dans chaque *pull request* : identification et liste de vérification. | L'administrateur |
| `CODEOWNERS` | Désigne le réviseur obligatoire de toute modification. | L'administrateur |
| `workflows/controle-et-documents.yml` | Deux jobs : `verification` sur chaque *pull request*, et `document` après chaque fusion. | L'administrateur |
| `workflows/deployer-gabarit.yml` | Copie le gabarit dans les dossiers d'équipe et ouvre une *pull request*. Lancé à la main. | L'administrateur |

### Les liens entre les fichiers

- `equipes.yml` → `deployer-gabarit.yml` : la liste des équipes détermine les
  dossiers créés. Le workflow lit les lignes `equipe-NN:` **indentées de deux
  espaces** ; une autre indentation les rend invisibles.
- `equipes.yml` → `controle-et-documents.yml` : titre, cours, établissement,
  auteurs et licence de chaque page titre, et nom de chaque PDF.
- `.github/gabarit/strategie_recherche.md` → `controle-et-documents.yml` : un
  fichier d'équipe **identique octet pour octet** au gabarit est considéré
  comme vierge et ne produit pas de PDF. Toute modification du gabarit doit
  donc être suivie d'un redéploiement (voir plus bas).
- `controle-et-documents.yml` → *ruleset* : le nom du job `verification` est
  inscrit dans les contrôles exigés. Le renommer bloque toutes les fusions.
- `CODEOWNERS` → *ruleset* : la révision du propriétaire de code est exigée.
  Un propriétaire inexistant ou sans accès en écriture est ignoré **sans
  avertissement**.

---

## Ce que font les workflows

### `controle-et-documents.yml`

**Job `verification`** — sur chaque *pull request*, sans filtre de chemin.

1. Examine tous les fichiers `equipes/**/*.md` et refuse :
   - une suite de huit chiffres (matricule), après avoir neutralisé les PMID
     étiquetés, les DOI et les URL ;
   - une adresse courriel ;
   - un numéro de téléphone nord-américain.
2. Compare `equipes.yml` aux dossiers présents et émet des avertissements
   (⚠ jaunes) en cas d'incohérence. Ces avertissements ne bloquent rien.

**Job `document`** — après chaque *push* sur `main` qui touche `equipes/**`,
`equipes.yml` ou le workflow lui-même, ou sur demande (**Run workflow**).

1. Ignore les fichiers d'équipe identiques au gabarit.
2. Construit les métadonnées de chaque PDF à partir d'`equipes.yml`. La date
   est celle du dernier *commit* du fichier de l'équipe.
3. Produit les PDF avec pandoc et XeLaTeX. La mention de licence est injectée
   dans la page titre.
4. Dépose les PDF comme *artifact* (90 jours), puis **supprime et recrée** la
   release `documents-finaux` avec les PDF courants.

> La release ne contient jamais que l'état actuel de `main`. Un PDF disparaît
> de la release dès que le fichier de l'équipe redevient vierge.

### `deployer-gabarit.yml`

Lancé à la main : **Actions → Déployer le gabarit → Run workflow**.

- `ecraser: false` : n'installe le gabarit que dans les dossiers qui n'ont pas
  encore de fichier. Sans danger en cours de session.
- `ecraser: true` : remplace **tous** les fichiers d'équipe par le gabarit.
  Écrase le travail des équipes.

Le workflow n'écrit jamais dans `main` : il ouvre une *pull request* signée
`github-actions[bot]`, que l'administrateur relit et fusionne.

> **Cette pull request n'aura pas de contrôle `verification`.** GitHub ne
> déclenche aucun workflow pour un événement produit par le `GITHUB_TOKEN`
> (sauf `workflow_dispatch` et `repository_dispatch`). Le contrôle exigé
> restera en attente : il faut fusionner en contournant la règle, ce que
> seul un compte autorisé à le faire peut réaliser.

---

## Réglages GitHub hors du dépôt

Ces réglages ne sont pas versionnés. Ils sont décrits ici d'après les
commentaires des fichiers ; **à vérifier dans Settings** et à tenir à jour
dans ce document.

| Où | Réglage | Pourquoi |
|---|---|---|
| Settings → Rules → Rulesets | *Ruleset* sur `main` : *pull request* obligatoire, contrôle `verification` exigé, révision du propriétaire de code exigée | Personne n'écrit directement dans `main`, et rien n'est fusionné sans contrôle ni révision |
| Settings → Collaborators and teams | Étudiants : **Write**. Enseignant : **Write** au minimum | Write permet de créer une *branch* et d'ouvrir une *pull request* dans le dépôt |
| Settings → General → Pull Requests | **Automatically delete head branches** activé | Les *branches* des équipes disparaissent après la fusion |
| Settings → Actions → General → Workflow permissions | **Allow GitHub Actions to create and approve pull requests** activé | Sans ce réglage, « Déployer le gabarit » ne peut pas ouvrir sa *pull request* |

> Le dépôt a été transféré de `hugobibliothecarius` vers l'organisation
> `bibudem`. Pour un dépôt d'organisation, le réglage des permissions des
> workflows est hérité de l'organisation : si l'organisation l'interdit, il
> ne peut pas être activé pour le dépôt.

---

## Début de session

1. **Mettre à jour `equipes.yml`** : `session`, `cours` au besoin, et la liste
   des équipes.
2. **Recueillir le consentement écrit** de chaque étudiant à la publication
   sous son nom, sous licence CC BY. Prévoir la voie de remise non publique
   pour qui refuse.
3. **Inscrire les noms** dans `equipes.yml`, **une seule fois**, avant la
   première remise. L'historique Git est définitif : un nom inscrit y reste.
   Pour une équipe dont un membre refuse, laisser sa liste `membres` vide :
   son PDF signera « Équipe NN ». Le réglage `auteurs:` vaut pour tout le
   fichier, pas pour une équipe.
4. **Archiver la session précédente** si ce n'est pas fait (voir « Fin de
   session »).
5. **Déployer le gabarit** avec `ecraser: true`, puis fusionner la *pull
   request* du workflow après avoir vérifié **Files changed**.
6. **Donner les accès** : étudiants en Write, enseignant en Write.
7. **Vérifier `CODEOWNERS`** : ouvrir le fichier dans GitHub (les propriétaires
   invalides y sont surlignés), puis ouvrir une *pull request* de test et
   confirmer que la révision est demandée automatiquement.
8. **Faire un essai complet** avec un compte de test : remise, contrôle,
   *review*, fusion, PDF dans la release. Remettre ensuite le fichier de
   l'équipe de test à neuf (`ecraser: true`) et supprimer la release et le
   *tag* `documents-finaux` produits par l'essai.

## Pendant la session

- Les avertissements ⚠ dans les *pull requests* signalent un problème de
  configuration (`equipes.yml`), jamais un problème de l'équipe.
- Une demande de refus transmise par l'enseignant : retirer les noms de
  l'équipe d'`equipes.yml` (liste `membres` vide) **avant** sa première
  fusion. Les noms déjà inscrits restent dans l'historique.
- Ne pas modifier le gabarit en cours de session. Si c'est indispensable,
  redéployer avec `ecraser: false` ne mettra **pas** à jour les fichiers déjà
  présents : le changement ne touchera que les nouveaux dossiers.

## Fin de session

1. **Télécharger tous les PDF** de la release `documents-finaux` et les
   conserver hors de GitHub. Au prochain redéploiement `ecraser: true` suivi
   d'une fusion, la release sera remplacée par les PDF de la nouvelle cohorte.
2. **Déposer dans Papyrus** les travaux admissibles (voir la section
   « Admissibilité » de `GRILLE_CORRECTION.md`). Le titre propre à chaque
   équipe se renseigne dans `equipes.yml` (`titre:`).
3. **Retirer les accès** des étudiants de la session.
4. **Vider les noms** d'`equipes.yml` pour la cohorte suivante. Ils restent
   dans l'historique, comme annoncé aux étudiants.

---

## Changer d'administrateur

1. Donner au nouvel administrateur un accès **Admin** au dépôt.
2. Remplacer le propriétaire dans `CODEOWNERS`. Après le transfert vers
   `bibudem`, une équipe d'organisation (`@bibudem/nom-equipe`) avec un accès
   Write **explicite** au dépôt est préférable à un compte individuel.
3. Vérifier `CODEOWNERS` comme en début de session.
4. Mettre à jour la déclaration en bas du README et le tableau des réglages
   ci-dessus.

---

## Pièges connus

| Piège | Conséquence | Parade |
|---|---|---|
| Renommer le job `verification` | Toutes les *pull requests* restent bloquées sur un contrôle qui ne vient jamais | Changer le *ruleset* en même temps |
| Ajouter un filtre `paths` au déclencheur `pull_request` | Même conséquence pour les *pull requests* hors périmètre | Ne pas en ajouter |
| Propriétaire invalide dans `CODEOWNERS` | La révision obligatoire disparaît sans avertissement | Vérifier après tout changement d'accès |
| Modifier le gabarit sans redéployer | Les fichiers d'équipe ne sont plus identiques au gabarit : la fusion suivante produit des PDF vierges | Redéployer avec `ecraser: true` avant la première remise |
| `ecraser: true` en cours de session | Écrase le travail des équipes | Vérifier **Files changed** avant de fusionner |
| Release supprimée à la main | Elle est recréée à la fusion suivante ; un *tag* resté en place peut subsister | Supprimer aussi le *tag* sous **Releases → Tags** |
| Indentation dans `equipes.yml` | Une équipe mal indentée n'est pas déployée | Deux espaces avant `equipe-NN:` |

---

## Sources

- [About code owners — GitHub Docs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)
- [Managing GitHub Actions settings for a repository — GitHub Docs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository)
- [Triggering a workflow — GitHub Docs](https://docs.github.com/en/actions/how-tos/write-workflows/choose-when-workflows-run/trigger-a-workflow)
- [Managing releases in a repository — GitHub Docs](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository)
- [Managing branches within your repository — GitHub Docs](https://docs.github.com/en/pull-requests/how-tos/commit-changes/managing-branches-within-your-repository)
