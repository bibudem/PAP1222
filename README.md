# PAP1222 — Savoirs scientifiques en pharmacie : stratégies de recherche

## Description

Ce dépôt a été conçu pour répondre aux besoins des étudiants et de l'enseignant dans le cadre d'un cours portant sur les stratégies de recherche. Il permet :

1. **aux étudiants** : de disposer d'un espace de travail partagé pour rédiger les travaux et les soumettre à l'enseignant pour correction ;
2. **à l'enseignant** : de corriger les travaux, de communiquer ses corrections ou recommandations, puis de les approuver. La fusion d'un travail approuvé lance la production d'un document final en format PDF, prêt à être récupéré par les étudiants ;
3. **aux étudiants et à l'enseignant** : de consulter les travaux produits par les cohortes successives du cours.

---

## Modalités et fonctionnement

Tout se fait à partir du navigateur Web. Il n'y a rien à installer et aucune ligne de commande à entrer.

**Les équipes n'ont aucune information administrative à saisir.** Les noms, le sigle du cours, la date et la licence sont ajoutés automatiquement. Il ne reste qu'à rédiger le travail.

> Les mots en **gras** sont des boutons à cliquer. Les mots en *italique* sont des termes de GitHub.
> L'interface de GitHub n'est pas traduite en français : par souci de clarté et de cohérence, ce document
> emploie donc les termes anglais d'origine. Un lexique, en fin de page, fait le lien entre ces termes et
> les concepts qu'ils désignent.

---

## Important : à lire **avant** de commencer

### Renseignements personnels

Ce dépôt est public : un travail versé ici est publié **sous le nom de ses auteurs**, et n'importe qui peut le consulter.

Un *repository* Git conserve tout. Une fois les noms enregistrés, **ils continuent d'apparaître**, même si :

- la ligne est retirée du fichier plus tard ;
- l'équipe décide finalement de ne pas déposer son travail dans Papyrus ;
- l'étudiant quitte le cours.

Ce qui est enregistré ici y reste.

### Droit de refus

L'utilisation de cette plateforme se fait sur une base volontaire : chaque étudiant a le droit de refuser.

**Avant toute contribution, l'étudiant qui refuse en avise l'enseignant.** Une voie de soumission non publique est toujours offerte, et l'évaluation porte sur le même travail. Le refus n'a pas à être justifié et n'a aucune incidence sur la note.

### Facultatif : masquer l'adresse courriel

Photo de profil, en haut à droite → **Settings** → **Emails**, puis cocher **Keep my email addresses private**.

Sans ce réglage, l'adresse courriel apparaît publiquement dans l'historique du *repository* et, comme pour les noms, il est impossible de corriger un *commit* déjà fait. Ce réglage se fait **avant** la première contribution.

### Droit d'auteur

Les noms des auteurs figurent sur la page titre du document final, sous licence **Creative Commons Attribution 4.0 (CC BY 4.0)**.

La licence **CC BY** permet à quiconque de reprendre et d'adapter le travail, y compris à des fins commerciales, **à condition de créditer ses auteurs**.

Une fois rédigés, corrigés et approuvés, les travaux peuvent aussi être déposés dans **Papyrus**, le dépôt institutionnel de l'Université de Montréal, où ils reçoivent une adresse permanente et d'où ils peuvent être cités.

---

## Guide d'utilisation

### 1. Accéder au fichier de travail

Ouvrir le fichier de l'équipe :

`equipes/` → dossier de l'équipe → fichier `strategie_recherche.md`

C'est le seul fichier à modifier.

Le rôle attribué aux étudiants ouvre techniquement tout le dépôt : rien n'empêche d'ouvrir le fichier d'une autre équipe. Le chemin affiché en haut de l'éditeur doit porter le numéro de l'équipe.

En cas d'erreur, Git conserve toutes les versions. L'erreur est visible dans la soumission, et l'enseignant peut demander de la corriger.

---

### 2. Rédiger

L'icône ✏️, en haut à droite du fichier, ouvre l'éditeur. L'onglet **Preview** montre le rendu.

Écrire dans les champs prévus. **Les consignes** sont encadrées par `<!--` et `-->` :

- celles du haut donnent les deux règles de saisie ;
- les autres expliquent chaque section.

**Laisser les consignes en place et écrire en dessous.** Les effacer complique inutilement la correction : l'enseignant verrait apparaître des dizaines de lignes supprimées qui n'ont rien à voir avec le travail.

Les consignes ne sont visibles que dans l'éditeur et dans l'onglet **Files changed** de la soumission, qui montre le texte brut. Elles n'apparaissent ni dans l'affichage du fichier ni dans le document final. L'onglet **Preview** montre le rendu réel du document de travail.

---

### 3. Soumettre pour correction

1. Cliquer sur **Commit changes…**, en haut à droite.
2. Effacer ce que GitHub propose (« Update strategie_recherche.md ») : **cette ligne devient le titre de la soumission**, et c'est grâce à elle que l'enseignant la repère au moment de corriger. Respecter la convention suivante :

   ```
   Équipe [numéro de l'équipe] — [question ou sujet]

   Exemple : Équipe 03 — Simulation en chirurgie cardiothoracique
   ```

3. Ne rien changer d'autre : tout est déjà présélectionné. GitHub ne permet pas d'écrire directement dans `main` ; selon la version, l'option est grisée ou absente.
4. GitHub présente ensuite le formulaire de soumission, déjà rempli en partie. Compléter l'identification de l'équipe : le numéro d'équipe, le travail et les **identifiants GitHub** des membres, pas leurs noms.
5. Cliquer sur **Create pull request**.

Le travail est soumis. Ce clic crée la soumission et ouvre directement sa page, où la liste de vérification permet de confirmer que les critères de soumission sont respectés.

- Cocher les cases, qui sont devenues cliquables.

Il n'y a rien à enregistrer : chaque case se sauvegarde d'elle-même au clic.

---

#### 3.1. Contrôle automatique de la soumission

Quelques secondes plus tard, au bas de la page :

- ✓ vert — tout va bien.
- **Skipped** à côté de « Production des PDF » — c'est normal : le document final n'est produit qu'une fois le travail accepté.
- ✗ rouge — un renseignement personnel a été détecté. **Details** montre la ligne en cause ; une fois la ligne corrigée, le contrôle repart tout seul.

Puisque le dépôt est public, ce contrôle cherche dans la soumission les éléments qui pourraient compromettre la protection des renseignements personnels (outre les noms) et les refuse :

- un numéro de matricule ;
- une adresse courriel ;
- un numéro de téléphone.

Le contrôle des matricules repère toute suite de huit chiffres consécutifs, sans espace ni tiret (p. ex. « 12345678 »). Trois cas peuvent donc le déclencher involontairement :

- **Une date écrite sans tirets.** Écrire `2026-09-15`, jamais `20260915`.
- **Un PMID sans étiquette.** Il passe s'il est précédé de « PMID : » (p. ex. « PMID : 30234752 »). Les DOI et les liens PubMed complets ne posent aucun problème.
- **Un grand décompte de résultats.** Au-delà de dix millions, un nombre écrit sans séparateur compte huit chiffres. Séparer les milliers par une espace (p. ex. « 12 345 678 ») : c'est d'ailleurs la typographie correcte en français.

---

#### 3.2. Continuer de travailler

Une fois le travail soumis, il reste modifiable. Passer alors toujours par la *pull request* de la soumission, jamais par le fichier du dossier `equipes/`.

Marche à suivre :

1. Onglet *Pull requests* → ouvrir celle de l'équipe. La mettre en signet : elle servira souvent.
2. Onglet *Files changed* :
   - cliquer sur les trois points ⋯ à droite du nom du fichier → **Edit file** ;
   - modifier le texte, puis cliquer sur **Commit changes**. Cette fois, laisser sélectionnée l'option d'enregistrement direct (*commit* direct).

Les modifications s'ajoutent à la *pull request* de la soumission initiale. Ne surtout pas en ouvrir une deuxième.

> **Pourquoi ne pas passer par le dossier de l'équipe ?** Le dossier `equipes/` affiche la version officielle
> du travail, celle qui a déjà été acceptée : elle se trouve sur la *branch* `main`. L'ébauche en cours, elle,
> se trouve sur la *branch* de l'équipe, accessible par sa *pull request*. Passer par celle-ci garantit de
> modifier le bon fichier.

---

### 4. Correction : approbation, demande de changements et commentaires

L'enseignant corrige le travail dans l'onglet **Files changed** de la *pull request*, où il peut ajouter des commentaires. C'est ce que GitHub appelle une *review*. La correction aboutit à l'un de trois scénarios :

1. **Le travail est approuvé.** L'enseignant fusionne alors la soumission : le travail rejoint le dossier de l'équipe sur `main`, et le document final est produit automatiquement, avec une page titre aux noms des auteurs.

2. **Des changements sont demandés.** La fusion reste bloquée tant que le texte n'a pas été repris. Il y a deux façons de le faire, selon la forme du commentaire :

   - **Une ou plusieurs suggestions sont formulées** — un encadré montre la ligne corrigée. Un bouton sous l'encadré applique la correction : il n'y a rien à modifier à la main.
   - **Aucune suggestion** — modifier le fichier comme à la section précédente. L'éditeur n'affiche pas les commentaires : garder la soumission ouverte dans un onglet pour lire les annotations, et l'éditeur dans un autre.

3. **Des commentaires simples, sans demande de changements.** Ni approbation ni correction exigée : l'équipe décide de la suite à leur donner. La soumission reste en attente jusqu'à ce que l'enseignant l'approuve.

Les commentaires de l'enseignant s'affichent dans l'onglet **Files changed** de la soumission, sous la ligne concernée. Chacun ouvre un fil de discussion où l'équipe peut répondre : poser une question, demander une précision, expliquer sa démarche.

---

## Règles

1. Une seule *pull request* ouverte par équipe et par travail.
2. Ne modifier que le fichier de son équipe.
3. Ne jamais utiliser le bouton **Merge pull request** : c'est le rôle de l'enseignant.
4. Aucun renseignement personnel dans le document.
5. Usage de l'IA générative : l'autorisation de l'enseignant est requise, et l'usage doit être déclaré. Le plan de cours prime sur tout ce qui est écrit ici. La [boîte à outils des bibliothèques](https://boite-outils.bib.umontreal.ca/trouver-evaluer/iag?p=5377614) explique comment citer, signaler et déclarer.

---

## Licence

Les stratégies de recherche réunies dans ce dépôt sont diffusées sous licence **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

Elles peuvent être partagées et adaptées, y compris à des fins commerciales, à condition de créditer les autrices et auteurs.

Chaque stratégie a ses propres autrices et auteurs, indiqués sur la page titre du document : citer la stratégie réutilisée, pas le dépôt au complet. Le gabarit, les grilles et la chaîne de production sont diffusés sous la même licence.

Le fichier `LICENSE` contient le texte officiel, en anglais. Le résumé destiné aux non-juristes se trouve sur le site de Creative Commons, en français : <https://creativecommons.org/licenses/by/4.0/deed.fr>

---

## Lexique

| Terme | Ce que ça veut dire |
|---|---|
| *repository* (dépôt) | l'ensemble des fichiers du cours, avec tout leur historique |
| *commit* (enregistrement) | une modification enregistrée, datée et signée. Rien ne s'efface d'un *commit* |
| *branch* (branche) | une ligne de travail en parallèle. Celle de l'équipe porte son travail en cours sans toucher à la version officielle |
| `main` | la *branch* officielle, celle qui fait foi. Personne n'y écrit directement |
| *pull request* (demande de fusion) | la demande d'intégrer la *branch* de l'équipe dans `main`. Ici, c'est la soumission : le travail, la discussion et la correction s'y trouvent tous |
| *check* (contrôle) | une vérification automatique lancée à chaque *commit*. Celui-ci cherche les renseignements personnels |
| *review* (révision) | la lecture commentée de l'enseignant, ligne par ligne |
| *merge* (fusion) | l'intégration du travail accepté dans `main`. Réservée à l'enseignant |
| *issue* (ticket) | une question posée dans l'onglet **Issues**, visible de tous |

---

## Dépannage

Ouvrir une *issue* dans l'onglet **Issues** plutôt que d'écrire un courriel : la réponse servira aux autres équipes.

Pour la syntaxe Markdown : [guide de GitHub](https://docs.github.com/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

---

<sub><strong>Avec l'assistance de l'IAg.</strong> Les consignes, le gabarit et l'automatisation de ce dépôt ont été conçus avec l'aide de Claude Opus 5 (Anthropic), en août et en septembre 2026. Les décisions, la vérification et les tests relèvent de Hugo Bernier, bibliothécaire – expérience numérique en recherche, Université de Montréal. Cette déclaration ne porte pas sur les travaux déposés ici.</sub>
