# Dify Stack v5 - Hardened & Verified

Cette stack est une version sécurisée et mise à jour de Dify (v0.15.3), utilisant **SeaweedFS** comme alternative performante à MinIO.

## 🚀 Caractéristiques
- **Versions Vérifiées** : Toutes les images Docker utilisent des tags précis et récents (30/03/2026).
- **Sécurité** : 
  - Traefik configuré avec `no-new-privileges`.
  - Headers HTTP sécurisés activés.
  - Volumes en `read_only` là où c'est possible.
- **Stockage** : Remplacement de MinIO par SeaweedFS (plus léger, compatible S3).

## 🛠 Installation

1. Clonez le repository :
   ```bash
   git clone https://github.com/opinaka-attik/dify-stack-v5.git
   cd dify-stack-v5
   ```

2. Configurez l'environnement :
   ```bash
   cp .env.example .env
   # Modifiez le SECRET_KEY dans le fichier .env
   ```

3. Lancez la stack :
   ```bash
   docker compose up -d
   ```

## 📊 Services
- **Dify Web UI** : `http://localhost`
- **SeaweedFS S3** : `http://localhost:8333`
- **Traefik Dashboard** : `http://localhost:8080` (si activé)

## 🔒 Sécurité
Cette configuration suit les meilleures pratiques de hardening Docker. N'oubliez pas de changer les mots de passe par défaut dans le fichier `.env`.
