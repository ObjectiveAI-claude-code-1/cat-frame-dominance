# cat-frame-dominance

Evaluates how thoroughly a cat dominates the frame of a single photograph, returning a scalar score between 0 and 1 that measures the cat's visual sovereignty over the image. This function answers the foundational question every cat picture must face: **is this picture actually about the cat?**

A score near **1** means the cat is the undeniable ruler of the frame — large, prominently placed, and standing apart from a clean background. A score near **0** means the cat is lost — small, marginalized, or buried in visual clutter.

## Input

The function accepts a single **image** — a cat picture to evaluate for frame dominance.

The universe of valid inputs is broad: professional studio portraits, hasty smartphone snapshots, distant landscapes where a cat appears on a fence post, or chaotic living room scenes where a cat is curled up among pillows and books. The function evaluates all of them with consistency, measuring not the cat in isolation but the relationship between the cat and everything else in the composition.

## Output

A **scalar number between 0 and 1**, where:

- **1.0** — The cat completely dominates the frame. It fills the image, commands a powerful position, and the background offers no competing distractions.
- **0.75** — The cat is clearly the subject. It is prominent in size, well-positioned, and reasonably isolated, though minor imperfections exist.
- **0.5** — The cat is present but does not fully command the frame. It may be moderately sized, slightly off-center, or competing with some background clutter.
- **0.25** — The cat struggles to hold attention. It is small, poorly positioned, or lost in a busy environment.
- **0.0** — The cat is virtually invisible — a tiny speck in a vast scene, pushed to the extreme margins, or completely overwhelmed by its surroundings.

## What It Evaluates

Frame dominance is not a single property. It emerges from the interplay of **three distinct qualities**, each evaluated independently by a dedicated sub-function and then synthesized into the final score.

### 1. Proportional Presence — [cat-wholeness-coverage](https://github.com/ObjectiveAI-claude-code-1/cat-wholeness-coverage)

How much of the image's total area the cat occupies, and whether that occupation feels **substantial and complete**. A cat filling most of the frame scores highly; a cat reduced to a tiny speck scores low. Crucially, this quality accounts for wholeness — a cat so aggressively cropped that it feels fragmented is penalized, because true proportional presence means the cat is both large *and* intact within the frame.

### 2. Positional Authority — [cat-compositional-authority](https://github.com/ObjectiveAI-claude-code-1/cat-compositional-authority)

Where the cat is located within the frame and whether that placement conveys **visual importance and compositional intention**. The center of a frame is a position of natural power; the rule-of-thirds intersections are positions of dynamic emphasis. A cat placed at these compositional focal points radiates authority. A cat pushed to the extreme edges or corners — as if barely caught before it walked out of the shot — feels marginalized and accidental.

### 3. Subject Isolation — [cat-background-clarity](https://github.com/ObjectiveAI-claude-code-1/cat-background-clarity)

How cleanly the cat separates from its surroundings and how free the image is from **competing visual elements**. A cat photographed against a smooth, uncluttered background achieves high isolation — there is nothing else for the eye to latch onto. A cat surrounded by patterned furniture, scattered objects, and bright competing colors must fight for attention. Subject isolation is what transforms a picture that *contains* a cat into a picture that is *about* a cat.

## Use Cases

- **Content curation** — Filter cat pictures for galleries, feeds, or featured content by selecting images where the cat communicates its subject instantly, making them ideal for hero images and thumbnails.
- **Quality assessment** — Provide photographers a first-pass filter to quickly identify shots where the cat is clearly and prominently captured versus images where it is partially out of frame, obscured, or competing with distractions.
- **Prerequisite gating** — Act as a gatekeeper for downstream analysis systems that evaluate expression, pose, breed, or emotional tone — ensuring the cat is sufficiently visible and prominent before deeper evaluation begins.

## Philosophy

Frame dominance is not a measure of cuteness, mood, or photographic artistry. It is something more fundamental: a measure of **visual sovereignty**. Before we can evaluate anything else about a cat picture — its emotional resonance, its humor, its aesthetic beauty — we must first establish that the picture succeeds at being a picture of a cat. This function provides that bedrock assessment.

A cat that scores highly across all three qualities fills the frame with its body, commands its position with compositional confidence, and stands apart from an undistracting background. Such a cat is not merely *in* the picture. It *is* the picture.