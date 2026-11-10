# VEILFORGE NEXUS ENGINE — READ ME FIRST

This is the command manual published by the Nexus app in the customer's own GitHub repository. It is intended for the customer's ChatGPT. Read this before sending any new instruction, and re-read when the app updates.

Repository: heraitousir/vf-nexus-open-34b8c7f3dfb432bb
Device ID: 34b8c7f3dfb432bb3a4010d540e78903

## How to use the bridge

Read bridge/NEXUS_START_HERE_v2.md for original creation, bridge/NEXUS_CAPABILITIES_v8.md for the geometry schemas and restrictions, bridge/NEXUS_MODEL_WORKBENCH_v1.md for import/inspection/editing/final exports, and bridge/NEXUS_TECHNIQUES_v1.md for learned Blender modeling/material techniques.

1. Use a GitHub tool with read and WRITE permission to this repository. A read-only ChatGPT cannot operate Nexus; do not pretend.
2. Create a NEW JSON file at requests/34b8c7f3dfb432bb3a4010d540e78903/<NEW_ID>.json; NEW_ID is a unique 8–32 character alphanumeric value and must match the request id field. Include device_id 34b8c7f3dfb432bb3a4010d540e78903.
3. Nexus executes only permitted typed jobs within its local workspace. Check the matching receipts/34b8c7f3dfb432bb3a4010d540e78903/<NEW_ID>.json. Require result=completed for success. A blocked/staged result does NOT mean the object/mod was finished.
4. When preview sharing is enabled by the PC owner, inspect the model-only preview_url in the receipt. Choose the next change based on what you actually see. The repo may be PUBLIC; never post screenshots of the desktop, full .blend files, or confidential data.
5. Repeat inspect, edit/refine, inspect until the user approves the appearance; then export the model to their Desktop using model_export.

## Exact supported actions

| type | Purpose | Fields / limits |
| --- | --- | --- |
| pair | One-time approval on PC | standard request fields |
| ping or status | Verify PC listener | standard request fields |
| create_project | Workspace | name, template Game/Model/3D World/Blank |
| model_create | NEW Blender geometry from a natural language idea | name, prompt 12–1800 characters |
| model_prompt | NEW Blender model with ChatGPT-designed geometry | name, model_spec (8–55 component objects) |
| model_inspect | Render and inspect an existing model | name = project ID; user must enable model preview sharing |
| model_edit | Change existing Blender mesh objects or add real geometry | name = project ID, edits array of 1–24 vetted operations |
| model_refine | Rebuild structured-model geometry within same project | name = project ID, complete revised model_spec |
| model_export | Save a portable final editable Blender .blend | name = project ID, copies to the fixed Desktop/VEILFORGE Finished Models folder |
| open_viewport | View latest existing Blender model | no model creation; cannot replace model_create |
| sims_mod | Stages a Sims 4 mod request | name, category, prompt; NOT a finished package |
| model_test | Legacy fixed Blender regression model | never use for creating original user content |

## Request examples (replace placeholders)

Create new helmet:
~~~json
{"id":"<NEW_ID>","device_id":"34b8c7f3dfb432bb3a4010d540e78903","type":"model_create","name":"Copper Helm Study","prompt":"Create a distinctive copper knight helmet with layered metal cheek guards, broad visor, crest and engravings."}
~~~

Inspect the helmet; read matching receipt plus preview_url:
~~~json
{"id":"<NEW_ID>","device_id":"34b8c7f3dfb432bb3a4010d540e78903","type":"model_inspect","name":"<PROJECT_ID>"}
~~~

Modify an object from the inspection list, and add real new geometry:
~~~json
{"id":"<NEW_ID>","device_id":"34b8c7f3dfb432bb3a4010d540e78903","type":"model_edit","name":"<PROJECT_ID>","edits":[{"object":"<EXACT_EXISTING_MESH_NAME>","operation":"bevel","value":0.045},{"object":"Extra Helmet Crest","operation":"add_part","value":{"shape":"cube","position":[0,0,2.8],"scale":[0.55,0.12,0.42],"rotation":[0,0,0],"color":"#B99B74","metallic":0.8,"roughness":0.24}}]}
~~~

Available model_edit operations: translate, rotate, resize, material, bevel, subdivide, smooth, remove_object, add_part. Send only validated data; Blender code is internal, never supplied by GitHub. For a complete new layout on a structured Nexus model use model_refine with the full specification. An imported Blender model may instead use model_inspect and model_edit.

Save the finished editable model to her own Desktop:
~~~json
{"id":"<NEW_ID>","device_id":"34b8c7f3dfb432bb3a4010d540e78903","type":"model_export","name":"<PROJECT_ID>"}
~~~

## Local Nexus Modeling Studio controls

IMPORT BLENDER FILE: user selects a .blend or .glb in a local Windows picker; Nexus retains a copy and generates an editable model, inspection report and preview. ChatGPT cannot provide import paths.

INSPECT + RENDER: generate object names, counts and a rendered model-only image.

SHARE MODEL PREVIEW: works only after the PC owner explicitly enables model-preview sharing in Settings. It shares only a small JPG in the customer's GitHub repository, not a screen capture or full project.

COPY CHATGPT REFINEMENT REQUEST: provides this bridge information and project ID for continuing work.

EXPORT EDITABLE .BLEND: copies a portable editable Blender project, preview and quality report into Desktop/VEILFORGE Finished Models/<PROJECT_ID>, keeping original and prior revisions.

## Security and honesty

No generic command prompt, Python supplied by GitHub, engine source modification, arbitrary local file access, desktop control, APK/EXE creation, or live wallpapers. User modeling is limited to original Blender models, bounded mesh modifications and structured rebuilds. Refinement with preview_url is an iterative render/review cycle, NOT shared real-time viewport control. Sims mod-request staging is not .package or .ts4script production. Never report unsupported capabilities as already working.
