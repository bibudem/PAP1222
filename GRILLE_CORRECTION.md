# Grille de correction

Les douze critères du cours, chacun avec l'échelle du formulaire d'évaluation,
la section du travail qui s'y rapporte, et les questions de lecture qui aident
à trancher.

**Pour corriger une remise :** copiez tout ce qui suit la ligne de séparation
dans une *review* de la pull request de l'équipe. Les cases deviennent
cliquables une fois la review publiée. Les commentaires ligne par ligne, eux,
se posent directement dans l'onglet **Files changed** — c'est là qu'ils sont le
plus utiles à l'équipe.

Les questions en retrait ne sont pas des critères : ce sont des points de
repère pour la lecture. L'équipe n'a pas à y répondre une à une.

---

## 1. Formulation de la question

*Section 1 du travail*

- [ ] Difficile à comprendre
- [ ] Relativement clair
- [ ] Très clair

> La question permet-elle d'identifier les concepts sans ambiguïté ?
> Est-ce une question, ou seulement un sujet ?

## 2. Justification de la pertinence clinique

*Section 2 du travail*

- [ ] Difficile à comprendre
- [ ] Relativement clair
- [ ] Très clair

> La pertinence est-elle argumentée, ou seulement affirmée ?
> Nomme-t-elle la décision que la recherche doit éclairer, et pour qui ?

## 3. Identification des concepts à chercher

*Section 3 du travail — bloc de code et justification*

- [ ] Trop de concepts (trop restreint)
- [ ] Pas assez de concepts (trop large)
- [ ] Logique à revoir
- [ ] Bonne identification

> Le découpage est-il juste — ni concept superflu qui restreint indûment, ni
> concept manquant qui élargit trop ?
> La portée déclarée de chaque concept correspond-elle à ce qui est cherché
> ensuite dans l'historique ?
> Les articles de consensus de la section 4 sont-ils repêchés ? Un consensus
> manqué signale souvent un concept mal posé.

## 4. Recherche par vocabulaire contrôlé

*Section 3 du travail — ligne « Vocabulaire contrôlé » et sa justification*

**Précision des termes choisis**

- [ ] 1
- [ ] 2
- [ ] 3

**Exhaustivité des termes choisis**

- [ ] 1
- [ ] 2
- [ ] 3

**Bonne utilisation de l'option Explode**

- [ ] 1
- [ ] 2
- [ ] 3

> Chaque descripteur existe-t-il dans la version du thésaurus indiquée ?
> Les descripteurs sont-ils ceux de la base déclarée — MeSH, CINAHL Headings et
> Emtree ne sont pas interchangeables ?
> Manque-t-il un descripteur évident pour l'un des concepts ?
> Explode est-il justifié ? Appliqué systématiquement sans réflexion, ou absent
> là où l'arborescence l'exigeait ? `NoExp` se justifie aussi.

## 5. Commentaires sur la recherche par vocabulaire contrôlé

<!-- Texte libre. Si le commentaire porte sur un descripteur précis, posez-le
     plutôt en annotation sur la ligne concernée, dans Files changed. -->

## 6. Recherche par vocabulaire libre

*Section 3 du travail — ligne « Vocabulaire libre » et sa justification*

**Précision des termes choisis**

- [ ] 1
- [ ] 2
- [ ] 3

**Exhaustivité des termes choisis**

- [ ] 1
- [ ] 2
- [ ] 3

**Bonne utilisation des champs de recherche**

- [ ] 1
- [ ] 2
- [ ] 3

> Les troncatures sont-elles placées au bon endroit — ni trop courtes, ce qui
> génère du bruit, ni trop longues, ce qui perd des variantes ?
> Les synonymes couvrent-ils les variantes orthographiques, les usages
> britannique et américain, les noms commerciaux ?
> Les champs interrogés sont-ils appropriés — titre, résumé et mots-clés
> d'auteur plutôt que tous les champs ?

## 7. Commentaires sur la recherche par vocabulaire libre

<!-- Texte libre. -->

## 8. Utilisation des opérateurs booléens

*Section 5 du travail — historique de recherche*

- [ ] À revoir
- [ ] Bien maîtrisé

> OU à l'intérieur d'un concept, ET entre les concepts ?
> L'équation reproduite correspond-elle aux termes déclarés en section 3 ?
> Les parenthèses ferment-elles ce qu'il faut ?
> Les lignes de combinaison renvoient-elles aux bons numéros ?
> Les opérateurs d'adjacence sont-ils utilisés à bon escient ?

<!-- Commentaire, s'il y a lieu. -->

## 9. Utilisation des filtres au besoin

*Section 5 du travail — « Filtres appliqués »*

- [ ] Utilisation non adéquate
- [ ] Bonne utilisation

> Les filtres sont-ils justifiés, et ne risquent-ils pas d'exclure des études
> pertinentes ?
> Le renvoi à la ligne de l'historique est-il fait ?
> Le nombre de résultats est-il plausible compte tenu de la stratégie ?
> La date d'exécution figure-t-elle pour chaque base ?

## 10. Déclaration de l'usage de l'IA générative

*Section 9 du travail*

- [ ] À revoir
- [ ] Bien maîtrisé

> La section est-elle remplie ? Une absence d'usage se déclare aussi.
> L'outil et sa version sont-ils nommés, et l'étape où il est intervenu ?
> L'équipe distingue-t-elle ce que l'outil a proposé de ce qu'elle a vérifié
> elle-même ? Un outil qui suggère des descripteurs ne les valide pas.
> L'autorisation préalable avait-elle été obtenue ?

## 11. Pertinence des améliorations proposées

*Section 8 du travail*

- [ ] À revoir
- [ ] Bien maîtrisé

> L'équipe nomme-t-elle une limite réelle de sa stratégie, ou se contente-t-elle
> de la présenter comme aboutie ?
> L'amélioration proposée lèverait-elle effectivement cette limite ?
> Le journal de recherche montre-t-il les impasses, ou seulement le chemin
> réussi ?

## 12. Appréciation générale du travail

<!-- Texte libre. -->

---

## Admissibilité au dépôt dans Papyrus

Hors grille : à vérifier avant de fusionner, parce que la fusion déclenche la
production du document final.

- [ ] Une personne extérieure pourrait réexécuter cette recherche telle quelle
- [ ] Le document se comprend sans le contexte du cours
- [ ] Aucun renseignement personnel ne figure dans `strategie_recherche.md`
- [ ] Les contrôles automatiques sont au vert
