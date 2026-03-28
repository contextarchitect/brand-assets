# Brand Assets (Public)

Public product reference images used by AI image generation tools (Nano Banana Pro, Kie API) that require publicly accessible URLs.

## Purpose

This repo exists because AI image generation APIs (like Kie.ai's Nano Banana Pro) need to fetch reference images via public URLs. Our brand context repos are private, so image URLs from those repos use temporary tokens that expire — causing generation failures.

**This repo contains ONLY product photography reference images. No strategy documents, brand guidelines, or sensitive business context.**

## Structure

```
regrowth/
  product-images/
    IMG_8425.png          (REF-001)
    IMG_8455.png          (REF-002)
    IMG_8503.png          (REF-003)
    ...
    README.md             (REF index mapping)
protocel/
  product-images/
    ...
mgmens/
  product-images/
    ...
```

## Usage

Reference images via raw URLs:
```
https://raw.githubusercontent.com/contextarchitect/brand-assets/main/regrowth/product-images/IMG_8425.png
```

These URLs are permanent and don't require authentication tokens.

## Important

- **DO NOT** add brand strategy documents, system prompts, avatar research, or any sensitive business context to this repo
- This repo is PUBLIC — only product images that are already visible on brand websites/ads
- Keep filenames identical to the private repo for REF index compatibility
