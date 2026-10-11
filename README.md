# BedModder — prototype 0.1

Free, browser-based Minecraft Bedrock add-on maker. No sign-in or server required.

## Run

Upload `index.html`, `style.css`, and `app.js` to a GitHub Pages repository, or open `index.html` in a browser. An internet connection is required to load JSZip from cdnjs for `.mcaddon` exporting. You can host JSZip locally later for fully offline use.

## Included

- Project settings: name, namespace, description, version.
- Custom item editor: identifier, display name, stack size, creative menu, tool display, icon selection.
- 16×16 transparent pixel editor; PNG import/export.
- Local project persistence via localStorage; `.bedmodder` backup and restore.
- Basic project validation.
- `.mcaddon` export with linked behavior and resource packs, manifests, item definitions, and PNGs.

## Scope

This is a small proof of concept, not yet the full BedModder editor. No blocks, entities, command functions, Scratch logic, multiplayer, or complex scripts are implemented. Editing an imported `.mcaddon` is not implemented. Test exports in a disposable Minecraft Bedrock world. Real game behavior has not been verified here.

## Security and storage

Projects are saved only in the current browser profile. Browser-data clearing removes those saves; download a `.bedmodder` backup regularly. The app makes no account or analytics requests. The third-party JSZip CDN is used solely to load the ZIP generator.

## Minecraft format

Manifest format 2, items format 1.21.30, resource-pack item atlas, PNG icon assets. The resource pack is declared as a behavior-pack dependency. The selected minimum engine version is exported in pack manifests. Validate and test for each target Bedrock build.
