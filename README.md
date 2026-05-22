# COSMOS Mainsail Theme

A lightweight custom theme for [COSMOS](https://github.com/OpenCentauri/cosmos) firmware on Centauri Carbon printers. There is no installer script - copy the files by hand to avoid extra load on the printer.

## What’s included

| File | Purpose |
|------|---------|
| `custom.css` | Colors, scrollbars, panels, and editor styling |
| `sidebar-logo.png` | Logo in the sidebar |
| `sidebar-background.png` | Sidebar background |
| `main-background.png` | Main content area background |
| `favicon-16x16.png` | Browser tab icon (16×16) |
| `favicon-32x32.png` | Browser tab icon (32×32) |

Every file is optional. Mainsail only loads what you place in `.theme`.

## Requirements

- COSMOS Firmware installed and working on your printer.

## How to install

If you are using COSMOS, you probably know what you are doing already. However, if you have no brain and can't figure it out by yourself, here's a guide.

### 1. Create the theme folder

**Mainsail file manager:** open **Machine** → config files, enable **Show hidden files** in the cog menu (the folder name starts with a dot), then create `.theme`.

### 2. Copy theme files

Copy all files from this repository into `.theme` so the layout looks like:

```text
~/printer_data/config/.theme/
├── custom.css
├── favicon-16x16.png
├── favicon-32x32.png
├── main-background.png
├── sidebar-background.png
└── sidebar-logo.png
```

### 3. Reload Mainsail

- Hard-refresh the browser so CSS and images are not cached: **Ctrl+Shift+F5** (Windows/Linux) or **Cmd+Shift+R** (macOS).
- No Klipper restart is required; theme assets are served by Moonraker/Mainsail from disk.

If something does not appear, confirm filenames match the table above exactly (including extensions).

## Partial install

You can copy only the assets you want - for example, only `custom.css` for colors without custom backgrounds or logo.

## Customize colors

Edit `custom.css`. Panel backgrounds use the CSS variable `--v-panel-base` in `:root`; change that value to adjust matching surfaces in one place.

## Remove the theme

Delete the files in the `.theme` folder, or remove the entire `.theme` folder, then hard-refresh the browser.

## References

- [Mainsail custom themes](https://docs.mainsail.xyz/features/custom-themes/)
- [Custom CSS](https://docs.mainsail.xyz/features/custom-themes/custom-css/)
- [COSMOS Firmware](https://github.com/OpenCentauri/cosmos)
- [Mainsail for Neptune (for the original theme)](https://github.com/zzcatvs/mainsail-for-neptune)

## Special thanks
- [ELEGOO](https://www.elegoo.com) - for designing such shit firmware and hardware components that we had to replace the entire firmware just to get a decent UI.