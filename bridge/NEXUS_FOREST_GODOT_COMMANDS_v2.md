# VEILFORGE NEXUS — FOREST AND GODOT COMMANDS v2

This command list is written BY THE RUNNING NEXUS CONSUMER ENGINE
to its paired personal GitHub repository. These are safe typed commands,
NOT a general shell or a copy/paste terminal interface.

Create a fresh JSON file at requests/<DEVICE_ID>/<NEW_ID>.json using the
current device_id. Always read receipts/<DEVICE_ID>/<NEW_ID>.json;
result=completed is required. Never infer completion from the request.

The moonlit forest tutorial must be started inside the installed app first.
The same editable 3D stream/forest base stays in the Foundry viewport.
It is NOT a prebuilt finished native scene. Maya and Unreal may be
skipped without pretending their stages ran.

* foundry_stones: name=moonlit-forest-workshop.
  Runs native Foundry stone geometry with GLB/SHA-256 receipt.
* forest_attach_model: name=<EXISTING_MODEL_PROJECT_ID>.
  Attaches a previously-created original Blender prompt model to the
  forest scene using verified local .blend, GLB, render and QA evidence.
  It can recover items created before this consumer update without
  remaking them. Does NOT mark the entire Blender forest tutorial verified.
* model_create or model_prompt: optional scene_id=moonlit-forest-workshop
  alongside their normal prompt or model_spec fields. A successfully
  generated new model is then immediately registered into the editable
  forest Godot scene after evidence checks. Without this scene_id, Nexus
  correctly saves the model as an independent project instead.
* forest_vegetation: name=moonlit-forest-workshop.
  Runs the bundled original Blender vegetation producer HEADLESS;
  saves the original .blend, FBX, GLB, rendered preview and SHA report.
  No duplicated Blender editor windows or fixed per-item cooldown.
* forest_godot_prepare: name=moonlit-forest-workshop.
  Builds editable Godot scene source from the forest/stream layout,
  and includes only verified native Blender/Foundry GLB pieces.
  Requires no Godot installation simply to create source. This
  DOES NOT certify that Godot imported or ran the scene.
* game_qa: name=Moonlit Forest Workshop.
  Requires installed Godot editor, runs headless native --import and
  120 frames, writes source-hash-bound PASS/FAIL receipt.
  The tutorial last step is VERIFIED only after real native success.
  For another existing local game, use its exact original project name.
* game_export_debug: name=Moonlit Forest Workshop; platform=windows
  OR platform=android (lowercase). This requires existing native
  game_qa PASS and installed Godot export templates. Android may also
  require a configured SDK/JDK. Builds verified debug EXE or APK in
  the selected project's builds folder, not on the remote phone.
  It DOES NOT use or claim a publicly trusted publisher certificate,
  native APK device testing, or a Play Store release.

Use NEW job IDs for each action. Sample:
~~~json
{"id":"<NEW_ID>","device_id":"<DEVICE_ID>","type":"forest_godot_prepare","name":"moonlit-forest-workshop"}
~~~
~~~json
{"id":"<NEW_ID>","device_id":"<DEVICE_ID>","type":"game_qa","name":"Moonlit Forest Workshop"}
~~~
~~~json
{"id":"<NEW_ID>","device_id":"<DEVICE_ID>","type":"game_export_debug","name":"Moonlit Forest Workshop","platform":"windows"}
~~~
~~~json
{"id":"<NEW_ID>","device_id":"<DEVICE_ID>","type":"game_export_debug","name":"Moonlit Forest Workshop","platform":"android"}
~~~

If Godot is missing, no test or export is claimed. If an import,
script or template errors, report the precise sanitized failure receipt
to the user and revise only allowlisted user-owned project files.
No arbitrary remote Python, mayapy scripts, Windows shell, or licensing
bypass is authorized.

Installed Autodesk Maya 2027 through 2018 may be detected by Nexus.
Licenses remain the customer's responsibility; a Maya optional step
can be SKIPPED without marking it verified. A skipped stage is not
a fake checkmark. Installed Maya Python errors can be diagnosed from
the native runner's output, but the paired bridge never executes
arbitrary user-supplied code.
