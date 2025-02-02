# Fiche ACV – File Test Device avec GNSS
## 1. Introduction
Le projet consiste à développer un dispositif IoT portable intégrant un module GNSS pour détecter des paramètres tels que :  
- **Température**,  
- **Pression atmosphérique**,  
- **Localisation**,  
- **Altitude**.  

L’objectif est d’assurer un suivi précis des équipements dans divers environnements tout en minimisant l’impact environnemental du dispositif.

## 2. Analyse des étapes du cycle de vie

| **Étape**         | **Impact clé**                                 | **Mesure de réduction**                    |
|--------------------|-----------------------------------------------|--------------------------------------------|
| **Fabrication**    | Consommation de ressources pour les capteurs et GNSS | Utilisation de composants recyclables      |
| **Transport**      | Émissions CO₂ liées au transport mondial      | Optimisation des chaînes d'approvisionnement |
| **Utilisation**    | Consommation énergétique continue (batterie)  | Intégration de capteurs basse consommation |
| **Fin de vie**     | Déchets électroniques non recyclés            | Mise en place d’un programme de recyclage  |

## 3. Impact environnemental global

La carte envoie les données toutes les minutes. Les principales sources de consommation d'énergie du système sont les suivantes :

### Module LoRaWAN
- **Mode de fonctionnement** : 214 μA/MHz à 868 MHz pendant 1 seconde.  
- **Mode veille** : 0.9 μA pendant 59 secondes.  
- **Consommation totale pour LoRaWAN** : **321.1 μAs**.

### Microcontrôleur STM32
- **Consommation** : 60 μA pendant 60 secondes.  
- **Consommation totale pour STM32** : **3600 μAs**.

### Module GPS
- **Consommation** : 40 mA pendant 1 secondes.  
- **Consommation totale pour le GPS** : **40 mAs**.

### Consommation totale du système
- **Consommation totale** : **229.4 mAs** par cycle.  
- **Consommation moyenne** : **12.61 mW** avec une alimentation de **3.3V**.  
- **Répartition énergétique** :  
  - **Module GPS** : 81%.  
  - **Microcontrôleur STM32** : 1.57%.  
  - **Module LoRaWAN** : 17.43%.

## 4. Recommandations prioritaires

### Optimisation du GPS et du microcontrôleur
- Réduire le temps d'acquisition du GPS et utiliser ses modes à faible consommation.  
- Activer les modes veille du STM32 pour économiser de l'énergie.

### Optimisation du module LoRaWAN et des envois
- Réduire la durée de transmission et ajuster les paramètres LoRaWAN.  
- Augmenter l'intervalle entre les envois pour limiter la fréquence des transmissions.
