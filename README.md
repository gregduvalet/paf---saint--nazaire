# PAF — Saint-Nazaire

Projet collaboratif entre **Les Pieds dans le PAF** et **TAPAJ**

## Objectif

Visualiser sur une carte 3D de Saint-Nazaire les lieux où des jeunes
ont capté vidéos et sons, et les restituer via des fiches descriptives
interactives.

Un outil de réappropriation du territoire par le médias audiovisuel.

## Fonctionnalités

- 🗺️ Carte 3D de Saint-Nazaire (CesiumJS + Google 3D Tiles)
- 📍 Points d'intérêt (POI) géolocalisés avec ligne verticale animée
- 🔍 Recherche et filtrage des POI
- 🎬 Lecture de vidéos YouTube embarquées dans les fiches POI
- 🔊 Lecteur audio intégré avec barre de progression
- 🔄 Animation d'orbite automatique autour du POI sélectionné
- 📦 Support de modèles 3D GLB comme marqueurs

## Stack technique

- [CesiumJS](https://cesium.com) — moteur de globe 3D
- Google 3D Tiles via Cesium Ion (asset 2275207)
- YouTube IFrame API (embed nocookie)
- HTML / CSS / JavaScript vanilla — aucune dépendance npm

## Structure
paf-saint-nazaire/
├── poi_viewer.html    ← application principale
└── README.md

## Configuration des POI

Les points d'intérêt sont définis dans le tableau `POIS` au début
du fichier `poi_viewer.html`. Pour chaque POI :

```javascript
{
  id: 'p1',
  name: 'Nom du lieu',
  category: 'Patrimoine',   // Patrimoine | Industrie | Culture | Nature | Commerce
  lon: -2.2045, lat: 47.2785,
  thumbnail: 'URL image',
  modelUrl: null,            // ou chemin vers un .glb
  card: {
    title: 'Titre complet',
    image: 'URL photo',
    description: 'Texte descriptif',
    youtube: 'https://youtu.be/...',
    audio: './audio/fichier.mp3'
  }
}
```

## ⚠️ Prérequis

- Un token **Cesium Ion** valide (compte gratuit sur [cesium.com](https://cesium.com))
- Le token ne doit pas être commité en clair dans le code

## Partenaires

- Les Pieds dans le PAF
- [TAPAJ](https://tapaj.org)

## Statut

🚧 En cours de développement — phase prototype
