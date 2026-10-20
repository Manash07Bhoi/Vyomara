# VYOMARA Asset Research & Acquisition Log

**Research date:** 2026-10-20  
**Target:** Godot 4.x / Android-first / offline / no paid APIs  
**Rule:** research shortlist is not a claim that a downloadable file was obtained, imported or approved for the final game. Verify the actual item page and its license on the date of acquisition.

## Engine and formats

| Topic | Finding | Production decision | Source |
|---|---|---|---|
| Godot Android editor | Official editor can author/run 2D/3D, but is early access; mobile UX is limited, no C#/Mono, Forward+ is not recommended on phones due performance issues. | Use GDScript. Prefer Compatibility renderer initially and test on the real phone. | https://docs.godotengine.org/en/4.6/tutorials/editor/using_the_android_editor.html |
| Renderer | Compatibility targets broad low-end/mobile coverage; Mobile renderer uses newer Vulkan/RenderingDevice path and should be compared on device. | Choose Compatibility for baseline; consider Mobile only after tests. | https://docs.godotengine.org/en/4.6/tutorials/rendering/renderers.html |
| 3D interchange | Godot recommends glTF 2.0 (`.glb`/`.gltf`) for importing 3D assets. | Prefer `.glb`, inspect material/scale/orientation and collision after import. | https://docs.godotengine.org/en/stable/tutorials/assets_pipeline/importing_3d_scenes/available_formats.html |
| Android export | Export needs setup and matching templates; Android editor workflow may differ from desktop setup. | Do not label anything APK-ready until template/export and device test are complete. | https://docs.godotengine.org/en/4.6/tutorials/export/exporting_for_android.html |

## Asset shortlist — licenses and decisions

| Asset / source | Creator / type | License reported by source | Known technical / art facts | Download status in this package | Decision |
|---|---|---|---|---|---|
| Poly Haven — https://polyhaven.com/license | Poly Haven; PBR textures, HDRIs and models | CC0 per site | Suitable source for environment textures and lighting assets. | **Not downloaded** in this packaging environment because outbound DNS/network access was unavailable. | First-choice environment texture/HDRI source in a network-enabled agent workspace. Add specific item URLs to ledger after choosing assets. |
| Kenney Nature Kit — https://kenney.nl/assets/nature-kit | Kenney; 3D nature props | CC0 per asset page | Page has a compact nature collection (trees, rocks and related props). | **Not downloaded** here; download attempts failed at network/DNS. | Acquire only needed props, not the whole pack; preserve included README/license. |
| Kenney Prototype Kit — https://kenney.nl/assets/prototype-kit | Kenney; modular prototype 3D props | CC0 per asset page | Useful for blockout/replacing placeholders; production-style deity model not included. | **Not downloaded** here; download attempts failed at network/DNS. | Optional helper assets only; not a final art solution. |
| Quaternius — https://quaternius.com/license.html | Quaternius; game-ready model/animation packs | Quaternius Asset License (QAL v1.0, page states updated 2026-08-28); free commercial use, no credit required; standalone asset redistribution prohibited. | Need check the exact license bundled with every downloaded pack and whether selected pack has mobile-friendly geometry/materials. | **Not downloaded** here. | Viable candidate for environment props/animation only after selected pack review. Keep as in-game assets, never redistribute as an asset pack. |
| South Indian Temple Modular Kit — https://sketchfab.com/3d-models/south-indian-temple-modular-kit-25f0176668004faa98ec351e04e58920 | rSquare; modular architectural model | Listed CC BY on model page | Page reports about 8.3k triangles; creator says it is not based on a specific real temple, but was inspired by references. Verify current downloadable files and attribution requirements. | **Not downloaded or inspected as a file** in this package. | Strong candidate to evaluate; must cite creator/source/license and optimize collision/materials. Not pre-approved for public release until downloaded and reviewed. |
| Hanuman (Animated) — https://sketchfab.com/3d-models/hanumananimated-c5af66701ee940f69a6b68384a5ba725 | NG Creations; deity character candidate | Listed CC BY on model page; listing marked AI-generated | Page reports around 177.2k triangles and 88.6k vertices. High for close-up Android mobile without reduction. Need inspect actual rig, animations, textures, tail, model quality and iconographic fit. | **Not downloaded or inspected as a file** in this package. | Do not use as-is. Only test if downloadable, exact license and attribution are preserved, and optimized result passes cultural/art review. |
| Hanumanji — https://sketchfab.com/3d-models/hanumanji-5605eca5dc8d467686cc0771685ef9c4 | bothe.h; stylized character candidate | Listed CC BY on page; listing marked AI-generated | Page reports around 27.6k triangles; toy-like/stylized appearance may not match the current premium cinematic target. Rig and animations require verification. | **Not downloaded or inspected as a file** in this package. | Fallback visual study only if it passes deity portrayal and style review. Do not select merely because it is low-poly. |
| Mixamo — https://helpx.adobe.com/creative-cloud/faq/mixamo-faq.html | Adobe; humanoid characters and animations | Adobe says Mixamo characters/animations may be used in games under its terms; requires Adobe ID. | Auto-rig targets bipedal humanoids; extra tail/appendage motion may not rig properly. | No Mixamo model or animation bundled. | Optional for compatible humanoid animation experiments. Verify each exported character/animation and license context. |
| Mixkit SFX — https://mixkit.co/free-sound-effects/ and https://mixkit.co/license/modal/sfxFree/ | Mixkit; SFX | Free SFX license page allows use in video, social and video-game projects subject to license restrictions; not standalone redistribution. | Select exact sound and save its page/license in the ledger. | No Mixkit SFX bundled. Existing SFX in this project are synthesized locally. | Optional, not required; original audio is the baseline. |

## Included, actually generated resources

- Five original AI-generated concept reference images under `assets/reference_art/` (world, celestial gateway, and concept references for Hanuman, Shiva and Vishnu). They are **references only**, not rigged meshes or runtime 3D content.
- `assets/music/vyomara_original_synthetic_score.ogg`: synthesized procedural music bed with no third-party recording intentionally used.
- `assets/sfx/temple_bell_synthetic.wav`, `divine_pulse_synthetic.wav`, `stone_impact_synthetic.wav`, `wind_swell_synthetic.wav`: synthesized procedural effects with no third-party samples intentionally used.
- Procedural primitive-mesh environment and character proxies are built by GDScript, not downloaded 3D models.

## Acquisition blocker and mandatory next step

This authoring runtime could not resolve external hosts through DNS, so it could not fetch Kenney/Poly Haven/Sketchfab/Mixkit asset binaries. Only their source pages and reported license/spec information were researched. No third-party asset download or import is claimed. The Arena Agent Master Prompt requires a network-enabled workspace to repeat the research, download only from legal official flows, inspect files, optimize/import/test them, and update `docs/ASSET_LEDGER.md` with the actual chosen files.

## Minimum requirements before a third-party asset is accepted

1. Open the individual source page on acquisition day; capture exact title, creator, license version/text, source URL and access date.
2. Confirm an official/authorized download is available. Never bypass authentication or protected access controls.
3. Inspect actual file format, mesh/triangle count, texture resolution, material count, skeleton/animations, scale, orientation, collision and cultural/style fit.
4. Import into the target Godot version; check mobile draw calls, frame time, material compatibility and file size on device.
5. Add required attribution/license text in `docs/ASSET_LEDGER.md` and `docs/THIRD_PARTY_CREDITS.md`.
6. Keep source assets inside their permitted game use; do not redistribute third-party packs separately.
