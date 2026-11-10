# VEILFORGE NEXUS — PROJECT ASSET TREE / TEXTURES v1

The customer can already share MODEL-ONLY screenshot previews. This guide adds structured, safe READ access to the assets inside the selected Nexus project — NOT arbitrary Windows desktop folders.

Repo: heraitousir/vf-nexus-open-34b8c7f3dfb432bb
Device ID: 34b8c7f3dfb432bb3a4010d540e78903

1. The PC owner opens Nexus Modeling Studio, chooses a model and imports texture images via IMPORT TEXTURE ASSET. The owner may also open FULL BLENDER EDITOR locally and inspect all Blender asset-browser panels manually.
2. After the user enables model-only sharing, submit a fresh GitHub request: {"id":"<NEW_ID>","device_id":"34b8c7f3dfb432bb3a4010d540e78903","type":"model_assets","name":"<PROJECT_ID>"}.
3. Read receipts/34b8c7f3dfb432bb3a4010d540e78903/<NEW_ID>.json. The completed receipt contains assets.tree.textures[] with content-addressed asset_id, image format and byte size, and assets.tree.materials[] from the current model inspection. No file paths or image bytes are shared; model-only preview sharing must be ON.
4. Use model_inspect to get an exact mesh object name, then submit a model_edit job with e.g. {"object":"EXACT MESH NAME","operation":"texture", "value":{"asset_id":"tx-24hexcharacters", "channel":"base_color","uv_smart":true}}.
5. Valid channels: base_color, roughness, metallic, normal, emission. Also available: operation uv_smart with value true, and pbr with color #RRGGBB, metallic 0..1, roughness .05..1. The engine validates all edits, applies native Blender UV/node operations in an isolated project revision, packs image data into the editable .blend, and renders for inspection.
6. To access a new image from outside the project, ask the PC owner to import it locally. The remote chat cannot browse her private desktop or submit arbitrary file paths, Python, shell commands, or unknown asset URLs.
