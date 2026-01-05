# 🌊 AquaFlow - Jellyfin Theme (SCSS)

Ein modernes, professionelles Jellyfin-Theme mit SCSS-Architektur.

## 📁 Dateistruktur

```
jellyfin-theme-scss/
├── main.scss                 # Haupt-SCSS-Datei (importiert alles)
├── package.json             # NPM Konfiguration
│
├── utils/                   # Hilfsfunktionen
│   ├── _variables.scss      # Farben, Abstände, Breakpoints
│   └── _mixins.scss         # Wiederverwendbare SCSS-Mixins
│
├── base/                    # Grundlegende Styles
│   ├── _reset.scss          # Reset & Root-Styles
│   ├── _background.scss     # Hintergrund-Styles
│   └── _animations.scss     # Animationen
│
├── components/              # UI-Komponenten
│   ├── _header.scss         # Kopfzeile
│   ├── _sidebar.scss        # Seitenleiste
│   ├── _cards.scss          # Medien-Karten
│   ├── _forms.scss          # Formulare & Inputs
│   ├── _episodes.scss       # Episoden-Ansicht
│   ├── _cast.scss           # Besetzung
│   └── _dialogs.scss        # Dialoge & Popups
│
└── layout/                  # Seitenlayouts
    └── _login.scss          # Login-Seite
```

## 🚀 Installation & Kompilierung

### 1. Node.js & NPM installieren
Falls noch nicht vorhanden: https://nodejs.org/

### 2. SCSS Compiler installieren
```bash
npm install -g sass
```

### 3. Theme kompilieren

**Einmalig kompilieren:**
```bash
cd jellyfin-theme-scss
sass main.scss:output.css
```

**Watch Mode (automatische Kompilierung bei Änderungen):**
```bash
sass --watch main.scss:output.css
```

**Komprimierte Version:**
```bash
sass --style compressed main.scss:output.min.css
```

**Mit NPM Scripts:**
```bash
npm run build       # Normale Kompilierung
npm run build:min   # Komprimierte Version
npm run watch       # Watch Mode
npm run dev         # Development Mode
```

## 📋 Theme in Jellyfin verwenden

1. Kompiliere das SCSS zu CSS (siehe oben)
2. Öffne die generierte `output.css` Datei
3. Kopiere den gesamten Inhalt
4. Gehe zu **Jellyfin Dashboard** > **Allgemein**
5. Scrolle zu **Benutzerdefiniertes CSS**
6. Füge den CSS-Code ein
7. Klicke **Speichern**

## 🎨 Anpassungen

### Farben ändern
Öffne `utils/_variables.scss` und passe die Farben an:

```scss
$primary-color: #00a4dc;     // Deine Akzentfarbe
$secondary-color: #1a1a1a;   // Dunkler Hintergrund
// ... weitere Farben
```

### Abstände anpassen
```scss
$spacing-sm: 8px;
$spacing-md: 12px;
$spacing-lg: 24px;
```

### Eigene Komponente hinzufügen
1. Erstelle neue Datei in `components/` (z.B. `_mycomponent.scss`)
2. Importiere sie in `main.scss`:
   ```scss
   @import 'components/mycomponent';
   ```
3. Kompiliere neu

## 🛠️ Verwendete SCSS-Features

- **Variablen**: Zentrale Farbverwaltung
- **Nesting**: Übersichtlichere Struktur
- **Mixins**: Wiederverwendbare Styles
- **Partials**: Modulare Dateiorganisation
- **Imports**: Klare Abhängigkeiten

## 💡 Tipps

- Ändere nur Dateien in `utils/`, `components/`, `layout/` oder `base/`
- Kompiliere nach jeder Änderung neu
- Nutze Watch Mode während der Entwicklung
- Versioniere deine Änderungen mit Git

## 📝 Vorteile gegenüber reinem CSS

✅ Variablen für einfache Theme-Anpassung
✅ Mixins für wiederverwendbare Styles
✅ Nesting für bessere Lesbarkeit
✅ Modulare Struktur für große Projekte
✅ Leichte Wartbarkeit

## 🐛 Troubleshooting

**Problem**: SCSS kompiliert nicht
- Lösung: Prüfe ob Sass installiert ist: `sass --version`

**Problem**: Änderungen werden nicht angezeigt
- Lösung: Leere den Browser-Cache (Strg + Shift + R)

**Problem**: CSS funktioniert nicht in Jellyfin
- Lösung: Stelle sicher, dass du die kompilierte `.css` Datei verwendest, nicht die `.scss`

## 📄 Lizenz

MIT License - Frei verwendbar für private und kommerzielle Projekte

---

**Viel Spaß mit deinem modernen Jellyfin-Theme! 🎉**
