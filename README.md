# Café-Littéraire — Maquette 3D interactive + Réalité augmentée

Maquette 3D immersive d'un projet de café-librairie, à explorer dans le navigateur, avec mode réalité augmentée sur mobile.

## 🚀 Voir en ligne

Une fois GitHub Pages activé :
- Vue 3D : `https://<ton-pseudo>.github.io/<nom-du-repo>/`
- Réalité augmentée : `https://<ton-pseudo>.github.io/<nom-du-repo>/ar.html`

## 🎮 Vue 3D (index.html)

Glisser pour tourner, molette / pincer pour zoomer. Boutons en haut à droite : reset vue, plein écran, export GLB, accès page RA.

## 📱 Réalité augmentée (ar.html)

Sur mobile (Android ou iPhone récent), le bouton **📱 Voir en réalité augmentée** ouvre l'appareil photo et projette le café à l'échelle dans ton vrai espace. Tu peux te déplacer autour, le redimensionner d'un pinch, le replacer.

## 🛠️ Générer le fichier GLB (à faire une fois)

La page 3D contient un bouton **📦 GLB** qui exporte la scène au format `.glb` (standard 3D du Web). Marche à suivre :

1. Ouvre `index.html` dans ton navigateur
2. Clique sur **📦 GLB** en haut à droite
3. Le fichier `cafe_litteraire.glb` se télécharge sur ton ordinateur
4. Upload-le dans le repo GitHub à côté des autres fichiers
5. Commit + push — `ar.html` le trouve automatiquement

## 🍎 Pour iOS (USDZ — optionnel)

Apple n'utilise pas le GLB pour la RA, il leur faut un `.usdz`. Sans ce fichier, la RA marchera sur Android mais pas sur iPhone.

Pour convertir :
- **Reality Converter** d'Apple (gratuit, Mac uniquement) : glisser-déposer le GLB → export USDZ
- **En ligne** : products.aspose.app/3d/conversion/glb-to-usdz ou similaire
- Place `cafe_litteraire.usdz` à côté du GLB dans le repo

## 🏗️ Ce que contient la scène

Façade haussmannienne en pierre avec vitrines transparentes et porte centrale, bibliothèques pleine hauteur avec échelle laiton, comptoir café carrelé blanc avec machine espresso et vitrine pâtisserie, barista derrière, deux colonnes en chêne reliées par un claustra ajouré pleine hauteur, coin lecture velours vert et cuir cognac, bar fenêtre avec tabourets en laiton, sept suspensions chaudes.

## 🛠️ Technique

- `index.html` : Three.js (r128) chargé depuis CDN, rendu WebGL custom
- `ar.html` : composant `<model-viewer>` de Google, gère WebXR (Android), Scene Viewer (Android) et Quick Look (iOS)
- Pas de build, pas de dépendances locales

## 📁 Structure

```
.
├── index.html             # Vue 3D interactive
├── ar.html                # Réalité augmentée
├── cafe_litteraire.glb    # Modèle 3D (à générer via le bouton 📦 GLB)
├── cafe_litteraire.usdz   # Optionnel, pour iPhone
└── README.md              # Ce fichier
```
