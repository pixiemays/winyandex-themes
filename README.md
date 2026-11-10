<h1 align="center">WinYandex Themes</h1>

<p align="center">
  <strong>Curated community theme repository and distribution catalog for WinYandex</strong>
</p>

<p align="center">
  <strong>English</strong> • <a href="README_ru.md">Русский</a>
</p>

<p align="center">
  <a href="https://github.com/pixiemays/WinYandex"><img src="https://img.shields.io/badge/Client-WinYandex%20v0.9.90-0078D4" alt="Client" /></a>
  <a href="https://github.com/pixiemays/winyandex-themes"><img src="https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D4?logo=windows" alt="Platform" /></a>
  <a href="https://github.com/pixiemays/WinYandex/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-GPL--3.0-blue.svg" alt="License" /></a>
</p>

---

This repository hosts curated custom themes and serves as the backend catalog for the in-app theme showcase in **[WinYandex](https://github.com/pixiemays/WinYandex)**.

---

## Catalog

### Mega Meow

* **Author:** [@pixiemays](https://github.com/pixiemays)
* **Accent Color:** `#FFF472B6`
* **Base Theme:** Dark
* **Backdrop:** MicaAlt

**[Download mega-meow.wytheme](https://github.com/pixiemays/winyandex-themes/raw/main/themes/mega-meow/mega-meow.wytheme)**  
*(after downloading, open the file or drag and drop it into the WinYandex window)*

---

## Installation Methods

### 1. In-App Showcase
1. Open **WinYandex** -> navigate to **Settings** -> **Appearance**.
2. Expand the **Community Themes** section.
3. Click **Install** / **Apply**.

### 2. One-Click Deep Link
Click the installation link (`winyandex://theme/install?url=...`) from the catalog. The client downloads, extracts, and applies the theme instantly.

### 3. Drag and Drop
Download the `.wytheme` or `.json` file and drop it anywhere onto the WinYandex window.

---

## Theme Specification

Themes are packaged as `.wytheme` (ZIP archives) or standalone `.json` files.

### Configuration (`theme.json`)

```json
{
  "id": "theme-identifier",
  "name": "Theme Name",
  "author": "Author Name",
  "version": "1.0",
  "description": "Short theme summary",
  "baseTheme": "Dark",
  "backdrop": "MicaAlt",
  "accentColor": "#FFF472B6",
  "backgroundColor": "#FF0B0E14",
  "cardColor": "#FF131924",
  "secondaryCardColor": "#FF1A2332",
  "backgroundImage": "background.jpg",
  "backgroundOpacity": 0.3
}
```

### Property Reference

| Property | Type | Description |
|---|---|---|
| `id` | String | Unique identifier in kebab-case. |
| `name` | String | Display name of the theme. |
| `author` | String | Creator handle or name. |
| `version` | String | Semantic version string. |
| `description` | String | Short summary displayed in the theme card. |
| `baseTheme` | String | Base palette: `"Dark"` or `"Light"`. |
| `backdrop` | String | Window backdrop material: `"Mica"`, `"MicaAlt"`, `"Acrylic"`, or `"Solid"`. |
| `accentColor` | Hex String | Primary accent color (`#AARRGGBB` or `#RRGGBB`) for buttons, sliders, and active items. |
| `backgroundColor` | Hex String | Window surface tint color. |
| `cardColor` | Hex String | Primary card surface color. |
| `secondaryCardColor` | Hex String | Secondary card and panel surface color. |
| `backgroundImage` | String | Relative filename of wallpaper image inside package (e.g. `background.jpg`). |
| `backgroundOpacity` | Number | Opacity multiplier for adaptive dimmer overlay (`0.05` to `0.90`). |

---

## Contributing Themes

1. Fork this repository.
2. Create a folder under `themes/<theme-id>/` containing:
   * `theme.json`
   * `preview.jpg` — screenshot of the theme running in WinYandex.
   * `<theme-id>.wytheme` — theme package exported from WinYandex.
3. Add the entry to `community_themes.json`:
   ```json
   {
     "id": "theme-id",
     "name": "Theme Name",
     "author": "YourHandle",
     "version": "1.0",
     "description": "Theme description",
     "accentColor": "#FF...",
     "previewUrl": "https://raw.githubusercontent.com/pixiemays/winyandex-themes/main/themes/theme-id/preview.jpg",
     "downloadUrl": "https://raw.githubusercontent.com/pixiemays/winyandex-themes/main/themes/theme-id/theme-id.wytheme"
   }
   ```
4. Submit a Pull Request.

---

## License

Distributed under the [GNU General Public License v3.0](https://github.com/pixiemays/WinYandex/blob/main/LICENSE).
