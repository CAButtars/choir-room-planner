# Choir Room Planner v0.9 preview

Open https://cabuttars.github.io/choir-room-planner/preview/ in Safari. To install a shortcut, choose **Share → Add to Home Screen → Add**. The shortcut is named **Choir Preview**. Internet access is needed; offline use is not guaranteed.

This is a review candidate. The room uses a tapered shell, curved terraces and individually editable furnishings. Absolute dimensions, ceiling height, opening positions, furniture proportions and arrangement remain provisional. It is not a surveyed model.

## Try it

- Drag with one finger to orbit; use two fingers to pan or zoom.
- **Top** opens the overhead planning view. Tap a chair or piano, choose **Move** or **Rotate**, and drag a colored handle.
- **Duplicate** copies furniture; **Delete** hides it. Undo/redo and Reset are in the menu. Architecture remains protected.
- **Eye** opens an interior view. Drag to look and use the arrow buttons to step. This mode has no collision detection or automatic stair climbing.
- The menu can hide or show walls, ceilings, chairs, pianos, cabinets and risers.

## Keep layouts

Save/Load uses this browser on this device. Nothing is uploaded, and saves do not sync across devices. Safari and a Home Screen shortcut may keep separate storage. Export JSON for a transferable backup; Import JSON restores a compatible preview layout.

This geometry revision uses `choirRoomLayoutReviewV09Section1`. The original planner's `choirRoomLayoutV07` records are untouched. Do not import old-version layouts: positions and object identities differ. Future geometry revisions need either a tested migration or a new storage namespace. Export a backup before updates.

## Distribution and updating

Only the reconstructed GLB, generated carpet texture, application, icons and vendored Three.js dependencies are included here. No original scan, photographs, videos, private comparison renders, Blender master or personal layouts are published. Three.js 0.128.0 is vendored with its MIT license; no paid service or external API is used.

GitHub Pages serves this folder at `/preview/`. Update only the curated preview files after local validation. The original root application and model can remain untouched while the preview is reviewed. The previous root version is recoverable from commit `c14a625ee38ae1cc0cca3505ce3685c3eb230336`.

## Validation and limits

Local desktop Chromium and emulated touch tests cover rendering, navigation, object selection, move/rotate, duplicate, hide, undo/redo, save/reload, JSON export/import, architecture protection, phone/tablet layouts and visible startup errors. Geometry checks cover terrace construction, chair and rail support, and intended door clearances. These checks do not certify physical measurements.

Physical iPhone/iPad Safari performance and gestures still need device verification. The web model is approximately 3.0 MB with 65,558 triangles. The front work area and several architectural details remain simplified.

## Material and lighting update

The first visual finish pass adds meter-scaled carpet flecks, subtle cabinet grain, chair weave, plaster surface detail, piano reflections and brighter interior fill lighting. Textures and the reflection environment are generated locally; no reference imagery is published. Object identities, geometry and layout storage remain unchanged. This improves material realism but does not make the provisional geometry a photographically accurate twin.

The second detail pass refines rounded chair seats and curved backs, adds ventilation-grille surfaces and upright-piano panel details, and uses brass pedal hardware. Plain unprinted pages suggest an open score without copying reference documents. Furniture layout identities and positions remain compatible with existing preview saves.

## Reference-guided surface pass

The carpet now uses an AI-synthesized swatch guided by the supplied carpet appearance, rather than wrapping a classroom photograph onto the room. Tan lower-wall finishes, pale upper acoustic-panel joints, smaller cabinet pulls, and recessed rear-speaker cones follow visible reference features. Joint spacing and furniture dimensions remain estimated. No room photographs, identifying text, or private comparison pages are included. Existing furniture-layout identities and positions remain compatible.

## Riser-end review update

Two straight riser fronts beside the upright-piano aisle were provisionally corrected using local scan evidence; poorly supported ends were left unchanged. The menu now offers **Face risers** and **Side aisle** interior views, with ceilings visible and eye-level movement enabled. Trim projects slightly from the walls to prevent overlapping-surface flicker. Furniture positions, editable IDs and layout storage are unchanged. These corrections do not certify staircase dimensions or architectural accuracy.
