# The screensaver

Leave the desk for ten minutes and the desktop dissolves into a screensaver:
your own screen, blurred and drifting behind a slow liquid warp, with the
time and date floating over it. Any key, click, or mouse movement brings it
straight back — nothing is asked for, so it is decoration, not a lock.
**Ctrl + Shift + S** shows it immediately.

Change the idle time (or turn it off) in **Settings → Appearance →
Screensaver** (see [Settings](#settings)). Video playback holds it off: an app that tells the desktop
it is playing something — Chrome, Firefox, a video player — keeps the
screensaver away for as long as it says so, so a film watched without
touching the mouse is never interrupted.

For **aerial footage** in place of the warp, drop a video file in
`~/.local/share/starling/aerials/`:

```
mkdir -p ~/.local/share/starling/aerials
cp ~/Downloads/coastline.mp4 ~/.local/share/starling/aerials/
```

The screensaver dissolves into it and loops it. Starling ships none of its own — the warp needs no assets, and the
clips worth watching are large. Any shape works: letterbox bars are cropped
away and the picture fills the screen.

> **Note.** The screensaver is not a lock: nothing is asked when it clears.
> See [Things to know in this release](#things-to-know-in-this-release).
