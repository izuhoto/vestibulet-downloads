# Vestibulet v1.0.15 2026-09-25

This release makes opening items from File Search results feel more natural.

#### Changes

- File Search results can now be opened by double-clicking an item.

# Vestibulet v1.0.14 2026-09-24

This release makes saved File Search conditions and search results easier to organize, and lets you choose how copied paths from search results are formatted.

#### Changes

- Saved File Search conditions can now be renamed in place.
- Saved File Search conditions can now be reordered by dragging them or using the menu.
- Search result columns can now be reordered by dragging them or using the menu.
- Search result column widths can now be adjusted by dragging, and double-clicking a divider fits the column to its contents.
- When a search result name or location is long, hovering over it now makes the full text easier to check.
- Copy Path in File Search results now lets you choose the path format that fits your use.
- Paths that include Japanese file or folder names now copy in a form that works more smoothly when pasted into Terminal and other tools.
- Renaming a saved condition no longer switches away from the search conditions you are currently editing.

# Vestibulet v1.0.13 2026-09-23

This release adds File Search, so you can find files and folders by conditions and send results straight to the shelf or open them in place.

#### Changes

- Added File Search from the menu bar, the shelf toolbar, and a keyboard shortcut.
- Search inside chosen folders, exclude folders, and filter by name, text, kind, date created, date modified, and date last used.
- Window and Quick Look commands now bring Vestibulet back to the front more consistently.

# Vestibulet v1.0.12 2026-08-31

This release fixes file additions from Terminal so files are found correctly after they appear on the shelf.

#### Changes

- Fixed a case where files added from Terminal could show as missing on the shelf even though they existed.
- File locations typed from the folder you are working in, including `~` home-folder shortcuts and `./` prefixes, now point to the expected file.

# Vestibulet v1.0.11 2026-08-26

This release makes temporary shelves and Mini Shelf more reliable across workspaces, so they open where you are instead of getting stuck on another desktop.

#### Changes

- Fixed a case where edge and cursor-near temporary shelves could appear only on one workspace.
- Fixed a case where opening Mini Shelf could unexpectedly switch you back to a previous workspace.

# Vestibulet v1.0.10 2026-08-08

This release makes temporary shelves and Mini Shelf more reliable during drag workflows, especially when moving across Spaces or canceling drags with ESC.

#### Changes

- Fixed cases where edge and cursor-near temporary shelves could stop appearing after switching workspaces (Spaces) or after the app had been hidden.
- When the cursor-near temporary shelf is visible and you move to the screen edge, Vestibulet now switches to the edge shelf and restores the cursor-near shelf after you leave the edge.
- After dismissing a temporary shelf with ESC, pressing ESC again now reaches the source app so the current drag can be canceled.
- If Vestibulet is brought to the front unexpectedly during a drag, it now restores focus to the original app so ESC-based drag cancellation still works.
- When dragging items out of the main shelf leaves it empty, the shelf window now closes automatically. It stays open when items remain or the drag is canceled.
- Window presentation commands now unhide Vestibulet when needed, so the shelf, Related Items, Folder Bookmarks, Settings, About and guide windows, and Quick Look previews can appear after the app was hidden.

# Vestibulet v1.0.9 2026-07-29

This release makes the shelf easier to keep in reach while you work by letting it stay above normal windows.

#### Changes

- The shelf window now appears above normal windows by default.
- Added a toolbar pin button to turn the shelf's always-on-top behavior on or off. The setting is saved for future launches.

# Vestibulet v1.0.8 2026-07-29

This release makes the shelf easier to use across multiple desktops (Spaces) and improves how groups appear in Mini Shelf (egress).

#### Changes

- While the shelf window is open, it now appears on all workspaces, so you can drop items in or out without switching Spaces.
- In Mini Shelf (egress), group rows now show child item names within the available space, in addition to the group name (with “+N more” when there are too many to list).

# Vestibulet v1.0.7 2026-07-29

This release improves the window behavior after opening items from Folder Bookmarks and Related Items.

#### Changes

- Folder Bookmarks and Related Items now close their window after the normal Open action succeeds for all selected items.
- Hold `Shift` while opening to keep the window open.
- In Folder Bookmarks, `⌘O` / `Return` opens and closes, while `⇧⌘O` / `⇧Return` opens and keeps the window.
- In Related Items, `⌘O` opens and closes, while `⇧⌘O` opens and keeps the window.
- The same behavior now applies to Open buttons, double-click actions, and context menu actions.
- Added menu items, shortcut hints, and tooltips for the “keep window open” flow.

# Vestibulet v1.0.6 2026-07-07

### New
- **Double-click** or right-click **Execute** to open items in the Related Items and Bookmark windows
- Right-click **Copy Path** / **Copy Link** now support multiple checked items

### Target selection
- Checked items → all checked
- No checks → clicked row only

# Vestibulet v1.0.5 2026-07-03

**Improved tag editing UI**

- Replaced comma-separated tag input with chip-based editing: add and remove tags one at a time
- Existing tags appear as suggestions you can add with a click
- Apply tags to multiple selected items at once in Bookmarks and Related Items
- When multiple items are selected, shared tags are shown together and can be removed from all at once

# Vestibulet v1.0.4 2026-07-02

### Fixes

- **Improved Slack current-item detection** — When a Slack channel is open, the Related Items panel now correctly detects and matches its URL. Release builds also prompt for Accessibility permission when needed.
- **Per-column tag filtering in Related Items** — Tag filters now apply only to the focused column (Library, Related Items, or Candidates), not all columns at once.

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
