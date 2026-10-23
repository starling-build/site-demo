# Workspaces — a desktop for your agent

**Ctrl + ↓** opens **workspace mode** — a room where one app drives and
everything it opens stays beside it. The workspace list is on the left, the
**driver** runs down the middle, and every window the driver opens lands as a
**tab** on the right — never on your desktop. **Ctrl + ↓** again (or
**Workspace** in the desktop menu) steps back out to the desktop you came
from; the workspace and its apps keep running, and the same key leads back in.

It is built for handing work to an AI agent — coding is the demo, not the
boundary: start a terminal as the driver, run an agent in it, and whatever
the agent opens to do its job — browsers, editors, documents — stacks up as
tabs in its room while your own windows never move. You can watch, and you
can step in — click into any pane and use it like any other window. There is
a three-minute recording of a coding agent doing exactly this on
[starling.build](https://starling.build/#agents).

### Handing a task to an agent

1. Press **Ctrl + ↓**. The room opens on the monitor the pointer is on.
2. Click **+ New** at the top of the list, type a name for the workspace and
   press **Enter**.
3. The empty room asks **Choose an app to work in** — pick **Terminal**. It
   becomes the driver, running down the middle.
4. In that terminal, go to the project and start the agent.
5. Hand it the task. Each window the agent opens — a browser to read docs, an
   editor, a document — lands as a tab on the right, never on your desktop.
6. Press **Ctrl + ↓** again to step back out and carry on with your own
   work; the agent keeps running. The same key leads back in.

Step 4, for a coding agent that runs in the terminal, is two lines:

```
cd ~/projects/my-app
claude
```

> **Tip.** If the agent takes over a window you need, press **Esc** to
> release it — see [Keyboard shortcuts](#keyboard-shortcuts).

### Working the room

- **+ New** (top of the list) creates a workspace and opens its name for
  editing in place — type and press **Enter** (**Esc** keeps the old name).
  Rename later from the **pencil** on the row you are pointing at, or
  right-click the row.
- An empty workspace shows **Choose an app to work in** — pick the driver.
- Drag the divider between the driver and the tabs to change the split.
- Right-click a tab to **Move to Desktop** (the window leaves the room) or
  **Close** it.
- The **trash** on a hovered row opens the same menu as a right-click, which
  holds the two ways out: **Remove** moves the workspace's windows to your
  desktop and drops the row; **Delete** stops every app in it. Both sit
  behind the menu on purpose — a stray click on a hover button must not be
  able to stop your agent's apps.
- Each monitor has its own workspace mode: **Ctrl + ↓** acts on the monitor
  the pointer is on and leaves the others alone.

---

