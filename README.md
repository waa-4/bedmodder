# BedModder v0.2

Free, locally saved Minecraft Bedrock add-on editor. No account, backend, or internet is required. Unzip the folder and open `index.html`, or upload all files to GitHub Pages.

## What changed from v0.1

- **Custom block editor:** full-cube blocks with a selected texture, mining hardness, friction, light emission, and creative inventory access.
- **Function editor:** create `.mcfunction` files with multiple commands. Type `/fi` at the start of a line and press Tab to complete `fill`; other common commands are suggested too. Any leading `/` is stripped during export.
- **Recipe editor:** crafting-table shaped and shapeless recipes with custom results and ingredients.
- **Loot table editor:** weighted entries and counts, exported as `loot_tables/bedmodder/<id>.json` (usable by other files/commands, but not automatically connected to mobs or blocks).
- **Language editor:** change exported US-English names for blocks and items.
- **Project search:** search items, blocks, functions, recipes, and loot tables.
- **Offline export:** JSZip is bundled locally; no CDN needed.
- **v0.1 compatibility:** existing browser saves use the same localStorage key, with new fields added. `.bedmodder` project backups can also be imported.
- Retains all earlier item and pixel-art features.

## Running and updating

Extract everything into one folder. Open `index.html` in a browser. If you are replacing an existing website, **keep all five files together**: `index.html`, `style.css`, `app.js`, `addon-v02.js`, `jszip.min.js`. Download a `.bedmodder` project backup before updating. Saving is browser-profile-local.

## Supported output

Behavior and resource pack manifests, Bedrock item and basic block definitions, textures, recipes, functions, simple loot tables, and English display names. Exports a `.mcaddon`. For function use, run `/function <path>` in game. Loot tables must be called/referenced from other content to have any effect.

## Boundaries

This is v0.2, not a complete engine. Script API, biome editing, entities, advanced blocks, custom block geometry, visual Scratch blocks, version-specific migration, and importing existing `.mcaddon` files are planned, **not included**. Validate exported add-ons in a disposable Minecraft Bedrock world. The JavaScript passes syntax checks, but browser interaction and in-game validation are still needed. Never test first on a valuable world.
