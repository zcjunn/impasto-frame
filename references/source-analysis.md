# Source Analysis and Image Roles

Read this whenever an image is supplied.

## Assign Roles Before Style

Give every image one primary role. For edit targets, choose six independent controls: identity/structure fidelity, transformation mode, scene emphasis, abstraction strength, exposure key, and color-authorship mode.

| Role | What may enter the result | Required handling |
|---|---|---|
| Pixel-locked region | Exact original pixels | Keep outside generative redraw; composite and verify deterministically |
| Edit target | Identity/object/scene structure | Use an actual image edit call and state invariants |
| Support insert | Named person, object, texture, or prop | Number inputs and limit each to its declared role |
| Semantic source | Relationship, action, palette role, or mood | Analyze first; original pixels need not appear |
| Style reference | Composition, value, color function, material, edge, FX | Extract grammar; exclude subject, text, brand, and exact layout |

Fidelity:

- **High:** preserve identity, count, proportions, signature features, object geometry, order, and recognizable color anchors.
- **Medium:** preserve the core subject and relationships; allow crop, surface, palette, and surrounding staging changes.
- **Low:** preserve only semantic relationships or visual grammar.

Transformation mode:

- **Identity-first:** preserve recognizable face/body/object geometry closely; redesign color, light, edges, and surfaces. Use when exact likeness or product/architecture recognition dominates.
- **Balanced:** preserve signature identity, count, pose, and structural relationships; allow controlled crop, planar facial stylization, silhouette cleanup, merged detail, and environment reshaping.
- **Style-first:** preserve the semantic minimum and recognizable anchors; deliberately reconstruct proportions, contours, planes, materials, and nonessential layout. Use when the user prioritizes a stronger painterly-animation result and permits departure from 1:1 realism.

Scene emphasis:

- **Character/Object:** an inspectable face, pose, creature, product, prop, or mechanism carries the focal event.
- **Environment:** landform, architecture, spatial void, weather, light, or directional flow carries the focal event.
- **Relationship:** subject and environment depend on each other; neither may be treated as a passive backdrop.

Abstraction strength:

- **Restrained:** preserve spatial distribution and recognizable geometry; simplify surfaces, repeated detail, light, and color grouping.
- **Expressive:** preserve a short anchor set while making one thumbnail-visible primary macro departure plus one supporting move. The primary move must change a major area, contour, overlap, focal scale, negative space, light shape, perspective/depth interval, or color-zone relationship; minor movement on several axes does not qualify.
- **Radical:** preserve only the semantic minimum and a few anchors; make at least two primary-level departures and permit major restaging, subjective graphic rupture, or strong area redistribution. Use only with clear user authorization.

Do not infer abstraction from exposure. For a Style-first environment with no protected geometry, default to Expressive rather than conventional scenic realism. For identity-first or protected architecture/product geometry, default to Restrained unless the user explicitly permits more.

Exposure key:

- **High-key:** broad light field with a dark/chromatic anchor.
- **Mid-key:** balanced light and shadow groups with one controlled apex.
- **Low-key:** dominant dark field with separated shadow structure and a limited light event.

Infer exposure from the source and story. Do not default to low-key because the request mentions this style family.

Color-authorship mode:

- **Preserve-and-refine:** keep source hue families and protected anchors; improve balance and hierarchy.
- **Rebalance:** keep the source's main color identity while changing area, value, saturation, adjacency, or spatial ownership.
- **Re-script:** assign new hue families and color roles while preserving declared anchors; use only when the source is not serving the intended frame and the transformation allows it.

Choose after the color audit in `color-authorship.md`. Do not infer Re-script from Style-first, or warm-cool contrast from any mode.

Temperature policy:

- **Source-neutral:** derive a believable neutral axis from reliable source materials and do not impose a new cast.
- **Preserve source bias:** retain a source-owned cool, warm, green, violet, dusk, night, snow, underwater, or mixed-light character.
- **Motivated shift:** change temperature only through a named light, atmosphere, material adjacency, spatial zone, or narrative transition with an explicit boundary.

For supplied images, default to Source-neutral or Preserve source bias. Do not infer a warm grade from portrait beauty, painterly style, subject illumination, or the word “cinematic.”

## Build a Source Card

Record compactly:

```yaml
file_facts:
  size: observed dimensions if available
  ratio: observed aspect ratio
  orientation: landscape / portrait / square
  quality_limits: blur, crop, occlusion, compression
image_role: one primary role
identity_fidelity: High / Medium / Low
transformation_mode: Identity-first / Balanced / Style-first
scene_emphasis: Character/Object / Environment / Relationship
abstraction_strength: Restrained / Expressive / Radical
exposure_key: High-key / Mid-key / Low-key
color_authorship_mode: Preserve-and-refine / Rebalance / Re-script
temperature_policy: Source-neutral / Preserve source bias / Motivated shift
distribution_policy: Preserve protected layout / Selectively restage / Major restage
observed:
  core_subjects: 1-2 identity-defining subjects
  supporting_facts: 2-4 scene facts
  identity_invariants: face, body, product, architecture, markings, wardrobe color
  focal_identity_signature: visible head/jaw, eyes/brows, nose-mouth-chin, expression, hair silhouette, object geometry, species traits, or other recognition relationships
  salient_prop_semantics: category, owner/contact, functional state, dominant colour, and only the motif/geometry cues necessary for recognition
  spatial_invariants: only declared count, left-right order, gesture, gaze, horizon, overlap, or scale relationships that must remain
  dominant_gesture: horizontal / vertical / diagonal / curve / gaze / motion
  current_visual_weight: area, value, chroma, texture, isolation
  color_audit:
    value_groups: large light/mid/dark ownership independent of hue
    hue_families: dominant, secondary, neutrals
    reliable_neutral_evidence: source whites, grays, snow, cloud, concrete, metal, fabric, or other known local colour; note clipping and coloured light
    temperature_map: spatial warm/cool distribution without assuming opposition
    saturation_map: muted, concentrated, clipped, or competing regions
    source_saturation_baseline: broad relationship between quiet, dominant, support, and peak-chroma regions
    spatial_material_ownership: subject, foreground, background, atmosphere, important materials
    protected_color_anchors: identity, wardrobe, product, brand, species, architecture, text
    light_shadow_reflection: source color, shadow color, reflected color, atmospheric shift
    strengths: relationships already supporting the frame
    problems: adjacency, hierarchy, material, depth, or balance issues actually needing correction
    contrast_audit: global span, local contrast, microcontrast, edge density, chroma, hue noise, texture/FX density and their current owners
  quiet_areas: low-information regions
  visible_text_brand: preserve exactly or exclude
inferred:
  narrative_event: what appears to be happening
  emotional_tension: restrained inference, not fact
semantic_minimum: facts required for recognition
recognition_anchors: identity, count, pose, signature silhouette, spatial relationship, color anchors
design_anchors:
  composition_authorship: crop, focal scale, headroom, negative space, overlap pressure, viewing path, and intended improvement
  focal_aesthetic_plan: identity-preserving face/object planes, expression treatment, silhouette cleanup, and protected asymmetries
  prop_reconstruction: silhouette rhythm, internal planes, motif grouping, material response, and overlap to redesign rather than trace
  subject_illumination: key direction, revealed planes, shadow-side separation, optional bounce, supportive background field, and focal accents
  grading_policy: successful source relationships to retain, relationships to rebalance, and limits on final grade
transformable_elements: any user-authorized crop, minor proportions, surface construction, repeated detail, secondary props, ornament, texture, or atmosphere
directorial_transform_proposal:
  dramatic_proposition: actor + visible pressure/counterforce + intended first read
  primary_macro_departure: one scale/area/crop/occlusion/perspective/negative-space/light/color-zone/subjective-graphic change
  supporting_move: one secondary visible change
  area_contour_impact: which major mass, silhouette, overlap, light shape, or color-zone relationship changes
  protected_invariants: what this proposal may not alter
  incidental_distribution_not_preserved: headroom, exact crop/horizon, repeated assets, secondary detail, or local contrast when allowed
contrast_ownership:
  tier_1_focal: owner plus selected peak value/edge/chroma/hue-boundary/texture/FX dimensions
  tier_2_support: structural owner plus medium cues retained for depth and relation
  tier_3_context: scene-owned chromatic-gray/colored field and dimensions compressed without losing depth/material
color_collision_decision:
  mode: None / Preserve existing / Author new
  owners_and_adjacency: who meets where
  dominance_and_function: which side owns area and why the collision exists
thumbnail_difference_target: one major mass/area/contour/overlap/focal-scale/light-topology/color-zone difference visible at 128–256 px
color_plan:
  temperature_policy:
    mode: Source-neutral / Preserve source bias / Motivated shift
    evidence: reliable source neutral, source cast, light, atmosphere, material, or narrative owner
    owned_shift_and_boundary: named owner, reachable region, direction, area dominance, and stopping point
    protected_neutrals: whites, grays, skin, snow, cloud, cloth, metal, or other local-colour anchors that may not receive a global cast
  primary_contrast: value / analogous / complementary / split-complementary / warm-cool / saturation / hue-boundary / near-monochrome rupture / local-color versus illumination
  subordinate_contrast: optional; do not maximize every axis
  dominant_field: spatial owner, hue family, value, chroma
  structural_counter: spatial/material owner and separation job
  focal_accent_apex: owner and attention job
  connector_echo: optional quiet recurrence
  neutral_bridge: low-chroma family preventing equal competition
  protected_anchors: colors that must remain recognizable
  chroma_budget: which owner is dominant, which owns peak chroma, which support/context regions stay quieter, and how this relates to the source baseline
  layered_colour:
    local_colour: source-informed material and identity families
    primary_illumination: motivated source, direction, colour influence, and affected planes
    environment_influence: limited reflected colour, bounce, atmosphere, and adjacency effects
    final_grade: restrained unifying shift that cannot overwrite source temperature policy, protected neutrals, local colour, material separation, or focal ownership
environment_design:
  hero_form: primary landform, structure, void, weather mass, or light shape
  counterform_current: opposing or guiding source-owned mass/direction
  visual_verb: presses / splits / climbs / funnels / opens / resists / another visible relation
  macro_shape_budget: usually 5-9 interlocking masses
  primary_macro_departure: one source-owned transformation that changes the composition decision
  supporting_move: a second move that reinforces the hero/counterforce relationship
  optional_additional_axes: only changes that remain visibly useful; axis count alone is not success
  repeated_detail_policy: which trees, rocks, windows, waves, foliage, rubble, or reflections become grouped rhythms
shape_rebuild:
  subject_planes: silhouette and 4-7 meaningful face/object planes
  environment_masses: broad graphic forms replacing repeated detail
  material_grammars: distinct marks for 3-5 important materials
light_depth_policy:
  depth_carriers: optional overlaps, contacts, form turns, directional crests or foreground separators that benefit from mild body
  quiet_fields: continuous, distant or identity-critical passages that stay broad and low-relief
  surface_response: optional narrow subordinate ridge catches; never global shine or colour replacement
allowed_changes: user-authorized changes
hard_avoids: identity drift, added objects, sample residue, text errors
```

Do not invent unseen facial features, object backs, hidden text, location, date, or story as observed fact.

## Translate the Source

1. Keep the semantic minimum and recognition anchors; do not automatically preserve every visible detail.
2. Read `aesthetic-direction.md` when a recognition-critical person, object, or prop exists. Separate preserved recognition anchors from authored design anchors. For a face, retain its visible identity signature while improving connected planes, expression edges, head/neck attachment, and light; for a salient prop, preserve semantics and essential motifs while redesigning incidental panels, repeat rhythm, folds, highlights, and contour accidents.
3. Apply the chosen transformation mode. In Balanced or Style-first work, simplify or redesign transformable elements instead of tracing them literally.
4. Rebuild the focal silhouette, internal planes, and major surrounding masses before adding brush marks. Apply the same logic to people, creatures, products, buildings, machines, and environments.
5. Read `directorial-contrast.md`. For Expressive/Radical work, require a dramatic proposition, one primary macro departure, one supporting move, and a thumbnail difference target. Fidelity protects declared recognition anchors; it does not silently preserve every area ratio, crop, horizon, or incidental distribution. State why the chosen crop, focal scale, negative space, overlap or viewing path improves the finished image.
6. For environment-emphasis, read `environment-abstraction.md`. Select a hero form, a counterform/current, and a visible verb. Make the primary departure change their scale, area, contour, overlap, negative-space, light-shape, perspective, or color-zone relationship rather than merely changing palette and brush texture.
7. Merge repeated micro-detail into larger shapes and assign each important material a distinct mark grammar derived from its behavior. Exact distributions of incidental trees, rocks, windows, waves, leaves, snow clumps, rubble, and reflections are not invariants unless declared.
8. Choose one focal event and one composition family from `style-system.md`; restage or crop only when permitted.
9. Assign focal/support/context contrast tiers. Lower context local contrast, microcontrast, edge density, hue noise, and texture frequency selectively; retain broad depth, material identity, motivated colour, and any protected subject geometry.
10. Read `color-authorship.md`. Audit what already works, choose Preserve-and-refine, Rebalance, or Re-script, and independently choose Source-neutral, Preserve source bias, or Motivated shift. Record reliable neutral evidence, source saturation baseline, protected neutrals/local colours, named temperature owners and boundaries, then assign one primary contrast axis, an optional subordinate axis, spatially owned color roles, and an explicit None/Preserve/Author color-collision decision. Separate local colour, primary illumination, environment influence and final grade. Keep source-derived color anchors when recognition depends on them; never add warm-cool, complementary contrast, a beauty-warm grade, or global saturation by reflex.
11. If light tactile depth is requested, read `light-depth-brushwork.md`. Name only the relationships that benefit from mild body and the continuous/distant/identity-critical fields that must remain low-relief. Do not use surface height to construct the whole image.
12. Change only what the user allowed.

For Edit Target, write prompt clauses as `Preserve anchors Y; reconstruct elements X`. Do not imply that “stylize” grants permission to change identity, count, protected geometry, or required text, but do not promote incidental photographic detail to an invariant either.

## Analyze Style References

For each reference, record:

- observed value groups and focal location;
- color roles and high-chroma area;
- light-source geometry;
- composition family and viewing path;
- material/edge/brush behavior;
- FX shape language;
- text, character, object, location, brand, and exact-layout residue.

Then separate:

- **Fixed:** repeats across multiple references and is necessary for family recognition.
- **Variable:** changes while the family remains recognizable.
- **Sample residue:** belongs to a particular frame and must not be generalized.

With one reference, label confidence as low and avoid claiming statistical rules. With multiple references, do not promote a feature merely because two frames from the same sequence share it.

## Multi-image Requests

Number inputs and state the interaction:

```text
Image 1 — High-fidelity edit target: preserve person A and clothing colors.
Image 2 — Support insert: use only the mechanical object; adapt its lighting.
Image 3 — Style reference: learn value topology and edge rhythm; copy no subject or text.
```

If two images compete to define identity, geometry, or output ratio and the user has not resolved the conflict, ask one necessary question.
