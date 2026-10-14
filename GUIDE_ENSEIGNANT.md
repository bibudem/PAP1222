# Corriger les remises

*Guide destiné à l'enseignant. Les consignes pour les équipes sont dans le
[README](README.md).*

Tout se fait dans le navigateur. Il n'y a rien à installer et rien à
configurer. L'enseignant n'a aucune métadonnée à saisir : la page titre, le
nom des fichiers et la licence sont produits automatiquement.

> Les mots en *italique* sont les termes de GitHub. L'interface n'est pas
> traduite en français, alors ils ne le sont pas ici non plus. Le lexique en
> fin de page les explique. Les mots en **gras** sont des boutons à cliquer.

---

## Ce que les étudiants doivent lire avant de commencer

Le README ouvre sur une section qui les avertit de trois choses : leurs noms
figureront sur la page titre sous licence CC BY, le dépôt est public et
l'inscription est **permanente** — un nom enregistré ne s'efface pas de
l'historique Git, même si l'équipe renonce au dépôt dans Papyrus.

Il leur indique aussi qu'une **voie de remise non publique** existe, et qu'il
faut en aviser l'enseignant *avant* de commencer. Quelques demandes sont donc
à prévoir en début de session. Deux choses à savoir pour y répondre :

- Le refus n'a aucune incidence sur la note, et l'étudiant n'a pas à se
  justifier. C'est écrit tel quel dans le README.
- Si le refus est individuel dans une équipe qui accepte, l'administrateur du
  *repository* peut laisser cette seule équipe non nominative.

Toute demande est à transmettre à l'administrateur : c'est lui qui inscrit les
noms, une seule fois, avant la première remise.

---

## Le tableau de bord

L'onglet **Pull requests** réunit les remises : chaque équipe y dépose la
sienne sous forme de *pull request*.

Trois filtres à coller dans la barre de recherche, et à mettre en signet :

| Filtre | Ce qu'il montre |
|---|---|
| `is:pr is:open review:required` | les remises pas encore regardées |
| `is:pr is:open review:changes-requested` | les équipes qui doivent corriger |
| `is:pr is:open review:approved` | les remises approuvées, prêtes pour le *merge* |

Le premier filtre constitue la file de correction.

---

## Commenter

Ouvrir une *pull request*, puis l'onglet **Files changed**. Passer la souris
sur une ligne, cliquer sur le `+` bleu et écrire le commentaire.

**Utiliser `Start a review` et non `Add single comment`.** Avec `Start a
review`, les commentaires sont regroupés et publiés seulement à la fin. Avec
`Add single comment`, chaque commentaire envoie un avis tout de suite. Sur
vingt équipes, la différence est importante, autant pour la boîte de réception
de l'enseignant que pour celle des équipes.

### Proposer la correction au lieu de la décrire

Dans la boîte de commentaire, une icône insère un **bloc de suggestion** déjà
rempli avec le contenu de la ligne. L'enseignant le corrige, et l'équipe
applique la correction **d'un seul clic**, sans ouvrir l'éditeur et sans rien
retaper.

La suggestion convient dès que la correction est concrète : remettre un
symbole de troncature, ajouter les champs `.ti,ab,kf.`, déplacer une équation
dans le bloc de code, corriger un descripteur. Elle est beaucoup plus efficace
qu'un commentaire en prose, et elle élimine le risque que l'équipe comprenne
de travers.

Le commentaire ordinaire reste pour ce qui demande une réflexion — « le
découpage en concepts mélange deux idées », « ce filtre exclut probablement
des études pertinentes ». Une suggestion n'y aurait aucun sens.

> **À savoir sur `Request changes`.** Une fois des corrections demandées,
> **seul l'enseignant qui les a demandées** peut lever le blocage, en
> soumettant une nouvelle révision approbatrice. L'approbation de quelqu'un
> d'autre ne suffirait pas.

---

## Ce que le contrôle automatique ne voit pas

Le *check* attrape les renseignements personnels — matricules, courriels,
téléphones. Il ne juge pas le contenu : cela revient à l'enseignant. Et une
chose précise est à surveiller, parce qu'elle **passe au vert sans rien
signaler**.

**La syntaxe écrite hors du bloc de code.** Les équations et les descripteurs
vont dans le bloc de code de la section 3, et nulle part ailleurs. Si une
équipe en recopie dans le texte courant, l'affichage sur GitHub reste
parfaitement correct — mais le document final perd les symboles. `diabet$`
devient `diabet`, et `diabet*, diabetic*` sort en italique sans ses
astérisques.

Autrement dit : ce qui est évalué disparaît du seul document archivé, et rien
ne le signale. Une équation ou un descripteur dans le texte courant appelle
une demande de déplacement avec **Request changes**.

C'est la seule vérification de fond que l'automatisation ne peut pas faire.

---

## Relire un travail corrigé

Quand une équipe a corrigé, inutile de tout relire. Dans **Files changed**, le
menu en haut à gauche affiche **All commits** par défaut : l'ouvrir et choisir
**Changes since your last review**.

Le diff ne montre alors que ce qui a bougé depuis la lecture précédente. La
différence est considérable, et pas pour la raison qu'on croit : en « All
commits », toutes les lignes de consigne que l'équipe a effacées en
remplissant le gabarit réapparaissent — souvent quarante lignes de
suppressions pour quinze lignes de travail.

---

## Conclure

Cliquer sur **Submit review**, en haut à droite. Trois choix :

- **Request changes** — il y a des corrections à faire. L'équipe modifie son
  texte, l'enseignant relit.
- **Approve** — le travail est accepté.
- **Comment** — des remarques, sans verdict.

Après l'approbation, cliquer sur **Merge pull request**. Le document final se
fabrique tout seul, page titre comprise, et la *branch* de l'équipe disparaît.

Le *merge* se fait dès l'approbation.

---

## Récupérer les documents

Sur la page d'accueil du *repository*, dans la colonne de droite, cliquer sur
**Releases** → **Documents finaux**. On y trouve un PDF par équipe, déjà titré
et nommé.

La liste se met à jour toute seule à chaque fusion d'une remise. Il n'y a rien
à lancer, et rien à faire dans l'onglet **Actions**.

> Ces fichiers n'expirent pas. Télécharger quand même le paquet à la fin de la
> session : c'est la pièce justificative en cas de contestation d'une note, et
> une copie hors GitHub vaut mieux qu'une seule.

---

## Si quelque chose bloque

**Un ✗ rouge apparaît sous une *pull request*.** Le *check* automatique a
trouvé un renseignement personnel : un matricule, un courriel ou un numéro de
téléphone. L'équipe corrige son texte et le *check* repart tout seul. Rien à
faire du côté de l'enseignant.

**Un ⚠ jaune apparaît.** C'est un problème de configuration, pas un problème
de l'équipe. Le *merge* n'est pas bloqué. Le signaler à l'administrateur et
continuer.

**GitHub affiche « You cannot approve your own pull request ».** C'est une
règle de GitHub, pas un réglage. Faire le *merge* directement.

**Une équipe ne retrouve plus son travail.** Elle est repartie du dossier
`equipes/` au lieu de sa *pull request*. Rien n'est perdu : son texte est sur
sa *branch* et il est visible dans l'onglet **Pull requests**.

**Une équipe a modifié le dossier d'une autre équipe.** Cela se voit dans
**Files changed** : plus d'un fichier apparaît. Demander la correction avec
**Request changes**. L'historique garde la trace de ce qui s'est passé.

---

## Lexique

| Terme | Ce que ça veut dire |
|---|---|
| *repository* (dépôt) | l'ensemble des fichiers du cours, avec tout leur historique |
| *commit* (enregistrement) | une modification enregistrée, datée et signée. Rien ne s'efface d'un *commit* |
| *branch* (branche) | une ligne de travail en parallèle. Chaque équipe a la sienne |
| `main` | la *branch* officielle, celle qui fait foi. Personne n'y écrit directement |
| *pull request* (demande de fusion) | la demande d'intégrer la *branch* d'une équipe dans `main`. C'est sa remise : le travail, la discussion et la correction s'y trouvent tous |
| *review* (révision) | la lecture commentée de l'enseignant, ligne par ligne |
| *merge* (fusion) | l'intégration du travail accepté dans `main`. Réservée à l'enseignant |
| *check* (contrôle) | une vérification automatique lancée à chaque *commit*. Celui-ci cherche les renseignements personnels |
| *Actions* | le service de GitHub qui exécute les *checks* et fabrique les PDF. Aucune intervention n'y est nécessaire |
| *release* (version publiée) | l'endroit où les PDF sont publiés, dans la colonne de droite de la page d'accueil. N'expire pas |
| *issue* (ticket) | une question posée par une équipe dans l'onglet **Issues** |

---

Pour tout le reste — la configuration, la liste des équipes, le journal
d'exécution, l'entretien — s'adresser à l'administrateur du *repository*, et
consulter le [guide d'administration](GUIDE_ADMINISTRATEUR.md).
