# cat-frame-dominance

Evaluates the frame dominance of a single cat picture — a measure of how completely the cat commands the physical space of the image. This function answers one foundational question: **is this picture actually about the cat?**

A cat may be technically present in a photograph and yet not be what the photograph is *about*. A small tabby on a distant windowsill, a calico half-hidden behind a stack of books — these are images that contain cats, but the cats do not own them. Frame dominance measures the degree to which a cat has risen above incidental status and claimed the image as its own, such that the viewer's eye goes to it first, stays on it longest, and finds no serious competition for attention.

## Input

The function accepts a single **image** — a cat picture to evaluate for frame dominance.

## Output

A **scalar score between 0 and 1**.

| Score Range | Interpretation |
|---|---|
| **0.8 – 1.0** | The cat is the undeniable focal point. It fills the frame with visual authority, sits prominently within the composition, and stands against a background that does nothing to challenge its primacy. |
| **0.5 – 0.8** | The cat is clearly the subject but with some compromise — moderate size, slightly off-center positioning, or mild background competition. |
| **0.2 – 0.5** | The cat is present but not dominant. It may be small, partially obscured, competing with clutter, or positioned at the margins. |
| **0.0 – 0.2** | The cat is marginal — tiny within a vast scene, heavily obscured, lost in clutter, or barely distinguishable from its surroundings. |

## What It Evaluates

Frame dominance is not a single, monolithic property. It emerges from the interplay of three distinct qualities, each evaluated by a dedicated sub-function:

### 1. Proportional Presence — [cat-visual-fill](https://github.com/ObjectiveAI-claude-code-1/cat-visual-fill)

How much of the frame the cat physically occupies relative to the total space available. A cat whose body fills a generous portion of the photograph carries inherent visual weight that is difficult to ignore. However, proportional presence is not simply about maximizing size. A close-up that crops the cat so aggressively that it clips away ears, paws, or half the body may technically fill the frame yet leave the viewer feeling the subject is incomplete. The ideal is a cat that appears both large *and* complete — generously sized within the boundaries of the image while still feeling fully contained.

### 2. Positional Authority — [cat-compositional-gravity](https://github.com/ObjectiveAI-claude-code-1/cat-compositional-gravity)

Where the cat sits relative to the natural focal points of the image — the center, the rule-of-thirds intersections, and the overall visual stage of the composition. A cat positioned at or near these points of natural visual gravity benefits from the geometry of human attention. A cat pushed to the far edges or corners of the frame, no matter how large, can feel like it is about to exit the scene rather than commanding it. A cat in the heart of the image radiates intentionality and ownership.

### 3. Visual Clarity — [cat-focal-clarity](https://github.com/ObjectiveAI-claude-code-1/cat-focal-clarity)

How cleanly the cat separates from its surroundings as the unambiguous subject. A cat photographed against a simple, uncluttered background benefits from having nothing else that pulls the viewer's eye away. A cat surrounded by clutter, busy patterns, or competing objects loses authority as the viewer's attention fragments. Visual clarity also encompasses how distinguishable the cat is from its background — a cat that blends into its surroundings through similar color, low contrast, or camouflage is harder to perceive as a distinct subject, even if it is large and well-positioned.

## Key Principles

- **Frame dominance is not simply about size.** A cat photographed from across a room may still dominate the frame if it is centrally positioned against an uncluttered background.
- **Completeness matters.** A close-up that clips half the cat out of frame may feel less dominant because the subject appears incomplete.
- **All three qualities must converge.** A cat that is large but shoved into a corner lacks positional authority. A cat that is centered but tiny lacks proportional presence. A cat that is large and centered but lost in visual clutter lacks clarity. True frame dominance requires all three.

## Use Cases

- **Content curation** — Surface cat images where the cat is truly the star, filtering out those where it plays a bit part in someone else's scene.
- **Content moderation** — Enforce a measurable threshold ensuring that images labeled as "cat pictures" actually deliver a cat-forward experience.
- **Compositional feedback** — Provide photographers with a signal indicating whether their intended subject is getting lost in the noise of its surroundings.
- **Visual attention research** — Quantify subject prominence in a structured, repeatable way across large datasets of cat imagery.