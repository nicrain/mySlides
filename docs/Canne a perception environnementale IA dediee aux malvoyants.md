---
marp: true
theme: gaia
paginate: true

---

# Système IA Portable d'Assistance Environnementale
## <!---fit---> *Pour les malvoyants, s'adapte à la canne ou se porte sur le torse*
---

# Introduction

- un system
- canne ou torse
- 
---

# Architecture

- Hardware:
  - Raspberry Pi 5
  - Raspberry Pi Camera Module 3
- AI Model:
  - YOLOv11n(Pour l'identification des images)
    - NCNN
- Telecommunication:
  - WIFI
    1. MQTT
    2. WebSocket
    3. HTTP
- Software:
  - Android APP
    - 语音播报: Text -> Audio(Offline TTS engine)
    - Format des données: JSON

---

# Défis
1. Lourd(ESP32??, Raspberry Pi, Caméra, Batterie)
2. Temps react
3. Stabilité
   - Beaucoup d'equipements, 单点故障率增加
4. Local big model est realisable?
5. Égilibre entre le poids et la durée de batterie
6. Vibration de caméra à cause de le terrain pas plat
   - 加入减震海绵
   - 佩带在胸前

---
# Merci