# Recording the screen

Starling records itself, with no extra software.

- **Record** (control centre, or **Ctrl + Shift + R**) captures the whole
  screen.
- **Record App** opens Mission Control and asks which window you want. It
  captures that window's own content, not the region of screen it sits in, so
  windows stacked on top never appear and moving or resizing the window
  mid-recording doesn't spoil the take. The pointer is drawn in and follows
  the window.

While a recording runs, a **red dot and a running clock** sit in the menu
bar, so a recording can never be going unnoticed. Stop it the same way you
started it.

Recordings land in **`~/Videos`** as MP4, and the
[Video Player](#the-apps) opens them; so does anything else that plays MP4.
Where the machine has a hardware H.264 encoder, the frame the compositor
already drew goes straight to it as a dma-buf and the CPU never touches a
pixel — on a modern laptop that costs about 0.05 of a core. Machines without
one fall back to a software encoder, which works but costs more.

---

