# ArtCraft Launcher assets

Pictures that [ArtCraft Launcher](https://github.com/storytold/craft-launcher) downloads at run
time instead of bundling: today, the screenshots on each Craft App's details page.

The launcher reads `https://raw.githubusercontent.com/storytold/craft-launcher-assets/<tag>/<app>/<key>.jpg`
at a pinned tag (`SCREENSHOTS_REV` in `crates/core/src/details.rs`), and keeps what it downloads
under that tag, so a published tag must never change.

## Changing a picture

1. Add or replace JPEGs (1200 × 750 px, 8:5, no metadata, ideally under 150 KB; the launcher
   refuses anything over 2 MB or not a JPEG).
2. Update `ATTRIBUTION.md` in the same change.
3. Tag the result (`v2`, `v3`…) and bump `SCREENSHOTS_REV` in the launcher. Older launchers keep
   reading the tag they know.

Every picture's license is in `ATTRIBUTION.md`: the apps' UI is under each app's own license, and
the artwork, photos and footage shown are public domain or were made with the apps themselves.
