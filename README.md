# Simulateur de note au bac général — session 2027

Site statique (un seul fichier `index.html`, sans dépendance) pour les élèves de terminale générale.

## Fonctions
- Saisie par semestre (S1 et S2) pour tout le contrôle continu et les options, en 1re comme en terminale : la moyenne annuelle est calculée automatiquement ((S1 + S2) ÷ 2), et un seul semestre saisi sert d'estimation
- Épreuves anticipées de français et de maths, EPS (note unique de CCF)
- Simulation de la terminale (contrôle continu, spécialités, philo, Grand oral, options), avec une hypothèse « même note pour les cases vides »
- Système en points : points obtenus, points encore en jeu, points restant à obtenir pour le bac et chaque mention, moyenne nécessaire sur ce qui reste
- Mentions (12 / 14 / 16 / 18) et simulateur d'oral de rattrapage (meilleures paires d'épreuves, note nécessaire)
- Bulles « ? » qui détaillent chaque calcul avec les notes de l'élève
- Sauvegarde automatique dans un cookie `simubac2027` (+ copie localStorage), bouton pour tout effacer
- Responsive (mobile d'abord), mode sombre automatique

## Coefficients utilisés (voie générale, session 2027)
| Bloc | Matière | Coef |
|---|---|---|
| Contrôle continu (40) | Histoire-géo, LVA, LVB, Enseignement scientifique | 3 en 1re + 3 en tle chacune |
| | EMC | 1 + 1 |
| | EPS (terminale) | 6 |
| | Spécialité arrêtée en 1re | 8 |
| Épreuves (60) | Français écrit / oral | 5 / 5 |
| | Maths anticipées (nouveauté 2027) | 2 |
| | Spécialité 1 / Spécialité 2 | 16 / 16 |
| | Philosophie | 8 |
| | Grand oral (10 → 8 en 2027) | 8 |
| Options (en plus des 100) | 2 coef par année suivie | 2 ou 4 |

Sources : education.gouv.fr (« Comment calculer votre note au baccalauréat », « Tout savoir sur le baccalauréat »), Éduscol (épreuves terminales, épreuve anticipée de maths), BO n°13 du 27 mars 2026 (points du jury).
Pensez à vérifier ces pages à chaque rentrée : si un coefficient change, il suffit de modifier la fonction `buildItems()` dans `index.html`.

## Mettre en ligne sur GitHub Pages
1. Créer un dépôt GitHub (ex. `simulateur-bac`), public.
2. Y déposer `index.html` (et ce README) à la racine : bouton **Add file → Upload files**, puis **Commit changes**.
3. Aller dans **Settings → Pages**, choisir **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**.
4. Après une à deux minutes, le site est disponible à `https://<votre-pseudo>.github.io/simulateur-bac/`.

Pour mettre à jour : modifier `index.html` dans le dépôt (icône crayon) et valider ; GitHub Pages se redéploie tout seul.
