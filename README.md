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

🚀 Getting Started
You can run this project in less than 10 seconds. No installation required.
💻 Option 1: Run Locally (For Development)
Download or clone this repository.
Locate the index.html file.
Double-click index.html to open it in Chrome, Edge, Safari, or Firefox.
Tip for developers: Use VS Code with the "Live Server" extension for hot-reloading while editing.
🌍 Option 2: Deploy to the Web (For Production)
You can host this for free in 1 click:
GitHub Pages: Push this to a GitHub repo and enable Pages in settings.
Netlify / Vercel: Drag and drop the ikcha-sonic-gem-chamber folder into their dashboard.
🕹️ User Guide
How to navigate the experience:
Enable Audio: Click the "Enable sound" button in the top right. (Browsers require user interaction before playing audio).
Browse the Catalog: Scroll down the right panel to see the 30 presets. Click any card to load the gem into the 3D stage.
Interact with the Scanner: In the Textural Reading section, drag your mouse or finger around the grid. Notice how the needle follows you and the sound gets more intense the faster you move.
Tour Mode: Click the "Tour mode" button to automatically cycle through the collection.
🔮 Future Roadmap
�Integrate 30+ gemstone presets.
�Add real-time procedural audio synthesis.
�Make the Textural Scanner responsive to touch/mouse speed.
�Add .glb / .gltf photorealistic 3D models to replace parametric shapes.
�Implement HDRI Environment maps for ultra-realistic studio reflections.
�Add multi-language support (English / Spanish).
👨‍💻 Author
Created by David Signals
Curated immersive jewelry experience blending web technology, DSP (Digital Signal Processing), and editorial design.
