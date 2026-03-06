# UNEARTHED — WebAR Excavación Arqueológica

Sistema de Realidad Aumentada para excavaciones arqueológicas. Ancla información sobre hallazgos en el espacio real usando ARCore (WebXR).

## Cómo funciona

1. Apunta al suelo de la excavación → ARCore detecta la superficie
2. Coloca el origen en la esquina A1 de la cuadrícula física
3. Gira para alinear con la cuadrícula real
4. Confirma → los hallazgos aparecen anclados en sus coordenadas exactas
5. Muévete libremente → los objetos quedan fijos en el mundo real

## Archivos principales

| Archivo | Descripción |
|---------|-------------|
| `ar-excavacion.html` | ✅ **Versión activa** — WebXR + ARCore hit-test + anclaje manual |
| `ar-test.html` | Marco CSS + Three.js (para Android sin ARCore) |
| `ar-v3.html` | Versión WebXR con carga de escaneo Scaniverse |
| `ar-viewer.html` | Visor básico del escaneo |
| `webxr-v3.html` | Prototipo WebXR anterior |

## Assets

- `modelo-nube-puntos.glb` — Escaneo Scaniverse (2.13 MB)
- `nube-puntos.ply` — Nube de puntos extraída (1,098 pts)
- `textura-escaneado.jpg` — Textura del escaneo (2.1 MB)

## Dispositivos

- ✅ Android con ARCore (Xiaomi Redmi Note 11 Pro, Samsung Galaxy A52+...)
- ⚠️ Android sin ARCore (Hafury) → usar `ar-test.html` (giroscopio)
- 🔲 iOS — pendiente test

## Live URL

https://espaciovivo.gal/unearthed/ar-excavacion.html

## Tecnología

- WebXR `immersive-ar` + `hit-test`
- Three.js r160
- ARCore SLAM para tracking
- Sin librerías nativas, sin app — funciona en Chrome Android
