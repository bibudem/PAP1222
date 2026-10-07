<!-- ─────────────────────────────────────────────────────────────────
     Vous n'avez aucune information administrative à saisir.
     Vos noms, le sigle du cours, la date et la licence sont ajoutés
     automatiquement à la page titre du PDF.

     Les blocs comme celui-ci sont des consignes. Ils n'apparaissent ni
     sur GitHub ni dans le PDF.

     LAISSEZ-LES EN PLACE. Ils ne coûtent rien — personne ne les voit —
     et les effacer alourdit énormément ce que l'enseignante doit relire :
     quarante lignes de consigne supprimées pour quinze lignes de travail.
     Écrivez simplement en dessous.

     DEUX RÈGLES DE SAISIE, ET C'EST TOUT :

     1. Toute syntaxe d'interrogation va dans un bloc de code — les
        trois accents graves ```. Les blocs sont déjà en place, en
        sections 3 et 5. À l'intérieur, rien n'est interprété : vos
        troncatures, astérisques, dièses, crochets et barres obliques
        sortent exactement comme vous les avez écrits.

        Ailleurs qu'entre ces accents, n'écrivez aucune syntaxe. Les
        descripteurs et les équations ne se recopient pas dans le
        texte courant : ils vivent dans les blocs, et on y renvoie.

        Collez l'historique DIRECTEMENT de la base de données vers le
        bloc. Word, Excel et Google Docs remplacent les guillemets
        droits par des guillemets courbes, et "Renal Insufficiency,
        Chronic"[Mesh:NoExp] devient une requête invalide sans que rien
        ne vous le signale.

     2. N'écrivez jamais huit chiffres de suite. Mettez des tirets dans
        les dates. Séparez les grands décomptes par une espace :
        écrivez 12 345 678, jamais collé ni avec des points. Un PMID
        passe s'il porte son étiquette.

     Rédigez, c'est tout.
     ───────────────────────────────────────────────────────────────── -->


## 1. Question de recherche

**Question :**
<!-- Une ou deux phrases. Une question, pas un sujet : « sémaglutide et
     insuffisance rénale » est un sujet ; « la sémaglutide diminue-t-elle
     le risque d'insuffisance rénale chronique chez les patients
     diabétiques de type 2 » est une question. -->


## 2. Pertinence clinique

<!-- Quelle décision cette recherche doit éclairer, et pour qui. Deux ou
     trois phrases. Ce n'est pas un paragraphe sur l'importance générale
     du sujet : c'est ce qui change selon la réponse trouvée. -->


## 3. Plan de concepts

**Base(s) de données interrogée(s) :**
<!-- Nommez-les ici. Le détail de chaque interrogation va en section 5. -->

<!-- Le plan de concepts est votre matrice de travail. Il tient dans un
     seul bloc de code, un concept après l'autre, parce que vos
     descripteurs contiennent des crochets, des guillemets et des
     virgules que seul un bloc de code préserve intacts.

     Trois lignes par concept, toujours dans cet ordre :

       Langage simple         le concept en français courant, un seul terme
       Vocabulaire contrôlé   les descripteurs du thésaurus de la base
       Vocabulaire libre      les mots-clés en texte, avec leurs champs

     Une valeur par ligne. Quand il y en a plusieurs, alignez-les sous
     la première — ne les séparez pas par des virgules, elles se
     confondraient avec celles des descripteurs.

     Dupliquez autant de blocs CONCEPT que nécessaire. Trois sont
     fournis ; supprimez ceux qui ne servent pas plutôt que d'en
     ajouter — supprimer casse moins que copier.

     Le modèle complet se trouve sous le bloc. -->

```
CONCEPT 1 ─
  Langage simple        
  Vocabulaire contrôlé  
  Vocabulaire libre     

CONCEPT 2 ─
  Langage simple        
  Vocabulaire contrôlé  
  Vocabulaire libre     

CONCEPT 3 ─
  Langage simple        
  Vocabulaire contrôlé  
  Vocabulaire libre     
```

<!-- Modèle, pour la forme attendue :

CONCEPT 1 ─ Médicament
  Langage simple        sémaglutide
  Vocabulaire contrôlé  "Semaglutide"[Mesh]
  Vocabulaire libre     semaglutide[tiab]
                        rybelsus[tiab]
                        wegovy[tiab]
                        ozempic[tiab]

CONCEPT 2 ─ Atteinte rénale
  Langage simple        insuffisance rénale chronique
  Vocabulaire contrôlé  "Renal Insufficiency, Chronic"[Mesh:NoExp]
                        "Kidney Failure, Chronic"[Mesh:NoExp]
  Vocabulaire libre     chronic kidney disease[tiab]
                        renal insufficiency chronic[tiab]
-->

### Justification du plan

<!-- Un bloc par concept, numéroté comme ci-dessus. C'est ici qu'on
     évalue votre raisonnement : le bloc de code dit QUOI, cette
     section dit POURQUOI.

     La précision et l'exhaustivité du vocabulaire contrôlé d'une part,
     du vocabulaire libre d'autre part, sont évaluées séparément. D'où
     les deux rubriques distinctes. -->

#### Concept 1 —

- **Portée retenue :**
  <!-- Ce que le concept inclut, et surtout ce qu'il exclut. Une
       frontière mal posée se paie plus tard, en bruit ou en silence. -->
- **Vocabulaire contrôlé — choix des descripteurs :**
  <!-- Pourquoi ces descripteurs plutôt que d'autres. Sont-ils ceux de
       la base déclarée ? MeSH, CINAHL Headings et Emtree ne sont pas
       interchangeables. En manque-t-il un, évident, pour ce concept ? -->
- **Explode :** oui / non — pourquoi :
  <!-- Pour chaque descripteur où la question se pose. Exploser ramène
       tous les termes plus spécifiques : c'est un choix d'exhaustivité,
       pas un réflexe. L'inverse non plus : NoExp se justifie. -->
- **Vocabulaire libre — choix des mots-clés et des champs :**
  <!-- Pourquoi ces synonymes en plus du vocabulaire contrôlé. Avez-vous
       couvert les variantes orthographiques, les usages britannique et
       américain, les noms commerciaux ? Pourquoi ces champs — titre,
       résumé et mots-clés d'auteur plutôt que tous les champs ? Où
       avez-vous placé vos troncatures, et pourquoi là ? -->

#### Concept 2 —

- **Portée retenue :**
- **Vocabulaire contrôlé — choix des descripteurs :**
- **Explode :** oui / non — pourquoi :
- **Vocabulaire libre — choix des mots-clés et des champs :**


## 4. Articles de consensus

<!-- Les articles dont vous savez d'avance qu'ils répondent à votre
     question, et qui servent à valider la stratégie : si votre équation
     ne les repêche pas, c'est qu'elle a un trou.

     Ce n'est pas la même chose que les références retenues de la
     section 10, qui sont le résultat de votre tri.

     Pour chacun : la référence complète, puis dites si votre stratégie
     finale le retrouve. Un article de consensus manqué est une
     information, pas un échec — expliquez pourquoi. -->

1. **Référence :**
   - **Repêché par la stratégie finale :** oui / non — si non, pourquoi :

2. **Référence :**
   - **Repêché par la stratégie finale :** oui / non — si non, pourquoi :


## 5. Stratégies exécutées

<!-- Une section par base interrogée. C'est la partie qui rend votre
     travail reproductible : quelqu'un doit pouvoir rejouer votre
     recherche à partir de ces seules lignes.

     Collez l'historique tel que la plateforme vous le donne, dans le
     bloc de code.

     NE RENUMÉROTEZ RIEN, NE RÉORDONNEZ RIEN. PubMed exporte son
     historique du plus récent au plus ancien : votre dernière ligne
     apparaît en premier. C'est normal. Vos lignes de combinaison
     renvoient à des numéros — #1 OR #2 — et les toucher casse le
     renvoi.

     Si votre export contient les colonnes « Sort By », « Filters »,
     « Search Details » et « Time », gardez « Search Details » : c'est
     la traduction exacte de votre requête par la plateforme, et c'est
     elle qui prouve la reproductibilité. « Time » ne sert à rien. -->

### Base 1 —

<!-- Le nom exact, le segment et la couverture, tels qu'affichés par la
     plateforme. Exemples : PubMed, ou Ovid MEDLINE(R) ALL <1946 au
     28 mai 2026> -->

- **Plateforme et interface :** <!-- PubMed, Ovid, EBSCO, interface native… -->
- **Mode d'interrogation :** <!-- Advanced ou Basic -->
- **Date d'exécution :** <!-- format AAAA-MM-JJ, tirets compris -->

**Historique de recherche**

```
#    Requête                                                      Résultats
```

<!-- Modèle — export PubMed, ordre décroissant conservé :

#    Requête                                                      Résultats
16   ((#1 OR #2 OR #3 OR #4 OR #5) AND (#7 OR #8 OR #9 OR #10))
     AND (#12 OR #13 OR #14)                                            192
15   #12 OR #13 OR #14                                               285 709
14   Non-Insulin-Dependent Diabetes[Title/Abstract]                    8 807
12   "Diabetes Mellitus, Type 2"[Mesh:NoExp]                         203 287
11   #7 OR #8 OR #9 OR #10                                           205 482
 7   "Renal Insufficiency, Chronic"[Mesh:NoExp]                       47 825
 6   #1 OR #2 OR #3 OR #4 OR #5                                        5 726
 1   semaglutide[MeSH Terms]                                           2 398

Modèle — export Ovid, ordre croissant, blocs de concepts nommés
entre crochets selon la convention professionnelle :

#    Recherche                                                    Résultats
1    exp Cardiac Surgical Procedures/                               256 597
2    (cardiac* or cardiothorac*).ti,ab,kf.                          453 322
3    or/1-2  [chirurgie cardiothoracique]                           770 224
4    simulation training/                                             8 049
5    3 and 4  [croisement]                                            2 431
6    limit 5 to yr="2000 -Current"  [résultats retenus]               2 277
-->

**Traduction de la requête par la plateforme** <!-- « Search Details » chez PubMed. Facultatif si votre plateforme n'en fournit pas. -->

```
```

**Filtres appliqués :**
<!-- Renvoyez au numéro de la ligne de l'historique, et justifiez.
     Par exemple : « ligne 8, années 2000 et suivantes — la molécule
     n'était pas commercialisée avant ». Ou : aucun filtre, et pourquoi.
     Un filtre de langue ou de date exclut des références : il se
     justifie, il ne se subit pas.
     Ne recopiez pas la syntaxe ici — elle est dans l'historique. -->

**Légende des opérateurs employés**

```
Ne gardez que ce que vous avez réellement utilisé.
```

<!-- Modèle PubMed :

[Mesh]           terme d'indexation, avec explosion automatique
[Mesh:NoExp]     terme d'indexation, sans les termes plus spécifiques
[tiab]           titre et résumé
[Title/Abstract] idem, forme longue
[tw]             tous les champs textuels
*                troncature à droite

Modèle Ovid :

ti = titre          ab = résumé          kf = mot-clé d'indexation
/           terme d'indexation (descripteur)
exp         le descripteur et tous ses termes plus spécifiques
adj3        mots à trois positions ou moins l'un de l'autre, tout ordre
*           toutes les variantes de suffixe de la racine
-->

### Base 2 —

- **Plateforme et interface :**
- **Mode d'interrogation :**
- **Date d'exécution :**

**Historique de recherche**

```
#    Requête                                                      Résultats
```

**Filtres appliqués :**

**Légende des opérateurs employés**

```
```

### Dédoublonnage

<!-- Combien de références au total, combien après retrait des doublons,
     et par quel moyen. Si vous n'avez interrogé qu'une seule base,
     écrivez-le. -->

- **Total avant dédoublonnage :**
- **Total après :**
- **Moyen employé :** <!-- fonction de la plateforme, Zotero, EndNote… -->


## 6. Critères d'inclusion et d'exclusion

<!-- Ce qui a servi à trier les résultats, pas ce qui a servi à les
     trouver. Les filtres de la section 5 sont autre chose. -->

**Inclusion**

- Critère — justification :

**Exclusion**

- Critère — justification :


## 7. Journal de recherche

<!-- Consignez chaque tentative, y compris celles qui n'ont rien donné :
     les impasses font partie du raisonnement et sont évaluées. Un bloc
     par tentative. -->

### 2026-MM-JJ —

- **Ce que nous avons essayé :**
- **Résultats obtenus :**
- **Ce que nous en avons tiré :**


## 8. Ajustements et améliorations proposées

<!-- Deux choses, et la seconde est évaluée pour elle-même.

     D'abord ce que vous avez modifié en cours de route, et pourquoi.

     Ensuite ce que vous amélioreriez en reprenant depuis le début :
     quelle est la limite connue de votre stratégie, et qu'est-ce qui
     la lèverait. Une proposition d'amélioration pertinente vaut mieux
     qu'une stratégie présentée comme parfaite. -->

**Ce que nous avons ajusté en cours de route :**

**Ce que nous améliorerions :**

**Limite connue de notre stratégie :**


## 9. Déclaration de l'usage de l'intelligence artificielle générative

<!-- Cette section est obligatoire et elle est évaluée. Elle se remplit
     même si vous n'avez rien utilisé — dans ce cas, écrivez-le.

     L'autorisation de l'enseignante est requise avant tout usage, et le
     plan de cours prime sur ce qui est écrit ici.

     Nommez l'outil et sa version, dites à quelle étape il a servi et ce
     que vous en avez fait, puis ce que vous avez vérifié vous-mêmes. Un
     outil qui propose des descripteurs ou des synonymes n'est pas un
     outil qui les valide : la vérification dans le thésaurus vous
     revient.

     La boîte à outils des bibliothèques explique comment citer,
     signaler et déclarer :
     https://boite-outils.bib.umontreal.ca/trouver-evaluer/iag -->

- **Outil(s) et version :** <!-- ou : aucun usage -->
- **À quelle étape :**
- **Ce que nous en avons fait :**
- **Ce que nous avons vérifié nous-mêmes :**


## 10. Références retenues

<!-- Le résultat de votre tri, selon le style de citation demandé dans
     le plan de cours. À distinguer des articles de consensus de la
     section 4, qui servaient à valider la stratégie.

     Un PMID compte huit chiffres, autant qu'un matricule. Le contrôle
     automatique l'accepte seulement s'il porte son étiquette, comme
     dans « PMID : » ou « PMID: ». Un identifiant tout seul sera refusé.
     Les DOI et les liens PubMed complets passent sans problème. -->

1.
2.
3.


## 11. Filiation

<!-- Si ce travail dérive d'une stratégie déjà versée dans le
     repository, collez son permalien ici et dites ce que vous en avez
     repris. Sinon, écrivez : travail original. -->
