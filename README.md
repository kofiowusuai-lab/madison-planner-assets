# Madison planner assets

A static image library for the **Popstar in Progress** planner: Notion home covers, section banners and numbered page banners. This repository contains finished JPEG assets and design variants, rather than an application or an editable Notion template.

## Browse the assets

| Location | Contents |
| --- | --- |
| [`notion-page-banners/`](notion-page-banners/) | Original 63-image set |
| `notion-page-banners-v2/` through `notion-page-banners-v7/` | Six alternative 63-image sets |
| [`notion-page-banners-v10-red-pants/`](notion-page-banners-v10-red-pants/) | Named red-pants variant, 63 images |
| [`notion-page-banners-v12-handwriting-canvas/`](notion-page-banners-v12-handwriting-canvas/) | Handwriting/canvas variant, 63 images |
| [`notion-page-banners-v13-title-only-handwriting-canvas/`](notion-page-banners-v13-title-only-handwriting-canvas/) | Title-only handwriting/canvas variant, 63 images |
| Root `notion-banner-*.jpg` files | Five standalone home/cover variants |

There are **635 JPEGs** in the committed library: ten sets of 63 plus five root covers. Each page set follows a numbered home/section/page sequence, with names describing the destination. The sequence covers start-here guidance, future identity, dream-life scripts, weekly planning, reframing, confidence, money, mental reset, milestones, notes and closing. Most images are 1500 × 600 pixels (634 files); one root cover is 1280 × 511 pixels. Version numbers record alternatives; there is no manifest declaring which version is approved or currently used.

## Use in Notion

1. Browse a complete set and choose its visual treatment.
2. Open the matching planner page in Notion.
3. Add or change its cover and upload the corresponding JPEG.
4. Reposition the cover and preview desktop and mobile crops.
5. Repeat for section and numbered pages, keeping one variant consistent across the planner.

For a local copy, install Git and run:

```bash
git clone https://github.com/kofiowusuai-lab/madison-planner-assets.git
cd madison-planner-assets
```

No Node/Python dependencies, environment variables, account credentials, install scripts or build command are needed to view the images. A Notion account and an existing page/template are needed to apply them there. Downloading the images does not create the planner's pages, databases or links.

## Asset workflow and publishing

The directory is the workflow boundary: select a version, map each numbered filename to its destination, and upload or reference that image in the publishing platform. This repository does not include generation scripts, editable source artwork, a Notion import package or automatic upload tooling. The JPEGs themselves are the delivered artifacts.

Keep the original filenames when possible so the page purpose remains discoverable. When publishing outside Notion, use descriptive alt text based on the actual image and page, such as “Popstar in Progress weekly planning page cover.” Do not imply an unrelated endorsement or brand ownership. Platform cropping and metadata handling vary; the surrounding page title and description also matter.

## Validation and limitations

There is no automated test suite. Before publishing, visually inspect the chosen images, verify page-to-banner pairing, and check that titles remain legible in the platform's crop. You can confirm the local inventory without opening every file:

```bash
python3 - <<'PY'
from pathlib import Path
root = Path('.')
for folder in sorted(root.glob('notion-page-banners*')):
    print(folder.name, len(list(folder.glob('*.jpg'))))
print('Total JPEGs:', len(list(root.rglob('*.jpg'))))
PY
```

If a cover looks clipped, adjust Notion's cover position or try another included variant. If a page name differs, match by the descriptive filename rather than assuming the numeric prefix is the displayed planner page number: section banners are included in the sequence.

No licence or third-party permission statement is included in this snapshot. Public availability alone does not establish permission to redistribute or sell the artwork; retain any applicable creator and product rights when using it.
