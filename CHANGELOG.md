# Changelog

All notable changes to PulsePilot.

## [1.1.0] — 2026-11-01 (pre-release)

PulsePilot now keeps working comfortably in the background.

### Added
- **Runs in the system tray by default.** Clicking the window's close button (red ×) keeps PulsePilot running in
  the tray, so your hotkeys keep working. The first time, a notification tells you how to quit
  (right-click the tray icon → **Exit**). You can change this in **Settings → Close to system tray**.
- **Notifications while PulsePilot is hidden.** When the window is minimised or in the tray and you use a hotkey,
  a Windows notification confirms what happened — e.g. *"Auto Clicker started — Primary click every 1000 ms at
  screen position 460, 1009, starting in 1.0 s"*, *"Auto Clicker stopped"*, *"Macro playing"*, *"Emergency stop"*.
  Errors are reported the same way. Turn them off with **Settings → Show informational notifications**.
- **Tray icon shows activity.** A small dot on the tray icon: **green** while a task runs, **amber** when
  automation is paused, **red** while recording. No dot when idle.

### Changed
- Existing installations: **Close to system tray** is switched on once when you update. If you turn it off again,
  it stays off.

### Notes
- Hotkeys and tasks have always worked while PulsePilot is minimised. If "nothing seems to happen", check where the
  Auto Clicker clicks: with **Fixed screen position** it clicks that spot, not where your mouse is — the new
  notification now tells you the position.

## [1.0.0] — 2026-11-01 (pre-release)

First public release.

- Auto Clicker (primary/secondary/middle/Mouse 4/5, single or double click, fixed position picker, run modes).
- Click Holder, Key Presser (single, sequence, combination) and Key Holder (*Hold* and *Repeat*).
- Macro Studio: record keyboard, clicks, moves and scrolling; playback 0.25×–4× with loops; timeline editor;
  import/export; PulsePilot minimises itself during playback.
- Global hotkeys with Emergency Stop (Ctrl + Alt + F12) and Release All.
- Follows the Windows primary mouse button, with an override in Settings.
- Profiles, history, dashboard statistics, diagnostics.
- Rounded window with a custom title bar.
