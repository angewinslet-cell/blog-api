Blog API

API RESTful de gestion d'articles de blog développée avec Node.js et SQLite. Permet de créer, consulter, filtrer et gérer des articles.

📋 Table des matières

· Fonctionnalités
· Technologies utilisées
· Prérequis
· Installation
· Configuration
· Utilisation
· Structure du projet
· Documentation de l'API
· Auteur

✨ Fonctionnalités

· ✅ Création d'articles (titre, contenu, auteur, catégorie, tags)
· ✅ Consultation de tous les articles
· ✅ Filtrage des articles par :
  · Catégorie
  · Auteur
  · Date
· ✅ Base de données SQLite légère et autonome

🛠️ Technologies utilisées

· Node.js - Environnement d'exécution JavaScript
· SQLite - Base de données relationnelle légère
· JavaScript (ES6) - Langage de programmation

📦 Prérequis

· Node.js (version 14 ou supérieure)
· npm (gestionnaire de paquets)

🔧 Installation

1. Cloner le dépôt
  
   git clone https://github.com/angewinslet-cell/blog-api.git
   cd blog-api
   
2. Installer les dépendances
  
   npm install
   
3. Configurer la base de données
   · Assurez-vous que le fichier de configuration config/db.js est correctement paramétré
   · La base de données SQLite sera créée automatiquement au premier lancement
4. Lancer l'application
  
   npm start
   
   ou en mode développement :
  
   npm run dev
   
⚙️ Configuration

Créez un fichier .env à la racine du projet (optionnel) :

PORT=3000
DB_PATH=./database/blog.db
📁 Structure du projet

blog-api/
├── config/
│   └── db.js              # Configuration de la base de données
├── models/
│   └── ArticleModel.js    # Modèle de gestion des articles
├── controllers/
│   └── articleController.js # Logique métier
├── routes/
│   └── articleRoutes.js   # Routes de l'API
├── app.js                 # Point d'entrée de l'application
├── package.json
└── README.md
📚 Documentation de l'API

Créer un article

POST /api/articles
Corps de la requête :

{
  "titre": "Mon premier article",
  "contenu": "Contenu de l'article...",
  "auteur": "John Doe",
  "date": "2026-03-23",
  "categorie": "Technologie",
  "tags": "nodejs,api"
}
Récupérer tous les articles

GET /api/articles
Filtrer les articles

GET /api/articles?categorie=Technologie&auteur=John Doe&date=2026-03-23
Paramètres de filtre :

· categorie : Filtrer par catégorie
· auteur : Filtrer par nom d'auteur
· date : Filtrer par date (format YYYY-MM-DD)

👤 Auteur

Nzeusseu Angé Winslet - GitHub
