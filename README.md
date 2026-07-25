Ikcha · Sonic Gem Chamber
An immersive, single-page high-jewelry sensory experience that combines a real-time 3D gemstone viewer, a curated catalog of gem presets, a tactile “textural reading” scanner, and a procedural sound engine. The project is designed as a polished landing page / showcase piece for an editorial jewelry experience, with a strong visual identity and a premium dark aesthetic.
Overview
Ikcha · Sonic Gem Chamber is a browser-based interactive art and product-style experience built around gemstones as expressive objects. Each gem is presented as a sculptural 3D form, paired with a descriptive curatorial voice, a value tier, and a sonic profile that reacts to interaction.
The experience is built to feel somewhere between a luxury product microsite and a digital exhibition: the hero stage presents the selected gemstone in a rotating 3D scene while the side panels provide catalog browsing, mineral notes, sonic behavior, and an atlas of gem families.
What it does
Renders a rotating gemstone in a Three.js scene.
Uses physically based materials to suggest crystal, refraction, and glossy jewelry surfaces.
Displays a catalog of gemstone presets with small thumbnail previews.
Lets the user select different stones and update the hero scene.
Includes a “textural reading” panel that responds to pointer or touch movement.
Modulates audio behavior live as the scanner moves across the surface.
Provides a didactic atlas of gemstone families and their sonic personalities.
Uses a responsive layout that works on desktop and mobile.
Main features
1. Immersive 3D hero stage
The central visual focus is a gemstone that rotates continuously inside a dark atmospheric scene. The camera framing is tuned so the model sits lower in the composition and remains visible behind the header overlay.
2. Curated gemstone catalog
The catalog includes multiple gemstone presets, such as spinel, morganite, tourmaline, ruby, sapphire, diamond, emerald, aquamarine, amethyst, smoky quartz, and onyx. Each card includes a thumbnail, family label, name, description excerpt, and value tier.
3. Textural reading scanner
The scanner panel behaves like a tactile analytical surface. Pointer and touch movement immediately move the reading head, and the gesture speed changes the sound in real time so the interaction feels more alive.
4. Procedural sonic layer
The sound design is procedural and reacts to the active gemstone and the scanner movement. Higher motion increases brightness, filter movement, and intensity.
5. Didactic atlas
The lower section of the page groups gem families into a readable reference atlas, giving the project a more editorial and educational feel.
Technologies used
HTML5.
CSS3.
Vanilla JavaScript.
Three.js via CDN.
Web Audio API.
Responsive layout techniques with CSS Grid and Flexbox.
Project structure
ikcha-sonic-gem-chamber/
├── index.html
├── README.md
└── assets/
Files
index.html — Main application file. Contains the full experience: layout, styles, Three.js scene, audio engine, catalog behavior, and interaction logic.
README.md — Project documentation.
assets/ — Optional future folder for textures, local images, logos, or 3D models.
How to run
Option 1: Open locally
Save the file as index.html.
Double-click it or open it in a modern browser.
Allow audio when prompted.
Option 2: Run from a static host
You can deploy it to:
GitHub Pages.
Netlify.
Vercel.
Any static web host.
Because this is a front-end only project, no build step is required.
Browser requirements
For the best experience, use a modern browser with support for:
ES modules.
WebGL.
Web Audio API.
CSS variables and backdrop blur.
Recommended browsers:
Chrome.
Edge.
Firefox.
Safari.
Usage guide
Switching gemstones
Click any catalog card to load a different gemstone in the hero view. The selected gemstone updates the title, description, structure, frequency, and visual tone.
Enabling sound
Press Enable sound to activate the procedural audio. The page will then respond to the active gemstone and scanner movement.
Using the textural reading panel
Drag or move your finger across the scanner panel. Faster movement produces more dramatic sonic changes, while slower movement gives a softer, more controlled response.
Tour mode
Use Tour mode to cycle through the gemstone presets automatically.
Design intent
The project is intentionally styled as a luxury editorial digital piece. The tone combines:
Jewelry showroom aesthetics.
Scientific mineral references.
Esoteric / emotional language.
Cinematic lighting.
Soft glass-like panels over a dark background.
The result is meant to feel premium, immersive, and slightly ceremonial.
Implementation notes
The gemstone mesh is created with procedural geometry rather than external model files.
The gem materials use physically based rendering to simulate polished stone and crystal-like surfaces.
The scanner interaction is intentionally responsive: it updates quickly so it feels like a live reading, not a slow animation.
The layout is responsive, with the stage remaining visually prominent even when the page scrolls.
Known considerations
The experience depends on browser support for WebGL and Web Audio.
Mobile devices may render the 3D scene at a slightly lower visual fidelity for performance reasons.
Audio will not start until the user interacts with the page due to browser autoplay policies.
Deployment tips
Keep index.html at the root of the repository.
If you add textures or media later, place them in assets/.
For GitHub Pages, deploy from the main branch root.
For Netlify, you can drag and drop the folder as-is.
Suggested future enhancements
Add real gemstone textures or normal maps.
Replace procedural gem shapes with custom GLB models.
Add environment maps for more realistic reflections.
Add a loading animation for a more premium entry sequence.
Add multilingual support for English / Spanish copy.
Add screenshot export or share links.
Credits
Created as a curated immersive jewelry experience. Final footer credit used in the page: By David Signals.
License
No license has been specified yet. Add one if you plan to publish, reuse, or distribute the project publicly.
