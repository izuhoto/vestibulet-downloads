# Vestibulet v1.0.3 2026-07-01

### Improvements

**Settings window follows the active workspace**
- The settings window now opens on the currently active desktop (Space), consistent with folder bookmarks, related items, and the main shelf.
- Window position and size continue to be saved and restored.

**Mini Shelf (egress) default**
- In Settings → Mini Shelf (egress), **Keyboard egress** is now enabled by default for new installations and when using **Restore defaults**.

**Finder intake behavior (“Notification only”)**
- Fixed an issue where the shelf window could still appear when **After adding from Finder** was set to **Notification only**.
- This applies only to Finder-driven intake via:
  - Finder Service / Quick Action (“Add to Vestibulet Shelf”)
  - The global shortcut for sending Finder selection to the shelf
- Intake via temporary shelves (edge drop, mini drop, etc.) is **not** affected and keeps its existing behavior.

# Vestibulet v1.0.2 2026-07-01

**Fixed ESC key behavior for the temporary shelf**

Fixed an issue where pressing ESC while the temporary shelf was visible during a drag did not dismiss the shelf and instead sent the key event to Finder (often canceling the drag).

- Pressing ESC while the temporary shelf is visible now dismisses only the shelf; the drag continues
- Works for edge, hold-to-show, and modifier-triggered temporary shelves
- After dismissing with ESC, the temporary shelf stays hidden for the rest of that drag (resets when you release the mouse button)

*Requires Accessibility permission (System Settings → Privacy & Security → Accessibility).*

# Vestibulet v1.0.1 2026-06-30

**Windows now open on the current workspace (Space)**

- The shelf, Related Items, and Locations windows now appear on the Space you're currently on when reopened, instead of switching back to the Space where they were last closed.
- Each window's position and size are preserved exactly as before — only the workspace follows you to the active Space.

# Vestibulet v1.0.0 2026-06-30

This is the first release of Vestibulet.
You can use the basic features for temporarily storing files and text while dragging, Finder integration, history management, and organizing frequently used items in a unified library.

## Highlights
- Drag-and-drop shelf for temporarily holding files and text
- Shelf access from the screen edge, near the cursor, or via keyboard shortcuts
- File actions such as copying paths, Quick Look preview, and revealing in Finder
- Unified library for files, folders, web pages, and app-related items
- Navigation through related items
