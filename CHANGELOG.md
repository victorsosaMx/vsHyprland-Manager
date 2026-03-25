# Changelog — vsHyprland Manager

All notable changes to this project are documented here.
Format: [SemVer](https://semver.org) — newest first.

---

## [1.1.0] — 2026-03-25

### Changed

- **Wallpaper** — Migrated `swww` and `swww-daemon` to `awww` and `awww-daemon` following the official renaming. See: [Renaming swww](https://www.lgfae.com/posts/2025-10-29-RenamingSwww.html)

---

## [1.0.0] — 2026-03-22

Initial release.

### Features

- **Appearance** — General (gaps, border size, rounding, layout), Decoration (active/inactive border colors, opacity), Shadow (enable, range, color, offset), Blur (enable, size, passes, noise, contrast, brightness, vibrancy), XWayland (force zero scaling); wallpaper managed via desktop tool (e.g. awww)
- **Animations** — 6 out-of-the-box presets (None, Subtle, Smooth, Bouncy, Snappy, Cinematic) plus full manual editor: Bezier curve editor (add/remove named curves with control points) and animation assignments list (name, enabled, speed, curve, type)
- **Input** — Keyboard (layout, variant, options, numlock, caps remap), Mouse (sensitivity, accel profile, scroll factor, natural scroll, follow mouse), Touchpad (enable, natural scroll, tap to click, tap button mapping, scroll factor), Dwindle layout (pseudotile, preserve split, smart split, smart resizing), Master layout (new on top, new is master, no gaps when only)
- **Hot Corners** — per-corner actions with a Cairo visual monitor diagram; preset actions (hyprexpo, rofi, swaync, lock, shutdown) or custom command
- **Monitors** — Monitor list (add/remove rows: name, resolution, position, scale, transform, disabled)
- **Keybindings** — Variables tab (`$VAR = value`) + Keybindings tab (modifier, key, dispatcher, argument); profile save/load
- **Rules** — Window Rules, Layer Rules, and Blur Layers each in their own tab; profile save/load
- **Autostart** — exec-once list (add/remove commands)
- **Environment** — environment variable list (add/remove: key, value)
- **Plugins** — Loaded & Active, Available, and Repos in separate tabs; panels for HyprExpo, HyprFocus, Hyprbars, Borders++, Hyprtrails, HyprScrolling, Split Monitor Workspaces, Hyprgrass, Hyprwinwrap; add/remove repos; auto-refresh after changes
- **Scripts** — built-in editor for auxiliary scripts (`hotcorner.sh`, `awww-random.sh`, etc.); Save (with automatic backup), Reload, Load Default and Run buttons; execute-permission toggle (`chmod +x`)
- **vsHub** — discover, launch, and install the full vsHyprSettings suite; shows install status, Launch / GitHub / Install (AUR) buttons per tool; fetches a remote manifest from GitHub in the background; falls back to local cache or built-in list when offline
- **About** — app icon, version, author block, link buttons (GitHub, Hyprland, victorsosa.com), safety section with originals-folder shortcut and one-click restore
- **Modular config** — each section writes to its own file under `~/.config/hypr/modules/`; your other includes are untouched
- **Timestamped backups** — every apply creates `YYYYMMDD_HHMMSS_` backups in `~/.config/hypr/backups/`
- **Dark / Light editor theme** toggle (Forest Night palette)
- **Apply** writes all config files and runs `hyprctl reload`
- Consistent design system with vsWaybar Studio (Forest Night theme, GTK3, JetBrainsMono Nerd Font, borders-only depth)