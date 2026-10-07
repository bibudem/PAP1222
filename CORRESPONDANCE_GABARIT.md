# Du classeur Excel au gabarit GitHub

Ce document explique où chaque partie du travail se retrouve après la
transition, et ce qui change pour les étudiants comme pour la correction.
Rien n'est retiré du travail demandé : la matière est la même, répartie
autrement.

---

## Correspondance

| Onglet du classeur | Section du gabarit | Critère(s) de la grille |
| --- | --- | --- |
| NOMS | — *(voir plus bas)* | — |
| PLAN DE CONCEPT | 3. Plan de concepts | 3, 4, 6 |
| JUSTIFICATION | 2. Pertinence clinique | 2 |
| ARTICLES DE CONSENSUS | 4. Articles de consensus | 3 |
| HISTORIQUE DE RECHERCHE | 5. Stratégies exécutées | 8, 9 |
| COMMENTAIRES — AMÉLIORATIONS | 8. Ajustements et améliorations | 11 |

Six sections du gabarit n'avaient pas d'onglet correspondant :

| Section du gabarit | Pourquoi | Critère |
| --- | --- | --- |
| 1. Question de recherche | L'onglet la logeait dans une cellule du plan de concepts | 1 |
| 6. Critères d'inclusion et d'exclusion | Distingue le tri des résultats du filtrage à l'interrogation | — |
| 7. Journal de recherche | Rend visibles les tentatives infructueuses, qui sont évaluées | 11 |
| 9. Déclaration de l'usage de l'IA générative | **Était évaluée sans que les étudiants aient d'endroit où la faire** | 10 |
| 10. Références retenues | Résultat du tri, distinct des articles de consensus | — |
| 11. Filiation | Permet aux cohortes suivantes de reprendre une stratégie | — |

---

## Les trois décisions de conception

### Le plan de concepts reste une matrice, dans un bloc de code

L'onglet PLAN DE CONCEPT croise les concepts et trois niveaux de vocabulaire :
langage simple, descripteurs, mots-clés. Cette structure est conservée, mais
transposée — un bloc par concept, trois lignes dans chacun — et placée dans un
bloc de code.

La raison est concrète. Un descripteur s'écrit
`"Renal Insufficiency, Chronic"[Mesh:NoExp]` : virgules, guillemets droits et
crochets dans la même expression. Hors d'un bloc de code, GitHub interprète
une partie de ces caractères et le descripteur ressort déformé dans le
document final. Dans un bloc de code, rien n'est interprété.

C'est aussi pour cette raison que le plan n'est pas un fichier CSV : les
virgules des descripteurs se confondraient avec les séparateurs de colonnes.

### La justification du vocabulaire est scindée en deux

La grille évalue séparément la **précision** et l'**exhaustivité** du
vocabulaire contrôlé (critère 4), puis du vocabulaire libre (critère 6). Le
gabarit demande donc deux justifications distinctes par concept, plus celle de
l'option Explode. Un seul paragraphe fourre-tout rendait ces trois notes
difficiles à asseoir.

### L'historique se colle tel quel, sans renumérotation

Le gabarit demande explicitement aux équipes de **ne pas réordonner** leur
export. PubMed exporte du plus récent au plus ancien — la ligne 16 en
premier — et les lignes de combinaison renvoient à des numéros (`#1 OR #2`).
Renuméroter casse les renvois, silencieusement.

Quand la plateforme fournit une colonne « Search Details » — la traduction
exacte de la requête — le gabarit prévoit un bloc pour l'accueillir. C'est
elle qui établit la reproductibilité.

---

## Ce qui change pour les étudiants

Ils remplissent un seul fichier au lieu d'un classeur à six onglets, et ils ne
saisissent plus aucune information administrative : noms, sigle du cours, date
et licence sont ajoutés automatiquement à la page titre du document final.

Deux règles de saisie, rappelées en tête du gabarit : la syntaxe va dans les
blocs de code déjà en place, et on n'écrit jamais huit chiffres de suite — un
contrôle automatique cherche les matricules, et un décompte de résultats collé
sans espaces y ressemble.

L'onglet NOMS disparaît. Le dépôt étant public, les noms ne sont pas saisis
par les équipes : ils sont inscrits une fois par l'administrateur du dépôt et
n'apparaissent que sur la page titre du PDF produit après approbation. Les
étudiants s'identifient par leur identifiant GitHub dans le formulaire de
remise.

---

## Ce qui change pour la correction

La grille d'évaluation est reprise intégralement — douze critères, mêmes
échelles — dans `GRILLE_CORRECTION.md`. Elle se copie dans une *review* de la
remise ; les cases y deviennent cliquables.

La différence tient à l'endroit où se posent les commentaires. Dans l'onglet
**Files changed** de la remise, un commentaire s'attache à une ligne précise :
le descripteur discutable, la ligne de filtre, l'équation mal parenthésée.
L'équipe voit la remarque en regard de ce qu'elle a écrit, et peut répondre
dans le même fil. Les champs de commentaires de la grille restent utiles pour
l'appréciation d'ensemble.

Les trois issues de la correction — approbation, demande de changements,
commentaire simple — correspondent aux trois façons de clore une *review* sur
GitHub.

---

## Ce qui ne se transpose pas

**Les macros du formulaire Word.** Le document `ModeleEvalDevoir.docm`
contient un projet VBA qui gère les boutons radio et les champs de formulaire.
Rien n'en est reproduit : la grille devient du texte avec des cases à cocher.

Le formulaire Word est retiré — la *review* GitHub le remplace comme support
de correction.

**L'exemple rempli.** Aucun n'est fourni. Le classeur transmis contient le
travail d'une équipe réelle, avec les noms de trois étudiantes : il ne peut
pas servir de modèle dans un dépôt public.

Les équipes ne travaillent pas pour autant à l'aveugle : chaque section du
gabarit porte, dans ses consignes, un modèle de la forme attendue — plan de
concepts, historique PubMed, historique Ovid, légende des opérateurs. Ces
modèles sont visibles dans l'éditeur et n'apparaissent pas dans le document
final.

---

## Le point à trancher avant la première remise

Le dépôt est public, et `equipes.yml` associe chaque équipe aux noms de ses
membres pour la page titre des PDF. Une *review* publiée sur une pull request
est donc publique elle aussi : les cases cochées de la grille, les
commentaires, l'appréciation générale — tout cela devient consultable par les
autres équipes et par n'importe qui, et rattachable à des personnes nommées.

C'est acceptable pour la **correction formative** : des annotations ligne par
ligne sur un descripteur ou une équation, c'est précisément ce qu'on veut
rendre visible et réutilisable d'une cohorte à l'autre.

Ça l'est beaucoup moins pour l'**évaluation sommative** : une échelle 1-2-3
publique sur le travail d'une équipe nommée, c'est un résultat scolaire
exposé.

La séparation la plus simple, puisque StudiUM demeure :

- **Dans la review GitHub** — les commentaires qualitatifs, les suggestions,
  les demandes de changement. La partie qui fait apprendre.
- **Dans StudiUM** — les échelles et la note. La partie qui compte au dossier.

La grille de `GRILLE_CORRECTION.md` sert alors de trame commune aux deux : on
la lit pour corriger, on reporte les échelles dans StudiUM, et on écrit dans
GitHub ce qui aide l'équipe à reprendre son travail.

---

## À décider

- Les articles de consensus sont-ils imposés par l'enseignante, ou trouvés par
  les équipes ? Le gabarit suppose actuellement qu'ils sont connus d'avance.
- Combien de blocs CONCEPT pré-remplir dans le gabarit ? Trois actuellement :
  supprimer les blocs inutilisés est plus sûr que d'en dupliquer.
