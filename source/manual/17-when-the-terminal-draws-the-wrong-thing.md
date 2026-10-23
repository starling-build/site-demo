# When the terminal draws the wrong thing

Press **⌘⇧R** (`Ctrl+Shift+R`) while the wrong thing is on screen. Two files
land at the top of your home folder:

```
starling-terminal-report-20260819-103759.txt
starling-terminal-report-20260819-103759.png
```

Attach both to the issue. The `.txt` says what the terminal believed was on
screen, along with the fonts it loaded, the size of its cells and which glyph
path drew them; the `.png` is that same frame as it was painted, recorded
inside the terminal rather than captured from the display.

The pair is what makes a rendering bug fixable, because between them they say
*which half* is wrong — text right and picture wrong is a drawing bug, text
already wrong is not. A photograph of the screen cannot distinguish those, and
almost every such report arrives as a photograph.

The `.txt` includes the text that was on your screen when you pressed the
chord (scrollback is not included). Read it before you attach it.

One thing worth trying first, and worth saying in the issue either way: start
the terminal with the atlas painter off:

```
STARLING_TERM_ATLAS=0
```

That swaps the whole glyph-drawing path for an older one kept for exactly
this comparison. If it fixes what you
are seeing, that halves the search.

---

*See also: [Things to know in this release](#things-to-know-in-this-release),
and the project [README](https://github.com/starling-build/starling) for the
technical picture and what does and doesn't work yet.*
