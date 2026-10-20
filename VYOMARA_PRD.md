# VYOMARA — The First Light of Dharma
## Product Requirements Document (PRD) · Android-first Godot 3D Vertical Slice

**Creator credit:** A VISION BY JP  
**Creator:** Jaya Prakash Sahu (JP)  
**Working game title:** VYOMARA  
**Tagline:** *Across the Yugas. Through the Realms. Guided by Dharma.*  
**Engine:** Godot 4.x, GDScript, Compatibility renderer for baseline Android support  
**Release intent:** Offline-first Android prototype; no backend, account, paid API or online requirement  
**Status:** Prototype starter exists in this ZIP; asset acquisition and Godot editor/runtime validation remain open gates.

---

## 1. Executive summary

Build a beautiful, playable 3D first-look slice for **VYOMARA**, a Hindu mythology-inspired action-adventure game. The output must be a real editable Godot project, not only a game design document, image slideshow, website, or rendered concept trailer. It must include a 3D environment that can be explored, an on-screen third-person character controller, a meaningful mission loop, a small set of VFX/SFX, UI, save/load, original visual identity, a defensible asset license ledger, and a mobile test report.

The reveal video already establishes a cinematic language: a creator credit reading **“A VISION BY JP”**, then the title VYOMARA, then an epic temple-world reveal, respectful divine glimpses, and a final branded card. The game scene must translate this aesthetic into real-time geometry and lighting, but it must never pretend concept art is real gameplay.

## 2. Goals

### Product goals
1. Deliver a minimum playable offline 3D prototype which opens in Godot Android Editor.
2. Translate the glimpse into a coherent first environment: ancient Indian-inspired temple court, celestial gateway, water, mountain silhouettes, golden-hour light, and a dignified mythological character presentation.
3. Prove the complete game loop: start → explore → encounter → use action ability → activate shrine/objective → victory → persist completion locally → replay.
4. Use assets suitable for a potential commercial game with documented rights. Default to CC0 or CC BY. No ripped film/television/game content.
5. Give Arena Agent Mode a measurable implementation brief, acquisition plan, code/testing workflow, and a required final Godot ZIP.
6. Remain mobile-first and realistic for a developer working on Android with free tools.

### Non-goals for this slice
- No open-world streaming, live service, online multiplayer, PvP, accounts, cloud saves, monetization, analytics SDK, or paid API.
- No claim of AAA/production readiness, investor readiness, “high rating”, or market popularity merely from a prototype.
- No recreation of a film/game's identifiable visuals or soundtrack.
- No claim that invented gameplay events are direct scripture.
- No final animation quality claim until the selected deity model is rigged, optimized, imported, and tested in-game.

## 3. Cultural and story boundaries

The intended genre is Indian/Hindu mythological action-adventure. **JP is only the creator/developer credit**; JP is not a character. Do not insert Rimi or other personal real-world relationships as in-world figures. The initial art glimpse shows Lord Shiva, Lord Vishnu, and Lord Hanuman as visual candidates; this is not yet a finalized character roster.

For the first playable slice, use **Hanuman as the art-direction candidate for the playable character**, because his devotional and courageous iconography appeared in the glimpse. Do not claim the prototype's invented mission is an episode from the Ramayana. “The First Light of Dharma”, the shrine activation, celestial gate, “Shadow Sentinel”, and a generic game-only pulse effect are original fiction. The Shadow Sentinel is an original non-divine enemy, not a canonical asura unless later research establishes and labels such a relationship.

Before a public/monetized release, source-review the story against a clearly selected tradition (e.g., Valmiki Ramayana or Ramcharitmanas; do not silently blend variants) and ask a knowledgeable cultural reviewer to check the art/character/action staging. Never make a revered deity the boss to be killed, use a deity as comic relief, place sacred symbols randomly as floor decoration, or fabricate quotes and attribute them to scripture. Respectful presentation outweighs spectacle.

The current proxy mesh is a **temporary procedural placeholder**, not a final deity model. Replace it only after a candidate is legally downloadable, visually reviewed, technically inspected, optimized, and properly credited. If no acceptable model is available, keep the prototype proxy clearly labelled and report the blocker honestly.

## 4. Experience and platform

- **Primary device:** Android phone, 12 GB RAM, more than 15 GB available storage (user-reported).
- **Engine:** Godot 4.x; preferred verification target Godot 4.6 stable if the installed editor supports it.
- **Language:** GDScript only (Godot Android editor has no C#/Mono support).
- **Renderer:** Compatibility renderer as the broad-compatibility baseline. Do not use Forward+ for the Android Editor target. The agent may compare Mobile renderer on-device only if Vulkan support and actual performance are verified.
- **Orientation:** Landscape (16:9 reference layout).
- **Input:** Touch joystick on left; large action buttons on right; optional keyboard fallback for desktop/test.
- **Persistence:** local `user://` save file. The complete core mission must work in airplane mode.
- **Cost:** no paid assets or APIs are required. Free services may have rate limits, account requirements or terms changes; do not claim a tool is unlimited unless verified.

## 5. Art direction

### Visual pillars
1. **Mythic, not generic medieval:** visual language draws from Indian temple forms, carved stone, mandala-like geometry, saffron banners, lamps, lotus/water motifs, and Himalayan/celestial vistas. Any fictional temples must be described as inspired designs, not replicas of a specific sacred site.
2. **Premium readability:** a strong focal hierarchy, controlled highlights, clear silhouettes, readable enemy telegraphs, restrained UI, and carefully staged camera angles.
3. **Blue and antique gold:** midnight/deep blue ambience, warm sandstone, antique gold accents, devotional saffron, luminous cyan only for portal/shrine effects.
4. **Mobile-aware detail:** texture atlases or shared materials where practical, small/medium textures, baked/static lighting where possible, restrained real-time shadows, no unnecessary transparency or hundreds of dynamic lights.
5. **Consistent style:** avoid combining photoreal PBR gods, toon props, unrelated low-poly vegetation and mismatched animation rigs without harmonization.

### Visual target
A compact, hand-directed 3D courtyard with a prominent sanctuary/gopuram-inspired silhouette, symmetrical columns, steps, lanterns, modest water planes, distant mountains, floating celestial silhouettes, a shrine focal point and a closed gate that changes appearance when the mission is complete. Treat distant/skyline elements as background geometry. The scene must be beautiful from the game camera and playable scale, not merely a pretty screenshot.

### Current starter state
The provided project already contains a procedural-mesh environment, low-poly hero proxy, original fictional sentinel, touch HUD, shrine objective, simple save service, a world concept image as the menu backdrop, and synthesized audio. These are foundations that must be audited and improved by the agent, not accepted blindly. The agent must open and validate every scene/script in Godot and fix all errors.

## 6. First playable chapter: The First Light of Dharma

**Narrative framing:** a short original myth-inspired vignette, not a claim about a canonical scriptural event. A temple court has gone quiet. The hero crosses the court, faces an original shadow-guardian, and awakens an ancient shrine that illuminates a celestial gateway.

### Required scene flow
1. **Title menu:** a compact “A VISION BY JP” creator credit, VYOMARA title, tagline, “ENTER THE FIRST REALM”, settings/options (at minimum master/music/SFX volume or clear note if deferred), and a visible “prototype / in development” disclosure.
2. **3D entry beat:** a short optional camera reveal or restrained title overlay, skippable after a few seconds. Do not hold the player captive.
3. **Exploration:** third-person movement, collision, camera follow, atmospheric audio and visible shrine/gateway target.
4. **Encounter:** one original Shadow Sentinel with readable telegraph, health, damage reaction, one basic attack, one cooldown-based game-only effect, dodge/invulnerability window, feedback and defeat state.
5. **Shrine interaction:** approach within a clear radius and press ACT; interaction is unavailable while the sentinel remains alive; feedback explains why.
6. **Victory:** a cinematic shrine/gate state change, clear success screen, replay/return-to-title actions, and a saved completion flag.
7. **Failure/retry:** hero health reaching zero shows a retry state; the restart path resets the level cleanly.

### Required controls
- Move using a responsive analog-style touch joystick.
- Action buttons: GADA/basic attack, PULSE (the pulse is a game-only mechanic and must not be claimed as canonical), DODGE, ACT/interact.
- Keyboard fallback: WASD, J=attack, K=pulse, L=dodge, E=interact; do not advertise unsupported keys.
- Ensure touches do not pass through overlays and do not cause accidental attacks when operating the joystick.

## 7. Character requirements

### Hero
- Use a properly licensed, inspectable, rigged Hanuman candidate if a suitable file can be obtained and checked. The current procedural proxy is only a fallback.
- Model must preserve recognisable devotional iconography while avoiding grotesque, disrespectful or generic “monkey soldier” treatment.
- Target Android-ready model: preferably 30–60k triangles after optimization/LOD where visual quality allows; 1–2 shared material/texture sets; no 8K textures. This is a project target, not an engine law.
- Ensure consistent scale/origin, root motion handling (prefer in-place animation for the prototype), correct forward axis, collision capsule and animation state transitions.
- Minimum animation states: idle, walk, run, attack, hit/damage, dodge, victory; if fewer assets exist, keep clear transitions with the available set and list gaps.
- Do not rely on Mixamo auto-rigging for a model with non-human appendages (e.g. tail) without testing: its documented auto-rigger is intended for bipedal humanoids.

### Enemy
- One original, clearly fictional non-divine guardian model. Keep silhouette distinct from deity iconography.
- Basic idle/move/attack/hit/defeat animation, simple telegraph VFX, health UI and functional AI.
- Never use real gods as hostile enemies or bosses.

## 8. Environment, VFX and audio requirements

### Environment
- The main scene is a compact traversal loop, not an endless terrain.
- Add layered foreground/midground/background to create depth. Main corridor and shrine must have readable navigation.
- Collisions for ground, pillars and blockers; decorative props can omit collision where it improves reliability.
- Optimize collision meshes; use primitive collision shapes where practical.
- Add small vegetation clusters, rocks, lamps, carvings and decals only when they serve composition/navigation.

### Effects
- Shrine: controlled light pulse, orbiting motes, activation cue, gate light state change.
- Combat: swing trail or brief arc, hit spark, enemy flash/stagger, cooldown feedback, pulse ring/particles.
- Ambient: few lightweight motes/fireflies/dust. Avoid full-screen particles on low-end devices.
- Keep gameplay effects readable and restrained around sacred iconography.

### Audio
- The ZIP includes an original synthesized music bed and procedural SFX examples; audit their loudness and repetition.
- Required sound categories: music bed, bell/shrine cue, footsteps or cloth/gear movement, melee whoosh/impact, pulse/wind effect, enemy hit/defeat, UI click, soft ambient wind/water.
- Use Mixkit only under its free sound-effect licence and do not redistribute a sound effect as a standalone asset. For external music, verify the individual licence; never use a popular film/serial soundtrack or devotional recording without explicit rights.
- Provide volume controls or clearly defer them with a backlog item. Avoid clipping and harsh looping.

## 9. Technical architecture

Use modular GDScript and Godot scenes, avoid a single giant script, and use simple data-driven resources where they add value. No backend/network dependencies.

Suggested organization:

```text
VYOMARA_Android_Prototype/
├── project.godot
├── scenes/
│   ├── menu/MainMenu.tscn
│   ├── world/FirstRealm.tscn
│   ├── player/Hero.tscn
│   └── enemies/ShadowSentinel.tscn
├── scripts/
│   ├── player/             # movement, animation, combat
│   ├── enemies/            # sentinel AI, health, telegraphs
│   ├── world/              # world setup, interactables, scene flow
│   ├── ui/                 # title, touch controls, HUD, overlays
│   └── systems/            # versioned local save, audio/settings
├── assets/
│   ├── characters/ environments/ animations/ textures/ materials/
│   ├── music/ sfx/ vfx/ ui/
│   └── reference_art/      # reference only, not assumed gameplay geometry
├── docs/                   # asset ledger, attribution, test reports
└── tests/
```

### Engineering requirements
- No invalid node paths, missing resources, hardcoded absolute machine paths or untracked generated assets.
- Use signals for decoupled health/UI/mission state where appropriate.
- Explicit scene transitions; handle restart without duplicated nodes/signals.
- Local save versioning, safe failure behavior if save is missing/corrupted/outdated.
- Use exported tuning values or constants centralised for combat speed/damage/radius/cooldowns.
- Use groups or references safely; avoid invalid instance access after an enemy is freed.
- Use `CharacterBody3D` / `move_and_slide()` for character control as in the official Godot 3D tutorial.
- Prefer `.glb`/glTF for 3D imported assets because Godot documents it as a recommended interchange format.

## 10. Asset research/acquisition and licensing requirements

This is a mandatory workstream, not a suggestion. In the network-enabled Arena workspace:

1. Browse each candidate source and inspect the exact asset page and license before download.
2. Download actual files (not just links) using official download flows. Do not bypass authentication, scrape protected resources or circumvent website controls. If a download requires account interaction, ask only when genuinely necessary; otherwise move to a legal alternative.
3. Extract into project asset folders; remove unused contents but keep `LICENSE`, `README`, source URL and author attribution as required. Never repackage third-party packs as a standalone asset download.
4. Import every selected `.glb`/`.gltf`/texture/audio into Godot and verify it appears correctly. List every skipped or failed resource and why.
5. Keep an `ASSET_LEDGER.md` with title, creator, source URL, date accessed, exact license, changes/optimization, in-game locations and attribution text.
6. Do not equate likes/download count with quality. Review topology, textures, rig, animations, scale, import settings, art fit, permissions and license.

### First research shortlist (candidates only; not pre-approved to ship)
- Godot Android editor limits / official docs: https://docs.godotengine.org/en/4.6/tutorials/editor/using_the_android_editor.html
- Godot renderer comparison: https://docs.godotengine.org/en/4.6/tutorials/rendering/renderers.html
- Godot 3D scene formats: https://docs.godotengine.org/en/stable/tutorials/assets_pipeline/importing_3d_scenes/available_formats.html
- Godot first 3D game / movement concepts: https://docs.godotengine.org/en/4.6/getting_started/first_3d_game/index.html
- Kenney Nature Kit, 3D foliage/rocks/trees, CC0: https://kenney.nl/assets/nature-kit
- Kenney Prototype Kit, 3D prototype props, CC0: https://kenney.nl/assets/prototype-kit
- Poly Haven CC0 models/textures/HDRIs: https://polyhaven.com/license and https://polyhaven.com/models
- South Indian Temple Modular Kit by rSquare, Sketchfab CC BY, about 8.3k triangles per listing: https://sketchfab.com/3d-models/south-indian-temple-modular-kit-25f0176668004faa98ec351e04e58920
- Hanuman (Animated) by NG Creations, Sketchfab CC BY candidate, listed at about 177k triangles and marked AI-generated: https://sketchfab.com/3d-models/hanumananimated-c5af66701ee940f69a6b68384a5ba725
- A low-poly stylized Hanumanji candidate by bothe.h, Sketchfab CC BY, listed around 27.6k triangles and AI-generated; art direction may be too toy-like: https://sketchfab.com/3d-models/hanumanji-5605eca5dc8d467686cc0771685ef9c4
- Mixamo official FAQ: free with Adobe ID and allows use of characters/animations in games, but auto-rigger is for bipedal humanoids: https://helpx.adobe.com/creative-cloud/faq/mixamo-faq.html
- Mixkit SFX library/license: https://mixkit.co/free-sound-effects/ and https://mixkit.co/license/modal/sfxFree/

Prior research shows at least one detailed Hanuman candidate at roughly 177k triangles marked AI-generated, and other deity statues often have 400k+ triangles or are not rigged. **Do not import a high-poly deity model as-is just because it is free.** Prefer an inspectable, appropriately licensed candidate that can be optimized without damaging important iconography. If a candidate cannot be obtained and reviewed, retain the proxy for dev testing and write an explicit blocker.

## 11. Quality, performance and QA gates

### Gate A — Project integrity
- Project opens in Godot without parse errors.
- All resource paths resolve; no external plugin/API required.
- No new warnings from untyped or invalid calls that indicate likely runtime failure.

### Gate B — Playable loop
- Menu button loads FirstRealm.
- Hero moves relative to the camera, has collision and respects the world boundary.
- Touch joystick + action buttons work on the actual Android device.
- Sentinel pursues and damages the hero; hero attacks it; pulse/dodge cooldown works.
- Sentinel defeat unlocks shrine; shrine interaction opens gateway and wins mission.
- Death/retry/replay work without duplicate UI or signals.

### Gate C — Offline and persistence
- All gameplay works in airplane mode.
- Completion saves to `user://` and loads after restart.
- Missing or corrupt saves fail safely.

### Gate D — Visual/audio quality
- No missing textures, magenta materials, broken rigs, floating props, severe clipping, broken normals, visibly wrong forward axis, or camera obstruction in the core route.
- Main scene reads well at actual phone resolution.
- SFX and music are balanced; not clipping; repeated sound does not become harsh.
- Deity appearance receives an art-direction and cultural review; do not mark final while proxy remains.

### Gate E — Device performance
- Record Godot version, device GPU/chipset if available, renderer, resolution, frame-rate readings and test duration.
- Target a stable 30 FPS on the target device with no crashes during a 10–15 minute run; this must be measured, not assumed.
- Include a low/medium quality setting if needed. One shadow-casting directional light initially; keep transparent effects limited.

### Gate F — Delivery
- Final Godot folder has `project.godot` at root.
- All used assets and credits are included, with no source media that is not licensed for inclusion.
- Deliver final `.zip`, checksum, asset ledger, import/export instructions, test report, screenshots, known issues and a list of incomplete art/content items.
- Deliver APK only if exported through a matching Godot template and actually verified. If no Android export template/build path is available, don't fabricate an APK; provide the Godot project ZIP and exact remaining steps.

## 12. Done means

The first vertical slice is done only when the agent can open the project in Godot, run the title/menu, play the 3D mission, complete/fail/retry it, save locally, test airplane mode, import at least the selected legal environment asset(s), provide the attribution manifest, and submit a test report that separates passed, failed, untested, and blocked items.

An art-only render, untested scripts, a README that says the game is complete, or an APK that hasn't been launched on Android does not satisfy “done”.

## 13. External references

- Godot Android editor and limitations: https://docs.godotengine.org/en/4.6/tutorials/editor/using_the_android_editor.html
- Godot renderer comparison: https://docs.godotengine.org/en/4.6/tutorials/rendering/renderers.html
- Godot supported 3D formats: https://docs.godotengine.org/en/stable/tutorials/assets_pipeline/importing_3d_scenes/available_formats.html
- Godot Android exports and matching templates: https://docs.godotengine.org/en/4.6/tutorials/export/exporting_projects.html
- Arena Agent Mode overview and output behavior: https://help.arena.ai/articles/5432423882-how-to-use-agent-mode
