---
marp: true
theme: gaia
paginate: true
style: |
  section {
    font-size: 20px; 
  }
  h1, h2 { 
    color: #2C3E50;
    border-bottom: none !important;
  }
  strong { 
    color: #E74C3C;
  }
  pre, code {
    font-size: 0.9em;
  }
  section::after {
    content: attr(data-marpit-pagination) " / " attr(data-marpit-pagination-total);
  }
---

# <!--fit--> Système IA Portable d'Assistance Environnementale

#### *Pour les malvoyants — adaptable à la canne ou portable sur le torse*

<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>

Zhaoyu WANG

---

## Introduction

Un **système** d'assistance environnementale, conçu spécifiquement pour les personnes malvoyantes.

- **Modalités de portage** :
  - Intégré ou fixé sur une **canne** blanche
  - Ou porté discrètement sur le **torse**

- **Fonction principale** :
  - Identifier en temps réel les **obstacles** et **éléments environnementaux** (escaliers, passages piétons, etc.).
  - Transmettre ces informations par **synthèse vocale**

---

## Architecture du Système (1/2)

### **Matériel (Hardware)**
- **Cerveau du système** : Raspberry Pi 5
- **Œil du système** : Module caméra Raspberry Pi 3
- **Alimentation** : Batterie portable

### **Application Mobile (Software)**
- **Plateforme** : Application Android
- **Fonctionnalité principale** : **Synthèse vocale** hors ligne(TTS)
- **Format d'échange** : **JSON**

---

## Architecture du Système (2/2)

### **Intelligence Artificielle (IA)**
- **Modèle de vision** : **YOLOv11n** (optimisé pour la détection en temps réel)
- **Moteur d'inférence** : **NCNN** (exécution accélérée sur Raspberry Pi)

### **Communication**
- **Connexion** : Wi-Fi
- **Protocoles envisagés** :
  1. **MQTT** (léger, idéal pour l'IoT)
  2. **WebSocket** (communication bidirectionnelle temps réel)
  3. **HTTP** (simplicité de déploiement)

---

## Limitations du Système Actuel

1.  **Poids et encombrement**
    - *Solution envisagée* : Optimisation de l'ergonomie

2.  **Temps de réaction**
    - *Solutions potentielles* :
      - Ajout d'un **ESP32** comme coprocesseur de traitement d'image: [**Camera** -- **ESP32** -- **Pi 5**]
      - Remplacement par **NVIDIA Jetson Orin Nano**

3.  **Stabilité du système**
    - Architecture à renforcer contre les points de défaillance uniques

4.  **Faisabilité du modèle local**
    - *Question* : La puissance de calcul du Pi 5 est-elle suffisante ?

5.  **Autonomie énergétique**
    - *Défi* : Équilibre entre **performance**, **poids** et **autonomie**

6.  **Stabilité de l'image**
    - *Problème* : Vibrations en milieu extérieur
    - *Solutions* :
      - **Mousses anti-vibrations**
      - **Portage sur le torse** 

---

# <!--fit--> Merci pour votre attention

### Questions ?