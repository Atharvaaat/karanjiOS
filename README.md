# karanjiOS 2.0

A desktop operating system that runs entirely in the browser — in **one self-contained `index.html`**.
Open the file (or host it on GitHub Pages) and it boots. No build step, no dependencies.

Made for Karan's birthday.

## What's inside

**Desktop shell**
- Two layouts: **Taskbar** (Windows/KDE style, start menu, centered or left) or **Dock + menu bar** (macOS/GNOME style, magnifying dock)
- Window manager: drag, resize from any edge, **edge/corner snapping**, **snap layouts** on the maximize button, always-on-top
- **Workspaces** (1–9) and **Task View / Mission Control** overview with drag-to-workspace
- Launchpad (Alt+A): every app in one full-screen grid with categories and search
- Status tray / menu-bar extras for things running in the background (music keeps playing after you close Karanify, timers, recording)
- Motion: spring window open from where you clicked, genie minimize, workspace slides, circular theme reveal, wallpaper parallax
- Alt+Tab switcher, universal **search launcher** (apps, files, settings, calculator, web, terminal commands)
- Quick Settings (dark mode, night light, do-not-disturb, full screen, brightness, volume), notification center, calendar
- Login and lock screen, multiple user accounts, sign out / switch user / restart / shut down
- Light and dark themes, accent colours, wallpapers (built-in or your own images), transparency, corner radius, text size, Windows- or macOS-style window buttons

**Linux-style system**
- Inode filesystem stored in IndexedDB, with **owners, groups, rwx permissions, setuid/setgid/sticky bits, symlinks**, `/tmp`, `/dev/null`
- Real `/etc/passwd`, `/etc/group`, `/etc/shadow` (salted SHA-256), `sudo` group, polkit-style password prompts in the GUI
- Freedesktop-compatible Trash with restore

**Apps**
| App | Highlights |
|---|---|
| KaranShell (Terminal) | bash-like shell: pipes, redirection, `&&`/`||`, variables, `$(...)`, `$((...))`, globs, `if`/`for`/`while`/`case`, functions, scripts, aliases, history, tab completion, tabs, themes; 130+ commands including `ls find grep sed awk sort cut xargs diff chmod chown sudo su passwd useradd usermod top ps kill curl neofetch` |
| Karanplorer (Files) | grid/list views, breadcrumbs, search, drag & drop, cut/copy/paste, rename, Quick Look (Space), properties with permission/owner editor, import from your computer |
| KaranjiFox (Browser) | tabs, address bar with suggestions, bookmarks, history, Wikipedia reader view, YouTube embedded player, `file://` access to your files |
| Karan Code (Editor) | tabs, syntax highlighting, find & replace, Markdown and HTML live preview, save as administrator |
| Karan Settings | appearance, taskbar/dock, windows, users & groups, date & time, sound, default apps, storage, backup & restore |
| KaranTop (System Monitor) | processes (end task), live CPU / memory / FPS charts |
| Karangram, Karanify, KaranFlix, KaranCam | gallery and viewer with edits, player with visualizer, video player with playlist, photo + video capture |
| Need for Karan | pseudo-3D arcade racer with curves, hills, traffic, nitro and engine sound |
| Karan 2048, KaranSweeper, Karanconda | puzzle classics and snake |
| KaranPaint | brush, pencil, shapes, fill, spray, text, picker, undo/redo, save to Pictures |
| Karan Keep | sticky notes with colors, pins, search, export |
| KaranCalc, KaranClock | standard/scientific; world clock, alarms, stopwatch, timer |

## Getting started

Default account: **karan** (no password — set one in Settings › Users or with `passwd`).
A second account, **guest**, is a standard (non-admin) user.

Useful shortcuts: `Alt+Space` search · `Alt+Tab` switch · `Alt+Q` task view · `Alt+T` terminal · `Alt+E` files · `Alt+L` lock · `Alt+Shift+Arrows` snap.
Use **Quick Settings › Full screen** so the browser lets karanjiOS capture keys like Alt+Tab.

## Notes
- Everything is stored locally in your browser. Use Settings › Storage › Export backup to save a copy.
- A web page can't embed a real browser engine, so KaranjiFox fetches pages through a public CORS relay and renders them in a locked sandbox (links and forms stay inside KaranjiFox). Sites that need logins or heavy scripts may still need a real tab — there's a button for that. Don't log in to your bank here.
