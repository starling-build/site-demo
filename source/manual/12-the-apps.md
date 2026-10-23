# The apps

Nine first-party apps ship with Starling, all written against its Swift
framework:

- **Settings** — appearance, displays, network, sound, and system information.
  See [Settings](#settings).
- **Files** — browse your home directory and the filesystem.
- **Terminal** — a real terminal with a PTY; runs your login shell (`$SHELL`,
  falling back to bash). TUI programs like `vim` and `htop` work. If it ever
  draws the wrong thing, see
  [When the terminal draws the wrong thing](#when-the-terminal-draws-the-wrong-thing).
- **Text Editor** — a plain-text editor.
- **Calculator** — a basic calculator.
- **App Store** — install more applications. See
  [Installing more apps](#installing-more-apps).
- **Task Manager** — CPU, memory, disk and network with live sparklines, a
  sortable process table, and End Process.
- **Video Player** — plays your recordings and other video. For Starling's own
  recordings it decodes on the GPU and never copies a frame through the CPU.
- **Image Viewer** — opens images from Files.

---

