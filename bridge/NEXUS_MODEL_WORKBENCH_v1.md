# VEILFORGE Nexus Model Workbench v1

User-controlled Blender model import, visual inspection, incremental refinement, and Desktop export. The customer's GitHub bridge is PUBLIC by default: only model-only preview images and bounded object summaries may be shared, and ONLY when the PC owner has enabled model preview sharing. Never publish full .blend, .glb, desktop screenshots, personal file paths or credentials.

## Import a Blender file

The PERSON must open Nexus Modeling Studio and select IMPORT BLENDER FILE; Nexus displays a local Windows file picker for .blend or .glb. This does NOT authorize ChatGPT to read arbitrary Windows paths. An original copy is stored in a new Desktop/projects/<slug>/models project, and Blender creates an editable nexus-working-model.blend, prompt-preview.png, and model-inspection.json. No prebuilt sample substitution.

## Ask ChatGPT to inspect a model

Submit a NEW job JSON at requests/<device_id>/<new_id>.json with:
{"id":"<new_id>","device_id":"<device_id>","type":"model_inspect","name":"<project_id>"}
Use the exact project_id shown by Nexus; do not submit a Windows path. If sharing is disabled, ask the user to turn it on in Nexus Settings; don't request desktop access. Once sharing is enabled, read receipts/<device_id>/<new_id>.json, require result=completed, inspect summary and preview_url (model-only image). The summary contains safe mesh names to use as edit targets.

## Incremental edits to the SAME Blender model

Submit model_edit with project_id in name and an edits array of 1-24 approved operations. Example:
{"id":"<new_id>","device_id":"<device_id>","type":"model_edit","name":"<project_id>","edits":[{"object":"Helmet Visor","operation":"translate","value":[0,-0.1,0]},{"object":"Helmet Visor","operation":"material","value":"#80E8FF"}]}
Operations: translate in scene units [-5,5] each axis; rotate [-180,180] degrees; resize multiplicative [.05,6] each axis; material uses #RRGGBB; bevel takes a width .001-.30; subdivide takes level 1 or 2; smooth takes true/false; remove_object deletes one named mesh from the current revision. The original .blend remains archived. To add actual new geometry instead of simply changing colors or moving components, use add_part with an explicit primitive. Object names MUST be exact matches from the latest model_inspect receipt. Nexus runs its OWN approved Blender script. It does not execute remote Python or OS commands, and preserves the previous .blend in revisions/ before promoting the new version. Fetch the model_edit receipt and, if present, preview_url for further comparison.

For new prompt-authored models, model_refine with a COMPLETE new 8-55-part model_spec remains available. It reconstructs geometry in the same project with a saved previous revision. model_edit instead makes bounded changes to the actual imported or previously created .blend. You can also use model_create to produce a new object from a descriptive idea.

## Save a finished personal file

The person can select EXPORT EDITABLE .BLEND in Nexus Modeling Studio. Nexus copies the latest working Blender model into Desktop/VEILFORGE Finished Models/<project-id>/ alongside its preview and inspection report. The original Nexus project and previous revisions remain. An approved remote model_export job can create this fixed-folder export by project ID only; it cannot choose a destination or access unrelated files. The user may then double-click the .blend and continue editing in Blender independently.

Always be truthful: inspecting a small rendered image plus a list of mesh names is useful but is not the same as a fully interactive Blender editing session in ChatGPT. The consumer supports bounded object edits and structured replacement designs, not unrestricted sculpting or desktop control.

### Add new geometry to an existing model

Example model_edit request for a helmet with a new crest (one of up to 24 edits):

```json
{"id":"<new_id>","device_id":"<device_id>","type":"model_edit","name":"<project_id>","edits":[{"object":"New helmet crest","operation":"add_part","value":{"shape":"cube","position":[0,0,3],"scale":[0.55,0.13,0.45],"rotation":[0,0,0],"color":"#DDAAFF","metallic":0.55,"roughness":0.33}}]}
```

The add_part shape is one of cube/sphere/cylinder/cone/icosphere/torus. Its position has three components in [-6,6]; scale in [.04,5.5], rotation in [-180,180]; metallic and roughness optional. The object name must be new and unique. Combine with bevel/subdivide/material operations in additional jobs. This is authentic Blender mesh editing, not arbitrary scripting or freehand sculpting. Always fetch the current inspection report, the completed receipt, and the new preview before choosing the next edit.
