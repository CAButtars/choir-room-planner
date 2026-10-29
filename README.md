# Choir Room Planner v0.7

A free, mobile-friendly 3D room-layout planner using an approximate classroom reconstruction. This is a planning prototype, not a surveyed architectural or safety/egress plan.

**Open:** https://CAButtars.github.io/choir-room-planner/

## Use the planner

- Drag the room to orbit; use two fingers to pan/zoom on touch devices, or the mouse wheel to zoom. **Top** opens an overhead view; **3D** returns to the room view.
- Tap furniture to select it. Choose **Move** or **Rotate**, then drag a colored gizmo handle. **Duplicate** creates a copy. **Delete** hides the selection; Undo can restore it.
- The menu contains Focus, Lock, Save/Load, Undo/Redo, Reset, JSON Export/Import, and Show/Hide ceilings.
- Architecture is protected from editing, deletion, duplication, and unlocking. Ceilings start hidden for an unobstructed planning view; their geometry remains in the original model.
- Reset restores original furniture and removes duplicates. Undo can reverse a reset. Reset does not erase the saved layout until Save is pressed.

## iPhone and iPad

Open the website directly in Safari, then choose **Share → Add to Home Screen → Add**. The app includes a title, standalone manifest, safe-area viewport settings, and a Home Screen icon. Internet access is required to load the site; offline use is not guaranteed.

## Save and transfer layouts

**Save layout** stores the current furniture configuration in this browser on this device. **Load layout** restores it, including duplicates. Saves do not sync across devices and are not uploaded to GitHub. Browser data clearing may erase them, and Safari and a Home Screen app may use separate storage.

Use **Export JSON** for a backup. Move that file using Files, AirDrop, or another method, then use **Import JSON** on the other device. Press **Save layout** after importing to keep it in that browser. Import accepts this planner's layout format; invalid files show an error. Existing v0.7 records with matching object names are supported; old saves that captured only the entire `world` container cannot recover individual furniture positions.

## Project and deployment

GitHub Pages publishes `main` at `/ (root)` automatically after each push. No paid service, API, account login, or build step is required to use the app.

- `index.html`: interface, viewer, and layout logic.
- `room.glb`: original supplied model, unchanged.
- `vendor/`: pinned Three.js 0.128.0 and controls/loader, with its MIT license. Libraries load from this site rather than a third-party CDN.
- `manifest.webmanifest`, `icon-*`, `icon.svg`: mobile installation metadata and icons.
- `.nojekyll`: serves the static files directly.

To preview locally, run `python3 -m http.server 8000` in this directory and open `http://localhost:8000`.

Before an update, export a layout backup. Edit and test locally, commit, and push to `main`; check the Pages deployment in GitHub Actions. Keep the `choirRoomLayoutV07` storage key and stable model object names/IDs to preserve saved configurations. A model replacement or schema change needs an explicit migration and restore test. Do not commit personal layout backups, photos, raw scans, credentials, or student information.

## Validation and limits

Deployment fixes address the model's Z-up orientation, individual-object selection, centered edit pivots, architecture protection, duplicate persistence, undo/reset, and visible loading errors. The model file is unchanged; the viewer applies its orientation and pivots at runtime. Existing shapes and component boundaries remain as supplied, including separate piano and conductor-stand components.

Desktop Chromium testing covers rendering, navigation, overhead view, pointer selection, move/rotate gizmo dragging, duplication, hide/undo, save/load after reload, JSON export/import, reset, architecture protection, phone/tablet viewport layout, and missing-model error reporting. Physical iPhone/iPad testing and native Safari touch gestures require device verification. This repository does not contain classroom photographs, raw scans, or student data; its reconstructed model is publicly downloadable.
