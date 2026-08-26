# Prompt Compiler

Compile research and Source Cards into visible pixel decisions. Keep the final prompt shorter than the analysis.

## Compiler Order

1. **Canvas:** output count, aspect ratio, orientation, finished borderless image, shot scale.
2. **Source contract:** image role, semantic minimum, recognition anchors, identity/object signature, authored design anchors, transformable elements, identity fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, color-authorship mode, source-led temperature policy, and allowed changes.
3. **Directorial proposition:** actor, visible pressure/counterforce, intended first read, one primary macro departure from the structural options in `directorial-contrast.md`, its aesthetic payoff, one supporting move, protected anchors, and a thumbnail difference target.
4. **Focal actor and transformation:** one readable verb/relationship; identity-preserving aesthetic plane/light treatment; salient-prop semantic anchors versus redesigned silhouette/panels/motif rhythm; for environment-emphasis, name the hero form, counterform/current, merged repeated detail, and the major area/contour/overlap/light/color impact of the primary departure.
5. **Attention geometry:** composition family, central attention zone, perspective, quiet area, viewing path.
6. **Value, subject light, and contrast ownership:** three mass groups; motivated key geometry; planes revealed on the focal subject; shadow-side separation; optional limited bounce; supportive background field; brightest/deepest placement; haze/rim restraint; and focal/support/context contrast tiers.
7. **Layered color authorship:** source strengths/problems; reliable neutral evidence and source saturation baseline; Preserve-and-refine, Rebalance, or Re-script; Source-neutral, Preserve source bias, or Motivated shift; named temperature owners/boundaries; protected neutrals and local-colour owners; primary illumination; limited environment influence; restrained final grade; one primary contrast axis and at most one subordinate axis; dominant field, structural counter, focal apex, optional connector/neutral bridge; context chromatic-gray/quiet-color family; optional color-collision owners/adjacency/dominance/function; protected anchors.
8. **Shape and surface:** silhouette/plane reconstruction first; then material-specific marks, edge/detail hierarchy, spatial depth, and limited graphic 2D intervention.
9. **Optional light tactile depth:** name only the overlap, form turn, contact, directional crest or foreground separation that receives mild body; state which continuous/distant fields stay low-relief.
10. **FX:** only if story-motivated; unique shape language and edge hierarchy.
11. **Avoids:** the shortest relevant list of likely model errors and sample residue.

Do not include a rule that cannot become a visible pixel, tool parameter, source-role mapping, or quality check. Keep generation prompts compact: lead with the six to ten highest-impact decisions, remove redundant adjectives, and avoid long inventories that dilute shape reconstruction.

## Portable Core Before Model Wording

Write one model-neutral render contract before adding optional phrasing for a particular runtime. Keep its decisions concrete enough to survive paraphrase:

```text
Portable render contract:
- Canvas and anchors: [count, ratio, orientation, recognition/topology invariants; authored design anchors].
- Macro map: [five-to-nine named interlocking masses and their area/overlap relationship].
- Value and colour roles: [three value groups; dominant field, structural counter, focal apex, neutral bridge; protected colours; source-relative chroma budget].
- Contrast ownership: [Tier 1 focal peaks; Tier 2 support cues; Tier 3 context reductions].
- Focal aesthetic and prop design: [identity signature; connected face/object planes and flattering light; prop semantic anchors; redesigned silhouette/panels/motif rhythm rather than traced detail].
- Subject light and grade: [motivated key, shadow-side separation, limited bounce, supportive background field; local colour / illumination / environment / restrained grade; source neutral evidence and Source-neutral / Preserve source bias / Motivated shift temperature policy].
- Shape reconstruction: [silhouette breaks; meaningful focal planes; merged repeated detail].
- Material grammar: [material A plane scale/direction/edges/reflectance]; [B different]; [C different when present].
- Edge hierarchy: [hardest, medium, soft/lost owners].
- Optional light depth: [named spatial carriers] receive mild body; [continuous/distant fields] remain low-relief and connected.
- Anti-filter gate: [what must visibly differ from photographic underpainting at thumbnail, mid, and close scale; reject mosaic/patchwork relief].
```

Treat this block as required decisions, not prose to copy verbatim. Put recognition invariants and the primary macro departure near the beginning of the final prompt and repeat the shortest critical preservation/avoid clause at the end. Avoid sampler, seed, model-version, quality-tag, or house-style vocabulary in the portable core; those controls do not transfer reliably between model families. See [model-consistency.md](model-consistency.md).

## Base Generate Template

```text
Create exactly one original [ratio/orientation] painterly-animation keyframe, a finished borderless image.

Scene and verb: [original subject, environment, one readable action/relationship]. Keep the focal event perceptually dominant inside the middle attention zone through [isolation/value/chroma/edge/perspective], while [quiet/occluding region] occupies a substantial part of the frame. Use [one composition family] and a believable spatial camera with clear foreground, middle, and atmosphere.

Directorial proposition: [actor] is [visible pressure/relationship] against [counterforce]; the first read is [event]. Make [specific primary macro departure] so [major area/contour/overlap/focal-scale/light/color-zone relationship] is unmistakable at 128–256 px and improves [beauty/expression/clarity/tension/rhythm/depth/story]; reinforce it with [supporting move]. Preserve [declared anchors], but do not preserve [incidental distribution].

Value, subject light, and contrast ownership: organize the frame into three large value groups: [dominant field], [supporting mass], and [small apex]. The primary light is [visible/motivated source with geometry] and reveals [focal planes] while retaining [shadow-side separation]; use only [limited bounce/reflected colour] and let [background field] separate the focal silhouette. Reserve the brightest useful accent and deepest useful contact/occlusion for [focal path]. Tier 1 [focal owner] peaks in [two or three selected contrast dimensions]; Tier 2 [support] keeps medium structural cues; Tier 3 [context] becomes a unified [scene-owned colored/chromatic-gray] field through lower [local contrast/microcontrast/edge density/hue noise/texture frequency] while retaining [depth/material cues]. Avoid a global rim, face glow sticker, uncontrolled haze, and broad bloom.

Color authorship: use [Preserve-and-refine/Rebalance/Re-script] because [source/story reason]. The temperature policy is [Source-neutral/Preserve source bias/Motivated shift] from [reliable neutral/source evidence]; only [named light/atmosphere/material/depth owner] may shift [reachable region] toward [direction], and [protected neutrals/local colours] remain stable. Establish [source-informed local-colour owners], let [primary illumination] modify only [reachable planes], add [limited environment reflection/atmosphere], then apply [restrained final grade and its limits]. Keep overall chroma [at/below/reallocated from] the source baseline according to the selected mode. Use [primary contrast strategy] with [optional subordinate strategy]. Assign [dominant field: spatial owner, hue family, value, chroma], [structural counter: owner and separation job], [focal accent/apex: owner and attention job], and [optional connector/neutral bridge]. Color collision is [None/Preserve existing/Author new: owners, adjacency, dominant side, function]. These roles may share one hue family when value/chroma does the work. Preserve [protected local-color anchors]. Warm-cool is optional; avoid automatic warm beauty grading, universal cool shadows, formulaic teal-orange, purple-neon, global gray fog, equal saturated competition, dirty mid-chroma, and a final grade that overwrites skin or material colour.

Rendering: grounded stylized proportions, spatial 3D depth with a hand-painted 2D finish, faceted color/value planes, broad peripheral brush masses, selective sharp edges at [eyes/gesture/object], and soft or lost edges in haze and shadow. Differentiate skin, cloth, metal, wall, smoke, and energy by plane size and edge behavior. If FX are present, use [unique graphic shape language] with one sharp core, broad motion forms, sparse particles, and no global glow.

Light tactile depth, only if requested: keep most of the painting low-relief. Add slight loaded body only where [named overlap/form turn/contact/directional crest/foreground separation] clarifies depth. Keep [sky/haze/skin/distant or other continuous fields] broad and connected. Surface catches are narrow and subordinate to the painted colour and light.

Avoid: franchise characters, logos, runes, copied architecture or camera layouts; photoreal plastic skin; generic anime cel shading; uniform black outlines; all-over texture; excessive bloom, sparks, wet gloss, crushed muddy blacks, repeated equal-size paint tiles, palette-knife mosaic, or full-frame 3D relief.
```

Replace brackets. Remove irrelevant clauses rather than leaving generic filler.

## Edit Target Templates

Lead with change plus preservation:

```text
Edit Image 1 into one finished [ratio] painterly-animation keyframe.

Preserve as recognition anchors: [identity, count, relationship, gesture, signature silhouette, protected geometry, wardrobe/object color anchors, required text]. Do not add or remove subjects.
Identity and design: preserve [visible face/object signature]. Improve [connected focal planes, expression/shape edges, head-neck or support attachment, flattering motivated light] without generic beautification. For [salient prop], preserve [category, owner/contact, functional state, dominant colour, essential motif] but redesign [silhouette rhythm, panels, repeat grouping, material, highlights and overlap] instead of tracing incidental detail.
Reconstruct: [transformable proportions/contours, crop/headroom, minor folds/hardware, repeated props, environment micro-detail, area/value/color/light/contrast organization]. Use [Identity-first/Balanced] transformation, [Restrained/Expressive] abstraction, [High/Mid/Low]-key exposure, [Preserve-and-refine/Rebalance/Re-script] color authorship, and [Source-neutral/Preserve source bias/Motivated shift] temperature policy from [source evidence]. Make [primary macro departure and aesthetic payoff] plus [supporting move] without changing [protected anchors].

[Then add attention geometry, three-group value plan, color roles, motivated light, faceted material/edge treatment, optional light-depth carriers/quiet fields, and relevant avoids from the base template.]
```

Do not claim exact pixels. If pixels or typography must be exact, keep those regions outside the generative edit and composite deterministically.

For **Style-first** photo remakes, use this shorter contract:

```text
Rebuild Image 1 as one finished [ratio] painterly animation keyframe; do not put an oil-paint texture over photographic shading.

Keep only these recognition anchors: [subject identity/count, action or pose, signature color anchors, essential spatial relationship]. Permit [crop, controlled proportion and contour stylization, merged folds/hardware/foliage/props, redesigned atmosphere and environment shapes].

Directorial abstraction: [dramatic proposition]. Make [specific primary macro departure] so [major area/contour/overlap/focal-scale/light/color-zone relation] visibly differs from the source at 128–256 px; reinforce it with [supporting move]. Do not preserve [incidental distribution].

Focal design, shape, and contrast: preserve [identity/object signature] while rebuilding [connected face/object planes, expression edges and flattering motivated light]. Preserve [prop semantics and essential motif] but redesign [silhouette/panels/repeat rhythm/material/overlap]. Use [Restrained/Expressive/Radical] abstraction; [subject silhouette and meaningful face/object planes]; [broad environment masses]; [material A mark grammar versus material B and C]. Exposure is [high/mid/low]-key because [scene reason], with [three value groups]. Assign Tier 1 [focal], Tier 2 [support], and Tier 3 [chromatic-gray/scene-owned context quieting plus retained depth/material cues]. Color authorship is [mode] because [source/story diagnosis], with [Source-neutral/Preserve source bias/Motivated shift] temperature policy from [reliable source evidence] and no automatic warm beauty cast; establish [local colours], [primary light], [limited environment influence], and [restrained final grade]; use [primary contrast], spatially assign [dominant/structural/focal/neutral roles], decide [None/Preserve/Author] color collision, and preserve [color anchors]. Make [focal event] the first read through [two cues]. Add [one restrained natural or FX graphic intervention].

If light tactile depth is requested, localize it to named overlaps, form turns, contacts, directional crests or foreground separators; keep continuous and distant fields low-relief. Avoid photographic underpainting, source/result thumbnail layouts that differ only in surface texture, global impasto/filter texture, identical marks across materials, literal micro-detail, generic anime outlines, plastic skin, franchise motifs, unnecessary darkness, passive source color, forced warm-cool, global gray fog, global LUT color, palette-knife mosaic, and all-over 3D paint relief.
```

For a **Style-first environment-emphasis** remake, use this explicit abstraction contract instead of a generic landscape prompt:

```text
Rebuild Image 1 as one finished [ratio] painterly animation environment keyframe. Use Medium/Low structural fidelity, Style-first transformation, [Expressive/Radical] abstraction, and [High/Mid/Low]-key exposure. Do not preserve scenic realism beneath painted texture.

Preserve only: [principal landform/structure, foreground-middle-distance relationship, dominant direction, protected geometry/color anchors, ratio if required]. Treat [tree/rock/window/wave/foliage/rubble/reflection counts and minor positions] as transformable; merge them into a few rhythm groups.

Environmental drama: make [hero form] [visual verb] against [counterform/current]. Reduce the frame to about five to nine interlocking macro masses. Make [primary macro departure] so [major area/contour/overlap/light/color relationship] changes at thumbnail scale; reinforce it with [supporting move] [plus a second primary-level departure for Radical]. Permit controlled restaging of [crop/horizon/overlap/spacing/local perspective] without breaking the preserved anchors. Make [focal event] the first read through [two cues] and keep [quiet field] intentionally broad.

Value/light/contrast: [three value groups] and [motivated light geometry]. Exposure remains [selected key]; do not use darkness as a style shortcut. Tier 1 [hero/focal event] owns [selected peak dimensions], Tier 2 [counterform] keeps [medium cues], and Tier 3 [context] compresses [local contrast/microcontrast/edge density/hue noise/texture frequency] into [chromatic-gray/scene-owned quiet family] while retaining [depth/material]. Color authorship: use [mode] because [source diagnosis], with [Source-neutral/Preserve source bias/Motivated shift] temperature policy from [reliable neutral/source evidence], [primary contrast strategy], and spatially owned [dominant field/structural counter/focal apex/optional connector or neutral bridge]; color collision is [None/Preserve/Author with owners and boundary]; preserve [protected color anchors and neutrals]. Do not add a warm beauty grade, universal cool shadows, warm-cool, or complementary opposition unless a named owner and scene function require it.

Material design: [material A] uses [large-shape/edge/mark grammar], [B] uses [different grammar], and [C] uses [different grammar]. Add [restrained broken contour/dry-brush vector/flat shadow seam] over spatial depth. If tactile depth is requested, add mild body only to [named near overlap/turn/contact/crest] and keep [continuous atmosphere/distant field] low-relief.

Avoid conventional scenic realism, source/result blur maps with the same major area ratios, generic matte-painting polish, literal repeated asset counts, photographic underpainting, global brush or color filters, identical marks across materials, uniform volumetric or gray fog, forced color-wheel formulas, franchise motifs, and invented text or subjects.
```

State concrete deformations and a thumbnail difference target; words such as “dramatic,” “stylized,” “abstract,” or “painterly” alone do not satisfy the environment contract.

## Semantic-source or Analyze + Generate

Compile in two stages:

1. State extracted semantic minimum and visual grammar without names, copied text, or exact objects/layout.
2. Generate a new subject, action, camera, environment, prop set, and exact palette. Keep only the abstract relationships and fixed system.

## Prompt-only

Return the compiled prompt plus an input-role map when images are expected. End with: `No image was generated or visually verified.`

## Reference Analysis Output

Return:

1. Observed evidence per reference
2. Inferred narrative/emotional intent
3. Fixed system with confidence
4. Variable system
5. Sample residue/no-copy list
6. One reusable operational prompt

Do not invoke an image tool unless the user also asks for a result.

## Tool Execution

- Use the runtime's real image generation/editing mechanism; attach every Edit Target and Support Insert through tool parameters, not prose alone.
- Use the requested ratio when supported. If a backend supports only nearby sizes, preserve composition intent and disclose the actual output.
- Default to one result. Generate a batch only when requested.
- After tool output, inspect the actual image before describing it as successful.

## Compact Source-led Example

This example uses a value-led narrow-hue relationship; it demonstrates prompt syntax, not a default palette. Analogous, saturation-led, localized warm-cool, complementary, and near-monochrome solutions are equally valid only when justified by the color audit.

```text
Create one original 16:9 painterly-animation keyframe of a lone maintenance diver bracing a failing pressure door in an abandoned underwater transit hub. A pale circular window behind the diver forms the central focal island; near-black pipes and a cropped foreground valve create an asymmetrical aperture. Three value masses: deep blue-green structure over most of the frame, desaturated blue-gray machinery as support, and a small cold-white window/helmet apex. Preserve a cool underwater source bias; the window is the motivated key light and no automatic warm accent or teal-orange grade is added. Grounded stylized anatomy, faceted painted planes, spatial depth, broad shadow masses, sharpest edges at the eyes, gripping hands, and door seam, lost edges in drifting silt. Flat graphic pressure fractures radiate from one seam with a tight core and almost no particles. Avoid franchise motifs, generic neon, glossy skin, uniform rim light, excessive sparks, and muddy blacks.
```
