🚗 Classic Cars – Application Web (Frontend + API REST)
📌 Présentation générale

Classic Cars est une application web permettant de gérer une collection de voitures classiques.
L’application repose sur une architecture Frontend / Backend et communique via une API REST sécurisée par clé API.

Le projet met en œuvre les concepts fondamentaux du développement web moderne. Il a été réalisé dans le cadre du module Développement Web du S9:

Fetch API

Async / Await

Architecture modulaire JavaScript

Communication Front ↔ API

Gestion des erreurs HTTP

Interface dynamique sans rechargement de page

🧩 Architecture du projet

Le projet est divisé en deux parties distinctes :

🔹 Backend (API REST)

Fournit les données des voitures

Gère les routes HTTP

Sécurisé par une clé API

Déployé sur Render

🔹 Frontend

Interface utilisateur responsive

Développée en HTML / CSS / JavaScript

Utilise Bootstrap 5

Communique avec l’API via fetch

Déployée sur GitHub Pages
✨ Fonctionnalités principales

📋 Affichage dynamique de la liste des voitures

🔍 Consultation du détail d’une voiture

➕ Ajout d’une voiture via un formulaire (modal Bootstrap)

🗑️ Suppression d’une voiture avec confirmation

⚠️ Gestion des erreurs (404, 500, réseau)

🔄 Mise à jour dynamique de l’interface (sans rechargement)

🔐 Authentification via API Key

🧪 Gestion du cas désynchronisé (ressource supprimée dans un autre onglet)

🛠️ Technologies utilisées
Frontend

HTML5

CSS3

Bootstrap 5

JavaScript ES6 (modules)

Backend

Node.js

Express.js

Outils

Git & GitHub

Render

GitHub 

📁 Organisation des fichiers (Frontend)

front/
│
├── index.html          # Page d’accueil (liste des voitures)
├── car.html            # Page de détail d’une voiture
│
├── js/
│   ├── config.js       # Configuration de l’API (URL, clé, endpoints)
│   ├── api.js          # Appels API (GET, POST, DELETE…)
│   ├── ui.js           # Gestion UI (loading, erreurs)
│   ├── dom.js          # Manipulation du DOM
│   ├── utils.js        # Fonctions utilitaires
│   ├── home.js         # Logique de index.html
│   ├── car-details.js  # Logique de car.html
│   └── script.js       # Point d’entrée principal
│
└── imgs/               # Images et assets

🚀 Installation et lancement en local
1️⃣ Lancer le backend (API)

À la racine du projet : 
npm install
npm start
L’API est accessible à l’adresse :http://localhost:3000/api

2️⃣ Lancer le frontend

Depuis le dossier front/ : npx live-server

Le site est accessible via l’URL indiquée dans le terminal.

⚙️ Configuration de l’API (Frontend)

Dans le fichier front/js/config.js :

export const API_CONFIG = {
  baseURL: "http://localhost:3000/api",
  apiKey: "ma-super-cle-api-2024",
  endpoints: {
    cars: "/cars",
  },
};

⚠️ Important
La clé API doit être envoyée dans les headers de chaque requête HTTP.

🔎 Gestion des erreurs
L’application gère plusieurs types d’erreurs :

❌ API inaccessible (erreur réseau)

❌ Erreurs HTTP (404, 500)

❌ Ressource inexistante (voiture supprimée)

❌ Données manquantes

Les erreurs sont :

affichées clairement à l’utilisateur

journalisées dans la console

gérées avec try / catch

👩‍💻 Auteurs

Esther Evelyne BEUGRE (TP3)