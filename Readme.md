# Déploiement OwnCloud + Collabora Online

## 1. Informations étudiant
- **Nom** : SOFO
- **Prénom** : DIDIER BRASSY
- **Matricule** : 23U2914
- **Option** : Systèmes et Réseaux
- **Cours** : INF3611 - Administration Systèmes

## 2. URL de l'application
**https://23U2914.systeme-res30.app**

## 3. Description de l'application et cas d'utilisation en entreprise

### OwnCloud
OwnCloud est une plateforme de stockage cloud open-source auto-hébergée qui permet le partage et la synchronisation de fichiers. Elle offre des fonctionnalités similaires à Dropbox ou Google Drive, mais avec un contrôle total sur les données.

### Collabora Online
Collabora Online est une suite bureautique collaborative basée sur LibreOffice, permettant l'édition en temps réel de documents Word, Excel et PowerPoint directement dans le navigateur.

### Cas d'utilisation en entreprise
1. **Stockage sécurisé** : Hébergement interne de documents sensibles
2. **Collaboration** : Édition simultanée de documents par plusieurs utilisateurs
3. **Contrôle d'accès** : Gestion fine des permissions de fichiers
4. **Synchronisation** : Accès aux fichiers depuis n'importe quel appareil
5. **Conformité** : Respect des réglementations sur la protection des données (RGPD, etc.)

## 4. Instructions pour démarrer l'application

# 1. Se connecter au VPS
ssh sofodidier@37.60.250.220

# 2. Se rendre dans le dossier de déploiement
cd /home/sofodidier/23U2914

# 3. Lancer les conteneurs Docker
docker compose up -d

# 4. Vérifier l'état des services
docker compose ps

# 5. Installer OwnCloud (première fois seulement)
# Accéder à https://23U2914.systeme-res30.app et suivre l'assistant d'installation
# ou utiliser la CLI :
docker exec owncloud_app_23U2914 php occ maintenance:install   --database=mysql   --database-name=owncloud   --database-user=owncloud   --database-pass=DbPass123   --database-host=owncloud-db   --admin-user=admin   --admin-pass=AdminPass123


