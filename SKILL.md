---
name: cubist-image
description: Transform photos or text prompts into original, strongly deconstructed Cubist artwork with fractured geometry, multiple viewpoints, displaced facial features, collage color blocks, and expressive paint texture. Use when the user asks for 毕加索风格, 立体主义, Cubist portraits, geometric face deconstruction, avant-garde collage, or a strongly abstract reinterpretation of people, architecture, objects, or landscapes.
---

# Cubist Image

Create original Cubist reinterpretations with the built-in image generation tool. Default to strong deconstruction rather than a mild filter.

## Workflow

1. Inspect every edit target with `view_image` before generating.
2. Treat an uploaded photo as an edit target. Treat a text-only request as a new generation.
3. Read `references/presets.md` and select one preset. Default to `fractured-primary` when the user only says “毕加索风格”.
4. Use the built-in image generation tool. Do not use local pixel filters or the image-generation CLI for normal requests.
5. Generate one output per requested image or variant. For batches, issue one built-in call per source image.
6. Inspect the result for the requested subject, deconstruction strength, composition, unwanted text, and accidental extra figures. Iterate with one targeted correction if necessary.
7. Save project-bound finals into the workspace without overwriting source images. Report the final paths and the preset used.

## Default transformation contract

- Strongly reconstruct the image as an original early-20th-century Cubist painting.
- Use multiple simultaneous viewpoints, asymmetrical geometry, displaced facial features, interlocking planes, bold contours, flattened depth, and tactile oil-paint or paper-collage texture.
- Preserve the number of main subjects, the dominant pose or silhouette, the main scene category, and one or two identifying scene anchors.
- Do not preserve exact facial geometry, photographic realism, small text, logos, or architectural details; strong deconstruction intentionally changes them.
- Do not reproduce, trace, or closely imitate any specific existing artwork. Create a new composition.
- Add no captions, signatures, watermarks, frames, or logos unless the user supplies exact text.

## Prompt scaffold

Use this structure and adapt only the relevant fields:

```text
Use case: style-transfer
Asset type: original Cubist artwork derived from the input photo
Primary request: transform the edit target into a strongly deconstructed Picasso-inspired Cubist image
Input image: edit target; retain subject count, dominant pose/silhouette, framing, and major scene anchors
Style/medium: original Cubist painting; multiple viewpoints; fractured interlocking planes; displaced features; bold contour drawing; tactile oil paint and cut-paper texture
Composition: keep the source orientation and broad subject placement, but aggressively reconstruct internal geometry
Color palette: <selected preset palette>
Constraints: strong deconstruction; original composition; preserve no photographic realism; no extra people or objects
Avoid: exact reproduction of an existing painting, photorealism, readable source text, logos, signatures, captions, watermark
```

For portraits, explicitly request a split-profile/front-facing face, non-aligned eyes, and a nose seen from a second viewpoint. For architecture, request skewed perspective, overlapping elevations, and faceted structural rhythm. For landscapes, request compressed depth and interlocking spatial planes.

## Strength control

- `strong` (default): recognizable subject category and silhouette, heavily reconstructed internal forms.
- `extreme`: prioritize abstraction and visual impact; identity and structural accuracy may be lost.
- `moderate`: use only when the user explicitly asks for greater recognizability.

Read `references/presets.md` for palette and subject-specific prompt additions.
