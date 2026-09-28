# Adding a plugin to the site

PascalPatch plugins are written by the community. To get yours onto the app's **Browse** page:

1. **Build it.** Follow the guide at [PascalPatch/docs/plugins](https://github.com/Dylan-Demolder/PascalPatch/blob/master/docs/plugins/README.md). It takes you from the SDK template to your plugin running in game.
2. **Check it** with the same script this repository's CI runs:
   ```
   python <PascalPatch>/tooling/check_plugin.py path/to/<id> --community --build
   ```
3. **Open a pull request** that adds its source as `community/<id>/`: `plugin.json`, `README.md`, `native/` (and optionally `LICENSE`). Send source only, with no DLLs and nothing from the game.
   Title it `<Name> <version>`. In the description, say what it does, how you tested it, and whether it changes the game (writes memory, drives a controller, loads states, hooks functions).
4. **Review.** The *Community plugins* check builds it and attaches the ZIP. A reviewer reads the source and tries it in game.
5. **Publish.** Once merged, the maintainer builds it from the reviewed source, signs the index and publishes it. It then shows up in every PascalPatch app.

Updates work the same way: bump `version`, write what changed in `changes`, and open a pull request.

## The rules

- **Offline only.** No networking, no telemetry, and nothing for netplay.
- **No game data.** Players bring their own game.
- **GPL-2.0-or-later**, with the source here.
- **No harm.** Nothing that damages saves, hides what it does, collects data, or writes outside its own folder.
- **Credit** the research and ideas you build on.

The full review checklist is in [Publishing and contributing](https://github.com/Dylan-Demolder/PascalPatch/blob/master/docs/plugins/publishing.md#the-review-checklist).
