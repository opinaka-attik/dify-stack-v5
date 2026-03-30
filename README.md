# Dify Stack v5 - Full Hardened Solution

Cette stack est une version complète, sécurisée et optimisée de **Dify v1.13.3**, intégrant une architecture multi-couches pour la production.

## 🏗️ Architecture
- **Reverse Proxy** : Traefik v3.6.12 avec Docker Socket Proxy pour une isolation maximale.
- **SSO / Auth** : Authentik 2026.2.1 pour la gestion des accès.
- **VDB / Knowledge** : Weaviate v1.36.8.
- **Storage** : SeaweedFS v4.17 (Compatible S3, remplacement MinIO).
- **Core** : Dify API, Worker & Web v1.13.3.
- **Bases de données** : PostgreSQL 17 & Redis 8.6.

## 🚀 Caractéristiques de Sécurité
- **Docker Socket Proxy** : Traefik n'accède pas directement au socket Docker.
- **Hardening** : `no-new-privileges`, `read_only` sur les sockets, isolation réseau.
- **Healthchecks** : Monitoring automatique de l'état des services.

## 🛠️ Installation Quickstart

1. **Cloner le projet** :
   ```bash
   git clone https://github.com/opinaka-attik/dify-stack-v5.git
   cd dify-stack-v5
   ```

2. **Environnement** :
   ```bash
   cp .env.example .env
   # Remplissez les clés secrètes et mots de passe
   ```

3. **Lancement** :
   ```bash
   docker compose up -d
   ```

## 📊 Accès
- **Dify UI** : `http://localhost`
- **Authentik** : `http://localhost:9000`
- **Traefik Dashboard** : `http://localhost:8080`
- **SeaweedFS S3** : `http://localhost:8333`

---
*Dernière mise à jour : 30 Mars 2026*
