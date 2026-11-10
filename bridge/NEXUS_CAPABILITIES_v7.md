# VEILFORGE NEXUS CONSUMER — CHATGPT MODELING GUIDE v7

Personal repository: heraitousir/vf-nexus-open-34b8c7f3dfb432bb
Device ID: 34b8c7f3dfb432bb3a4010d540e78903

Read bridge/NEXUS_START_HERE_v1.md FIRST. For an ORIGINAL model use model_create (simple natural-language idea) or model_prompt (advanced ChatGPT-authored components). Never use model_test or open_viewport when a new object is requested.

HOW TO USE:
1. Pair once with PC approval, then ping. Read matching completed receipts.
2. Interpret the user's idea into an identifiable 3D silhouette. Choose meaningful parts, sizes, shapes, colors, positions and rotations that visually express the prompt.
3. Create a NEW GitHub file requests/34b8c7f3dfb432bb3a4010d540e78903/<NEWID>.json (replace <NEWID> everywhere with the same fresh alphanumeric 8-32 character ID).
4. Send type model_prompt with a model_spec object containing title and 8-55 authored parts. Every part must include name, shape, position, scale, rotation, color.
5. Read receipts/34b8c7f3dfb432bb3a4010d540e78903/<NEWID>.json. Only say complete when result=completed. The PC stores .blend/.glb (where supported), prompt-preview.png, model spec and quality report under Desktop/projects and opens the Blender viewport.
6. For a second attempt, invent DIFFERENT geometry, not a renamed clone. Duplicate geometry is rejected.

JOB FORMAT, shortened example of two parts (you MUST EXPAND to at least eight):
{"id":"<NEWID>","type":"model_prompt","device_id":"34b8c7f3dfb432bb3a4010d540e78903","name":"Crystal Manta First Draft","model_spec":{"title":"Crystal Manta","parts":[{"name":"Body","shape":"sphere","position":[0,0,1.5],"scale":[1.5,.7,.45],"rotation":[0,0,0],"color":"#71BFFF","metallic":0.5,"roughness":0.3},{"name":"Wing","shape":"cube","position":[-.9,0,1.5],"scale":[1.8,.45,.12],"rotation":[0,0,19],"color":"#B8E7F9","mirror_x":true}]}}

The example has only TWO model parts; it is not a valid runnable job until you add at least SIX more meaningful parts.

REUSABLE BLENDER TECHNIQUE LIBRARY:
Before making any stone ruins, walls, garden steps, paved floors or pond coping, READ bridge/NEXUS_TECHNIQUES_v1.md. That catalog records the authentic Blender Greenhouse stone technique and describes how to reuse it on NEW models. Add the part field technique: stone_weathered_limestone, stone_mossy_coping, or stone_wet_flagstone. Use shape stone_slab for battered flagstones; cube for steps and structural stone. Use natural staggered joints and a consistent stone material rather than checkerboard tiles. The engine performs real Blender UV mapping, bevels, PBR albedo, roughness and normal maps with a provenance report. It will use photographic CC0 maps ONLY if explicitly supplied by this PC owner; otherwise it generates portable image maps.

MODEL SPEC LIMITS:
- Title and part names: simple short ASCII descriptions.
- 8 to 55 distinct part objects, each with a meaningful visible role.
- Valid shapes: cube, sphere, cylinder, cone, torus, icosphere, stone_slab.
- position [x,y,z]: numbers from -6 through 6.
- scale [width,depth,height]: each between 0.04 and 5.5.
- rotation [x,y,z] degrees: -360 through 360.
- color: #RRGGBB hex string.
- optional metallic 0-1, roughness .09-1, emission 0-4, mirror_x boolean.
- Use detailed layered parts and symmetry where appropriate. The same staging lights can be used while MODEL GEOMETRY must change.
- Never send executable Python, a user script, a shell command, local paths or credentials via GitHub.

MODEL REFINEMENT / VISUAL FEEDBACK LOOP:
After a model_prompt finishes, read the matching GitHub receipt's preview_url IF present. That URL points to a 640px maximum JPG of the rendered MODEL ONLY, not a desktop screenshot. Inspect the image alongside the completed receipt and quality metrics; identify problems with the silhouette, material, geometry, proportion, lighting or details. To modify the same saved model, submit a NEW model_refine job with a fresh ID: {"id":"<NEWID>","type":"model_refine","device_id":"34b8c7f3dfb432bb3a4010d540e78903","name":"the-existing-project-slug","model_spec":{"title":"Revised model","parts":[...]}}. The parts field must contain the FULL replacement model design with 8-55 meaningful parts. Nexus builds it in a temporary directory, validates the .blend and PNG, archives the old model in revisions/, then replaces the active model and opens Blender's viewport. The receipt includes a new preview_url if the PC owner enabled model preview sharing. Continue iterating until the user is satisfied. Do NOT claim continuous live video; this is a job-based screenshot/refine loop, typically seconds to minutes per render.
MODEL PREVIEW PRIVACY: The user's repository is PUBLIC by default. No preview is uploaded unless the user selects YES during the one-time pairing or enables it via Nexus Settings > Toggle Model Preview Sharing. If no preview_url exists, ask them to enable sharing; never request desktop screenshots or copy local files into the public repository without authorization.
The old model_test command still exists for pipeline regression ONLY; do not use it to demonstrate new prompt understanding.

EXAMPLE DIVERSE IDEAS (not recipes): clockwork stag, crystalline jellyfish, tiny gothic observatory, angular locomotive, lantern creature, armored space beetle, clock tower robot. Build your OWN distinct geometry plan for any chosen topic.

SIMS MOD FORGE TASK HANDOFF (NOT A COMPLETED MOD):
For Sims 4 mod requests, Nexus accepts sims_mod, with name, category (clothing/accessory/hair/object/build_buy/tuning/trait/career/interaction/script/other) and prompt (12-3000 characters). It stages a local Desktop/projects/<project>/sims/mod-request.json for the existing Sims Mod Forge workflow. This does NOT synthesize a usable .package or .ts4script yet. The matching receipt uses result=staged, NOT completed. It must still go through Sims Mod Forge and Sims 4 Studio export and real Sims 4 in-game validation. Never say a mod is installed or functional based solely on a staged request. Arbitrary script execution from public GitHub is not supported. Do not silently touch the Sims game Mods folder.
OTHER JOB TYPES: pair (ONE PC approval), ping, status, create_project (Game/Model/3D World/Blank workspaces), model_refine (rebuild same Blender project and archive old version), open_viewport (reopen last model), model_test (legacy fixed sample).

SECURITY: Public GitHub repos allow anyone to READ model names and receipts. Only authorized GitHub writers can submit bounded jobs; writers are not cryptographically identified as ChatGPT. Never grant unknown people write permission. After first pairing, permitted actions do not ask for repeated approval. The engine will not run arbitrary PC commands, remote Python, private-file reads, executables or unbounded file edits. This is prompt-based component modeling, NOT unrestricted organic AAA sculpting, rigging, animation or full owner-VEILFORGE parity.
