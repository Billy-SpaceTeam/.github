<img src="/assets/IMG_Main.png">

# 🛰️ Billy Space Team — Projet CubeSat Billy

Bienvenue sur le profil officiel de l'équipe **Billy Space Team** !  
Ce projet s'inscrit dans le cadre de notre cursus en **BUT Génie Électrique et Informatique Industrielle (GEII)** à l'**IUT d'Annecy (Université Savoie Mont Blanc)**, spécialité **Électronique et Systèmes Embarqués (ESE)**

---

## 📌 Présentation du Projet

**Billy** est une maquette fonctionnelle de nano-satellite au format standardisé **CubeSat 1U (10 × 10 × 10 cm)**.  
Il s'agit d'un système embarqué communicant conçu pour récolter des données télémétriques de vol, transmettre ses mesures en temps réel et assurer un contrôle d'attitude autonome.

### 🌟 Fonctionnalités clés
* **Orientation automatique :** asservissement via une roue de réaction (moteur brushless) couplée à des photodiodes / phototransistors pour pointer automatiquement le satellite vers le Soleil
* **Déploiement motorisé :** ouverture contrôlée des panneaux solaires par servomoteur une fois le pointage lumineux établi
* **Affichage embarqué :** écran LCD intégré sur une face latérale pour l'état du système et le monitoring direct
* **Télémétrie multi-liaisons :** communication série (UART/debug), bus I2C interne et transmission sans fil

---

## ⚙️ Architecture Système & Matériel

* **Cerveau de bord :** Carte de développement **STM32 Nucleo**
* **Capteurs & Instrumentation :**
  * 🌡️ Température (I2C)
  * 🌪️ Pression atmosphérique (I2C)
  * 🧭 Gyroscope / IMU (I2C)
  * ☀️ Mesure de luminosité (acquisition analogique / photodiodes)
* **Actionneurs & Interfaces :**
  * 🔄 Roue de réaction pilotée en PWM (moteur brushless)
  * 📐 Servomoteur pour le déploiement des panneaux
  * 🖥️ Afficheur LCD & LEDs d'état
* **Contraintes mécaniques & spatiales :**
  * Format CubeSat 1U ($10 \times 10 \times 10\text{ cm}$), masse $< 2\text{ kg}$
  * Redémarrage automatique en cas de défaut électrique / court-circuit

---

## 🕹️ Modes de Fonctionnement

1. **Mode Manuel :** contrôle direct des actionneurs (liaison filaire ou sans fil) et affichage local sur écran LCD sans télémétrie distante.
2. **Mode Passif :** émission continue des trames de télémétrie en temps réel sans actionnement mécanique.
3. **Mode Actif (Autonome) :** asservissement complet — tracking solaire automatique via la roue de réaction, déploiement des panneaux solaires et transmission continue des données de vol.

---

## 👥 L'Équipe

Projet développé en binôme par :
* **Clément PILI**
* **Jérémie PERRIN**

*IUT d'Annecy — Université Savoie Mont Blanc (Promotion 2026/2027)*
