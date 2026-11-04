# PulsePilot

**Automate every action. Control every input.**

PulsePilot is a free Windows desktop app that automates your mouse and keyboard: an auto clicker, a mouse-button
holder, automatic key pressing and key holding, global hotkeys, and a keyboard/mouse macro recorder with playback
and a timeline editor. Everything runs locally on your PC — no account, no cloud, no telemetry.

> **Status: v2.0.0 pre-release.** Color Hunter is included as a preview and is **under development**. PulsePilot works and has been tested, but this build is still in final acceptance
> testing. Please report any problem in [Issues](../../issues). See what's new in the [Changelog](CHANGELOG.md).

---

## Download

Go to **[Releases](../../releases/latest)** and download **one** of these:

| File | Use it if… |
|---|---|
| **`PulsePilot_2.0.0_x64-setup.exe`** (recommended) | You want a normal installation. Installs for your user only, no administrator rights needed, adds Start Menu and desktop shortcuts. |
| `PulsePilot_2.0.0_x64_en-US.msi` | You prefer an MSI package (installs for all users; needs administrator rights). |
| `PulsePilot_2.0.0_x64_portable.exe` | You don't want to install anything. Just run the file. |

**Requirements:** Windows 10 or 11, 64-bit. PulsePilot uses Microsoft Edge WebView2, which is already part of
Windows 11 and up-to-date Windows 10 (the installer downloads it if it is missing).

### "Windows protected your PC"

PulsePilot is not code-signed yet, so Windows SmartScreen may warn you the first time. Click **More info → Run
anyway**. If your antivirus is cautious about tools that send keyboard and mouse input, allow PulsePilot. You can
check that your download is genuine by comparing its SHA-256 with `SHA256SUMS.txt` in the release:

```powershell
Get-FileHash .\PulsePilot_2.0.0_x64-setup.exe
```

---

## What you can do with it

| Feature | What it does |
|---|---|
| **Auto Clicker** | Clicks for you: primary, secondary, middle, Mouse 4/5; single or double clicks; any interval from hours down to milliseconds; until stopped, for a set time or a set number of clicks; at the cursor or at a fixed screen position (pick it with a crosshair). |
| **Click Holder** | Holds a mouse button down until you stop it or for a set time. |
| **Keyboard → Auto Presser** | Presses a key, a sequence of keys (with delays) or a combination such as Ctrl + S, repeatedly. |
| **Keyboard → Key Holder** | Keeps keys held down (*Hold*), or holds modifiers and repeats other keys like a physically held key (*Repeat*). |
| **Macro Studio** | Records your keyboard, clicks, mouse movement and scrolling, then plays it back at 0.25×–4× speed, with loops and delays. Edit recordings in a timeline editor; import and export them. |
| **Color Hunter** *(under development)* | Pick an exact screen colour and click every matching spot: Spawn Detection (click each new appearance) or Loop Detection (repeat). Exact RGB only. Results may be incomplete while this module is being finished. |
| **Hotkey Manager** | Start and stop everything from any application with global shortcuts you can change. |
| **Profiles, History, Dashboard** | Separate setups for different tasks, a local log of every run, and statistics. |

## Quick start

1. Install and open PulsePilot.
2. Open **Auto Clicker**, choose the button and interval, and click **Start clicking** (or press **Ctrl + Alt + F6**
   from any app). Press it again to stop.
3. To record a macro: **Macro Studio → Record**, do your actions, **Stop**, give it a name, **Save**. Select it and
   press **Play** (or **Ctrl + Alt + F8**).

### Default hotkeys

| Hotkey | Action |
|---|---|
| **Ctrl + Alt + F12** | **Emergency Stop** — stops everything and releases all keys and buttons (cannot be disabled) |
| Ctrl + Alt + F11 | Release all held keys and buttons |
| Ctrl + Alt + F6 | Start/stop Auto Clicker |
| Ctrl + Alt + F5 | Start/stop Click Holder |
| Ctrl + Alt + F10 | Start/stop Key Presser |
| Ctrl + Alt + F3 | Start/stop Key Holder |
| Ctrl + Alt + F7 | Start/stop recording a macro |
| Ctrl + Alt + F8 | Play/pause the selected macro |
| Ctrl + Alt + F9 | Pause/resume everything |

Change them in **Hotkey Manager**. On laptops you may need to hold **Fn** for the F-keys.

## Tips

- **Primary / secondary button:** PulsePilot follows your Windows mouse setting (left- or right-handed). You can
  override it in **Settings → Primary mouse button**.
- **Recording and playing macros:** press **Record** (or your hotkey) and PulsePilot steps aside (minimises) and
  gives the focus back to the app you were using — just do your actions there. Stop with your hotkey or the tray menu
  (**Start/Stop Recording**); PulsePilot comes back so you can **Save**. Playback also minimises PulsePilot and starts
  in the app you were using. Macros repeat keys and screen positions, not windows, so arrange your windows the way they
  were when you recorded. Scrolling over PulsePilot's own window is never recorded.
- **Runs in the background:** closing the window (red ×) keeps PulsePilot in the system tray, and all hotkeys keep
  working. The tray icon shows a **green** dot while a task runs, **amber** when paused and **red** while recording.
  While the window is hidden, a Windows notification confirms each hotkey action. To quit: right-click the tray icon →
  **Exit**.
- **Auto Clicker position:** with **Fixed screen position** it clicks that exact spot, not where your mouse is.
- **Privacy:** PulsePilot only watches your keyboard and mouse while you are recording. Don't record passwords.

## Troubleshooting

| Problem | Fix |
|---|---|
| A key or button seems stuck | Press **Ctrl + Alt + F12** (Emergency Stop) or **Ctrl + Alt + F11**. |
| A hotkey seems to do nothing | Look at the notification or the tray icon dot. With **Fixed screen position** the Auto Clicker clicks that spot, not where your mouse is. If PulsePilot was closed with tray mode off, it is not running — start it again. |
| Clicks or keys do nothing in one program | That program probably runs as administrator; Windows blocks input into it. Run it normally, or run PulsePilot as administrator. |
| A hotkey shows "Failed" | Another program already uses that combination — pick another one in Hotkey Manager. |
| A game ignores PulsePilot | Some games and anti-cheat systems ignore simulated input. PulsePilot does not try to bypass them. |
| Very fast intervals are slower than set | Windows can't guarantee timing below about 10 ms. |

## Uninstall

**Settings → Apps → PulsePilot → Uninstall** (portable version: just delete the file). Your settings and macros stay
in `%APPDATA%\com.pulsepilot.app` until you delete that folder.

## Use responsibly

Only automate software and websites where automation is allowed. You are responsible for following the rules of
the programs and services you use.

## License

[MIT](LICENSE) © 2026 PulsePilot contributors
