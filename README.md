# feline-authenticity-score

A scalar function that looks at a photograph of a cat and answers one question: **is this cat genuinely being itself?**

The Feline Authenticity Score draws a line between a cat captured in an honest moment and a cat made to perform for an audience. It returns a number between 0 and 1 — where 1 means the moment is unmistakably real and 0 means the moment is clearly manufactured, staged, or imposed on the cat.

This is not a judgment of photographic quality, artistic merit, or charm. Many staged cat photos are beautiful. But charm and authenticity are not the same thing. A cat stuffed into a shark costume may delight millions, but the cat did not choose that moment.

## Input

| Field | Type | Required | Description |
|---|---|---|---|
| `cat_image` | `image` | Yes | A photograph or image containing a cat. |

The image is the totality of the evidence. The function reads the cat's body, posture, eyes, environment, the presence or absence of human hands, surrounding objects, and every visible detail to determine how the moment came to be. There is no metadata, no backstory, no caption — the image must speak for itself.

## Output

A **scalar score** in the range **[0, 1]**.

| Score Range | Interpretation |
|---|---|
| **0.8 – 1.0** | Unmistakably authentic — the cat is clearly being itself in a genuine, unperformed moment. |
| **0.5 – 0.8** | Mostly authentic — the moment reads as largely natural with minor ambiguities. |
| **0.3 – 0.5** | Mixed signals — some elements feel genuine but others suggest staging or contrivance. |
| **0.0 – 0.3** | Clearly staged — the moment appears manufactured, forced, or imposed on the cat. |

A score of **0.5** represents a neutral midpoint where the evidence is evenly balanced between authentic and staged.

## What It Evaluates

The score is derived from three independent quality assessments, each examining the image through a different lens:

### 1. Bodily Naturalism

Examines the cat's physical state — posture, musculature, limb placement, eye state, and overall bodily configuration — to determine whether the cat's body arrived at its position voluntarily.

Cats are biomechanically honest. Genuine sleep produces a boneless surrender of limbs at improbable angles. A real pounce commits the whole skeleton — coiled haunches, forward-thrust chest, wide focused eyes. Contented kneading reveals itself through half-closed eyes and relaxed weight.

**Scores high when:** The cat's physical configuration is entirely consistent with voluntary feline behavior — natural sleep, alert hunting posture, relaxed sprawling, or any position a cat's body would actually adopt on its own.

**Scores low when:** The cat's posture is inconsistent with voluntary behavior — held aloft, balanced in unnatural configurations, or showing tension and constraint that suggest the cat was placed or arranged into position.

### 2. Environmental Integrity

Looks beyond the cat's body to the surrounding scene to determine whether the environment supports or undermines the story of a natural moment.

Authentic cat life unfolds in ordinary places — windowsills, cardboard boxes, rumpled beds, garden walls, cluttered desks, laptop keyboards. Human environments are entirely acceptable; cats live in human homes. The question is whether the setting is a plausible theater of real cat life, or whether it was constructed to produce an image.

**Scores high when:** The scene is a plausible, ordinary setting with no costumes, constructed props, studio backdrops, or visible staging. The cat appears to be in a place it would naturally be found.

**Scores low when:** The scene is clearly staged — costumes or accessories on the cat, miniature furniture arranged for effect, studio backdrops, visible treats positioned to lure attention, or any environment no cat would naturally inhabit.

### 3. Relational Genuineness

Assesses the nature of any interaction in the frame — between the cat and humans, objects, other animals, or the camera — to determine whether the cat is a willing participant or a passive subject.

Human presence does not diminish authenticity. A cat pressing into a person's hand, headbutting a chin, or curled in someone's lap can be deeply authentic. The distinction is agency: is the cat choosing to participate, or is the moment being done to the cat?

**Scores high when:** Interactions feel mutual and voluntary. The cat appears to be directing contact, choosing its state, or is simply unaware of the camera — giving the image the quality of a stolen moment.

**Scores low when:** The cat appears to be held, positioned, directed, or manipulated. The cat's relationship with humans, objects, or the camera feels forced, and the cat shows no signs of voluntary participation.

## Use Cases

- **Content curation**: Surface cat imagery that celebrates cats as they actually are, rather than as props or accessories.
- **Animal welfare**: Distinguish between imagery showing natural, stress-free behavior and imagery that may depict coercion or discomfort.
- **Candid photography**: Benchmark and validate the authenticity of animal photography work.
- **Platform moderation**: Identify and categorize the degree of staging or manipulation in animal content.
- **Research**: Study trends in how animals are represented and instrumentalized in visual media.

## Philosophy

The Feline Authenticity Score is built on a simple conviction: cats are most worth seeing when they are most fully themselves. The score does not measure whether an image is good, funny, or worthy of attention — it measures whether the cat in the frame is in a real moment. It is, at its heart, a small act of respect for the genuine lives of cats as they actually live them — peculiar, graceful, absurd, and entirely on their own terms.