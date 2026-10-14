# PAP1222 — Savoirs scientifiques en pharmacie : stratégies de recherche

## Description

Ce dépôt a été conçu pour répondre aux besoins des étudiants et de l'enseignant dans le cadre d'un cours portant sur les stratégies de recherche.

Il permet à:

- étudiants et enseignant : de disposer d'un espace de travail pour faire avancer les travaux étudiants et les soumettre à l'enseignant pour correction ;
- enseignant : de corriger les travaux, de communiquer ses corrections ou recommandations, puis de les approuver. La fusion d'un travail approuvé lance la production d'un document final en format PDF, prêt à être récupéré par les étudiants ;
- tous : de consulter les travaux produits par les cohortes successives du cours.

---

## Fonctionnement

Tout se fait à partir du navigateur Web. Il n'y a rien à installer et aucune ligne de commande à entrer.

**Vous n'avez aucune information administrative à saisir.** Vos noms, le sigle du cours, la date et la licence sont ajoutés automatiquement. Vous n'avez qu'à rédiger votre stratégie de recherche.

> Les mots en **gras** sont des boutons à cliquer. Les mots en *italique* sont des termes de GitHub.
> L'interface de GitHub n'est pas traduite en français : par souci de clarté et de cohérence, ce document
> emploie donc les termes anglais d'origine. Vous ne devriez pas avoir à vous y reporter, mais un lexique,
> en fin de page, fait le lien entre ces termes et les concepts qu'ils désignent.

---

## Important : à lire **avant** de commencer

### Renseignements personnels

Ce dépôt est public : si vous décidez d'y verser votre travail, il sera publié **sous votre nom**, et n'importe qui pourra le consulter.

Un *repository* Git conserve tout. Une fois vos noms enregistrés, **ils continueront d'apparaître**, même si :

- la ligne est retirée du fichier plus tard ;
- votre équipe décide finalement de ne pas déposer son travail dans Papyrus ;
- vous quittez le cours.

Considérez que ce qui est enregistré ici y reste.

### Droit de refus

L'utilisation de cette plateforme se fait sur une base volontaire : vous avez le droit de refuser.

**Avant de faire quoi que ce soit ici, avisez votre enseignant.** Une voie de soumission non publique vous sera toujours offerte, et vous serez évalués sur le même travail. Vous n'avez pas à vous justifier, et ce choix n'a aucune incidence sur votre note.

### Facultatif : masquer votre adresse courriel

Cliquez sur votre photo de profil, en haut à droite → **Settings** → **Emails**, puis cochez **Keep my email addresses private**.

Sans ce réglage, votre adresse courriel apparaît publiquement dans l'historique du *repository* et, comme pour vos noms, il est impossible de corriger un *commit* déjà fait. Faites-le **avant** votre première contribution.

### Droit d'auteur

Vos noms figureront sur la page titre du document final, sous licence **Creative Commons Attribution 4.0 (CC BY 4.0)**.

La licence **CC BY** permet à quiconque de reprendre et d'adapter votre travail, y compris à des fins commerciales, **à condition de vous créditer**.

Une fois rédigés, corrigés et approuvés, vos travaux pourront aussi être déposés dans **Papyrus**, le dépôt institutionnel de l'Université de Montréal, où ils recevront une adresse permanente et d'où ils pourront être cités.

---

## Guide d'utilisation

### 1. Accéder à votre fichier de travail

Ouvrez le fichier de votre équipe :

`equipes/` → votre dossier → fichier `strategie_recherche.md`

C'est le seul fichier que vous aurez à modifier.

Le rôle qu'on vous attribue ouvre techniquement tout le dépôt : rien ne vous empêche d'ouvrir le fichier d'une autre équipe. Vérifiez le chemin affiché en haut de l'éditeur : il doit porter le numéro de votre équipe.

Si vous faites une erreur, Git conserve toutes les versions. L'erreur sera visible dans votre soumission, et l'enseignant pourra vous demander de la corriger.

---

### 2. Rédiger

L'icône ✏️, en haut à droite du fichier, ouvre l'éditeur. L'onglet **Preview** vous montre le rendu.

Écrivez dans les champs prévus. **Les consignes** sont encadrées par `<!--` et `-->` :

- celles du haut donnent les deux règles de saisie ;
- les autres expliquent chaque section.

**Laissez-les où elles sont et écrivez en dessous.** Les effacer complique inutilement la correction : l'enseignant verrait apparaître des dizaines de lignes supprimées qui n'ont rien à voir avec votre travail.

Les consignes ne sont visibles que dans l'éditeur. Elles n'apparaîtront pas dans le document final. Pour vous en assurer, cliquez sur **Preview** : vous verrez le rendu réel de votre document de travail.

---

### 3. Soumettre pour correction

1. Cliquez sur **Commit changes…**, en haut à droite.
2. Effacez ce que GitHub propose (« Update strategie_recherche.md ») : **cette ligne devient le titre de votre soumission**, et c'est grâce à elle que l'enseignant la repérera au moment de corriger. Respectez la convention suivante :

   ```
   Équipe [numéro de votre équipe] — [votre question ou sujet]

   Exemple : Équipe 03 — Simulation en chirurgie cardiothoracique
   ```

3. Pour le reste, ne changez rien : tout est déjà présélectionné. GitHub ne vous laissera pas écrire directement dans `main` ; selon la version, l'option est grisée ou absente.
4. GitHub vous présente ensuite le formulaire de soumission, déjà rempli en partie. Complétez l'identification de votre équipe : le numéro d'équipe, le travail et vos **identifiants GitHub**, pas vos noms.
5. Cliquez sur **Create pull request**.

C'est fait : votre travail est soumis. Ce clic crée la soumission et vous amène directement sur sa page, où la liste de vérification s'affiche pour vous permettre de confirmer que vous avez respecté les critères de soumission.

- Cochez maintenant les cases, qui sont devenues cliquables.

Il n'y a rien à enregistrer : chaque case se sauvegarde d'elle-même dès que vous cliquez dessus.

---

#### 3.1. Contrôle automatique de la soumission

Quelques secondes plus tard, au bas de la page :

- ✓ vert — tout va bien.
- **Skipped** à côté de « Production des PDF » — c'est normal : le document final n'est produit qu'une fois le travail accepté.
- ✗ rouge — un renseignement personnel a été détecté. **Details** montre la ligne en cause ; corrigez-la et le contrôle repartira tout seul.

Puisque le dépôt est public, ce contrôle cherche dans votre soumission les éléments qui pourraient compromettre la protection de vos renseignements personnels (outre votre nom) et les refuse :

- un numéro de matricule ;
- une adresse courriel ;
- un numéro de téléphone.

Le contrôle des matricules repère toute suite de huit chiffres consécutifs, sans espace ni tiret (p. ex. « 12345678 »). Trois cas peuvent donc le déclencher sans que vous l'ayez voulu :

- **Une date écrite sans tirets.** Écrivez `2026-09-15`, jamais `20260915`.
- **Un PMID sans étiquette.** Il passe s'il est précédé de « PMID : » (p. ex. « PMID : 30234752 »). Les DOI et les liens PubMed complets ne posent aucun problème.
- **Un grand décompte de résultats.** Au-delà de dix millions, un nombre écrit sans séparateur compte huit chiffres. Séparez les milliers par une espace (p. ex. « 12 345 678 ») : c'est d'ailleurs la typographie correcte en français.

---

#### 3.2. Continuer de travailler

Une fois votre travail soumis, vous pouvez continuer à le modifier. Passez alors toujours par la *pull request* de votre soumission, jamais par le fichier de votre dossier `equipes/`.

Marche à suivre :

1. Onglet *Pull requests* → ouvrez la vôtre. Mettez-la en signet : vous y reviendrez souvent.
2. Onglet *Files changed* :
   - cliquez sur les trois points ⋯ à droite du nom du fichier → **Edit file** ;
   - modifiez votre texte, puis cliquez sur **Commit changes**. Cette fois, laissez sélectionnée l'option d'enregistrement direct (*commit* direct).

Vos modifications s'ajoutent à la *pull request* de votre soumission initiale. N'en ouvrez surtout pas une deuxième.

> **Pourquoi ne pas passer par votre dossier ?** Le dossier `equipes/` affiche la version officielle de votre
> travail, celle qui a déjà été acceptée : elle se trouve sur la *branch* `main`. Votre ébauche en cours, elle,
> se trouve sur votre propre *branch*, et vous y accédez par votre *pull request*. En passant par celle-ci,
> vous êtes sûrs de modifier le bon fichier.

---

### 4. Correction : approbation, demande de changements et commentaires

L'enseignant corrige votre travail dans l'onglet **Files changed** de votre *pull request*, où il peut ajouter des commentaires. C'est ce que GitHub appelle une *review*. La correction aboutit à l'un de trois scénarios :

1. **Le travail est approuvé.** L'enseignant fusionne alors votre soumission : votre travail rejoint le dossier de votre équipe sur `main`, et le document final est produit automatiquement, avec une page titre à vos noms.

2. **Des changements sont demandés.** La fusion reste bloquée tant que vous n'avez pas repris votre texte. Il y a deux façons de le faire, selon la forme du commentaire :

   - **Une ou plusieurs suggestions sont formulées** — un encadré vous montre la ligne corrigée. Un bouton sous l'encadré applique la correction : vous n'avez rien à modifier vous-même.
   - **Aucune suggestion** — modifiez le fichier vous-même, comme à la section précédente. L'éditeur n'affiche pas les commentaires : gardez votre soumission ouverte dans un onglet pour lire les annotations, et l'éditeur dans un autre.

3. **Des commentaires simples, sans demande de changements.** Ni approbation ni correction exigée : à vous de voir ce que vous en faites. Votre soumission reste en attente jusqu'à ce que l'enseignant l'approuve.

Les commentaires de l'enseignant s'affichent dans l'onglet **Files changed** de votre soumission, sous la ligne concernée. Chacun ouvre un fil de discussion où vous pouvez répondre : poser une question, demander une précision, expliquer votre démarche.

---

## Règles

1. Une seule *pull request* ouverte par équipe et par travail.
2. Ne modifiez que le fichier de votre équipe.
3. N'utilisez jamais le bouton **Merge pull request** : c'est le rôle de l'enseignant.
4. Aucun renseignement personnel dans le document.
5. Pour votre propre usage de l'IA générative : l'autorisation de l'enseignant est requise, et vous devez déclarer votre utilisation. Le plan de cours prime sur tout ce qui est écrit ici. La [boîte à outils des bibliothèques](https://boite-outils.bib.umontreal.ca/trouver-evaluer/iag?p=5377614) explique comment citer, signaler et déclarer.

---

## Licence

Les stratégies de recherche réunies dans ce dépôt sont diffusées sous licence **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

Vous êtes libre de les partager et de les adapter, y compris à des fins commerciales, à condition de créditer les autrices et auteurs.

Chaque stratégie a ses propres autrices et auteurs, indiqués sur la page titre du document : citez la stratégie que vous réutilisez, pas le dépôt au complet. Le gabarit, les grilles et la chaîne de production sont diffusés sous la même licence.

Le fichier `LICENSE` contient le texte officiel, en anglais. Le résumé destiné aux non-juristes se trouve sur le site de Creative Commons, en français : <https://creativecommons.org/licenses/by/4.0/deed.fr>

---

## Lexique

| Terme | Ce que ça veut dire |
|---|---|
| *repository* (dépôt) | l'ensemble des fichiers du cours, avec tout leur historique |
| *commit* (enregistrement) | une modification enregistrée, datée et signée. Rien ne s'efface d'un *commit* |
| *branch* (branche) | une ligne de travail en parallèle. La vôtre porte votre travail en cours sans toucher à la version officielle |
| `main` | la *branch* officielle, celle qui fait foi. Personne n'y écrit directement |
| *pull request* (demande de fusion) | la demande d'intégrer votre *branch* dans `main`. Ici, c'est votre soumission : votre travail, la discussion et la correction s'y trouvent tous |
| *check* (contrôle) | une vérification automatique lancée à chaque *commit*. Celui-ci cherche les renseignements personnels |
| *review* (révision) | la lecture commentée de l'enseignant, ligne par ligne |
| *merge* (fusion) | l'intégration du travail accepté dans `main`. Réservée à l'enseignant |
| *issue* (ticket) | une question posée dans l'onglet **Issues**, visible de tous |

---

## Dépannage

Ouvrez une *issue* dans l'onglet **Issues** plutôt que d'écrire un courriel : la réponse servira aux autres équipes.

Pour la syntaxe Markdown : [guide de GitHub](https://docs.github.com/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

---

<sub><strong>Avec l'assistance de l'IAg.</strong> Les consignes, le gabarit et l'automatisation de ce dépôt ont été conçus avec l'aide de Claude Opus 5 (Anthropic), en août et en septembre 2026. Les décisions, la vérification et les tests relèvent de Hugo Bernier, bibliothécaire – expérience numérique en recherche, Université de Montréal. Cette déclaration ne porte pas sur les travaux déposés ici.</sub>
