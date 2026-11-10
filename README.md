# 🧮 Simulateur de note au bac général, session 2027

**Le bac compté en points : les notes de 1re, des hypothèses pour la terminale, et ce qu'il reste à obtenir pour chaque mention.** Pour les élèves de terminale générale et leur professeur·e principal·e.

> Chaque élève saisit ses moyennes de 1re, semestre par semestre, et ses notes des épreuves anticipées, puis imagine sa terminale : note visée, moyenne actuelle, note d'un bac blanc. Le simulateur compte en points (2 000 au total, 1 000 pour avoir le bac) et dit **quelle moyenne il faut encore obtenir** pour le bac et pour chaque mention. Une case laissée vide devient une inconnue : la page calcule la note nécessaire dessus. Une bulle « ? » détaille chaque calcul, avec les notes de l'élève.

## 👉 [Essayer maintenant : babash.github.io/simulateur-bac](https://babash.github.io/simulateur-bac/)

**Gratuit · sans compte · rien à installer · aussi sur téléphone · ce qui est saisi reste dans le navigateur**

Le simulateur de note au bac fait partie des [Ressources NSI et SNT](https://babash.github.io/Babash-NSI-SNT/), rubrique [Professeur principal](https://babash.github.io/Babash-NSI-SNT/pp/).

---

## Ce que font les élèves

La page avance en quatre étapes, avec un bandeau en bas de l'écran qui donne les points, la moyenne et ce qui manque pour la mention suivante.

| Étape | Ce que fait l'élève |
|---|---|
| **1. Ton parcours** | Choisir ses deux spécialités de terminale, la spécialité arrêtée en fin de 1re, ses langues vivantes A et B et ses options : les intitulés et le total des coefficients suivent. |
| **2. Tes notes de 1re (acquises)** | Saisir les moyennes des semestres S1 et S2 de chaque matière du contrôle continu (la moyenne annuelle est calculée ; un seul semestre sert d'estimation), puis les notes des épreuves anticipées de français et de maths. |
| **3. Ta terminale (simulation)** | Faire des hypothèses, matière par matière, ou d'un coup : **Remplir les cases vides de terminale avec une même note**, **Reprendre mes moyennes de 1re en terminale**. Les cases laissées vides restent à calculer. |
| **4. Ton bilan en points** | Lire ses points sur 2 000 et sa mention, les points restant à gagner par matière, la moyenne nécessaire pour chaque objectif (rattrapage, bac, mentions), le poids du contrôle continu et des épreuves, et l'oral de rattrapage. |

Le simulateur d'oral de rattrapage choisit les paires d'épreuves qui rapporteraient le plus, et donne la note nécessaire.

## Pour quels usages

| Usage | Comment |
|---|---|
| **Sur téléphone** | La page est pensée d'abord pour le téléphone, avec un mode sombre automatique. |
| **Après un bac blanc** | Les notes du bac blanc deviennent des hypothèses de terminale : le bilan montre tout de suite ce qu'elles donnent. |
| **Pour viser une mention** | « Ce qu'il te reste à obtenir » donne, pour chaque mention, les points nécessaires et la moyenne à avoir sur ce qui reste. |
| **Sur plusieurs mois** | Les notes restent dans le navigateur de l'appareil (un cookie d'un an et une copie locale) : l'élève les complète à chaque bulletin. **Effacer toutes mes notes** les supprime. |

## Pourquoi ça marche

- **Des points plutôt qu'une moyenne** : les points de 1re sont acquis, et l'élève voit ceux qui restent en jeu.
- **Un objectif chiffré** : la moyenne nécessaire sur ce qui reste, pour le bac et pour chaque mention.
- **Chaque calcul expliqué** : les bulles « ? » détaillent le calcul avec les notes de l'élève.
- **Une simulation honnête** : la page rappelle que le contrôle continu peut être harmonisé, et que seul le jury délivre le diplôme et les mentions.
- **Rien à créer, rien d'envoyé** : ni compte ni serveur ; les notes restent sur l'appareil, et la page ne contacte aucun autre site (même ses polices sont dans le dépôt).

## Chaque rentrée : les coefficients

Les coefficients de la voie générale, session 2027, tels que le simulateur les utilise :

| Bloc | Matière | Coefficient |
|---|---|---|
| Contrôle continu (40) | Histoire-géographie, LVA, LVB, enseignement scientifique | 3 en 1re + 3 en terminale, pour chacune |
| | EMC | 1 + 1 |
| | EPS (terminale) | 6 |
| | Spécialité arrêtée en 1re | 8 |
| Épreuves (60) | Français écrit / oral | 5 / 5 |
| | Maths anticipées (nouveauté 2027) | 2 |
| | Spécialité 1 / spécialité 2 | 16 / 16 |
| | Philosophie | 8 |
| | Grand oral (10, puis 8 en 2027) | 8 |
| Options (en plus des 100) | 2 par année suivie | 2 ou 4 |

Les sources officielles, celles du pied de la page :
- sur education.gouv.fr : [le calcul de la note du bac](https://www.education.gouv.fr/reussir-au-lycee/comment-calculer-votre-note-au-baccalaureat-325511) (coefficients 2027, options) et [les questions sur le bac](https://www.education.gouv.fr/reussir-au-lycee/tout-savoir-sur-le-baccalaureat-les-reponses-vos-questions-325499) (rattrapage) ;
- sur Éduscol : [les épreuves terminales du bac général](https://eduscol.education.gouv.fr/5706/les-epreuves-terminales-du-baccalaureat-general) et [l'épreuve anticipée de mathématiques](https://eduscol.education.gouv.fr/5688/epreuve-anticipee-de-mathematiques-aux-baccalaureats-general-et-technologique) ;
- au Bulletin officiel : [BO n° 13 du 27 mars 2026](https://www.education.gouv.fr/bo/2026/Hebdo13/MENE2607843N) (points du jury limités à 50).

Vérifie ces pages à chaque rentrée. Si un coefficient change, il suffit de modifier la fonction `buildItems()` dans `index.html`.

## Pour aller plus loin

### Mettre ta copie en ligne

Le simulateur tient dans `index.html`, plus ses polices dans le dossier `fonts/` : aucune dépendance extérieure.

1. Crée un dépôt GitHub public, par exemple `simulateur-bac`.
2. Dépose `index.html` et le dossier `fonts/` à la racine : **Add file → Upload files** (le dossier se glisse tel quel dans la page), puis **Commit changes**.
3. Dans **Settings → Pages**, choisis **Deploy from a branch**, la branche `main` et le dossier `/ (root)`, puis **Save**.
4. Une à deux minutes plus tard, le site est en ligne : `https://<ton-pseudo>.github.io/simulateur-bac/`.

Pour le mettre à jour, modifie `index.html` dans le dépôt (icône crayon) et valide : GitHub Pages republie le site tout seul.

## Contact

Conçu par Babash - NSI Tani Malandi pour les classes de terminale générale de l'académie de Mayotte, développé avec l'aide de l'IA ([Claude Code](https://claude.com/claude-code)).
Une question, une idée, un bug ? Les [issues GitHub](https://github.com/babash/simulateur-bac/issues) du dépôt. Toutes les ressources sont sur le site [Ressources NSI et SNT](https://babash.github.io/Babash-NSI-SNT/).

## Licence

- **Le code** (le fichier `index.html`, sauf ses textes d'explication) est sous licence [MIT](LICENSE).
- **Les documents** (les textes d'explication de la page, dont les bulles « ? », et ce README) sont sous licence [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.fr).
- **Les polices** Atkinson Hyperlegible (Braille Institute of America) et Caveat (The Caveat Project Authors) : licence SIL OFL 1.1, hébergées dans `fonts/` avec leur licence ([Atkinson Hyperlegible](fonts/LICENCE-atkinson-hyperlegible.txt), [Caveat](fonts/LICENCE-caveat.txt)) ; fichiers repris de [Fontsource](https://fontsource.org).

Tu peux les réutiliser et les modifier, y compris pour tes classes, en mentionnant Babash - NSI Tani Malandi et la licence ; un document modifié se partage sous la même licence. Si tu utilises l'IA pour les modifier, merci de le préciser.
