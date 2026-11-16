# VEILFORGE NEXUS — VERIFIED NATIVE ROCK GENERATION v1

This is a NEW, allowlisted creative operation built into VEILFORGE Nexus.
It uses the real Foundry C# procedural stone mesh engine — no Blender,
Godot, Maya, Unreal, external scripts, proxy geometry, or downloaded assets.

FIRST, ensure the Nexus app on the owner's Windows PC has been upgraded to
the current stone-engine build and is RUNNING, the bridge is paired, and
the safe-job Auto Accept setting is enabled. The PC must be online for a
remote GitHub job; local tutorial generation works offline.

If working in the guided forest, click START THE GUIDED FOREST first,
which creates Desktop/projects/moonlit-forest-workshop.

Create a NEW JSON file at requests/<DEVICE_ID>/<NEW_ID>.json with a fresh
request id and the real device ID from the device's start guide:
{"id":"<NEW_ID>","device_id":"<DEVICE_ID>","type":"foundry_stones","name":"moonlit-forest-workshop"}

Other existing Nexus project IDs are permitted; absolute paths are not.
The native worker creates original triangulated stone geometry and writes
assets/foundry-native-stones/foundry-native-forest-stones.glb inside the
selected user's project, plus an engine provenance file with SHA-256.
Repeated requests reuse a VERIFIED asset rather than making duplicates.
The local tutorial stage is checked only after real evidence exists.

Read receipts/<DEVICE_ID>/<NEW_ID>.json and require result=completed
AND summary beginning FOUNDRY_STONES_VERIFIED. If the new action is
rejected as unsupported, the PC is still running an older Nexus build;
do not claim the rock was generated. No third-party installation or
arbitrary PC commands are necessary.

For a NEW rock-only project, use the normal foreman_production job with
a name and prompt about original rocks/flagstones/boulders; ALDER will
select the Foundry C# rock engine. For large scenes with vegetation,
the full multi-engine tutorial remains separate. This built-in stone
kit is a reproducible original collection, not a general-purpose
sculpting AI or a completed moonlit forest scene.
