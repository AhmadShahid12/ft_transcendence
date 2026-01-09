# ft_transcendence

Application web full-stack avec jeu Pong en ligne - Projet 42 Paris

## À propos

ft_transcendence est le projet final du cursus 42. C'est une application web complète qui inclut un jeu Pong en ligne, un système de tournois, un chat en temps réel, et bien plus encore.

C'est un projet ambitieux qui m'a permis de mettre en pratique toutes les compétences acquises : développement full-stack, gestion de bases de données, WebSockets, Docker, et architecture microservices.

## 🎮 Fonctionnalités

### Jeu Pong
- Jeu Pong en ligne en temps réel
- Mode local avec IA
- Système de matchmaking
- Statistiques de jeu

### Tournois
- Organisation de tournois
- Brackets automatiques
- Gestion des matchs

### Chat
- Chat en temps réel avec WebSockets
- Messages privés
- Canaux de discussion

### Profil utilisateur
- Authentification OAuth 42
- Authentification à deux facteurs (2FA)
- Statistiques personnelles
- Historique des matchs
- Amis et système de suivi

### Monitoring
- Dashboard Grafana
- Métriques Prometheus
- Logs centralisés avec Elasticsearch

## 🛠️ Technologies utilisées

### Backend
- **Node.js** avec Fastify
- **PostgreSQL** pour la base de données
- **WebSockets** pour le temps réel
- **OAuth 42** pour l'authentification

### Frontend
- **TypeScript**
- **Vite** comme build tool
- **WebSockets** pour la communication temps réel
- **Canvas API** pour le jeu Pong

### Infrastructure
- **Docker** et **Docker Compose**
- **Nginx** comme reverse proxy
- **Prometheus** pour les métriques
- **Grafana** pour la visualisation
- **Elasticsearch** et **Logstash** pour les logs

## 🚀 Installation

### Prérequis
- Docker et Docker Compose
- Node.js (pour le développement local)

### Configuration

1. Clonez le repository :
```bash
git clone https://github.com/OstriKeur/ft_transcendence.git
cd ft_transcendence
```

2. Créez un fichier `.env` à la racine (voir `.env.example` si disponible) :
```env
# Configuration OAuth 42
FT_CLIENT_ID=your_client_id
FT_CLIENT_SECRET=your_client_secret
FT_CALLBACK_URL=http://localhost:3000/auth/42/callback

# Base de données
DATABASE_URL=postgresql://user:password@db:5432/transcendence

# JWT Secret
JWT_SECRET=your_secret_key

# Autres variables d'environnement...
```

3. Lancez avec Docker :
```bash
make
# ou
docker-compose up --build
```

L'application sera accessible sur `http://localhost`

## 📁 Structure du projet

```
ft_transcendence/
├── backend/              # API Node.js
│   ├── src/
│   │   ├── routes/       # Routes API
│   │   ├── game/         # Logique du jeu
│   │   ├── config/       # Configuration
│   │   └── migrations/   # Migrations DB
│   └── Dockerfile
├── frontend/             # Application TypeScript
│   ├── src/
│   │   ├── game/         # Jeu Pong
│   │   ├── pages/        # Pages de l'application
│   │   ├── components/   # Composants réutilisables
│   │   └── services/     # Services API
│   └── Dockerfile
├── nginx/                # Configuration Nginx
├── monitoring/           # Prometheus et Grafana
├── logging/              # Elasticsearch et Logstash
└── docker-compose.yml    # Orchestration Docker
```

## 🎯 Ce que j'ai appris

- **Architecture full-stack** : Développement d'une application complète de A à Z
- **WebSockets** : Communication temps réel pour le jeu et le chat
- **Docker** : Containerisation et orchestration avec Docker Compose
- **Microservices** : Architecture modulaire avec services séparés
- **TypeScript** : Développement frontend typé
- **Gestion de bases de données** : Migrations, seeds, relations complexes
- **OAuth** : Intégration avec l'API 42
- **Authentification sécurisée** : JWT, 2FA, gestion des sessions
- **Monitoring** : Mise en place d'un système de monitoring complet
- **DevOps** : Configuration Nginx, reverse proxy, SSL

## 🎮 Utilisation

Une fois l'application lancée :

1. **Connexion** : Utilisez votre compte 42 pour vous connecter
2. **Profil** : Configurez votre profil et activez la 2FA si souhaité
3. **Jeu** : Jouez au Pong en ligne ou contre l'IA
4. **Tournois** : Participez ou créez des tournois
5. **Chat** : Discutez avec les autres joueurs

## 📊 Monitoring

Accédez aux dashboards :
- **Grafana** : `http://localhost:3001`
- **Prometheus** : `http://localhost:9090`

## 🔒 Sécurité

- Authentification OAuth 42
- Authentification à deux facteurs
- JWT pour les sessions
- Validation des entrées
- Protection CSRF
- HTTPS en production

## 📝 Note importante

Le fichier `.env` n'est pas inclus dans le repository pour des raisons de sécurité. Vous devez le créer localement avec vos propres credentials.

---

**Projet réalisé dans le cadre du cursus 42 Paris**
