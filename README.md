<<<<<<< HEAD
# 📦 Blog Platform - Installation Guide

## 🚀 Quick Start

### Prerequisites
- Docker Desktop installed
- Git
- 8GB RAM minimum

### Installation Steps

```bash
# 1. Navigate to project folder
cd project

# 2. Start Docker containers
docker-compose up -d

# 3. Wait for containers to start (30-60 seconds)
docker ps

# 4. Install backend dependencies
docker exec -it blog_backend composer install

# 5. Setup Laravel
docker exec -it blog_backend cp .env.example .env
docker exec -it blog_backend php artisan key:generate

# 6. Run migrations and seeders
docker exec -it blog_backend php artisan migrate:fresh --seed

# 7. Install frontend dependencies (if needed)
docker exec -it blog_frontend npm install
```

### 🌐 Access the Application

- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:8000/api
- **MySQL**: localhost:3306

---

## 🛠️ Useful Commands

### Backend Commands

```bash
# Access backend container
docker exec -it blog_backend bash

# Run migrations
docker exec -it blog_backend php artisan migrate

# Seed database
docker exec -it blog_backend php artisan db:seed

# Clear cache
docker exec -it blog_backend php artisan cache:clear

# View logs
docker logs blog_backend -f
```

### Frontend Commands

```bash
# Access frontend container
docker exec -it blog_frontend sh

# Rebuild frontend
docker exec -it blog_frontend npm run build

# View logs
docker logs blog_frontend -f
```

### Database Commands

```bash
# Access MySQL
docker exec -it blog_mysql mysql -u blog_user -p
# Password: blog_password

# Backup database
docker exec blog_mysql mysqldump -u blog_user -pblog_password blog_db > backup.sql

# Restore database
docker exec -i blog_mysql mysql -u blog_user -pblog_password blog_db < backup.sql
=======
# 🚀 Challenge Technique - Développeur Full Stack

Ce challenge simule une situation réelle que vous rencontrerez en entreprise : **rejoindre une équipe et résoudre des problèmes sur une application existante**.

Contrairement aux exercices traditionnels où vous créez une application from scratch, ici vous devez :
- ✅ Comprendre du code existant
- 🐛 Identifier et corriger des bugs
- 🔒 Résoudre des failles de sécurité
- ⚡ Optimiser les performances
- 🔧 Mettre à jour des dépendances

**C'est exactement ce que vous ferez 80% du temps en tant que développeur !**

---

## 🎯 Objectif

Vous recevez une **plateforme de gestion de blog** fonctionnelle (Laravel + React + MySQL) avec plusieurs problèmes à résoudre.

**Mission** : Résoudre au moins **70% des tickets** du backlog pour être invité à l'entretien oral.

---

## 📁 Structure du challenge

```
/fullstack-challenge/
├── README.md                 ← Vous êtes ici
├── CHALLENGE.md              ← Description détaillée du challenge
├── TICKETS.md                ← Liste des tickets à résoudre (votre mission)
└── /project/                 ← Le code source de l'application
>>>>>>> 22516913bc1a4bb1766e61e8ab3d945cf30a41c3
```

---

<<<<<<< HEAD
## 🔄 Restart / Stop

```bash
# Stop all containers
docker-compose down

# Stop and remove volumes (⚠️ deletes database)
docker-compose down -v

# Restart containers
docker-compose restart

# Rebuild containers (after Dockerfile changes)
docker-compose up -d --build
```

---

## 📁 Project Structure

```
/project/
├── docker-compose.yml          # Docker orchestration
├── backend/                    # Laravel API
│   ├── app/
│   │   ├── Models/            # Database models
│   │   ├── Http/Controllers/  # API controllers
│   │   └── ...
│   ├── database/
│   │   ├── migrations/        # Database schema
│   │   └── seeders/           # Sample data
│   ├── routes/api.php         # API routes
│   └── .env.example
├── frontend/                   # React application
│   ├── src/
│   │   ├── components/        # React components
│   │   ├── services/          # API calls
│   │   └── App.jsx
│   └── package.json
└── README.md                   # This file
```

## 📞 Need Help?

If you're stuck:
1. Check Docker logs: `docker logs blog_backend -f`
2. Verify all containers are running: `docker ps`
3. Check the main CHALLENGE.md for more details

---

Good luck! 🚀
=======
## 🚦 Démarrage rapide

### 1. Lisez la description complète
👉 **[Consultez CHALLENGE.md](./CHALLENGE.md)** pour comprendre le contexte et les règles

### 2. Consultez les tickets à résoudre
👉 **[Consultez TICKETS.md](./TICKETS.md)** pour voir la liste des problèmes à corriger

### 3. Forkez le repository (IMPORTANT - à faire en premier !)
👉 **Forkez** https://github.com/voidagency/stages-fullstack-challenge.git sur votre compte GitHub

Cliquez sur le bouton **"Fork"** en haut à droite du repository GitHub.

### 4. Clonez VOTRE fork et lancez l'application

Suivez les instructions détaillées dans **[CHALLENGE.md](./CHALLENGE.md)** section "Instructions de Travail"

### 5. Résolvez les tickets
- Créez une branche par ticket (`BUG-001`, `SEC-002`, etc.)
- Committez régulièrement avec des messages clairs
- Créez une Pull Request pour chaque ticket résolu
- Mergez vos PRs dans votre branche `main`

### 6. Soumettez votre travail
📌 **Livrable** : Lien vers votre fork GitHub avec toutes les PRs mergées

Voir **[CHALLENGE.md](./CHALLENGE.md)** pour les détails du workflow Git

---

## ⏱️ Durée

**Format flexible** : Prenez le temps nécessaire, vous pouvez travailler en plusieurs sessions.

Temps estimé : **8-10 heures** selon votre niveau.

---

## 🆘 Besoin d'aide ?

- 📖 Consultez la documentation officielle (Laravel, React, Docker)
- 🤖 **Vous pouvez utiliser l'IA** (ChatGPT, Copilot, etc.) - voir CHALLENGE.md
- 🔍 Google, StackOverflow sont vos amis

## 🎓 Technologies utilisées

- **Backend** : PHP 7.4, Laravel 10
- **Frontend** : React 18, Vite
- **Base de données** : MySQL 8
- **Infrastructure** : Docker, Docker Compose

---

## 🤝 Bonne chance !

Ce challenge teste vos compétences réelles de développeur. Montrez-nous votre capacité à :
- 🔍 Analyser et comprendre du code existant
- 🐛 Débugger méthodiquement
- 🛠️ Proposer des solutions robustes
- 📝 Communiquer clairement vos choix

**Prêt ? Rendez-vous dans [CHALLENGE.md](./CHALLENGE.md) !** 🚀
>>>>>>> 22516913bc1a4bb1766e61e8ab3d945cf30a41c3

