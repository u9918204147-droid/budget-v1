# Mon Budget

Application de gestion de budget personnel (React + TypeScript + Tailwind CSS + Recharts).
Toutes les données sont enregistrées dans le `localStorage` du navigateur : une fois l'app
déployée, tes chiffres restent stockés en permanence sur ton appareil, comme une vraie
application — pas de backend ni de compte requis.

## Développement local

Prérequis : [Node.js](https://nodejs.org) 18 ou plus.

```bash
npm install
npm run dev
```

L'application est alors disponible sur `http://localhost:5173`.

## Mettre le projet sur GitHub

```bash
git init
git add .
git commit -m "Première version de Mon Budget"
git branch -M main
git remote add origin https://github.com/<ton-utilisateur>/mon-budget.git
git push -u origin main
```

## Héberger gratuitement sur GitHub Pages

Deux façons de faire, au choix :

### Option A — avec le paquet `gh-pages` (le plus simple)

```bash
npm install
npm run deploy
```

Cette commande construit l'application puis pousse le résultat sur une branche `gh-pages`.
Ensuite, dans les paramètres du dépôt GitHub (**Settings → Pages**), choisis la branche
`gh-pages` comme source. Ton site sera disponible à l'adresse :

```
https://<ton-utilisateur>.github.io/mon-budget/
```

### Option B — avec GitHub Actions (déploiement automatique à chaque `push`)

Un workflow est fourni dans `.github/workflows/deploy.yml`. Il suffit d'activer GitHub Pages
avec la source **GitHub Actions** dans **Settings → Pages**, puis de pousser sur `main` :
le site se reconstruit et se met à jour automatiquement.

## Autres hébergements possibles

Le projet fonctionne aussi tel quel sur **Vercel** ou **Netlify** (détection automatique
d'un projet Vite : commande de build `npm run build`, dossier de sortie `dist`).

## Notes sur la persistance des données

- Les données sont propres à **chaque navigateur et appareil** (pas de synchronisation
  automatique entre ton téléphone et ton ordinateur).
- Vider le cache/les données de navigation du site effacera l'historique du budget.
- Pour changer d'appareil sans perdre tes données, tu peux exporter le contenu de
  `localStorage` (clé `mon-budget-data-v1`) et le réimporter ailleurs — une fonctionnalité
  d'export/import JSON peut être ajoutée facilement si tu en as besoin.
