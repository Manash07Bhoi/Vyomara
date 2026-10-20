# Starter QA Report (pre-Godot-runtime)

**Date:** 2026-10-20  
**Status:** Partial static review only. This is not an engine/runtime QA sign-off.

## Checks run in the authoring environment

- Confirmed expected `project.godot`, scene, script, image-reference and audio files are present.
- Confirmed all 17 distinct local `res://` path literals extracted from scripts, scene files and project settings resolve to files in this project.
- Confirmed the configured main scene is `res://scenes/menu/MainMenu.tscn` and the `SaveService` autoload path exists.
- Opened and verified all 5 included WebP concept-reference images using Pillow.
- Checked all 4 WAV files with Python's `wave` reader: each has a valid header, mono 22050 Hz audio, and durations between 0.45 and 1.8 seconds.
- Confirmed the music file is an Ogg Vorbis audio stream, stereo at 48000 Hz.
- Manual source review found and corrected a malformed nested `else` in `scripts/enemies/shadow_sentinel.gd` and adjusted the fixed trailing camera / starting heights before packaging.
- Confirmed `godot` / `godot4` executables are not installed in the authoring environment, so no Godot headless parse/import/run test was possible.
- External asset download attempts failed because outbound DNS/network access was unavailable; no third-party 3D packs are bundled.

## Not tested / blocked

- Godot parser and resource import.
- In-editor run of menu/first realm.
- Touch controls on a physical Android device.
- Enemy combat, collision paths, shrine interaction, restart and local-save round trip.
- Performance/FPS/thermal stability.
- Godot Android export templates, APK export, installation and offline runtime.
- Third-party asset imports, optimization and attribution verification.

## Required next smoke test

1. Import `VYOMARA_Android_Prototype/project.godot` in the Godot Android editor.
2. Wait for all project assets to import; open and run the project.
3. Resolve parse errors first, one by one, retaining raw errors and a copy of fixed files.
4. Tap ENTER THE FIRST REALM, dismiss intro, move with joystick, attack, pulse and dodge, defeat the Shadow Sentinel, reach the shrine and press ACT.
5. Restart, confirm first-completion save is still present; repeat in airplane mode.
6. Record actual device model, editor version, renderer, frame rate and test duration.
7. Do not claim an APK exists unless it is exported and launched successfully.
