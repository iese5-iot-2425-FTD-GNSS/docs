# Security & Privacy

Le document "Security & Privacy" décrit des mesures qui peuvent être mises en place pour garantir la protection des données et sécuriser les communications dans ce mini-projet IoT FTD GNSS.

## 1. Introduction
La sécurité et la confidentialité sont des aspects critiques dans les systèmes IoT. En effet, la collecte de données, leur transmission et le stockage sont des phases sensibles.

## 2. Sécurité des données

### 2.1. Collecte des données
- **Capteurs utilisés** : Les données de température, de pression atmosphérique et de position (longitude, latitude, altitude) sont collectées via les capteurs ST LPS22HB et Grove SIM28.
- **Solution** : Les données brutes des capteurs cités ci-dessus, sont validées pour s'assurer qu'elles ne contiennent pas d'informations corrompues ou malveillantes (cybersécurité).

### 2.2. Transmission sécurisée
- **Protocole de communication** : Les données sont transmises via le protocole LoRa, qui utilise un chiffrement AES-128 pour sécuriser les messages.
- **Solution** : Chaque module LoRa est configuré avec des clés uniques.

### 2.3. Stockage des données
- **Base de données** : Les données sont stockées dans InfluxDB, une base de données qui suit les trames dans le temps.
- **Solution** :
  - identifiants et des mots de passe forts pour les admin.

## 3. Sécurité des plateformes et des outils
- **Node-RED** :
  - Accès sécurisé par authentification utilisateur avec mot de passe personnalité.
- **Grafana** :
  - Accès sécurisé par authentification utilisateur avec mot de passe personnalité et pour accès au tableau de bord.

## 4. Mesures contre les attaques
- **Attaques DDoS** : Surveillance du serveur Chirpstack pour détecter et limiter les tentatives de surcharge par communication LoRa.
- **Mises à jour régulières** : Les composants logiciels et firmwares sont maintenus à jour pour se protéger contre les vulnérabilités connues.

## 5. Politique de confidentialité
- Les données collectées (GPS, temperature et pression) sont utilisées uniquement pour les besoins du projet et ne seront pas partagées avec des tiers. Les données peuvent être conservé pendant une période déterminée, puis supprimées de manière sécurisée une fois inutiles.

## 6. Améliorations futures
- Intégration d'une authentification multi-facteurs (2FA) pour les plateformes utilisées.
- Utilisation de techniques de chiffrement plus fort.
