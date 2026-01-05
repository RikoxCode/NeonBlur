# 🌊 AquaFlow - Jellyfin Theme (SCSS)

A modern, professional Jellyfin theme with SCSS architecture.

## 📁 File Structure

```
jellyfin-theme-scss/
├── main.scss                 # Main SCSS file (imports everything)
├── package.json             # NPM configuration
│
├── utils/                   # Utility functions
│   ├── _variables.scss      # Colors, spacing, breakpoints
│   └── _mixins.scss         # Reusable SCSS mixins
│
├── base/                    # Base styles
│   ├── _reset.scss          # Reset & root styles
│   ├── _background.scss     # Background styles
│   └── _animations.scss     # Animations
│
├── components/              # UI components
│   ├── _header.scss         # Header
│   ├── _sidebar.scss        # Sidebar
│   ├── _cards.scss          # Media cards
│   ├── _forms.scss          # Forms & inputs
│   ├── _episodes.scss       # Episode view
│   ├── _cast.scss           # Cast
│   └── _dialogs.scss        # Dialogs & popups
│
└── layout/                  # Page layouts
    └── _login.scss          # Login page
```

## 🚀 Installation & Compilation

### 1. Install Node.js & NPM
If not already installed: https://nodejs.org/

### 2. Install SCSS Compiler
```bash
npm install -g sass
```

### 3. Compile Theme

**Compile once:**
```bash
cd jellyfin-theme-scss
sass main.scss:output.css
```

**Watch mode (automatic compilation on changes):**
```bash
sass --watch main.scss:output.css
```

**Compressed version:**
```bash
sass --style compressed main.scss:output.min.css
```

**Using NPM scripts:**
```bash
npm run build       # Normal compilation
npm run build:min   # Compressed version
npm run watch       # Watch mode
npm run dev         # Development mode
```

## 📋 Using the Theme in Jellyfin

1. Compile the SCSS to CSS (see above)
2. Open the generated `output.css` file
3. Copy the entire content
4. Go to **Jellyfin Dashboard** > **General**
5. Scroll to **Custom CSS**
6. Paste the CSS code
7. Click **Save**

## 🎨 Customization

### Change Colors
Open `utils/_variables.scss` and adjust the colors:

```scss
$primary-color: #00a4dc;     // Your accent color
$secondary-color: #1a1a1a;   // Dark background
// ... more colors
```

### Adjust Spacing
```scss
$spacing-sm: 8px;
$spacing-md: 12px;
$spacing-lg: 24px;
```

### Add Custom Component
1. Create new file in `components/` (e.g., `_mycomponent.scss`)
2. Import it in `main.scss`:
   ```scss
   @import 'components/mycomponent';
   ```
3. Recompile

## 🛠️ SCSS Features Used

- **Variables**: Centralized color management
- **Nesting**: Clearer structure
- **Mixins**: Reusable styles
- **Partials**: Modular file organization
- **Imports**: Clear dependencies

## 💡 Tips

- Only modify files in `utils/`, `components/`, `layout/`, or `base/`
- Recompile after each change
- Use watch mode during development
- Version control your changes with Git

## 📝 Advantages Over Plain CSS

✅ Variables for easy theme customization
✅ Mixins for reusable styles
✅ Nesting for better readability
✅ Modular structure for large projects
✅ Easy maintainability

## 🐛 Troubleshooting

**Problem**: SCSS won't compile
- Solution: Check if Sass is installed: `sass --version`

**Problem**: Changes don't appear
- Solution: Clear browser cache (Ctrl + Shift + R)

**Problem**: CSS doesn't work in Jellyfin
- Solution: Make sure you're using the compiled `.css` file, not the `.scss` file

## 📄 License

MIT License - Free to use for private and commercial projects

---

**Enjoy your modern Jellyfin theme! 🎉**

