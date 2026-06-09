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
