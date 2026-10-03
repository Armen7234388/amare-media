# AMARE Media

Public media storage for AMARE marketplace product content.

## Purpose

This repository contains only approved public marketplace assets:
- product images;
- product videos;
- media manifests.

No API keys, credentials, private documents, customer data, supplier documents, or internal AMARE data may be stored here.

## Product layout

```
products/<offer_id>/
  images/
    01-main.jpg|png
    02-*.jpg|png
    ...
    08-*.jpg|png
  video/
    01-main.mp4
  manifest.json
```

## Stable URLs

Files on the `main` branch are exposed to Ozon using:

```
https://raw.githubusercontent.com/Armen7234388/amare-media/main/products/<offer_id>/images/<file>
```

Video files use the same pattern under `video/`.

## Publication rule

Only the exact owner-approved media set may be published to Ozon.

Before publication:
1. verify file names and order;
2. verify image count;
3. verify hashes where available;
4. never regenerate or substitute approved files;
5. publish;
6. read back from Ozon and confirm the final media set.

For the default AMARE card:
- 1 primary image;
- 7 additional images;
- optional 1 product video.

Generated media is considered public once committed here.
