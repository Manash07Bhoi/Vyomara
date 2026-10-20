# MASTER EXECUTION PROMPT — VYOMARA ANDROID 3D GAME BUILD

You are the lead technical director, Godot 3D gameplay engineer, environment artist, technical artist, animation/rigging integrator, audio designer, QA engineer and release engineer for **VYOMARA — The First Light of Dharma**. Do not stop after research or produce only a plan. Research, acquire legally usable assets, implement the project, run tests, iterate, and produce the final importable Godot project ZIP wherever your workspace tools permit.

## 0. Product identity (do not alter)

- Game: **VYOMARA**
- Creator credit: **A VISION BY JP** (JP = Jaya Prakash Sahu). JP is the creator/developer, not an in-world hero.
- Tagline: **Across the Yugas. Through the Realms. Guided by Dharma.**
- Genre: 3D Hindu mythology-inspired action-adventure.
- Primary platform: Android phone; Godot Android editor workflow. User-reported hardware: 12 GB RAM, >15 GB free space, Godot is already working.
- First deliverable: a small but convincing real-time 3D playable glimpse, not another static image montage.
- Engine: Godot 4.x GDScript only; prefer Godot 4.6 stable if available/compatible. Use Compatibility renderer as safe baseline. No C#, paid plugins, paid APIs, server, login, or online dependency.
- Offline-first: entire vertical slice must be playable in airplane mode and save locally.
- Visual reference: the user already has a cinematic reveal sequence showing a dark/gold JP credit, the VYOMARA title, a celestial temple world, and visual concept glimpses of Lord Shiva, Lord Vishnu and Lord Hanuman. Reference files are concept art, not actual 3D game assets and not proof of gameplay.
- Character guardrail: do NOT add JP, Rimi, or other private/personally related people as in-world heroes. Divine/mythological figures belong in the game based on researched traditions. For the first playable slice, Hanuman is the current art-direction candidate. Don't imply an invented mission is a scriptural event.

## 1. Mandatory execution order

**Stage 1 — Inspect and report the environment.**
1. List available files and identify whether this workspace contains an existing Godot project. Do not overwrite unrelated files or use destructive commands.
2. Inspect `project.godot`, all `.tscn`, scripts, current assets and the current asset ledger if present. If using the supplied starter, review its code rather than trusting its comments.
3. Record Godot version, available CLI/executable, Blender or mesh tools, audio tools, free disk space, and whether internet downloads work in this sandbox.
4. If this workspace contains `VYOMARA_Android_Prototype`, continue from it, retain useful assets and edit in place. Otherwise create an equivalently organized project from scratch and document that choice.
5. Never claim a command/test ran unless you ran it and captured the exit code/output.

**Stage 2 — Research, compare and choose assets.**
1. Search official docs and source asset pages. Read the individual license, not just a search snippet. Verify actual download availability. Research the Godot Android editor, renderer support, glTF import, and Android export/template requirements.
2. Build an `ASSET_RESEARCH.md` with date, candidate, direct source page, creator, exact license, model triangle/texture/rig details when available, download outcome, risks and decision.
3. Prefer CC0, or CC BY with documented attribution. Do not use NC, ND, unclear licensing, leaked/ripped media, subscription-only assets, or protected downloads without permission. Avoid share-alike unless you explain compatibility first.
4. Attempt to download the official free **Kenney Nature Kit** (https://kenney.nl/assets/nature-kit; listed CC0), **Kenney Prototype Kit** (https://kenney.nl/assets/prototype-kit; listed CC0) and use only what improves the result. For materials/environment, evaluate Poly Haven (https://polyhaven.com/license, CC0; https://polyhaven.com/models). Do not download the entire internet or import all 300 files; select only needed objects to limit build size.
5. Evaluate the South Indian Temple Modular Kit by rSquare (https://sketchfab.com/3d-models/south-indian-temple-modular-kit-25f0176668004faa98ec351e04e58920; listed CC BY; roughly 8.3k triangles per page). If downloaded, preserve author/title/source/license attribution and note any transformations.
6. Evaluate the animated Hanuman model by NG Creations (https://sketchfab.com/3d-models/hanumananimated-c5af66701ee940f69a6b68384a5ba725; listed CC BY, approximately 177k triangles, listing marked AI-generated). Also compare other models where useful, but do not choose solely by likes/downloads. Verify the model can actually be downloaded, inspect quality and animations, check its cultural/iconographic fit, optimize/LOD it, and credit it. Never ship at 177k triangles without testing/optimization. The smaller stylized Hanumanji by bothe.h (https://sketchfab.com/3d-models/hanumanji-5605eca5dc8d467686cc0771685ef9c4; listed CC BY, about 27.6k triangles, AI-generated/toy-like) is a fallback candidate only if its art style fits. A highly detailed static deity statue is not a valid replacement for a playable rigged hero.
7. Animation: Mixamo (https://helpx.adobe.com/creative-cloud/faq/mixamo-faq.html) is free with Adobe ID and permits using its characters/animations in games, but the auto-rigger is designed for bipedal humanoids; test any tail/extra appendage handling. Do not claim Mixamo auto-rig works for a monkey-like deity until it is verified.
8. Sound effects: first use included original synthetic audio, then evaluate Mixkit (https://mixkit.co/free-sound-effects/; free license details https://mixkit.co/license/modal/sfxFree/) or other clearly licensed sources. Confirm whether attribution is required and never redistribute a stock SFX as a standalone pack. No film/TV music, unlicensed bhajan, or copied game audio.
9. If outbound network is blocked or a source needs an unavailable login, document it and continue using the included original art, synthetic sounds and procedural assets. Never invent a successful download. **Do not block the entire project on a difficult model download.**
10. At the end, `ASSET_LEDGER.md` must list every used third-party item: exact title, creator, original page, exact license, transformations, use location and complete attribution. Include license files where redistribution permits. Never claim a resource is CC0 unless the source page says so.

**Stage 3 — Build the actual 3D vertical slice.**
Work code-first, not picture-first. The project must open/run in the Godot Editor.

### A. Look and feel
- Premium mythic Indian temple-world: warm sandstone and carved details, aged gold, deep indigo/celestial blue, devotional saffron accents, dramatic sunrise, water, distant layered mountains, restrained particles and a strong sanctuary/gateway focal point.
- Use the included generated concept art only as menu/visual reference. Do not bake the entire concept poster into the 3D level and claim it is the world.
- A single dominant golden-hour directional light with measured shadows, cool ambience, fog only if supported and performant in chosen renderer; emissive materials for shrine/gateway; shared materials; readable visual hierarchy.
- Build one polished compact 3D playable court with foreground, midground and skyline, a clear traversal route, temple structure, lamps/banners, water or waterfalls if performant, shrine and gateway. Make collisions correct; avoid decorative obstacles being silently non-collidable on the main path.
- If a real temple asset is added, blend it stylistically and technically; set scale/origin/materials/LODs and collision meshes. Don't use a real sacred building's name unless the model is an accurate depiction and usage/context are appropriate.

### B. Hero
- Replace the current procedural avatar proxy with an appropriate legally obtained and technically sound Hanuman model if possible. Use a respectful silhouette and iconography. If no model passes license/quality/rig checks, keep the current proxy for internal mechanics testing, label it as proxy in UI/docs, and state it blocks a public-quality build. Do not use an obviously toy-like or mangled asset just to check a box.
- Configure humanoid rig/skeleton, root transform, scale, collision capsule, material settings and animation library. If you cannot implement a model, leave the project playable with proxy and do not call art complete.
- Minimum animation states where a suitable rig permits: idle, walk, run, basic gada strike, hit/damage, dodge, divine/game-only pulse pose, victory. Ensure state transitions don't pop or break rotation.
- Player movement relative to camera, smoothing, gravity/collision, camera follow, short dodge and invulnerability window. Use in-place animations unless root-motion testing proves reliable.
- Touch controls must be thumb-friendly: analog virtual joystick on bottom-left, action buttons bottom-right with safe spacing; attack, PULSE, DODGE, ACT. Keyboard fallback for tests. Show clear cooldown/readiness.

### C. Enemy and encounter
- Create one visually distinct **original fictional Shadow Sentinel**, never a deity. Provide idle/approach/attack/telegraph/hit/defeat behavior; enemy health display; player health; short cooldowns; damage numbers or hit sparks where tasteful.
- Basic attack is a short-range forward attack (GADA). PULSE is an explicitly invented game mechanic; do not attribute it to sacred texts. It has a cooldown and clear VFX/SFX, and affects enemies within a defined radius. DODGE has a brief, bounded invulnerability window and feedback.
- On sentinel death, remove collision/group and safely trigger objective changes once. Guard against access to freed nodes, repeated victory signals and duplicate HUD.

### D. Quest flow
- Start objective: reach the shrine / face the guardian (choose a clear first prompt).
- Enemy must remain alive until defeated. Interacting too far away says “Move closer”; trying before the sentinel is defeated says it is still guarding the shrine.
- Shrine ACT interaction toggles shrine/gateway state with visual/audio feedback, marks the chapter completed and writes local `user://` save.
- If player dies, show retry. Victory overlay offers replay and return to title. Restart must reset all scene state without duplicate signals.
- Save file has a version number and safely handles missing/corrupted/outdated data. No cloud/server is used.

### E. UI, menu and audio
- Title screen: “A VISION BY JP”, VYOMARA, tagline “Across the Yugas. Through the Realms. Guided by Dharma.”, clear “ENTER THE FIRST REALM”, disclosure that this is a prototype/concept in development.
- HUD: objective, player health, enemy health only while relevant, message/toast, action buttons, optional fps/debug display behind a developer toggle.
- Results overlay: “FIRST LIGHT RESTORED”, locally saved status, replay/menu.
- Audio: original included synthesized score, bell, pulse, impact; add footsteps, wind/water ambience or interface clicks only from sources with compatible licences. Volume must be sensible and optional audio sliders should work if included.
- Scene sounds must work in airplane mode; no streaming music or online asset fetching at runtime.

**Stage 4 — Asset integration and technical polish.**
1. Copy downloaded assets into organized folders (`assets/characters`, `environments`, `materials`, `animations`, `audio`, `vfx`). Keep references separated from game files.
2. Import each 3D asset in Godot and inspect orientations/normals/materials. Prefer `.glb`/glTF; use Blender only if available and license-safe. Use mesh decimation/LOD only when it does not destroy sacred detail. Keep original source assets or source URLs/versions in your asset ledger.
3. Add optimized collision; avoid importing camera/light leftovers from DCC scenes. Fix scale/forward axis, texture paths and material roughness/metalness.
4. Add subtle VFX: dust motes, shrine ring, pulse, hit impact, transition; keep fill rate transparent effects restrained.
5. Add audio SFX; avoid harsh clipping/volume jumps. Mix music lower than interaction/impact cues.
6. Remove unused candidate downloads from the shipped game ZIP. Don't include giant archives as unused project baggage.

**Stage 5 — Test repeatedly.**
1. If a Godot CLI is available, run import/parse checks and headless execution on the actual project with the matching engine version. Capture raw output and exit codes. If not, say so and perform static resource/path validation. Do not fake tests.
2. Open/run the project in the editor if possible. Fix all GDScript parse errors, missing resources and warnings indicating likely crashes. If only Android editor is available to the user, provide a short phone smoke-test protocol and list which checks remain untested.
3. Test the entire mission loop from fresh launch through victory, death/retry, replay, return to menu and offline airplane mode. Test joystick on actual phone; simulate touch if automated tests cannot access touchscreen.
4. Measure frame rate on target device; goal is stable 30 FPS for 10–15 minutes, but only report measured results. Test actual landscape orientation, buttons not clipped, camera not obstructed, audio plays, and thermal behavior.
5. Test save file missing/corrupt/outdated handling and ensure the project never requires internet to start or play.
6. Write `QA_REPORT.md` with PASS/FAIL/UNTESTED/BLOCKED per item, Godot version, device/renderer, logs, known issues and next steps.

**Stage 6 — Delivery.**
- Output a complete project folder where `project.godot` is at ZIP root/project root and all needed files are included.
- Produce `VYOMARA_Android_Prototype_Final.zip` (or similarly clear final name). Include the actual source scenes/scripts, only assets that are used and licensed, `README.md`, `VYOMARA_PRD.md`, `ASSET_RESEARCH.md`, `ASSET_LEDGER.md`, attribution/license text, `QA_REPORT.md`, import instructions and `SHA256SUMS.txt`.
- If Android export templates are installed and export works, build an APK and install/launch it when possible. Do not promise or invent an APK if templates or runtime device are unavailable. Otherwise deliver the project ZIP ready to import and explain exact steps to export from Godot Android editor.
- If visual evidence can be captured, include screenshots of title menu, gameplay, encounter HUD, shrine victory, and imported asset inspection. Do not label concept art as gameplay screenshots.
- End with: files actually produced; assets downloaded successfully vs blocked; exact tests run vs not run; project import steps; remaining known issues. Clearly separate implemented, unverified and future work.

## 2. Starter project contents and usage

If available in the workspace, inspect and reuse:
- `project.godot`
- `scenes/menu/MainMenu.tscn`
- `scenes/world/FirstRealm.tscn`
- `scenes/player/Hero.tscn`
- `scenes/enemies/ShadowSentinel.tscn`
- scripts under `scripts/`
- `assets/reference_art/` (concept/reference only)
- `assets/music/` and `assets/sfx/` (original synthetic audio)
- `VYOMARA_PRD.md`, `docs/ASSET_LEDGER.md`, `docs/MYTHOLOGY_AND_CULTURAL_GUARDRAILS.md`, `docs/QA_TEST_PLAN.md`

The starter is not accepted as fully tested. Audit/fix it. If its GDScript parse errors block progress, fix them before adding features. Do not delete the asset ledger or change the creator/game identity.

## 3. Research references to cite in report

- Godot Android editor and limitations: https://docs.godotengine.org/en/4.6/tutorials/editor/using_the_android_editor.html
- Godot renderer comparison: https://docs.godotengine.org/en/4.6/tutorials/rendering/renderers.html
- Godot 3D scene import format guidance: https://docs.godotengine.org/en/stable/tutorials/assets_pipeline/importing_3d_scenes/available_formats.html
- Godot 3D CharacterBody example: https://docs.godotengine.org/en/4.6/getting_started/first_3d_game/index.html
- Poly Haven CC0 license: https://polyhaven.com/license
- Kenney Nature Kit: https://kenney.nl/assets/nature-kit
- Kenney Prototype Kit: https://kenney.nl/assets/prototype-kit
- Quaternius current license: https://github.com/Quaternius/quaternius.github.io/blob/main/license.html
- Mixamo official FAQ: https://helpx.adobe.com/creative-cloud/faq/mixamo-faq.html
- Mixkit SFX license: https://mixkit.co/license/modal/sfxFree/
- Temple kit: https://sketchfab.com/3d-models/south-indian-temple-modular-kit-25f0176668004faa98ec351e04e58920
- Hanuman animated candidate: https://sketchfab.com/3d-models/hanumananimated-c5af66701ee940f69a6b68384a5ba725
- Arena Agent Mode workflow and ZIP behavior: https://help.arena.ai/articles/5432423882-how-to-use-agent-mode

## 4. Non-negotiable quality standard

Do not return after summarizing the task, researching asset pages, or writing a plan. Continue to implementation. But do not overclaim. We want the best real deliverable the environment allows, with carefully researched assets, correct attribution, a real playable Godot scene, and honest test reporting—not a fake AAA claim, a pile of random downloads, an untested APK, or static illustrations presented as gameplay.
