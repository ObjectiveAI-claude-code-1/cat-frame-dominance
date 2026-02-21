# cat-frame-dominance

Evaluate the frame dominance of a single cat picture. Determine how much the cat commands the physical space of the image, producing a scalar score from 0 to 1 that answers the foundational question: **is this picture actually about the cat?**

## Input

The function accepts a single **image** — a cat picture to evaluate for frame dominance. The image can come from any source, at any resolution: a professional studio portrait, a casual phone snapshot, or anything in between. What matters is not the technical quality of the photograph but the compositional relationship between the cat and the space it inhabits within the frame.

## Output

A **scalar score between 0 and 1**.

- **Near 1** — The cat is the undeniable focal point of the image. It is large, prominently placed, and visually distinct against an uncluttered background. The photograph is unambiguously *about* the cat.
- **Near 0** — The cat is small, obscured, peripheral, competing with clutter, or barely distinguishable from its surroundings. The viewer must search to find it, and the image fails to deliver on the implicit promise that this is a cat picture.

## What It Evaluates

Frame dominance is not a single measurement — it is a composite judgment across three distinct dimensions of visual authority. Each is evaluated by a dedicated sub-function, and the final score is a weighted blend of all three.

### 1. Proportional Occupation

[{{ .Task0 }}](https://github.com/{{ .Owner }}/{{ .Task0 }})

How much of the frame does the cat physically fill? This sub-function measures the cat's spatial footprint relative to the image borders. A cat that occupies a generous portion of the frame commands more visual weight than one that takes up a tiny sliver. However, this is not simply about pixel coverage — a close-up that clips half the cat out of frame may feel less dominant because the subject feels incomplete. The ideal is a cat whose body is substantially and comfortably present, with a scale that feels generous, deliberate, and authoritative.

### 2. Positional Prominence

[{{ .Task1 }}](https://github.com/{{ .Owner }}/{{ .Task1 }})

Where is the cat placed within the frame? This sub-function evaluates the cat's position relative to the center of the image and the natural focal lines where the human eye tends to rest — such as rule-of-thirds intersections. A cat in these zones of visual gravity benefits from how human perception works: the eye arrives at it immediately and without effort. A cat pushed to a far edge or tucked into a corner forces the viewer to search, and that act of searching is the opposite of dominance. Positional prominence is about compositional placement, not size — even a modestly sized cat can score well if it sits at the frame's natural focal point.

### 3. Scene Clarity

[{{ .Task2 }}](https://github.com/{{ .Owner }}/{{ .Task2 }})

Does the surrounding environment cooperate with the cat's dominance? This sub-function shifts attention to everything in the image that is *not* the cat. A clean, simple background acts like silence around a single voice — it lets the cat speak. A busy, cluttered background creates visual noise that competes for the viewer's attention. Scene clarity also considers whether objects partially obstruct the cat, whether patterns or colors camouflage it, or whether the cat blends into its surroundings in a way that makes it visually indistinct. The ideal is an image where the rest of the photograph steps back, quiets down, and lets the cat be the unambiguous star.

## Use Cases

- **Gallery curation** — Surface cat photos where the cat is clearly and prominently featured, ideal for thumbnails and hero images.
- **Photo contest gatekeeping** — Ensure a photograph is genuinely *about* the cat before higher-order aesthetic judgments are applied.
- **Personal library ranking** — Help users find their best cat portraits by scoring which images feature the cat as a true visual centerpiece.
- **Content moderation** — Filter out images where the cat is too small, obscured, or lost in the background to serve as meaningful cat content.
- **Feed optimization** — Prioritize cat images with strong frame dominance for higher engagement in social media feeds and recommendation systems.