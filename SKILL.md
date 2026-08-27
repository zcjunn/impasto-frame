---
name: impasto-frame
description: Create or edit original painterly frames with authored composition, source-led colour control, identity-preserving focal beauty, redesigned salient props, subject-owned illumination, faceted material planes, and restrained tactile brush depth used only to clarify spatial relationships. Use when a photo or prompt should become a strongly stylized painted frame, or for reviewing warm/cool cast drift, dirty grading, unattractive faces, literal prop tracing, filter, mosaic, patchwork, and uniform-relief failures. Do not use for faithful photo correction, pixel-locked preservation, all-over heavy impasto, sculpted wall relief, or copying a named work, character, logo, or exact frame.
---

# Impasto Frame

Translate shorthand such as “hand-painted animated film” or “dark graphic cartoon mood” into an original, observable visual system. Optimize the finished frame, not resemblance to a protected sample.

## Model recommendation

When model selection is available, prefer **gpt-5.6 Luna** with reasoning effort set to **Extreme / 极高**. Model capability affects how reliably the workflow is carried through: composition decisions, source-led colour analysis, focal identity, material separation and small-scale detail may vary with the model. Treat this as a recommendation, not a hard dependency, and judge every result against the quality gate rather than assuming model choice guarantees a pass.

Treat any demonstrated photo or failed output as a regression case, not a content template. Generalize the failure class across portraits, environments, architecture, products, creatures, and action scenes; keep subject-specific materials and compositions conditional.

Tactile paint depth is a subordinate spatial cue, not the image's construction method. The composition, colour, value masses, shape design, overlap and edge hierarchy must establish depth first. Add only light local body where a stroke clarifies an overlap, contact, form turn, directional crest or foreground separation; keep continuous fields coherent and mostly low-relief.

## Route the Request

Choose the smallest route that satisfies the request.

- **Generate:** Create a new finished keyframe from text or semantic-source images.
- **Edit Target:** Restage or repaint a user image while preserving declared identity, object, or spatial invariants.
- **Reference Analysis:** Extract evidence, fixed rules, variables, and sample residue. Do not generate unless asked.
- **Prompt-only:** Return an executable prompt. Do not generate or claim visual inspection.
- **Analyze + Generate:** Analyze references, discard sample residue, then create a different subject and composition.

Default to one finished borderless image when the user asks to make an image and gives enough direction. Do not run an intake questionnaire when the answer can be safely inferred.

## Load Only Relevant References

- For every Generate, Edit Target, or Prompt-only task, read [references/style-system.md](references/style-system.md) and [references/prompt-compiler.md](references/prompt-compiler.md).
- For every supplied-image edit with a focal person, creature, product, prop, or other recognition-critical subject, read [references/aesthetic-direction.md](references/aesthetic-direction.md). Also read it when reviewing passive composition, unattractive faces, literal prop copying, weak subject light, dirty colour, or poor painterly finish.
- When light oil-paint dimensionality is requested or an output is being reviewed for mosaic/relief problems, read [references/light-depth-brushwork.md](references/light-depth-brushwork.md).
- For every Generate, Edit Target, Prompt-only, or finished-frame review task, read [references/model-consistency.md](references/model-consistency.md). It defines the portable render contract and the boundary between perceptual consistency and impossible pixel identity.
- For every Generate, Edit Target, Prompt-only, or finished-frame review task, read [references/directorial-contrast.md](references/directorial-contrast.md). This is the macro-departure and contrast-ownership contract.
- For every generation, edit, prompt-only, reference-analysis, or finished-frame review task, read [references/color-authorship.md](references/color-authorship.md). Source-led colour balance and an explicit temperature policy are required; warm-cool contrast is optional and never the default.
- When any image is supplied, also read [references/source-analysis.md](references/source-analysis.md).
- When the environment carries the focal event, no character/object anchor is present, or the user permits expressive scene distortion, also read [references/environment-abstraction.md](references/environment-abstraction.md).
- For multiple directions or a series, read [references/variation-engine.md](references/variation-engine.md).
- After generation/editing, or when reviewing a result, read [references/quality-gate.md](references/quality-gate.md).
- Read [references/research-basis.md](references/research-basis.md) only when the user asks how the system was derived, wants an audit, or supplies new style references to reconcile.

## Source and Reference Boundaries

Assign each supplied image exactly one primary role before prompting: pixel-locked region, edit target, support insert, semantic source, or style reference. Record identity/structure fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, and color-authorship mode separately. Never infer that stronger style means darker exposure, that recognizable identity requires photographic literalness, that an empty environment should remain a conventional realistic landscape, or that this visual family requires a fixed warm-cool/complementary palette.

- Do not promise machine-identical pixels from generative editing. Use deterministic compositing when exact pixels are required, or disclose the limitation.
- Preserve only the declared recognition-critical invariants before style. Nonessential folds, hardware, foliage, texture, atmospheric detail, and repeated props may be merged, exaggerated, or redesigned when the selected transformation mode allows it.
- Separate recognition anchors from design anchors. Preserve identity, action, ownership/contact, semantic object state, essential topology, and signature colour families; actively author crop, focal scale, negative space, silhouette rhythm, facial/object plane grouping, prop pattern rhythm, light envelope, colour-area balance, and final grade.
- For people, preserve the visible identity signature while improving its painted presentation. A recognizable but less coherent, less expressive, or less aesthetically resolved face fails unless deliberate discomfort is requested. Never replace the person with a generic beauty template.
- For salient props, preserve what the object is, who owns it, how it is held/used, its dominant colour, and only the few cues required for recognition. Redesign incidental contour, panels, repeat spacing, folds, highlights, material and overlap; recognizability does not authorize pixel tracing.
- In Style-first/Expressive work, preserve a short anchor set and deliberately transform the remaining scene through one primary macro departure plus one supporting move. The primary move must alter a major area, contour, overlap, focal scale, negative space, light shape, or color-zone relationship at 128–256 px; axis count and surface texture alone do not qualify.
- Treat source fidelity and source distribution separately. Preserve declared identity, count, action, protected geometry, text, and recognition colors; do not automatically preserve documentary headroom, crop, horizon, incidental asset positions, or local contrast distribution.
- Assign contrast ownership across focal, supporting, and context tiers. Non-focal regions may become quieter chromatic-gray fields through lower local contrast, microcontrast, edge density, hue noise, and texture frequency, but must retain broad depth, material, and motivated color.
- Tactile depth may reinforce declared foreground/background, overlap, contact, fold, crest, seam or contour relationships. It must not divide sky, haze, skin, water, snow, walls or other continuous fields into equal raised tiles, repeated knife rectangles or a full-frame height map.
- From style references, learn attention geometry, value topology, color function, material treatment, edge rhythm, and FX behavior. Exclude characters, text, branding, exact props, runes, locations, and camera layouts.
- Treat named-style shorthand as a discovery phrase. Compile it into visible decisions; do not leave a protected work's name as the main style instruction in the final image prompt.
- For supplied images, default to the source's believable white balance and temperature character. A flattering subject light does not authorize an amber skin shift, yellow-green vegetation wash, orange highlights, teal shadows, or any other full-frame warm/cool recipe. Any temperature departure needs a named light, material, spatial owner, and visible purpose.

## Decision Priority

1. User contract, safety, and image-role boundaries
2. Semantic minimum and declared identity/structure invariants
3. Focal identity signature, aesthetic presentation, semantic prop anchors, and authored design anchors
4. Selected transformation/abstraction mode, dramatic proposition, one dominant focal read, and purposeful composition improvement
5. Primary macro departure, supporting move, area/overlap/light/color topology, and viewing path
6. Scene-owned exposure, subject–illumination relationship, layered colour authorship, and restrained final grade
7. Material-specific planes, edge hierarchy, graphic 2D marks/FX, and optional light tactile depth at spatial carriers
8. Optional decoration and variant preferences

## Workflow

1. Inspect every target/reference image with the available image viewer. If a required image is unavailable, ask for it instead of guessing.
2. Build the Source Card from [references/source-analysis.md](references/source-analysis.md); separate `observed` from `inferred`, then choose identity fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, and color-authorship mode independently. When a focal person/object/prop exists, record its recognition anchors, identity or object signature, and separately authored design anchors from [references/aesthetic-direction.md](references/aesthetic-direction.md).
3. Distill recognition anchors from transformable detail. Write the dramatic proposition, purposeful composition improvement, primary macro departure, supporting move, contrast-ownership map, optional color-collision decision, and thumbnail difference target from [references/directorial-contrast.md](references/directorial-contrast.md). For a person, plan connected facial planes and a flattering identity-preserving light relationship; for a salient prop, retain semantic anchors while redesigning silhouette, internal planes, motif rhythm and overlap. Rebuild silhouette, internal planes, and large environment shapes before specifying brush texture. For environment-emphasis, define one hero form, one counterform/current, a macro-shape budget, and source-owned transform decisions from [references/environment-abstraction.md](references/environment-abstraction.md).
4. Audit the source palette and build a role-based color plan from [references/color-authorship.md](references/color-authorship.md). Record the source neutral/white-balance evidence, choose `Source-neutral`, `Preserve source bias`, or `Motivated shift`, then separate local colour, primary illumination, limited environment influence and final grade. Preserve successful source relationships; correct only the area/value/chroma/adjacency problems that weaken the focal path. Select one primary contrast axis and at most one subordinate axis, one composition family, one value plan, one subject-light hierarchy, and a different mark grammar for each important material. When tactile depth is requested, map a small set of relationship-driven depth carriers and explicitly keep broad continuous or distant passages low-relief using [references/light-depth-brushwork.md](references/light-depth-brushwork.md).
5. Compile a short priority-ordered prompt using [references/prompt-compiler.md](references/prompt-compiler.md). Before model-specific wording, write the portable render contract from [references/model-consistency.md](references/model-consistency.md): canvas and recognition/design anchors; macro masses; value and colour-role ownership; source neutral/temperature policy; focal/support/context contrast tiers; identity signature and focal plane map; prop semantic anchors and redesigned construction; subject–illumination relationship; restrained grade; material grammars; edge hierarchy; optional light-depth owners and quiet fields; and anti-filter failure conditions. Explicitly reject photographic underpainting with a global paint filter when the user wants strong stylization.
6. Use the runtime's image generation/editing tool once. Pass target images through the tool's actual reference-image mechanism.
7. Inspect the returned image beside the source at 128–256 px, blurred/thumbnail scale, mid scale, and close scale. Apply [references/quality-gate.md](references/quality-gate.md), the aesthetic gates in [references/aesthetic-direction.md](references/aesthetic-direction.md), and the contract-conformance test in [references/model-consistency.md](references/model-consistency.md). Fail a recognizable but aesthetically degraded face, a salient prop whose incidental construction was traced, a subject without motivated light ownership, an unjustified whole-frame warm/cool drift, or a final grade that makes the palette dirty or uniformly intense. For Style-first/Expressive edits, also fail when the macro/colour-block map remains essentially interchangeable with the source even if close-up brushwork is attractive. When comparing different models, judge whether every output passes the same contract; do not use pixel similarity, seed reuse, or an average score as proof of consistency. Fail all-over raised patchwork, tessellated knife marks, repeated equal-size paint tiles, or relief that competes with the composition and colour.
8. If a specific module fails, make at most one targeted correction. Preserve successful modules and correct only the face, prop, composition, light, colour, grade, material or tactile-depth failure.
9. Return the actual image or path plus a concise fidelity/limitation note. Never claim generation, inspection, or validation that did not occur.

Prompt-only and Reference Analysis routes stop before tool execution and clearly say no image was generated or verified.

## Output Contract

- **Generate/Edit Target:** requested number of finished images; default one. Include the actual result and mention only material preservation limits or an unresolved quality issue.
- **Reference Analysis:** observed evidence, inferred intent, fixed system, variable system, sample residue, and a reusable operational prompt.
- **Prompt-only:** one tool-ready prompt and any required input-role mapping; state that no image was generated or checked.
- **Failure:** identify the failed contract precisely. Do not present a draft or uninspected output as a pass.
