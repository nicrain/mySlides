---
marp: true
theme: gaia
paginate: true
style: |
  /* 全局减小字体大小，解决内容溢出问题 */
  section {
    font-size: 20px; /* 默认通常是24px或28px，调小即可 */
  }
  /* 保持标题和重点的突出 */
  h1, h2 { 
    color: #2C3E50;
    border-bottom: none !important;
  }
  strong { 
    color: #E74C3C;
  }
  /* 确保代码块也不溢出 */
  pre, code {
    font-size: 0.9em;
  }
---

# <!--fit--> Système IA Portable d'Assistance Environnementale

### *Pour les malvoyants — S'adapte à la canne ou se porte sur le torse*

---

## Introduction

Un **système intelligent** d'assistance environnementale, conçu spécifiquement pour les personnes malvoyantes.

- **Flexibilité du port** :
  - Intégré directement sur une **canne** blanche.
  - Ou porté discrètement sur le **torse**.

- **Fonction principale** :
  - Identifier en temps réel les **obstacles** et les **éléments environnementaux** (escaliers, passages piétons, etc.).
  - Transmettre ces informations par **synthèse vocale**.

---

## Architecture du Système(1/2) 

### **Matériel (Hardware)**
- **Cerveau du système** : Raspberry Pi 5
- **Œil du système** : Module Caméra Raspberry Pi 3
- **Alimentation** : Batterie portable haute capacité

### **Application Mobile (Software)**
- **Plateforme** : Application Android
- **Fonctionnalité principale** : **Synthèse vocale** hors ligne (TTS)
- **Format d'échange de données** : **JSON**

---

## Architecture du Système(2/2)  

### **Intelligence Artificielle (IA)**
- **Modèle de vision** : **YOLOv11n** (optimisé pour la détection d'objets en temps réel)
- **Moteur d'inférence** : **NCNN** (pour une exécution ultra-rapide sur Raspberry Pi)

### **Communication**
- **Connexion** : Wi-Fi
- **Protocoles envisagés** :
  1. **MQTT** (léger et idéal pour l'IoT)
  2. **WebSocket** (communication bidirectionnelle en temps réel)
  3. **HTTP** (simplicité de déploiement)



---

## Défis Techniques & Solutions

1.  **Poids et Encombrement**
    - *Solution* : Explorer l'utilisation d'un **ESP32** comme coprocesseur pour alléger la charge du Pi.

2.  **Temps de Réaction**
    - *Solution* : Optimisation du modèle YOLO et utilisation du moteur **NCNN** pour une inférence plus rapide.

3.  **Stabilité du Système**
    - *Solution* : Concevoir une architecture modulaire pour réduire les **points de défaillance uniques**.

4.  **Faisabilité du Modèle Local**
    - *Défi* : La puissance de calcul du Raspberry Pi 5 est-elle suffisante pour faire tourner un gros modèle localement ?

5.  **Autonomie Énergétique**
    - *Défi* : Trouver le juste équilibre entre la **puissance de traitement**, le **poids** de la batterie et l'**autonomie**.

6.  **Stabilité de l'Image**
    - *Problème* : Vibrations de la caméra dues aux déplacements sur terrain irrégulier.
    - *Solutions* :
      - Intégration de **mousses anti-vibrations**.
      - L'option "porté sur le torse" offre une stabilité naturelle supérieure.

---

# <!--fit--> Merci pour votre attention

### &nbsp;
