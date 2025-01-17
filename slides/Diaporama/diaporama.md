class: center, middle

# Projet : IoT Field Test Device-GNSS  
IESE 5 Communication IoT  

<br>

**CHEVALLIER Bastien**  
**LU Jiajin**  
**WANG Qi**  

<br>
<br>
.center[
<img src="images/polytech.png" alt="Logo Polytech" style="width:220px;"/>
]
---

# Sommaire

1. [Introduction et objectif](#introduction-et-objectif)
2. [Contenu du projet](#contenu-du-projet)
3. [Les équipements](#les-équipements)
4. [Format de données](#format-de-données)
5. [Bilan énergétique](#bilan-énergétique)
6. [Travail Réalisé - Chirpstack](#travail-réalisé---chirpstack)
7. [Travail Réalisé - NodeRed et InfluxDB](#travail-réalisé---nodered-et-influxdb)
8. [Travail Réalisé - Visualisation de Grafana](#travail-réalisé---visualisation-de-grafana)
9. [Conclusion](#conclusion)

---
## Introduction et objectif

- **Mesure :**
  - Température
  - Pression atmosphérique
  - Position géographique
- **Récupération et affichage des données** avec la base de données Docker

<br>

### Domaine d’utilisation
- Recherche environnementale, modélisation climatique et surveillance de la pollution.
- Détection des phénomènes météorologiques extrêmes et amélioration de la surveillance dans les zones isolées.

<br>

### Logos des technologies utilisées :
<center>
<img src="images/linux.jpg" alt="Linux" width="100">
<img src="images/riot.png" alt="RIOT" width="100">
<img src="images/chirpstack.png" alt="ChirpStack" width="100">
<img src="images/nodered.png" alt="Node-RED" width="100">
<img src="images/grafana-logo.png" alt="Grafana" width="100">
<img src="images/influxdb-logo.png" alt="InfluxDB" width="100">
</center>
---

# Contenu du projet

- le capteur ST LPS22HB
- le module de position Grove SIM28
- mesurer plusieurs paramètres (température, pression et position géographique)
- protocoles MQTT, NodeRED, InfluxDB, Grafana

<br>
 
<center>
<img src="images/linux.jpg" alt="Linux" width="100">
<img src="images/riot.png" alt="RIOT" width="100">
<img src="images/chirpstack.png" alt="ChirpStack" width="100">
<img src="images/nodered.png" alt="Node-RED" width="100">
<img src="images/grafana-logo.png" alt="Grafana" width="100">
<img src="images/influxdb-logo.png" alt="InfluxDB" width="100">
</center>

---

# Les équipements

<center>
<img src="images/schema.png" alt="Schema" width="600">
<img src="images/carte.jpg" alt="Carte" width="500">
</center>

---

# Format de données

<center>
<img src="images/payload.png" alt="Payload" width="500">
</center>

---

# Bilan énergétique

<center>
<img src="images/bilan.png" alt="Bilan" width="700">
</center>

---

# Travail Réalisé

- Les données générées par les capteurs seront envoyées via le module LoRa de la carte vers le serveur Campus IoT (Chirpstack)

<br>

<center>
<img src="images/Terminal.png" alt="Terminal" width="500">
</center>

---

# Travail Réalisé - Chirpstack

<center>
<img src="images/chirpstack1.png" alt="Chirpstack1" width="800">
</center>

---

# Travail Réalisé - Chirpstack

<center>
<img src="images/chirpstack4.png" alt="Chirpstack4" width="800">
</center>

---

# Travail Réalisé - Chirpstack

<center>
<img src="images/chirpstack2.png" alt="Chirpstack2" width="800">
</center>

---

# Travail Réalisé - Chirpstack

<center>
<img src="images/chirpstack3.png" alt="Chirpstack3" width="400">
</center>

---

# Travail Réalisé

- NodeRed pour récupérer les données via IOT Campus et les décodées
- InfluxDB pour stocker les données

---

# Travail Réalisé - NodeRed

<center>
<img src="images/nodered1.png" alt="Nodered1" width="600">
<img src="images/nodered2.png" alt="Nodered2" width="600">
</center>

---

# Travail Réalisé - NodeRed

<center>
<img src="images/nodered3.png" alt="Nodered3" width="200">
<img src="images/nodered1.png" alt="Nodered4" width="600">
</center>

---

# Travail Réalisé - InfluxDB

<center>
<img src="images/influxdb.png" alt="InfluxDB" width="800">
</center>

---

# Travail Réalisé - Visualisation de Grafana

<center>
<img src="images/grafana1.png" alt="Grafana1" width="800">
<img src="images/grafana2.png" alt="Grafana2" width="800">
</center>

---

# Conclusion

- 60 lignes de code ajouté 
- Technologies IoT de bout en bout avec le serveur LoRaWAN open-source ChirpStack
- Les conteneurs docker pour le backend avec NodeRED, InfluxDB et Grafana
- Applicaiton FTD

<br>
  
<center>
<img src="images/linux.jpg" alt="Linux" width="100">
<img src="images/riot.png" alt="RIOT" width="100">
<img src="images/chirpstack.png" alt="ChirpStack" width="100">
<img src="images/nodered.png" alt="Node-RED" width="100">
<img src="images/grafana-logo.png" alt="Grafana" width="100">
<img src="images/influxdb-logo.png" alt="InfluxDB" width="100">
</center>

---

class: center, middle

# Merci pour votre attention !  

.center[
<img src="images/polytech.png" alt="Logo Polytech" style="width:220px;"/>
]
