# Things to know in this release

Starling is an early preview (v0.4.0). A few limits you will notice:

- **No screen lock.** There is a [screensaver](#the-screensaver), but it is decoration:
  any key or mouse movement dismisses it, with nothing asked. Do not rely on
  it to secure an unattended machine.
- **Every display scales the same.** The session picks one scale for the whole
  desktop, from the primary panel's pixel density, and Settings → Displays
  moves it in 0.25 steps (fractional scales included — 1.25 and 1.5 render as
  crisply as 2.0). A second monitor of a different density therefore shares
  the first one's scale; per-display scale is not implemented yet.
- **Changing the scale does not rescale apps already open.** The desktop and
  Starling's own apps follow immediately; a third-party Wayland app keeps the
  size it started at until you restart it.
- **No display-mode picker.** The session uses the connector's preferred mode.
- **Zoom runs without audio.** It starts and reports `no pactl and pacmd
  found`. That message is expected: `pactl` is deliberately left off the system
  because Zoom crashes at startup when it is present. **Do not install
  `pulseaudio-utils` to fix it** — that trades a silent Zoom for one that will
  not start. Sound in other apps (Chrome, Slack, Teams) is unaffected.
- Verified on **AMD** and **virtio-gpu** graphics, and on **NVIDIA** as the
  second GPU of a hybrid laptop (per-app render offload). Intel, and NVIDIA
  driving the desktop itself, are not yet tested.

If something misbehaves, the session log is at
`/tmp/starling-session-<your-uid>.log`. The last fifty lines are usually the
ones that matter:

```
tail -n 50 /tmp/starling-session-$(id -u).log
```

Issues go to <https://github.com/starling-build/starling/issues>; attach that
log, and for a terminal rendering problem the report described in
[When the terminal draws the wrong thing](#when-the-terminal-draws-the-wrong-thing).

