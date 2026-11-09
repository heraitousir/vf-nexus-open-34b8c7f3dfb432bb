# VEILFORGE NEXUS CONSUMER — CHATGPT MODELING GUIDE v4

Personal repository: heraitousir/vf-nexus-open-34b8c7f3dfb432bb
Device ID: 34b8c7f3dfb432bb3a4010d540e78903

YOU, the connected ChatGPT, must invent the shape of each model from the user's text prompt. Do NOT choose the old default Aether Drone/Arcane Sentinel/Cinder Helm preset. The new command is model_prompt, which builds unique data-driven Blender geometry with materials and lighting.

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

MODEL SPEC LIMITS:
- Title and part names: simple short ASCII descriptions.
- 8 to 55 distinct part objects, each with a meaningful visible role.
- Valid shapes: cube, sphere, cylinder, cone, torus, icosphere.
- position [x,y,z]: numbers from -6 through 6.
- scale [width,depth,height]: each between 0.04 and 5.5.
- rotation [x,y,z] degrees: -360 through 360.
- color: #RRGGBB hex string.
- optional metallic 0-1, roughness .09-1, emission 0-4, mirror_x boolean.
- Use detailed layered parts and symmetry where appropriate. The same staging lights can be used while MODEL GEOMETRY must change.
- Never send executable Python, a user script, a shell command, local paths or credentials via GitHub.

The old model_test command still exists for pipeline regression ONLY; do not use it to demonstrate new prompt understanding.

EXAMPLE DIVERSE IDEAS (not recipes): clockwork stag, crystalline jellyfish, tiny gothic observatory, angular locomotive, lantern creature, armored space beetle, clock tower robot. Build your OWN distinct geometry plan for any chosen topic.

OTHER JOB TYPES: pair (ONE PC approval), ping, status, create_project (Game/Model/3D World/Blank workspaces), open_viewport (reopen last model), model_test (legacy fixed sample).

SECURITY: Public GitHub repos allow anyone to READ model names and receipts. Only authorized GitHub writers can submit bounded jobs; writers are not cryptographically identified as ChatGPT. Never grant unknown people write permission. After first pairing, permitted actions do not ask for repeated approval. The engine will not run arbitrary PC commands, remote Python, private-file reads, executables or unbounded file edits. This is prompt-based component modeling, NOT unrestricted organic AAA sculpting, rigging, animation or full owner-VEILFORGE parity.
