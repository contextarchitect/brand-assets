# Nano Banana Pro vs GPT Image 2 — Blind A/B Test v1

**Date:** 2026-04-23
**Purpose:** Determine which model wins across 6 common Creative Engine use categories so the `gpt-image-2-prompting` and `nano-banana-prompting` skills can encode empirical default routing.

## Methodology

- 12 concepts across 6 categories (2 concepts per category)
- Each concept generated on both models with prompts idiomatic to each framework:
  - Nano Banana → Three-Layer (Visible / Composition-constraints / Exclusion)
  - GPT Image 2 → Classify-Extract-Construct (scene, subject, secondary, materials, composition, lighting, style, constraints)
- SAME brief, SAME aspect ratio, SAME reference images per concept
- Blind-labelled a/b at download time from a randomized mapping; mapping sealed until scoring complete
- Scored by Hilal on 6 rubric dimensions (1-5 each, total /30)
- Category winner = higher combined score across the 2 concepts
- Results encoded back into the skills as default routing tables

## Categories & concepts

1. **Product placement**
   - Concept 1: Product on bathroom counter (4:5) — REF-001 + REF-007
   - Concept 2: Flat-lay with natural ingredients (1:1) — REF-001
2. **Product scale (models holding/using product)**
   - Concept 3: Woman holding bottle in bathroom (4:5) — REF-007
   - Concept 4: Man's hand picking up bottle from gym bag (3:2) — REF-009
3. **Models interacting with products**
   - Concept 5: Woman applying cream in front of mirror (4:5) — REF-007
   - Concept 6: Two women in kitchen passing bottle (3:2) — REF-007
4. **Detailed infographics**
   - Concept 7: Three-step routine infographic (4:5) — REF-012
   - Concept 8: Before/after comparison (16:9) — REF-001
5. **Animation-style images**
   - Concept 9: Flat-vector illustration of routine (4:5) — REF-012
   - Concept 10: Isometric 3D cartoon scene (1:1) — REF-012
6. **UGC content**
   - Concept 11: Mirror-selfie holding product (4:5) — REF-007
   - Concept 12: UGC unboxing on desk (4:5) — REF-001

## Reference Image Scale Context Rule applied

Concepts with human-product or object-product scale interaction use lifestyle references (REF-007, REF-009). Isolated product scenes and infographics use packshots (REF-001, REF-012).

## Rubric (per image, 1-5 each, total /30)

| Dimension | 1 | 5 |
|---|---|---|
| Prompt adherence | Ignored brief | Hit every explicit constraint |
| Photographic/visual quality | Artifacts, blur | Crisp, shippable |
| Subject accuracy | Wrong product | Exactly as described |
| Text rendering | Gibberish/missing | Perfect (N/A if no text) |
| Anatomy/scale | Body horror or wrong scale | Natural, correct scale |
| Overall usability | Regenerate | Ship it |

## Pricing reference

- Nano Banana Pro @ 2K resolution: 12 credits/image × 12 = 144 credits
- GPT Image 2: pricing captured on first task response

## Output

Results table pushed to `_skills/gpt-image-2-prompting/SKILL.md` and `_skills/nano-banana-prompting/SKILL.md` after scoring is complete.
