# VEILFORGE NEXUS — START HERE / UNIQUE BLENDER AUTHORING v2

Personal repository: heraitousir/vf-nexus-open-34b8c7f3dfb432bb
Device ID: 34b8c7f3dfb432bb3a4010d540e78903

First read NEXUS_ENGINE_READ_ME_FIRST.md in the repository ROOT to discover every command; then read bridge/NEXUS_MODEL_WORKBENCH_v1.md for inspection, genuine geometry editing, and exporting editable Blender files. Older preset examples are LEGACY. For any request to create an ORIGINAL Blender model, use model_create (natural-language prompt) or model_prompt (advanced authored geometry). Do NOT use model_test or open_viewport for creating something new.

## SIMPLE CREATION: MODEL_CREATE

Create a NEW JSON file at requests/34b8c7f3dfb432bb3a4010d540e78903/<NEWID>.json with this COMPLETE request shape. Replace NEWID with a fresh 8-32 character alphanumeric ID, identical inside the file and its filename. Replace the name and prompt for each request.

{"id":"<NEWID>","device_id":"34b8c7f3dfb432bb3a4010d540e78903","type":"model_create","name":"Unique Mossy Well","prompt":"Create an ancient moss-covered stone well with a wooden pitched roof, a crank, bucket and weathered limestone masonry."}

Nexus converts that text into new geometry components on this PC, launches only Blender, creates genuine editable Blender meshes, saves a .blend project and rendered PNG, and opens the resulting Blender viewport. It does NOT open a previous asset or execute arbitrary Windows commands. This local idea compiler is an early procedural planner for architecture, creatures, vehicles, plants, artifacts and sculptural forms; it does not guarantee detailed AAA sculpting or perfect recognition of every idea.

## ADVANCED CREATION: MODEL_PROMPT

For much more accurate results, ChatGPT should design all the actual shapes, sizes, positions, materials and proportions. Submit model_prompt with model_spec containing title and 8-55 part objects. Each part needs name, shape, position [x,y,z], scale [x,y,z], rotation [x,y,z] in degrees, and color "#RRGGBB". Available shapes: cube, sphere, cylinder, cone, torus, icosphere, stone_slab. Optional: metallic, roughness, emission, mirror_x, technique. The incomplete 2-part example from old guides is not valid. Full details: NEXUS_ENGINE_READ_ME_FIRST.md, bridge/NEXUS_MODEL_WORKBENCH_v1.md, bridge/NEXUS_CAPABILITIES_v8.md and bridge/NEXUS_TECHNIQUES_v1.md.

## VERIFY NEW BLENDER GEOMETRY

After the write, read receipts/34b8c7f3dfb432bb3a4010d540e78903/<NEWID>.json. Report success only for result=completed. The summary identifies the created project_id and authoring method. If preview_url exists, inspect that MODEL-ONLY image when reviewing the proportions; otherwise ask the user to look at the local Blender viewport. A blocked receipt is an error to diagnose, not permission to substitute an old asset.

For model inspection and *incremental* edits on an existing imported or created Blender model, read bridge/NEXUS_MODEL_WORKBENCH_v1.md and use model_inspect followed by model_edit. The user can export an editable finished .blend to Desktop/VEILFORGE Finished Models. For complete reconstruction, submit model_refine with the existing project_id as name and a complete revised model_spec. Nexus archives the prior .blend before replacing it. Continue only after checking the actual receipt.

## PRIVACY AND RESTRICTIONS

The GitHub repo is public by default. Never put private user content or desktop screenshots in a request. Model image sharing is opt-in. Pairing is approved once on the PC, then supported jobs do not ask again. Nexus cannot run an arbitrary command prompt, edit its own code, control unrelated desktop applications or read unrelated files. These restrictions stay intact.
