# Kikinatset Production

Page portail qui rassemble tous mes projets, avec deux onglets :

- **On joue directement** : liens vers les jeux en ligne (GitHub Pages).
- **On télécharge et on joue** : fichiers `.html` / `.zip` à télécharger.

## Ajouter ou modifier un projet

Tout se passe dans [`projects.json`](projects.json). Chaque projet ressemble à ça :

```json
{
  "id": "mon-jeu",
  "titre": "Mon jeu",
  "description": "Une phrase pour donner envie.",
  "onglet": "jouer",
  "url": "https://kevm29.github.io/MonJeu/",
  "depot": "https://github.com/kevm29/MonJeu",
  "tags": ["Action", "2 joueurs"],
  "emoji": "🚀",
  "couleur": "#f59e0b"
}
```

| Champ | Rôle |
| --- | --- |
| `onglet` | `"jouer"` (lien en ligne) ou `"telecharger"` (fichier à télécharger) |
| `url` | pour l'onglet `jouer` : l'adresse du jeu |
| `fichier` | pour l'onglet `telecharger` : un fichier du dossier [`telechargements/`](telechargements/) (ex. `telechargements/mon-jeu.html`) ou une adresse complète (ex. le `.zip` d'un dépôt) |
| `libelleFichier` | (facultatif) texte du bouton, par défaut « Télécharger ⬇ » |
| `depot` | (facultatif) lien vers le code, affiche un bouton « Code » |
| `image` | (facultatif) une image de couverture à la place de l'emoji |
| `emoji`, `couleur`, `tags` | l'apparence de la carte |

Un fichier local manquant affiche « Bientôt disponible » au lieu du bouton.

## Voir la page en local

`projects.json` est chargé par la page, donc il faut un petit serveur (le double-clic sur `index.html` ne suffit pas) :

```sh
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

## Mise en ligne

Settings → Pages → *Deploy from a branch* → `main` / `(root)`.
La page sera sur https://kevm29.github.io/KikinatsetProduction/
