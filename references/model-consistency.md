# Model Consistency Contract

Use this reference to keep the art direction recognizable across different image models. The target is **perceptual and directorial consistency**, not identical pixels. Different model families, versions, seeds, and inference systems will vary in brush placement, transformable small contours and texture; visible human geometry is not part of that allowed residue. Do not promise exact pixel reproduction across models.

## Consistency Boundary

Lock the decisions that define the visual system. Allow the model to vary only the residue that does not change those decisions.

### Required invariants

1. **Semantic and topology contract** — output count, ratio/orientation, subject identity/count/action, protected objects and colours, depth order, adjacency, and any declared camera or landmark relationship.
2. **Human preservation and recognition/design-anchor contract** — for every visible human Edit Target, lock facial landmarks/ratios, gaze/expression, head-neck attachment, body proportions, exact pose, limbs/joints, hands, feet, clothing silhouette and contacts. Separately lock the authored crop, uniform whole-person scale, negative space, surrounding overlap, prop reconstruction, subject-light relationship and grading limits. For non-human subjects, lock identity/object signatures, action, ownership/contact, semantic state, essential motifs and protected topology. Do not lock incidental pattern repeats or photographic accidents.
3. **Macro-mass contract** — name roughly five to nine interlocking masses and their area, contour, overlap, direction, or negative-space relationship. For expressive edits, state the primary macro departure, its aesthetic payoff and supporting move that must remain visible at 128–256 px.
4. **Value and layered-colour contract** — define three large value groups plus spatial owners for dominant field, structural counter, focal apex, and neutral bridge or connector. Lock local-colour families, primary illumination, limited environment influence, protected colours and final-grade limits—not exact RGB values.
5. **Contrast-ownership contract** — explicitly assign Tier 1/Tier 2/Tier 3 relationships for local contrast, microcontrast, edge density, chroma, hue noise and texture frequency; state which focal dimensions peak, which support cues remain, and which context dimensions are compressed without losing spatial/material information.
6. **Focal aesthetic and integration contract** — for a human Edit Target, keep the locked face/body geometry while defining connected light/paint planes, edge hierarchy and flattering motivated light inside it; require the same light field, color logic, abstraction family, edge hierarchy, material world, contact treatment and final grade across person and environment. For a salient prop, lock semantics and essential motif while requiring redesigned silhouette, panels, repeat grouping, material and overlap.
7. **Shape and plane contract** — require rebuilt silhouettes and grouped internal planes before texture. Give the focal face/object a small set of meaningful connected planes when appropriate; merge repeated foliage, windows, waves, folds, motifs or debris into broad rhythm groups.
8. **Material and edge contract** — for every important material, specify plane scale, mark direction, edge family, reflectance, and focal density. When three or more important materials are visible, at least three must have clearly different grammars. Assign hardest, medium, and soft/lost edge owners.
9. **Anti-filter, anti-trace, anti-grade, and anti-paste contract** — reject photographic shading beneath global texture; salient-prop incidentals that align as a copy; any human geometry/pose/contact drift; a geometrically preserved person that looks pasted, photographically rendered, differently lit or differently graded from the environment; local colour overwritten by illumination; and LUT/saturation doing the work of composition or light. The source/result difference must survive thumbnail inspection and human/material differences must survive close inspection.
10. **Optional light-depth contract** — only when tactile paint depth is requested, lock the spatial relationships that receive mild body and the continuous/distant fields that remain low-relief. Do not lock exact ridge placement or numerical height, and reject full-frame relief, repeated equal-size knife patches and mosaic tessellation.

### Allowed variation

- exact brush-stamp shape and placement;
- minor microtexture and broken contour placement;
- small secondary folds, leaves, stones, windows, droplets, or cloud fragments;
- subtle hue shifts that keep the same colour owner and dominance hierarchy;
- paint-edge and light-plane nuance inside locked human geometry, expression and pose;
- motif count and repeat placement inside a redesigned salient prop, provided the motif family and object identity remain clear;
- runtime-specific wording or parameters outside the portable core;
- exact mild ridge shape and position inside an approved depth carrier, provided it does not spread into a continuous quiet field.

Allowed variation becomes a failure when it changes human facial/body geometry, pose, limbs, hands, feet, clothing silhouette or contacts; changes the first read; breaks another recognition anchor; redistributes the required major masses; swaps colour roles; equalizes focal and background contrast; makes the person stylistically separate from the environment; or makes important materials share one surface treatment.

## Portable Render Contract

Before writing the final generation prompt, record this compact contract:

```text
Canvas/anchors: [count, ratio, identity, topology, protected colours]
Recognition/design anchors: [identity/object signature; semantic prop anchors; authored composition, focal aesthetic, prop redesign, subject light, grade limits]
Human lock/integration: [face/body/pose/limbs/hands/feet/clothing/contacts remain fixed; shared light/color/edge/plane/material/contact/grade system]
Macro map: [5–9 masses, primary departure, aesthetic payoff, supporting move, thumbnail target]
Value map: [dominant/support/apex]
Colour roles and layers: [dominant field / structural counter / focal apex / neutral bridge; local colour / primary illumination / environment influence / restrained grade]
Contrast tiers: [local contrast T1/T2/T3; microcontrast T1/T2/T3; edge density T1/T2/T3; chroma T1/T2/T3; hue noise T1/T2/T3; texture frequency T1/T2/T3]
Focal aesthetic/prop map: [identity-preserving connected planes and light; prop semantics versus redesigned silhouette/panels/motif rhythm]
Plane map: [silhouette and focal planes; repeated detail groups]
Material grammar: [material -> plane scale, direction, edge, reflectance]
Edge hierarchy: [hard / medium / soft-lost owners]
Optional light depth: [named overlap/turn/contact/foreground carriers; continuous and distant low-relief fields]
Anti-filter/trace/grade/paste gate: [thumbnail, mid-scale, close-scale failures, including human geometry drift, pasted-person separation, literal prop copying, dirty global grade, mosaic or all-over relief]
```

The final prompt may be shorter, but it must express every populated line as an observable visual decision. Use spatial owners and verbs: “the umbrella owns peak chroma,” “the forest becomes two broad wedges,” “skin uses quiet medium planes while metal uses sparse crisp streaks.” Do not depend on vague tags such as “high quality,” “masterpiece,” “more painterly,” or “same style.”

## Cross-model Evaluation

When actual multi-model comparison is requested:

1. Use the same source image, Source Card, portable render contract, output count, and aspect ratio for every model.
2. Keep required decisions identical; translate only the minimum syntax needed by each runtime.
3. Inspect every output at thumbnail, mid, and close scale with [quality-gate.md](quality-gate.md).
4. Mark each required invariant pass/fail. Do not average away a failure and do not select consistency by visual similarity alone.
5. A model set is consistent only when every output preserves the contract. Any model that changes human geometry or separates person and environment stylistically fails regardless of how attractive its background is. Report remaining variation as brush residue, micro-detail variance, colour-role drift, human-geometry drift, integration drift, or another specific module.
6. If one model fails, make at most one correction targeted to the failed module. If it still fails, report that model as outside the supported consistency envelope.

## What Cannot Be Guaranteed

The skill cannot guarantee identical pixels, brush stamps, or random detail across different models. It does require each model to preserve the source-visible human geometry within inspection tolerance; if the runtime cannot do so after one targeted correction, that output is outside the supported envelope and must not be called a pass. Seeds are not portable evidence. Consistency comes from shared visual invariants plus identical acceptance gates. For machine-identical regions, use deterministic compositing or another non-generative workflow.
