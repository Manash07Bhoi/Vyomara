# VYOMARA Asset Ledger — Starter Project

## Assets actually included in this ZIP

| File/family | Origin | Intended use | License/rights note |
|---|---|---|---|
| `assets/reference_art/world_celestial_kingdom.webp` | Original AI-generated concept image made for the VYOMARA project | Main-menu backdrop and visual reference | Project concept art; not a representation of real gameplay |
| `assets/reference_art/hanuman_concept_reference.webp` | Original AI-generated concept image made for this project | Art-direction reference only | Must be reviewed for iconographic accuracy before public use |
| `assets/reference_art/shiva_concept_reference.webp` | Original AI-generated concept image made for this project | Art-direction reference only | Must be reviewed for iconographic accuracy before public use |
| `assets/reference_art/vishnu_concept_reference.webp` | Original AI-generated concept image made for this project | Art-direction reference only | Must be reviewed for iconographic accuracy before public use |
| `assets/reference_art/celestial_gateway_reference.webp` | Original AI-generated concept image made for this project | Art-direction reference only | Concept art, not runtime geometry |
| `assets/music/vyomara_original_synthetic_score.ogg` | Original synthesized score composed procedurally for the preceding glimpse deliverable | Menu and low-volume world ambience | Original synthetic audio; no third-party recording embedded |
| `assets/sfx/*_synthetic.wav` | Procedurally synthesized short effects created for this starter | Prototype bell, pulse and impact feedback | No third-party samples embedded |

## Third-party packs

**No third-party 3D pack or downloaded deity model is bundled in this starter.** The authoring environment used to assemble this ZIP had no outbound DNS access, so downloading and validating those packages was not possible here. Do not assume they are present. The master Arena prompt contains a mandatory asset-acquisition workstream and source links.

## Candidate resources to acquire in the agent's network-enabled workspace

- Kenney Nature Kit — CC0, 3D trees/rocks/foliage: https://kenney.nl/assets/nature-kit
- Kenney Prototype Kit — CC0, temporary 3D geometry: https://kenney.nl/assets/prototype-kit
- Poly Haven — CC0 PBR textures/HDRIs/models: https://polyhaven.com/license
- South Indian Temple Modular Kit by rSquare — Sketchfab CC BY; credit the creator, retain license/source in game credits and asset ledger: https://sketchfab.com/3d-models/south-indian-temple-modular-kit-25f0176668004faa98ec351e04e58920
- Hanuman (Animated) by NG Creations — Sketchfab CC BY candidate; reported ~177k triangles and AI-generated. Download only if the file is accessible under the listed terms, inspect rig/mesh quality, reduce/LOD for mobile, and credit creator: https://sketchfab.com/3d-models/hanumananimated-c5af66701ee940f69a6b68384a5ba725
- Mixkit free SFX — check individual item and license; source page: https://mixkit.co/free-sound-effects/

## Asset acceptance policy

- Default to CC0 or CC BY only. Include creator, exact title, source URL, license and changes for every CC BY asset.
- Reject NC, ND, unclear, download-gated without permission, ripped from films/TV, leaked, and unlicensed assets. Avoid share-alike unless explain and document compatibility before use.
- Never put third-party assets on an external asset mirror or redistribute them as a standalone pack.
- Prefer `.glb`/glTF for 3D scene exchange; Godot recommends glTF 2.0 in its scene-import docs.
- Target Android optimization: test geometry counts; prefer under ~35k triangles for the close-up hero after LOD/decimation where quality allows, 1–2 material/texture sets, compressed textures, and no high-cost 8K textures. These are project targets, not universal engine limits.
- Before using a deity asset, review model quality, iconography, animations, download terms, authorship/license, and respectful presentation. A Creative Commons label does not guarantee that the art is theologically accurate or technically usable.
