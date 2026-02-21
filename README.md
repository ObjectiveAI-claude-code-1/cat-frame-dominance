# cat-frame-dominance

A scalar function that evaluates how much a cat commands the visual frame of a photograph. Given a single cat picture, it returns a score between **0** and **1** representing the degree to which the cat is the undeniable subject of the image — not merely present, but visually dominant.

## Input

| Field | Type | Description |
|-------|------|-------------|
| input | `image` | A cat picture to evaluate for frame dominance. |

The function accepts a single image file depicting at least one cat in any context — indoors, outdoors, close-up, or far away. It does not judge the artistic merit of the photograph, the beauty of the cat, or the technical quality of the camera. It evaluates only the spatial and compositional relationship between the cat and the frame it inhabits.

## Output

A scalar value between **0** and **1**.

- A score near **1** means the cat is the undeniable focal point — large, prominently placed, and set against a clean background that lets it shine.
- A score near **0** means the cat is incidental — small, marginal, lost in clutter, or competing with other visual elements for the viewer's attention.

## What It Evaluates

The function assesses frame dominance across three independent qualities. Each captures a different dimension of what it means for a cat to own its image, and no single quality alone is sufficient. The interplay of all three determines the final score.

### 1. Proportional Presence

How much physical space does the cat occupy within the boundaries of the image? A cat that fills the frame has inherent visual authority that a distant speck of fur cannot match. But this is not simply "bigger is better" — a cat so close to the camera that it is severely cropped feels incomplete. True proportional presence means the cat is *substantially there*: large enough to be unmistakable, complete enough to feel whole and intentional.

- **Scores high:** A cat whose body, face, and posture are legible and take up meaningful room.
- **Scores low:** A tiny, distant, or barely visible cat that requires effort to find.

> Sub-function: [{{ .Task0 }}](https://github.com/{{ .Owner }}/{{ .Task0 }})

### 2. Positional Authority

Where does the cat sit within the compositional geometry of the frame? A cat positioned in or near the center, or along natural focal lines where the eye is drawn, possesses a gravitational pull that a cat tucked into a far corner does not. A cat does not need to be mathematically centered — what matters is that its placement feels deliberate and dominant.

- **Scores high:** A cat whose position creates compositional gravity, as though the image was framed around it.
- **Scores low:** A cat pushed to the periphery, tucked into a corner, or placed in a way that feels accidental.

> Sub-function: [{{ .Task1 }}](https://github.com/{{ .Owner }}/{{ .Task1 }})

### 3. Environmental Clarity

Does the space surrounding the cat defer to it, or compete with it? Even a large, well-positioned cat can lose its grip on the frame if the environment is chaotic, cluttered, or filled with competing subjects. A plain wall, a soft blanket, or a blurred backdrop amplifies dominance. A messy desk, a crowd of objects, or other animals and people in the frame dilute it.

- **Scores high:** A clean, calm background where everything that is not the cat quietly steps aside.
- **Scores low:** A busy, cluttered environment where the cat must fight for the viewer's attention.

> Sub-function: [{{ .Task2 }}](https://github.com/{{ .Owner }}/{{ .Task2 }})

## Use-Cases

- **Content curation** — Surface images where the cat is genuinely the star, filtering out shots where it is a minor background element.
- **Cat adoption listings** — Guide shelter volunteers toward retaking photos that don't showcase their animals prominently, improving adoption outcomes.
- **Personal photo filtering** — Help cat owners find their strongest cat photos from thousands of candidates, prioritizing images where the cat commands the frame.
- **Quality evaluation pipelines** — Serve as the foundational first-pass in any system that evaluates cat photo quality. Before asking whether a cat photo is beautiful or emotionally compelling, establish that the photo is *about the cat at all*.

## Philosophy

Frame dominance is a measure of intentionality. The best cat pictures feel like they exist *for* the cat — the frame is a stage, and the cat is the performer. This function quantifies that feeling: the quiet, immediate certainty that when you look at this picture, you are looking at a cat, and nothing else matters.