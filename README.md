# Atelier PDF

Application web, en une seule page, pour réorganiser des PDF **au niveau des pages** : retirer des pages, les réordonner, les dupliquer, les faire pivoter et fusionner plusieurs PDF dans l'ordre voulu.

Tout se passe dans le navigateur : aucun fichier n'est envoyé sur un serveur.

## Utilisation

Ouvre `index.html` dans un navigateur (double-clic), ou publie le dépôt avec GitHub Pages.

1. **Importer** : glisse des PDF n'importe où sur la page, ou clique sur « + Ajouter des PDF ». Chaque PDF reçoit une lettre (A, B, C…).
2. **Assembler** : fais glisser les miniatures de la colonne *Sources* vers la colonne *Assemblage*, puis réordonne-les. Un clic sur une page source l'ajoute à la fin.
3. **Retirer** : la croix sur une page, ou sélection puis `Suppr`.
4. **Exporter** : choisis un nom, puis clique sur « Exporter le PDF ».

### Séquence rapide

| Saisie | Résultat |
|---|---|
| `A2, C4-5, A1-80` | page 2 de A, pages 4 à 5 de C, pages 1 à 80 de A |
| `pdf1p2 → pdf3p4-5 → pdf1p1à80` | même chose (pdf1 = A, pdf3 = C) |
| `B7-fin` | de la page 7 à la dernière page de B |
| `A10-1` | pages 10 à 1 de A, dans l'ordre inverse |
| `B` | tout le PDF B |
| `A1-3+7` | pages 1, 2, 3 et 7 de A |

### Raccourcis

- Clic : sélectionner · Ctrl/Cmd+clic : ajouter à la sélection · Maj+clic : sélectionner une plage
- `Suppr` : retirer · `Ctrl+Z` / `Ctrl+Maj+Z` : annuler / rétablir · double-clic ou loupe : aperçu

## Technique

- [pdf.js](https://mozilla.github.io/pdf.js/) 3.11.174 pour les miniatures et les aperçus
- [pdf-lib](https://pdf-lib.js.org/) 1.17.1 pour assembler le PDF final
- [SortableJS](https://sortablejs.github.io/Sortable/) 1.15.2 pour le glisser-déposer

Les bibliothèques sont chargées depuis cdnjs : il faut donc une connexion internet. Les PDF protégés par mot de passe ne sont pas pris en charge.
