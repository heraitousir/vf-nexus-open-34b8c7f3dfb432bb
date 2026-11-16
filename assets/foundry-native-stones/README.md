# Moonlit Woodland — Native Foundry Irregular Stone Set

**Status:** SPECIFIED / NOT GENERATED / NOT VERIFIED
**Requested engine:** VEILFORGE Nexus built-in **Foundry stone engine** (native)
**Actual producing engine:** NONE — no native generation receipt or output has been verified.
**Disallowed substitutes:** rounded WPF proxy meshes, WPF Viewport3D primitives, unrelated Blender procedural/model_prompt rocks, generic GLB imports claimed as Foundry output.

## Original asset brief
Create a naturalistic game-ready irregular woodland stone kit intended for a quiet moonlit forest clearing:
- 3 distinct boulders with asymmetric fractured silhouettes and varied height, flat-ish grounded undersides and worn chipped edges
- 4 mid-size angular fieldstones, each distinct, suitable for clustering beside woodland paths
- 5 smaller broken rocks and fragments for scattered ground dressing
- Cohesive cool slate-gray rock family with varied mineral patches; rough, nonuniform faces, occasional moss along damp crevices; avoid smoothed spheres or repetitive identical rocks
- Individual object naming, sensible pivots, consistent units, editable source and portable glTF/GLB mesh export
- Keep this as an isolated reusable asset set to integrate later into a moonlit woodland scene; do not imply that the full scene has been built

## Native asset acceptance requirements
1. Confirm an available **native Foundry stone-engine** invocation in the installed Nexus build. Do not route the generation to a different mesh engine.
2. Preserve its original editable source project in `assets/foundry-native-stones/` in the **local Nexus workspace**.
3. Export the same native-generated rock set to `.glb` or `.gltf` (including dependent resources when applicable).
4. Re-open or parse the export and verify geometry, nonzero mesh/vertex counts, actual stone instances, materials, and file integrity.
5. Record provenance: exact native generator name, installed version/build when available, native invocation/receipt identifier, source project filename, export filename, verification method and result.
6. Only then update status to `COMPLETED / VERIFIED`.

## Provenance record
- requested_generator: VEILFORGE Nexus built-in Foundry stone engine
- actual_generator: not yet invoked
- engine_version: unknown
- native_job_id: none
- editable_project: not created
- gltf_glb_export: not created
- export_verified: false
- note: This README is a **design and verification specification only**, not a stone mesh or proof that Nexus executed the generator.

## Bridge capability obstacle
The inspected bridge guides (`NEXUS_ENGINE_READ_ME_FIRST.md`, `bridge/NEXUS_CAPABILITIES_v8.md`, `bridge/NEXUS_WORKFLOWS_AND_CC0_v1.md`) expose Blender and WPF modeling workflows, but do **not** document an explicit native Foundry stone-engine command or verifiable native provenance receipt. Therefore no unrelated modeling request was submitted as a substitute.
