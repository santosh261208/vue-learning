# Vue.js Einführung Notes

## Was ist Vue.js?
- JavaScript Framework für moderne Web-Apps
- Erweiterung von HTML mit Template Syntax
- Automatische DOM-Aktualisierung bei Datenänderungen
- Für Desktop und Mobile geeignet

---

## Vorteile
- Dynamische Updates ohne komplette Page-Reloads
- Komponenten-Einbettung auf jeder Seite möglich
- Single-Page-Application (SPA)
- Serverseitiges Rendering möglich

---

## Vue Datei Aufbau (.vue)
Every Vue file has 3 parts:
```vue
<script setup>
  // JavaScript Logik
</script>

<template>
  <!-- HTML Anzeige -->
</template>

<style scoped>
  /* CSS Styling - nur für diese Komponente */
</style>
```

---

## API Styles
**Options API:**
- Logik wird in einem Objekt gekapselt
- Verwendet `data`, `methods`, `mounted`
- Eigenschaften via `this` aufrufen
- Geringere Komplexität

**Composition API (`<script setup>`):**
- Logik via importierte Funktionen definiert
- Moderner, wiederverwendbarer Code
- Variablen und Funktionen direkt im Template verwendbar
- Höhere Komplexität, aber besser für grosse Projekte

---

## Projektstruktur
```
vue-learning/
├── src/
│   ├── assets/       ← CSS, Bilder
│   ├── components/   ← Wiederverwendbare Komponenten
│   ├── App.vue       ← Hauptkomponente (wie Main.java)
│   └── main.js       ← App Setup (nicht anfassen)
├── index.html
├── package.json      ← Dependencies
└── vite.config.js    ← Build Config
```

---

## Build Tool: Vite
- Leichtgewichtiges Frontend-Build-Tool
- Unterstützt Hot-Reload (Seite updated automatisch beim Speichern)

---

## Wichtige Befehle
| Befehl | Was es macht |
|--------|-------------|
| `npm install` | Abhängigkeiten installieren |
| `npm run dev` | Dev-Server starten |
| `npm run build` | Produktions-Build erstellen |

---

## ⚠️ Wichtige Regeln
- README beim GitHub Repo erstellen NICHT anhaken wenn lokales Projekt schon existiert
- `node_modules` Ordner nie in Git pushen (steht in .gitignore)
- `scoped` in Style bedeutet: CSS gilt nur für diese Komponente