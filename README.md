# 💎 Ikcha · Sonic Gem Chamber 🎶

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=threedotjs&logoColor=white)

> **An immersive, single-page high-jewelry sensory experience.** 
> This project blends real-time 3D rendering, procedural audio synthesis, and an editorial UI to transform gemstones into audiovisual entities.

---

## 📑 Table of Contents
1. [📖 Overview](#-overview)
2. [✨ Core Features](#-core-features)
3. [🧠 How It Works (Didactic Architecture)](#-how-it-works-didactic-architecture)
4. [🗂️ Project Structure](#-project-structure)
5. [🚀 Getting Started](#-getting-started)
6. [🕹️ User Guide](#️-user-guide)
7. [🔮 Future Roadmap](#-future-roadmap)
8. [👨‍💻 Author](#-author)

---

## 📖 Overview

**Ikcha · Sonic Gem Chamber** is designed as a premium digital showroom. Instead of just looking at photos of jewelry, users can interact with parametric 3D gemstones. 

Every gemstone has its own:
*   **Visual Identity:** Unique cut (shape), color, roughness, and refraction.
*   **Sonic Signature:** A unique base frequency, tension, and energy level that drives a procedural audio synthesizer.
*   **Esoteric Narrative:** A curated description of its mineral and emotional properties.

---

## ✨ Core Features

| Feature | Icon | Description | Technology |
| :--- | :---: | :--- | :--- |
| **Real-time 3D Gems** | 🧊 | Parametric 3D meshes that rotate and react to lighting. Uses physical materials to mimic glass/diamonds. | `Three.js` |
| **Procedural Audio** | 🎛️ | Synthesizers generate sound based on the selected gem's frequency, density, and tension. | `Web Audio API` |
| **Tactile Scanner** | 👆 | A "textural reading" area where mouse/touch movement directly modulates the sound in real-time. | `JS Event Listeners` |
| **Dynamic Catalog** | 📇 | A beautifully styled grid with 30 curated gems, complete with CSS-drawn thumbnail previews. | `CSS Grid / Flexbox` |
| **Auto-Tour Mode** | ⏯️ | Sit back and relax while the system auto-cycles through the gem collection every 5 seconds. | `JavaScript` |

---

## 🧠 How It Works (Didactic Architecture)

This project is built to be **lightweight and completely frontend-based**. It requires no Node.js server or build tools (like Webpack or Vite). 

### 1. The 3D Visuals (`Three.js`)
We use a `MeshPhysicalMaterial` for the gems. Why? Because it calculates how light bounces and travels *through* an object. 
*   **`transmission`**: Makes the gem look like glass instead of plastic.
*   **`thickness`**: Gives the gem volume so it bends the light behind it (refraction).
*   **`ior` (Index of Refraction)**: Adjusted dynamically. A diamond bends light differently (IOR 2.4) than a quartz (IOR 1.5).

### 2. The Audio Engine (`Web Audio API`)
When you select a gem, we don't play an MP3. We generate the sound from scratch!
*   **Oscillators (`oscA`, `oscB`)**: Generate the base tone using Sine and Triangle waves based on the gem's frequency (e.g., 528Hz for Ruby).
*   **Filters (`BiquadFilterNode`)**: We pass the sound through filters.
*   **The Scanner Interaction**: When you drag your finger on the *Textural Reading* panel, we calculate the speed of your movement and use it to instantly open the filter and increase the gain. Faster movement = brighter, louder sound.

---

## 🗂️ Project Structure

Because this is a vanilla web application, the structure is incredibly simple:

```text
ikcha-sonic-gem-chamber/
│
├── index.html       # 🟢 MAIN FILE: Contains all HTML, CSS, and JS logic.
├── README.md        # 📖 You are reading this right now.
└── assets/          # 📁 (Optional) Folder for future 3D models (.glb), images, or fonts.
