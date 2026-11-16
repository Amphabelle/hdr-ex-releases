# HDR EX releases

HDR EX is a gameplay mod for Super Smash Bros. Ultimate built on top of
[HewDraw Remix](https://github.com/HDR-Development/HewDraw-Remix) v0.50.5. It ports the mechanics of the
Brawl mod *SD P++ EX*: always-on airdash and hitfall, tilt / aerial cancels, aerial parry, trade cancel,
faster throws with anti-chaingrab protection, a reverse ledge trump, and global damage / hitstun / shield tuning.

## Install (emulator)

**With the launcher (recommended).** Download `HDR-EX-Launcher-Setup-*.exe` from the
[launcher release](https://github.com/Amphabelle/hdr-ex-releases/releases/tag/launcher-v0.2.0), install it and
start it:

1. select your emulator (`eden.exe` for Eden);
2. confirm the SD card folder (Eden's `sdmc` folder is found automatically);
3. optionally select your Smash Ultimate game file, so that **Play** starts the game directly;
4. click **Install HDR EX**: it downloads everything as one zip (about 1.5 GB) and extracts it by itself.

**Update.** The launcher shows **Update (!)** when a new version is out, and only downloads the packages
that changed.

**Repair.** *Tools > Repair Install* downloads and reinstalls everything.

**By hand.** Download `hdr-ex-full.zip` from the [latest release](https://github.com/Amphabelle/hdr-ex-releases/releases/latest)
and extract it into your emulator's `sdmc` folder (it already contains `atmosphere/...` and `ultimate/...`).
If `hdr-ex-manifest.json` lists a package newer than the versions under `full`, extract that package's zip on top.

You need Super Smash Bros. Ultimate with the same game update as HDR v0.50.5 (the latest one). HDR EX replaces vanilla HDR (they use the same
`ultimate/mods/hdr` folder).

## Packages

| Package    | Content                                                      |
|------------|--------------------------------------------------------------|
| base       | skyline and the plugins HDR needs (ARCropolis, smashline...) |
| hdr-ex     | the HDR EX plugin and parameters (`ultimate/mods/hdr`)       |
| hdr-assets | HDR's assets (`ultimate/mods/hdr-assets`)                     |
| hdr-stages | HDR's stages (`ultimate/mods/hdr-stages`)                     |

Every release is built and checked on GitHub Actions: the HDR EX plugin is compiled from source, and the
assets, stages and plugins come from HDR's official v0.50.5 package, each file checked against HDR's published hashes.

## Credits

HDR EX is based on HewDraw Remix by the HDR Development team, and the launcher on the
[HDR Launcher](https://github.com/techyCoder81/hdr-launcher-react) by techyCoder81 (MIT). The assets, stages
and plugins are redistributed from HDR v0.50.5 and keep their authors' licenses.

## For the maintainer

Mod releases are tagged `vX.Y.Z` and must stay the repository's *latest* release (the launcher reads
`releases/latest/download/hdr-ex-manifest.json`). Launcher releases are tagged `launcher-vX.Y.Z` and created
with `--latest=false`.
