# VEILFORGE Nexus Consumer — Creative Reference & Capability Memory v1

*A living reference for the person creating, their paired ChatGPT, and the Nexus Modeling Studio. This is a creative vocabulary and capability map, NOT a fixed prompt recipe. Ideas need not match any example.*

## What this reference is for

Nexus is a **Blender-backed creative workshop**, not a vending machine with a small menu of preset objects. Think of it as a way to turn a description into editable geometry, inspect an actual render, revise the same project, combine techniques, and save a model that the person can open in Blender later. The person's preferences and the appearance they are trying to achieve matter more than any example in this document.

When a new ChatGPT conversation starts, or the assistant becomes unsure of Nexus's available tools, it should rediscover this versioned guide and the current capability index in the user's own Nexus GitHub bridge. A chat cannot be forced to remember past sessions simply because an app saved a file. The persistent reference is the **recoverable source of truth**; the assistant should read it again when needed.

**Read capabilities as creative possibilities, not mandatory commands.** For example, "a damp stone courtyard with carved reliefs" is a design idea. Its parts might combine repeated stone blocks, uneven paving, material roughness changes, moss accents, soft lighting and several correction passes. No single part name, primitive, size or technique is required merely because a guide showed an example.

## The creation space

### Original object design

A person can describe an original object and Nexus can attempt a real Blender model using its current local idea-to-geometry planner. Visual ideas can include machinery, fantasy props, architectural structures, stylized creatures, environment pieces, furniture, game objects and symbolic sculptures. The idea planner is **not** a general-purpose learned sculptor; it may build a rough component interpretation instead of a faithful organic model. The better approach when an idea needs precision is to articulate silhouette, proportions, components, surface treatments and reference views in stages.

For more controlled component construction, the paired assistant can plan a structured assembly with meaningful elements, dimensions, orientations and material properties. The current detailed single-job specification supports 8–55 parts. This is a per-job implementation bound, **not an artistic ideal or a promise of unlimited detail**. Large creations should be designed with iterative improvement in mind; native Blender can also handle more complex work locally.

### Existing models are canvases, not dead ends

A model already created in Nexus or imported by the user can be inspected, adjusted, extended and exported. Incremental edits can translate, rotate or resize a named mesh; adjust basic materials; bevel edges; subdivide or smooth surfaces; remove elements; and **add new primitive-based geometry**. For some structured Nexus creations, replacement refinement rebuilds a full layout while archiving the prior one. These are different modes: incremental editing changes the existing asset; rebuilding a structured specification replaces its generated structure.

The model's actual current inspection, not an old prompt, should determine the names and geometry targeted by an edit. View the latest result after each meaningful pass and adjust the strategy based on what changed.

### Full Blender editor — on the person's PC

Nexus offers a button that opens the selected project in Blender's full **local** editor. The person can then use Blender's ordinary modeling, sculpting, modifiers, UV editing, painting, rigging, shading, rendering, asset browser and material tools themselves, subject to Blender installation and hardware. This does **not** give the remote ChatGPT arbitrary Blender keyboard/mouse control, script execution, access to every asset library, or access to other desktop programs. The finished .blend is still independently editable by the owner.

## Asset-tree literacy: what the chat can actually see

Model screenshots and the **project asset tree** are complementary, not interchangeable. A screenshot lets the assistant critique a silhouette, lighting or texture appearance. It does not reveal every available material or image asset. The asset catalog lets the assistant reason about which **registered textures** are available for that Nexus project, without granting access to the entire computer.

When the user selects an existing model in Modeling Studio and imports a texture image, Nexus copies that user-selected file into that project's own texture library and gives it a **content-addressed texture asset ID**. The user can import several materials for different looks. Supported import candidates include PNG, JPEG, TGA, TIFF, EXR, HDR, BMP and WEBP, subject to format support in the installed Blender and practical limits. If an image is missing from the catalog, the user should import it with the local file picker rather than ask the chat to guess its Windows path.

Through the typed model_assets catalog, a paired chat can ask what resources are registered for a selected project, then choose techniques based on that real list. This is a memory aid, not an instruction to blindly apply every available image.

With the user's model-preview sharing enabled, the paired chat can request an inventory of that project's approved texture IDs, image formats and byte sizes, together with material names recorded by the model inspector. The user can turn sharing off. In the default public GitHub bridge, the catalog and object/material names may be visible to others, so use bland project names and avoid sensitive image content. **Image files, arbitrary directories, credentials and raw project files are not exposed in the catalog.** Asset IDs, not machine paths, are the safe way to refer to a texture.

The current catalog is **project-scoped**, not a mirror of Blender's global Asset Browser. It does not automatically crawl custom disk libraries or the owner's private file tree. Full Blender Asset Browser navigation remains a local Blender activity. Future library indexing could broaden discovery with explicit folder approval and permissions, but that is not a capability to claim today.

### What "apply a texture" can mean

A mesh needs appropriate UV coordinates to map a picture onto its surface. Nexus supports a basic smart UV-unwrapping option, and PBR material adjustment using Blender's nodes. A selected registered image can be connected to:
- **Base color**: the visual color or painted appearance (wood grain, stone, cloth weave, weathering).
- **Roughness**: how spread or sharp reflections appear (polished metal versus chalky stone).
- **Metallic**: the material's metal response.
- **Normal**: small-scale surface direction changes such as bumps, etched grooves and mortar joints; normal data is not the same as new physical geometry.
- **Emission**: visible self-lit accents such as runes, instrument screens and energized seams.

These channels are part of one surface story. A painted metal helmet might use a restrained metallic value, a roughness image to break up uniform highlights, and normal details for shallow engravings. Ancient stone may combine uneven color with high roughness, gentle normal relief and moss placed where water would collect. Good materials should support the form instead of disguising weak geometry.

Nexus can pack image assets into its saved Blender working file during the approved editing workflow. The user should still reopen exported files to check that image links, nodes and model appearance survived. A texture does not magically exist merely because the assistant suggested one; it must be in the registered project library.

## Technique vocabulary — combine freely

These are reference patterns distilled from previously tested Blender work, not locked recipes or a promise of AAA output.

**Weathered limestone and masonry.** Staggered blocks or irregular slabs, believable joints, subtly beveled edges, consistent material families, weighted normals, roughness variations and small color shifts make walls feel built instead of tiled. A block's silhouette and relationship to adjacent blocks are as important as the albedo image. Particularly useful for arches, steps, ruins, fountains and garden walls.

**Mossy coping and wet paving.** Visual wear should follow physical causes. Horizontal crevices, pond edges and sheltered seams collect dark moisture and moss differently from exposed stone faces. Keep the weathered material related to the drier counterpart so a single scene remains coherent. Wet areas usually need **controlled** reflections, not a giant glossy gray plane.

**Layered hard-surface forms.** A helmet, machine, chest, sword or sci-fi unit benefits from a readable primary mass, secondary functional structures and restrained tertiary accents. Think in terms of silhouette, function, negative space, edge bevels and material separation. A small bright trim should not overpower the object's identity. Avoid building the entire surface from identical spheres or boxes when a sculpted profile is needed.

**Organic forms and character design.** Begin with major anatomy masses, proportions and posture; check front, side and three-quarter views before adding fine surface detail. A creature made of primitives can be an intentional blockout, but a real production-grade character usually needs sculpting, retopology, UV seams, rigging and animation in Blender. Nexus's remote typed editing does not yet supply a complete autonomous organic modeling pipeline. The user can work in full Blender locally and bring that result back for inspection and bounded revision.

**Foliage, terrain and scenic props.** Use silhouette layers and variation in size, tilt and clustering rather than a carpet of identical assets. Think about terrain relief, contact with the ground, foliage density, areas of rest and focal composition. The current remote consumer tool is primarily a model workshop, not a guaranteed terrain physics simulator or an unrestricted scene generator.

**Lighting and presentation.** A model is easier to judge with a neutral turntable or three-quarter render and controlled key/rim illumination. Check silhouette without relying on glow. Inspect roughness under a grazing light; inspect texture scale close enough to see stretching and seams. The built-in preview is a diagnostic aid, not proof of full game-engine performance or photorealism.

**Reference discipline.** An external photograph or sample can inform proportion, material response or construction principles without being reproduced or claimed as a licensed asset. Keep the creative result original and respect asset permissions. The existing reusable stone techniques are a starting vocabulary, not an exclusive style.

## From an idea to a convincing custom creation

This is a useful way to reason, **not a compulsory sequence**. A person may start anywhere and return to earlier decisions.

1. **Intent and constraints.** Ask what the object should communicate: worn, ceremonial, industrial, playful, dangerous, elegant? Where will it be viewed, how large should it feel, what is its desired style? Distinguish required features from optional flourishes.
2. **Silhouette and scale.** Establish the big masses and compare from more than one view. Fix the outline before spending time on tiny rivets, texture noise or inscriptions.
3. **Structure and functionality.** Organize components so parts have reasons to exist: hinges belong where panels pivot; supports carry weight; straps attach to something; stone courses meet plausibly.
4. **Surface language.** Choose a coherent palette, materials and weathering causes. Use actual imported textures when available. The absence of an image texture should lead to a procedural or color-based placeholder, **clearly described as such**, rather than a claim that Nexus found a texture it cannot access.
5. **Topology, UVs and detailed forms.** Add geometry where the silhouette needs it, and texture/normal details where surface illusion suffices. Avoid gratuitous subdivisions and runaway memory demands.
6. **Preview, critique and revise.** Inspect what the model actually looks like, identify the most visible mismatch, and revise that cause. Repeat in meaningful passes. Do not pretend an attempted edit succeeded without the completed job receipt and rendered/inspection evidence.
7. **Export and handoff.** Preserve the editable .blend, any optional GLB export, render and inspection report. Open the final file in Blender when possible; check packed images, scale, orientation and geometry.

Helpful conversation might sound like: "This brass observatory has the right dome, but its supports are too thin; I'd strengthen the legs before working on window glass." Or "The pond edge would benefit from the mossy-coping technique and a darker roughness map, if a suitable texture is registered." These are *creative judgments*, not inflexible instruction strings.

## Inspiration to demonstrate combinations — never a fixed menu

**An ancient knight's visor:** a memorable silhouette, layered cheek plates, a hinge and fastening points, subtly worn bronze or steel, paint chips near striking surfaces and a fine roughness variation. Start from the head/helmet scale, then correct readability before ornament.

**A forest shrine:** intentionally uneven flagstone steps, moss along the sheltered side, twisted roots around masonry, a worn offering bowl and a single focal light. Combine the stone technique vocabulary with user-approved image materials, then check that the environment reads as one place.

**A mechanical moth:** a recognizable thorax and wing silhouette, segmented joints, semi-translucent membranes, metal struts and restrained emissive details. Geometry should make the wings legible; luminous texture should merely reinforce it.

**An old captain's desk:** a solid wood frame, drawers and handles that look functional, slightly different roughness on worn corners, leather or cloth details and believable joinery. Repeating wood texture alone will not replace modeled structure.

**A luminous spellbook:** thick page stacks, an articulated clasp, layered embossing, dark leather and localized emitted glyphs. Ask how the book opens and where its weight rests before applying magical effects.

**A creature or human figure:** use the consumer tool to establish design intent and block out recognizable masses, then treat organic detail, facial fidelity, fur, cloth drape and animation as work that may require native Blender and dedicated evaluation. Do not present a rough blockout as a finished character.

Nothing prevents ideas that combine these principles differently. The aim is for the assistant to propose techniques **because they solve a visual problem**, not because it has memorized a specific example.

## How the assistant should keep itself oriented

- **At the start of a fresh Nexus chat:** read the repository's README, this Creative Reference and the relevant latest v2/v8/v1 capability/asset guides. First verify that GitHub access is real and whether writing is permitted. If the chat cannot write to the repository, explain that plainly; a reference document does not grant credentials.
- **When the user asks "what can we make?"**: describe open-ended ideas and relevant techniques, with caveats based on current tools, rather than presenting 55 parts as a creative ceiling or presenting example objects as menu choices.
- **When the user asks to use textures:** find the actual registered assets with the project catalog if sharing is enabled; otherwise invite the user to import them locally. Do not infer image asset IDs from screenshots.
- **When a model looks wrong:** compare the latest inspection and preview, choose targeted changes and prefer incremental edits when preserving hand-built details. Mention native Blender edits when the request exceeds the bounded remote workflow.
- **When resuming later:** re-read the *versioned* guide and recent receipts; past ChatGPT conversations are not a reliable autonomous memory mechanism. A project ID, latest inspection and verified files are better anchors.
- **When reporting progress:** distinguish a proposed plan, a queued job, an actual completed job, a preview, and a verified user-installed build.

## Current boundaries and realistic expectations

This edition intentionally restricts **remote** actions to typed, project-scoped model operations. It cannot grant ChatGPT generic desktop control, unrestricted code execution, arbitrary filesystem browsing, full Blender UI input, or permission to modify the owner's Foundry engine. It supports a user-controlled full Blender editor on the PC, which is broader than the remote bridge.

Single advanced geometry submissions currently have 8–55 parts; model edits have 1–24 validated changes; preview import paths and resource budgets have safety restrictions (including mesh/triangle checks). These are current release limits and may evolve; do not describe them as unlimited. A long-term roadmap can add staged model composition, procedural instancing, resource-aware LOD, sculpting, retopology, texture baking and repeated quality passes. **These are future engineering goals, not shipped guarantees.**

Personal projects, prior revisions and original models belong to the person. Remote requests must not replace another project's files, upload original .blend contents to a public repo, access external libraries without approval or silently run installers. Saving a guide does not require sharing sensitive personal content.

### The most useful reminder

**Imagine freely. Choose techniques deliberately. Use only assets that are actually registered and permitted. Inspect the real result. Revise the same creation. Preserve an editable file. And never mistake a reference example for a rule.**
