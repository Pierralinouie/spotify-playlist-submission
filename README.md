# Spotify Playlist Submission Platform

Application web permettant aux artistes de soumettre leurs titres à des playlists Spotify avec système de paiement intégré.

## Fonctionnalités

- Soumission de titres à des playlists Spotify
- Système de paiement intégré avec Stripe
- Choix de la position du titre dans la playlist
- Interface d'administration pour les curateurs
- Gestion des remboursements et factures

## Installation

1. Cloner le dépôt :
```bash
git clone https://github.com/Pierralinouie/spotify-playlist-submission.git
cd spotify-playlist-submission
```

2. Installer les dépendances :
```bash
# Frontend
cd frontend
npm install

# Backend
cd ../backend
npm install
```

3. Configurer les variables d'environnement :
Créer un fichier `.env` dans le dossier backend avec :
```env
SPOTIFY_CLIENT_ID=your_client_id
SPOTIFY_CLIENT_SECRET=your_client_secret
SPOTIFY_REDIRECT_URI=your_redirect_uri
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_WEBHOOK_SECRET=your_webhook_secret
MONGODB_URI=your_mongodb_uri
```

4. Démarrer l'application :
```bash
# Frontend
cd frontend
npm run dev

# Backend
cd ../backend
npm run dev
```

## Technologies utilisées

- Frontend : React, TailwindCSS, shadcn/ui
- Backend : Express.js, MongoDB
- API : Spotify Web API, Stripe API

## Structure du projet

```
├── frontend/             # Application React
│   ├── src/
│   │   ├── components/   # Composants React
│   │   ├── pages/        # Pages de l'application
│   │   └── services/     # Services API
│   └── package.json
│
└── backend/             # Serveur Express.js
    ├── src/
    │   ├── routes/      # Routes API
    │   ├── models/      # Modèles MongoDB
    │   └── services/    # Services métier
    └── package.json
```

## Configuration Spotify

1. Créer une application sur [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Configurer l'URL de redirection
3. Copier le Client ID et Client Secret dans le fichier `.env`

## Configuration Stripe

1. Créer un compte sur [Stripe Dashboard](https://dashboard.stripe.com)
2. Copier les clés API dans le fichier `.env`
3. Configurer le webhook Stripe pour les événements de paiement

## Contribution

Les contributions sont les bienvenues ! N'hésitez pas à ouvrir une issue ou soumettre une pull request.