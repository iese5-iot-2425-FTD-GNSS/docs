# Introduction
# Domaine(s) d’utilisation
   Imaginé des cas d’usage
...
# Concurrence marché
# Equipements
# Bilan énergétique
Le système étudié transmet des données toutes les 2 minutes. Son bilan énergétique repose sur trois principaux composants : le module LoRaWAN, le microcontrôleur STM32 et le module GPS. Voici une analyse détaillée des sources de consommation énergétique de ces éléments :

## 1. Module LoRaWAN
Le module LoRaWAN est responsable de la communication sans fil, utilisant la bande de fréquence de 868 MHz. Son fonctionnement est caractérisé par deux modes :  
- **Mode actif** : pendant 1 seconde par cycle de 2 minutes, le module consomme **214 μA/MHz**, soit une consommation énergétique totale de **214 μAs**.  
- **Mode veille** : durant les 119 secondes restantes, la consommation chute à **0.9 μA**, correspondant à **107.1 μAs**.  

**Consommation totale pour le module LoRaWAN** : **321.1 μAs** par cycle de 2 minutes.  

## 2. Microcontrôleur STM32
Le microcontrôleur STM32, responsable de la gestion des opérations et de la coordination des modules, fonctionne de manière continue pendant le cycle de 2 minutes. Sa consommation est stable à **60 μA**, ce qui correspond à une consommation énergétique totale de **7200 μAs**.  

## 3. Module GPS
Le module GPS, utilisé pour obtenir les coordonnées de localisation, est actif pendant 30 secondes par cycle. Il consomme **40 mA**, soit une énergie totale de **1200000 μAs**.  

## 4. Consommation Totale du Système
En additionnant les contributions des trois modules, la consommation énergétique totale du système par cycle de 2 minutes s'élève à **1.208 As**. Avec une alimentation de **3.3V**, cela correspond à une puissance moyenne de **33.22 mW**.  

## 5. Répartition de la Consommation Énergétique
L'analyse des contributions montre que le module GPS domine largement la consommation énergétique du système, représentant plus de **99%** de l'énergie totale consommée. Les autres composants, bien que nécessaires, contribuent de manière négligeable :  
- **Module GPS** : 99.34%  
- **Microcontrôleur STM32** : 0.60%  
- **Module LoRaWAN** : 0.03%  

---

## Conclusion
Le bilan énergétique met en évidence que le module GPS est la principale source de consommation du système. Une optimisation de ce module, comme la réduction de la durée d'utilisation ou l'adoption d'une technologie moins gourmande en énergie, pourrait significativement améliorer l'efficacité énergétique globale.
# Format de données (payload)
# Métriques logicielles
# Nombre total de lignes de code / Nombre de lignes de code ajoutées-modifiées
# Taille du firmware (.bin)
