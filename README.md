# Café-Littéraire — Maquette 3D interactive

Maquette 3D immersive d'un projet de café-librairie, à explorer dans le navigateur.

## 🚀 Voir en ligne

Une fois GitHub Pages activé, le site sera disponible à :
`https://<ton-pseudo>.github.io/<nom-du-repo>/`

## 🎮 Navigation

- **Glisser** (souris ou tactile) — tourner autour de la scène
- **Molette / pincer** — zoomer
- **↺ Vue** — revenir à la vue d'ensemble
- **⛶ Plein écran** — immersion totale

La caméra tourne lentement toute seule au démarrage. Tu reprends la main dès que tu interagis ; l'auto-rotation reprend après 5 secondes d'inactivité.

## 🏗️ Ce que contient la scène

- **Façade haussmannienne** en pierre avec deux grandes vitrines transparentes et porte centrale
- **Bibliothèques pleine hauteur** sur les deux murs latéraux, avec ~200 livres aux dos colorés et échelle laiton
- **Comptoir café carrelé blanc** avec machine espresso, vitrine pâtisserie, ardoises de menu et arrière-bar fourni
- **Barista** stylisé derrière le comptoir, dans son couloir de travail
- **Deux colonnes en chêne** reliées par un claustra ajouré pleine hauteur (post-and-rail avec contreventement diagonal)
- **Coin lecture** avec sofa velours vert, fauteuil cuir cognac, table basse et tapis terracotta
- **Bar fenêtre** avec trois tabourets en laiton face à la rue
- **Présentoir Coups de cœur** en colonne ronde
- **Sept suspensions** avec halo chaud + lumière naturelle traversant les vitrines

## 🛠️ Technique

Page HTML unique, sans build. Charge [Three.js](https://threejs.org) (r128) depuis CDN. Pas de dépendances à installer, pas de framework — il suffit d'ouvrir `index.html` dans un navigateur moderne.

## 📁 Structure

```
.
├── index.html      # Toute la scène (HTML + CSS + JS Three.js)
└── README.md       # Ce fichier
```

## ✏️ Modifier la scène

Tout le code 3D est dans la balise `<script>` à la fin d'`index.html`. Les sections sont commentées et numérotées : façade, bibliothèques, comptoir, barista, colonnes/pans de bois, tables, coin lecture, bar fenêtre, éclairages, contrôles caméra. Tu peux ajuster positions, dimensions et couleurs directement dans le fichier.
