# Security & Privacy

## 1. Introduction
La sécurité et la confidentialité sont des aspects critiques dans les systèmes IoT, en raison de la collecte, de la transmission et de l'analyse de données sensibles. Ce document décrit les mesures mises en place pour garantir la protection des données et sécuriser les communications dans ce mini-projet IoT.

## 2. Sécurité des données

### 2.1. Collecte des données
- **Capteurs utilisés** : Les données de température, de pression atmosphérique et de position (longitude, latitude, altitude) sont collectées via les capteurs ST LPS22HB et Grove SIM28.
- **Validation des données** : Les données brutes des capteurs sont validées pour s'assurer qu'elles ne contiennent pas d'informations corrompues ou malveillantes.

### 2.2. Transmission sécurisée
- **Protocole de communication** : Les données sont transmises via le protocole LoRa, qui utilise un chiffrement AES-128 pour sécuriser les messages.
- **Authentification** : Chaque module LoRa est configuré avec des clés uniques pour prévenir les intrusions et éviter les attaques par usurpation d'identité.
- **Prévention des attaques Man-in-the-Middle** : L'utilisation de ChirpStack (serveur LoRaWAN) garantit l'intégrité des données grâce à un chiffrement de bout en bout (E2EE).

### 2.3. Stockage des données
- **Base de données** : Les données sont stockées dans InfluxDB, une base de données optimisée pour les séries temporelles.
- **Mesures de protection** :
  - Accès limité à la base de données par des identifiants et des mots de passe forts.
  - Segmentation réseau pour éviter l'accès non autorisé.

## 3. Confidentialité des données
- **Données personnelles** : Aucune donnée personnelle identifiable (PII) n'est collectée ou traitée dans ce projet.
- **Anonymisation** : Les données de position (longitude, latitude) sont agrégées pour éviter de révéler des informations sensibles sur l'emplacement exact.

## 4. Sécurité des plateformes et des outils
- **Node-RED** :
  - Accès sécurisé par authentification utilisateur.
  - Activation de HTTPS pour l'interface web.
- **Grafana** :
  - Utilisation d'authentification avec des rôles pour limiter les droits d'accès.
  - Protection par un mot de passe complexe pour les tableaux de bord.

## 5. Mesures contre les attaques
- **Attaques DDoS** : Surveillance des points d'accès réseau pour détecter et limiter les tentatives de surcharge.
- **Protection contre les accès non autorisés** : 
  - Pare-feu activé sur les serveurs.
  - Utilisation de VPN pour les communications avec les serveurs critiques.
- **Mises à jour régulières** : Tous les composants logiciels et firmwares sont maintenus à jour pour se protéger contre les vulnérabilités connues.

## 6. Politique de confidentialité
- Les données collectées sont utilisées uniquement pour les besoins du projet et ne seront pas partagées avec des tiers.
- Une politique de rétention des données est mise en place : les données sont conservées pendant une période déterminée et supprimées de manière sécurisée une fois inutiles.

## 7. Améliorations futures
- Intégration d'une authentification multi-facteurs (MFA) pour les plateformes utilisées.
- Renforcement de la surveillance des flux de données pour détecter les comportements anormaux.
- Utilisation de techniques de chiffrement homomorphique pour sécuriser les données lors de l'analyse dans le cloud.

