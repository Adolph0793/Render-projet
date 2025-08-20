# Projet Inscription Utilisateurs

## Description
Formulaire d'inscription en ligne avec backend Node.js/Express et base PostgreSQL. 
Les mots de passe sont hashés pour la sécurité. Frontend stylé avec Tailwind CSS.

## Installation

### Backend
1. Aller dans le dossier backend : `cd backend`
2. Installer les dépendances : `npm install`
3. Déployer sur Render/Railway
4. Ajouter la variable d'environnement `DATABASE_URL` avec l'URL PostgreSQL
5. Déployer le backend, URL publique fournie par Render

### Base de données
Exécuter la commande SQL pour créer la table `users` :
```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(150) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
