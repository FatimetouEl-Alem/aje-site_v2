# Agence judiciaire de l'État — Site institutionnel

Site statique bilingue (français / arabe), sans dépendance ni étape de compilation.

## Structure

```
index.html                  Page d'accueil et point d'entrée de toutes les pages
assets/css/styles.css       Styles d'origine (accueil, en-tête, pied de page, composants)
assets/css/pages.css        Design des pages intérieures (limité à #site-view)
assets/css/header.css       En-tête compact et menu responsive (chargé en dernier)
assets/js/main.js           Navigation, contenus FR/AR, rendu des pages intérieures
assets/img/                 Logo, favicon, photos d'actualités, couvertures de publications
```

## Pages

Toutes les pages sont servies par `index.html` grâce aux adresses `#/…` :

| Page | Adresse |
|---|---|
| Accueil | `#/accueil` |
| L'Agence | `#/agence` |
| Mot de l'Agent judiciaire | `#/mot-agent` |
| Cadre juridique | `#/juridique` |
| Guide des administrations | `#/guide` |
| Transmettre un dossier | `#/dossier` |
| Règlement amiable | `#/amiable` |
| Jurisprudence / fiche décision | `#/jurisprudence`, `#/decision/0` |
| Publications / fiche publication | `#/publications`, `#/publication/0` |
| Actualités / article | `#/actualites`, `#/actualite/0` |
| Contact | `#/contact` |
| Espace administrations (Mizan) | `#/connexion` |
| Mentions légales | `#/mentions` |
| Protection des données | `#/confidentialite` |
| Accessibilité | `#/accessibilite` |
| Guide d'identité visuelle | `#/identite` |
| Recherche | `#/recherche?q=…` |

La langue peut être forcée avec `?lang=ar` ou `?lang=fr`.

## Tester en local

Ouvrir directement `index.html` dans un navigateur, ou lancer un petit serveur :

```bash
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

## Mettre en ligne

Le dossier peut être déposé tel quel sur n'importe quel hébergement statique
(GitHub Pages, GitLab Pages, Netlify, Apache, Nginx…). Aucune réécriture d'URL
n'est nécessaire.

```bash
git init
git add .
git commit -m "Site AJE"
git branch -M main
git remote add origin <URL-du-dépôt>
git push -u origin main
```

## À compléter avant publication

- Coordonnées officielles (adresse, téléphone, courriel) dans `assets/js/main.js`
- Identité et texte de l'Agent judiciaire
- Textes juridiques, décisions et publications officiels (PDF)
- Couvertures réelles : remplacer les fichiers de `assets/img/publications/`
- Les chiffres de l'accueil sont marqués « d'illustration »
