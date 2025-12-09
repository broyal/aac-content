# AAC Content Packs

This repository contains vocabulary packs for Project AAC.

## Structure

```
aac-content/
├── catalog.json              # Master catalog of all packs
└── packs/
    └── {pack_id}/
        ├── pack.json         # Pack metadata and word definitions
        └── images/           # Pack images (PNGs)
            ├── word1.png
            └── word2.png
```

## Adding Images

For Phase 1, we're using SF Symbol fallbacks in the app. To add real images:

1. Create PNG files (recommended 512x512px)
2. Name them to match the `filename` in `pack.json`
3. Place in `packs/{pack_id}/images/`

## CDN Access

Files are served via jsDelivr CDN:
- Base URL: `https://cdn.jsdelivr.net/gh/YOUR-USERNAME/aac-content@main/`
- Example: `https://cdn.jsdelivr.net/gh/YOUR-USERNAME/aac-content@main/catalog.json`

## Pack Format

See `packs/basic_needs_toddler_v1/pack.json` for the schema.

### Key Fields:
- `schemaVersion`: Pack file format version (currently 1)
- `id`: Unique pack identifier
- `version`: Pack content version (increment when updating)
- `categories`: Array of vocab categories with words
- `images`: Array of image metadata for downloads

## Testing

Use the RemotePacksDebugView in the app to test pack loading.

