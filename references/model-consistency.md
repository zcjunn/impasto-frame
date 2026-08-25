# Model Consistency Contract

Use this reference to keep the art direction recognizable across different image models. The target is **perceptual and directorial consistency**, not identical pixels. Different model families, versions, seeds, and inference systems will vary in brush placement, small contours, texture, and facial nuance; do not promise exact reproduction across them.

## Consistency Boundary

Lock the decisions that define the visual system. Allow the model to vary only the residue that does not change those decisions.

### Required invariants

1. **Semantic and topology contract** — output count, ratio/orientation, subject identity/count/action, protected objects and colours, depth order, adjacency, and any declared camera or landmark relationship.
2. **Recognition and design-anchor contract** — lock identity/object signatures, action, ownership/contact, semantic prop state, essential motifs and protected topology; separately lock the authored crop, focal scale, negative space, overlap, focal silhouette/planes, prop reconstruction, subject-light relationship and grading limits. Do not lock incidental pattern repeats or photographic accidents.
3. **Macro-mass contract** — name roughly five to nine interlocking masses and their area, contour, overlap, direction, or negative-space relationship. For expressive edits, state the primary macro departure, its aesthetic payoff and supporting move that must remain visible at 128–256 px.
4. **Value and layered-colour contract** — define three large value groups plus spatial owners for dominant field, structural counter, focal apex, and neutral bridge or connector. Lock local-colour families, primary illumination, limited environment influence, protected colours and final-grade limits—not exact RGB values.
5. **Contrast-ownership contract** — state which two or three contrast dimensions belong to the focal tier, which structural cues remain in the support tier, and which local-contrast, microcontrast, edge-density, hue-noise, or texture-frequency dimensions are reduced in context.
6. **Focal aesthetic contract** — for a face, lock visible identity ratios, gaze/expression, important asymmetries, connected plane/edge hierarchy and flattering motivated light; for a salient prop, lock semantics and essential motif while requiring redesigned silhouette, panels, repeat grouping, material and overlap.
7. **Shape and plane contract** — require rebuilt silhouettes and grouped internal planes before texture. Give the focal face/object a small set of meaningful connected planes when appropriate; merge repeated foliage, windows, waves, folds, motifs or debris into broad rhythm groups.
8. **Material and edge contract** — for every important material, specify plane scale, mark direction, edge family, reflectance, and focal density. When three or more important materials are visible, at least three must have clearly different grammars. Assign hardest, medium, and soft/lost edge owners.
9. **Anti-filter, anti-trace, and anti-grade contract** — reject photographic shading beneath global texture; salient-prop incidentals that align as a copy; a recognizable but aesthetically degraded focal face; local colour overwritten by illumination; and LUT/saturation doing the work of composition or light. The source/result difference must survive thumbnail inspection and material differences must survive close inspection.
10. **Optional light-depth contract** — only when tactile paint depth is requested, lock the spatial relationships that receive mild body and the continuous/distant fields that remain low-relief. Do not lock exact ridge placement or numerical height, and reject full-frame relief, repeated equal-size knife patches and mosaic tessellation.

### Allowed variation

- exact brush-stamp shape and placement;
- minor microtexture and broken contour placement;
- small secondary folds, leaves, stones, windows, droplets, or cloud fragments;
- subtle hue shifts that keep the same colour owner and dominance hierarchy;
- facial nuance that preserves identity, expression, pose, aesthetic coherence, and plane/light hierarchy;
- motif count and repeat placement inside a redesigned salient prop, provided the motif family and object identity remain clear;
- runtime-specific wording or parameters outside the portable core;
- exact mild ridge shape and position inside an approved depth carrier, provided it does not spread into a continuous quiet field.

Allowed variation becomes a failure when it changes the first read, breaks a recognition anchor, redistributes the major masses, swaps colour roles, equalizes focal and background contrast, or makes important materials share one surface treatment.

## Portable Render Contract

Before writing the final generation prompt, record this compact contract:

```text
Canvas/anchors: [count, ratio, identity, topology, protected colours]
Recognition/design anchors: [identity/object signature; semantic prop anchors; authored composition, focal aesthetic, prop redesign, subject light, grade limits]
Macro map: [5–9 masses, primary departure, aesthetic payoff, supporting move, thumbnail target]
Value map: [dominant/support/apex]
Colour roles and layers: [dominant field / structural counter / focal apex / neutral bridge; local colour / primary illumination / environment influence / restrained grade]
Contrast tiers: [focal / support / context]
Focal aesthetic/prop map: [identity-preserving connected planes and light; prop semantics versus redesigned silhouette/panels/motif rhythm]
Plane map: [silhouette and focal planes; repeated detail groups]
Material grammar: [material -> plane scale, direction, edge, reflectance]
Edge hierarchy: [hard / medium / soft-lost owners]
Optional light depth: [named overlap/turn/contact/foreground carriers; continuous and distant low-relief fields]
Anti-filter/trace/grade gate: [thumbnail, mid-scale, close-scale failures, including unattractive face, literal prop copying, dirty global grade, mosaic or all-over relief]
```

The final prompt may be shorter, but it must express every populated line as an observable visual decision. Use spatial owners and verbs: “the umbrella owns peak chroma,” “the forest becomes two broad wedges,” “skin uses quiet medium planes while metal uses sparse crisp streaks.” Do not depend on vague tags such as “high quality,” “masterpiece,” “more painterly,” or “same style.”

## Cross-model Evaluation

When actual multi-model comparison is requested:

1. Use the same source image, Source Card, portable render contract, output count, and aspect ratio for every model.
2. Keep required decisions identical; translate only the minimum syntax needed by each runtime.
3. Inspect every output at thumbnail, mid, and close scale with [quality-gate.md](quality-gate.md).
4. Mark each required invariant pass/fail. Do not average away a failure and do not select consistency by visual similarity alone.
5. A model set is consistent only when every output preserves the contract. Report remaining variation as brush residue, micro-detail variance, colour-role drift, geometry drift, or another specific module.
6. If one model fails, make at most one correction targeted to the failed module. If it still fails, report that model as outside the supported consistency envelope.

## What Cannot Be Guaranteed

The skill cannot guarantee identical pixels, facial microgeometry, brush stamps, or random detail across different models. Seeds are not portable evidence: identical seed values can map to unrelated latent processes. Consistency comes from shared visual invariants plus identical acceptance gates. For machine-identical regions, use deterministic compositing or another non-generative workflow.
