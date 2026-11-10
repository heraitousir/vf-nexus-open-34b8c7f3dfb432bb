# VEILFORGE Nexus — Reusable Blender techniques v1

## Technique: Greenhouse stone / authentic material workflow

**Origin:** VEILFORGE Living Worlds, the original Enchanted Greenhouse Blender scene, developed November 9, 2026. Source reference: \`timmytwopointoh/emulator-tester/scenes/veilforge-trilogy/blender/build_enchanted_greenhouse.py\` (owner-developed source technique, not a customer's private asset).

**Problem solved:** Plain gray primitives and checkerboard-looking floor panels did not resemble masonry. The improved greenhouse uses staggered courses, natural limestone joints, gently beveled edges with weighted normals, and consistent PBR material families with color, roughness, and normal maps. Its pond surround uses mossy coping; rain-worn paths use darker/wetter stone. Previously installed, license-verified Poly Haven CC0 albedo/roughness/normal photographs were reused *when available*, with packed-image exports; otherwise original generated texture maps were baked so glTF exports could carry them.

**How a customer's ChatGPT applies it:** In any \`model_prompt\` or \`refine_model\` job, add \`"technique":"stone_weathered_limestone"\`, \`"technique":"stone_mossy_coping"\`, or \`"technique":"stone_wet_flagstone"\` to the parts representing masonry. Use \`"shape":"stone_slab"\` for battered flagstone geometry or \`"shape":"cube"\` for blocks, steps, and walls. Stagger neighboring slabs by an offset of around half a slab width; avoid alternating unrelated colors into a checkerboard. Distinguish wet areas and mossy coping with the corresponding surface style, not random unrelated texture tiles.

The rest of each part's model schema remains \`name\`, \`shape\`, \`position\`, \`scale\`, \`rotation\`, \`color\`, with optional \`metallic\`, \`roughness\`, \`mirror_x\`. \`technique\` is optional; ordinary model parts use \`standard\`.

**Engine behavior:** Nexus validates technique names, creates real Blender mesh objects, adds edge wear/weighted normals for stone slabs, applies normal/roughness/albedo texture nodes, bakes deterministic maps to PNGs, packs them in \`.blend\`, exports glTF where Blender supports it, and reports technique usage and texture provenance in \`quality-report.json\`. If the user explicitly supplies a \`provenance.json\` with \`"license":"CC0"\` and complete \`mossy_rock\`/\`worn_mossy_plasterwall\` photo map sets under \`Desktop/projects/material-library/CC0-Material-Library\`, Nexus uses those photographs; it does **not** copy a different user's files or download external images silently. If absent, it uses self-generated image-based PBR textures and reports that honestly.

This catalog is reusable and versioned, not a one-time model. Future techniques (hair systems, character skin, metal wear, terrain sculpt, water shaders) should be separate reviewed modules with example prompts, reproducible Blender checks, quality reports and explicit source/provenance.

**Safety boundary:** ChatGPT provides data-only model specifications. The engine doesn't accept arbitrary Python, shell commands or external file paths from a public GitHub request. After one-time pairing, approved bounded model jobs continue without extra approvals; potentially harmful system-wide operations are separate permissions.
