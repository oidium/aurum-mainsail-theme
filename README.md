# Aurum

A warm, gold-accented dark theme for [Mainsail](https://github.com/mainsail-crew/mainsail), inspired by a desktop system monitor using the Aamis palette.

- Near-black panels, cream text, and muted gold accents.
- Bundled JetBrains Mono Nerd Font, loaded locally without a font service.
- Thin gold borders, 4px corners, and spaced uppercase headings.
- Compact 3px dashboard gutters and outer margins on G-Code Files and G-Code Viewer.
- Gold outlines for unhomed toolhead actions; solid gold for homed actions. Other warning and error colors remain unchanged.

## Install

1. Download **Aurum-v1.0.0.zip** from [Releases](https://github.com/oidium/aurum/releases/latest) and extract it.
2. Open Mainsail and select the printer you want to theme.
3. Under **Machine**, enable **Hidden files**. Create or open `.theme` in the printer's configuration directory.
4. Back up existing theme files. Upload `custom.css`, `monitor-mono.ttf`, and `OFL.txt` from the archive's `.theme` directory directly into that directory on the printer.
5. In **Interface Settings**, select **Dark** mode. Set the primary and logo colors to **#e2be8a**, or **RGB(226, 190, 138)**.
6. Hard-refresh the page with **Ctrl+Shift+R**.

The extracted `.theme` folder is hidden on some systems; enable hidden files in your file manager. Do not upload the ZIP itself or nest another `.theme` directory inside the printer's `.theme` directory.

When one Mainsail server connects to several printers, install the files in each selected printer's configuration directory through Moonraker. They do not belong in the Mainsail web server's application directory. No Klipper or Moonraker restart is needed.

## Palette

| Use | Hex | RGB |
| --- | --- | --- |
| Background | `#0f0f0f` | 15, 15, 15 |
| Foreground | `#eadccc` | 234, 220, 204 |
| Gold | `#e2be8a` | 226, 190, 138 |

## Transparency

Aurum's page backgrounds are opaque by default. Desktop wallpaper showing through an entire browser window requires an operating-system window-opacity setting, which is separate from this theme. A suggested starting point is **92% opacity**. No desktop settings are installed by this package.

## Compatibility and limits

Designed for Mainsail's Vuetify 2 interface and a modern browser with CSS `:has()` support. Desktop appearance was reviewed using screenshots during development; mobile layouts have not been visually verified. Future Mainsail markup changes may require selector updates.

Light mode is left unchanged. The theme preserves Mainsail's layout and behavior; canvas-rendered chart fonts and 3D viewer colors are controlled by Mainsail rather than this stylesheet. There are no scripts, printer commands, or remote font requests in the theme.

## Uninstall

Rename `.theme/custom.css` to `custom.css.disabled`, or restore your previous theme files, then hard-refresh. Restore your previous primary and logo colors if desired.

## License

Theme CSS and documentation: [MIT](LICENSE), copyright 2026 oidium.

Bundled JetBrains Mono Nerd Font: [SIL Open Font License 1.1](.theme/OFL.txt). The font is redistributed unchanged; its copyright notices and license are included. See [JetBrains Mono](https://github.com/JetBrains/JetBrainsMono) and [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts).
