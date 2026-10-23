# Installing more apps

Starling launches applications that are installed on your machine — it does not
bundle them. Three ways to add them:

### Through the App Store

Open the **App Store** from the dock. It lists a curated set of applications —
Chrome, VS Code, Slack, Discord, Teams, Telegram, IntelliJ IDEA, GIMP, Blender,
Spotify, Zoom, and more. Click **Install** on one and Starling installs it
using your system's own `apt` (you may be asked to authenticate — this is
`polkit` authorising the install). When it finishes, the app appears in the
Launchpad and can be pinned to the dock.

A few things to know about the store in this release:

- The catalog is **small and curated** — every entry installs and launches,
  but it is not your whole software library.
- Tiles use **generic category glyphs**, not vendor logos, on purpose — those
  logos are trademarks and Starling ships none of them. Chrome and VS Code show
  their real icons in the Launchpad and dock (read from your system at
  runtime); the rest use a neutral glyph.

### From the command line

Every App Store entry can also be installed from a terminal, which is handy on
a machine you reach over SSH or set up from a script. The command takes the
app's id — the same names the store uses:

```
app-install chrome
app-install vscode
```

It installs the same way the store does, writes the app's record so the
Launchpad and [dock](#the-dock) pick it up at once, and prints what it did.
No relogin is needed.

### With your distribution's packaging

Anything you install the normal way — `sudo apt install <package>`, a `.deb`, a
Snap or Flatpak — is a native Linux app, and Starling will run it as a Wayland
client (or through the in-tree X server for X11 apps):

```
sudo apt install gimp
```

The major toolkits composite today: Chromium/Electron, Qt6, GTK3 and GTK4.

> **Note.** Whichever way an app arrives, it appears in the
> [Launchpad](#the-launchpad) under the name in its `.desktop` entry, and
> keeps its own icon where it ships one.

---

