# cat-frame-dominance

Evaluates how much a cat commands the visual space of a photograph by assessing its proportional presence within the frame, positional authority relative to compositional focal points, and visual isolation from competing background elements. Returns a score from 0 to 1 answering: is this picture actually about the cat?

## Purpose

Every cat picture makes an implicit promise: *this image is about the cat.* But not every image delivers. The cat might be a tiny shape on a distant couch, wedged into a corner behind a cluttered countertop, or half-cropped out of existence. **cat-frame-dominance** quantifies how well a photograph fulfills that promise by measuring the degree to which the cat is the undeniable focal point of the image — the thing the eye goes to first and stays on longest.

Frame dominance is not simply about size. A cat photographed from across a room may still dominate the frame if it is centrally positioned against an uncluttered background. Conversely, an extreme close-up that clips half the cat out of frame may feel less dominant because the subject appears incomplete. This function captures the nuanced interplay between scale, placement, and environment that determines whether a cat truly owns its photograph.

## Input

| Field | Type | Description |
|-------|------|-------------|
| input | `image` | A cat picture to evaluate for frame dominance. |

The input is a single photograph containing a cat. The range of valid inputs is broad: professional portraits with shallow depth of field, casual phone snapshots, wide-angle room shots where the cat is one element among many, or tight crops where the cat fills the entire frame. The function evaluates only dominance — the raw visual authority of the cat as a subject — not the beauty of the cat, the technical quality of the photography, or the emotional resonance of the moment.

## Output

A scalar score between **0** and **1**:

- **1.0** — The cat owns the image completely. It is generously scaled, prominently positioned, and set against a clean, cooperative background. There is zero ambiguity about the subject of this photograph.
- **0.5** — The cat is present and recognizable but shares attention with its environment. It may be moderately sized, somewhat off-center, or set against a mildly busy background.
- **0.0** — The cat is barely there. It is tiny, marginal, buried in a corner, or lost in visual clutter. The image does not meaningfully present the cat as its subject.

## What It Evaluates

The function decomposes frame dominance into three fundamental qualities, each assessed by a dedicated sub-function. The final score is a weighted combination of all three.

### 1. Proportional Presence — [cat-visual-presence](https://github.com/ObjectiveAI-claude-code-1/cat-visual-presence)

How much of the frame does the cat physically occupy? This is the most intuitive dimension of dominance. A cat that fills a substantial portion of the image has an undeniable physical claim on the viewer's attention. A cat that occupies a tiny sliver reads as a minor element in a larger scene.

Proportional presence rewards cats that are generously scaled while appearing whole and complete within the frame. It penalizes both extremes: cats that are too small to register as the subject, and cats that overflow the frame edges and feel clipped or fragmented. The ideal is a cat that is big enough to command attention and complete enough to be fully appreciated.

### 2. Positional Authority — [cat-compositional-placement](https://github.com/ObjectiveAI-claude-code-1/cat-compositional-placement)

Where in the frame is the cat located, and does that placement feel commanding? The human eye is naturally drawn to certain areas of an image — the center carries inherent weight, and the rule-of-thirds intersections are natural resting points for the gaze.

Positional authority rewards cats placed at or near these strong focal points, where their presence feels deliberate and intentional. It penalizes cats pushed to the far edges, buried in corners, or crowded against the margins — positions that suggest the cat was caught incidentally rather than framed as the subject.

### 3. Visual Isolation — [cat-background-separation](https://github.com/ObjectiveAI-claude-code-1/cat-background-separation)

How cleanly does the cat stand apart from its surroundings? Even a large, centrally positioned cat can lose dominance if the background is so visually noisy that the eye bounces restlessly between the cat and everything else in the scene.

Visual isolation rewards images where the background acts as a cooperative stage — simple, uncluttered, or softly blurred — allowing the cat to stand as the clear subject. It penalizes busy, chaotic environments full of competing objects, patterns, and textures. This quality measures the signal-to-noise ratio of the image, where the cat is the signal and everything else is noise.

## Use Cases

- **Social media curation** — Surface cat photos where the cat is the clear star, not an incidental background element.
- **Pet adoption platforms** — Flag profile pictures where the cat is too small, too obscured, or too lost in its environment to make a strong impression on potential adopters.
- **Photo library sorting** — Rank thousands of cat pictures by how effectively each one presents the cat as its subject.
- **Content moderation** — Verify that user-submitted cat photos actually feature the cat prominently.
- **Photography feedback** — Provide compositional guidance on whether a cat photo achieves strong subject presentation.

## Philosophy

The three qualities — proportional presence, positional authority, and visual isolation — form a complete framework for what it means for a cat to own its photograph. A dominant cat is one that is generously sized, confidently positioned, and clearly distinguished from a cooperative background. When all three align, the result is an image that leaves no ambiguity about its subject. The cat is not just *in* the picture. The cat *is* the picture.