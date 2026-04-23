# Regrowth+ Product Reference Images

Copy these files from the private repo (`context-architect-brands/regrowth/product-images/`).

Keep filenames identical for REF index compatibility.

## Public URL Pattern
```
https://raw.githubusercontent.com/contextarchitect/brand-assets/main/regrowth/product-images/{FILENAME}
```

## REF Index

| REF | Filename | Description | Scene context |
|-----|----------|-------------|---------------|
| REF-001 | IMG_8425.png | Isolated product shot | None (packshot) |
| REF-002 | IMG_8455.png | Product shot | None (packshot) |
| REF-003 | IMG_8503.png | Product shot | None (packshot) |
| REF-004 | IMG_8527.png | Product shot | None (packshot) |
| REF-005 | IMG_8551.png | Product shot | None (packshot) |
| REF-006 | IMG_8663.png | Product shot | None (packshot) |
| REF-007 | IMG_8933 feminine vibe.png | Female lifestyle | Yes (scene + scale) |
| REF-008 | IMG_8940 feminine.png | Female lifestyle | Yes (scene + scale) |
| REF-009 | IMG_8992 hold warm.png | **Male hand model holding bottle** | Yes (hand + scale) |
| REF-010 | Bundle-removebg.png | Bundle cutout | None (packshot) |
| REF-011 | Conditioner-removebg.png | Conditioner cutout | None (packshot) |
| REF-012 | Shampoo-removebg.png | Shampoo cutout | None (packshot) |
| REF-013 | logo.png | Brand logo | N/A |

## Reference selection guidance

Per the **Reference Image Scale Context Rule** in `nano-banana-prompting` and `gpt-image-2-prompting` skills:

- **Scene includes people, objects, or environments alongside the product** → use a reference with Scene context = "Yes". Isolated packshots provide no scale information and the model will default to whatever size fills the frame.
- **Scene is an isolated product shot, or the product is being composited onto a graphic layout** → isolated packshots (REF-001 through REF-006, REF-010 through REF-012) are correct.
- **Scene depicts a male subject interacting with the product** → use REF-009 for hand/grip scale. No other male reference currently exists.
- **Scene depicts a female subject interacting with the product** → use REF-007 or REF-008 for scene/scale context.

If a required reference type is missing (e.g. a male lifestyle shot on a bathroom counter), note the gap in the prompt rather than substituting an isolated packshot. The Universal Product Appearance Rule still requires a product reference; the Scale Context Rule additionally requires that the reference match the scene.
