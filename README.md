# The House of Rothschild - Genealogical Map

A 3D interactive genealogical visualization of the Rothschild family tree, built with Three.js. This project maps the descendants of Mayer Amschel Rothschild, highlighting the family's expansion across Europe, their strategic intermarriages, and their modern-day branches.

## Overview

The visualization is structured hierarchically along the Y-axis to represent generations:
- **Y = 100**: Generation 1 (Founder: Mayer Amschel Rothschild)
- **Y = 50**: Generation 2 (The Five Sons who established the European branches)
- **Y = 0**: Generation 3 (Grandchildren)
- **Y = -50**: Generation 4 (Great-grandchildren)
- **Y = -100**: Generation 5 (Great-great-grandchildren)
- **Y = -150 to -200**: Generations 6-7 (Modern/Contemporary descendants)

### Key Features
- **Hierarchical Layout**: Founder at the top, contemporary members at the bottom.
- **Branch Grouping**: Nodes are spatially grouped by their historical banking branch (Frankfurt, Vienna, London, Naples, Paris).
- **Intermarriage Links**: Red lines explicitly denote the family's well-documented strategy of endogamy (cousin marriages, uncle-niece marriages) to keep wealth and control within the family.
- **Interactive Nodes**: Click any node to view detailed biographical information, generation data, and a list of family connections.
- **Historical Headshots**: Portraits scraped from Wikipedia are displayed for most major figures.
- **3D Navigation**: Drag to rotate, scroll to zoom, and use the "Reset View" button to recenter.

## Primary Sources

The genealogical data and historical notes in this visualization were extracted directly from the following primary texts and resources:
1. *The House of Rothschild* by Niall Ferguson (Penguin Books, 1999)
2. *The Rothschild Dynasty* by Dr. John Coleman
3. Wikipedia: [Rothschild family](https://en.wikipedia.org/wiki/Rothschild_family) and its branch-specific articles (England, Austria, France, Naples).

Key extracted facts include:
- Mayer Amschel's five sons: Amschel Mayer, Salomon Mayer, Nathan Mayer, Carl Mayer, and Jacob (James) Mayer.
- Strategic marriages: e.g., James married his niece Betty (Salomon's daughter); Alphonse (James's son) married Leonora (Lionel's daughter); Anselm Salomon married Charlotte (Nathan's daughter).
- Branch specializations: Frankfurt (Amschel), Vienna (Salomon), London (Nathan), Naples (Carl), Paris (James).
- Modern continuity: The English branch (Jacob, 4th Baron; Nathaniel, 5th Baron) and French branch (David René, Alexandre) remain active in finance today.

## Project Structure

```
rothschild-map/
├── index.html          # Main 3D visualization (Three.js + CSS2DRenderer)
├── README.md           # This file
├── images/             # Directory for historical portraits (scraped from Wikipedia)
│   └── placeholder.jpg # Fallback for members without available portraits
└── resources/          # Additional reference materials or data files
```

## Usage

1. Open `index.html` in any modern web browser. No local server is strictly required, though running one (e.g., `python3 -m http.server`) is recommended for optimal asset loading.
2. **Navigate**: Left-click + drag to rotate the camera. Scroll to zoom in/out.
3. **Inspect**: Click on any sphere (node) to highlight it and display detailed genealogical information in the bottom panel.
4. **Explore Connections**: Click on linked names in the bottom panel to jump the camera focus to that family member.

## Customization

- **Adding Images**: Place historical portraits in the `images/` directory and update the `headshotImages` mapping in `index.html` to point to the correct filenames.
- **Adding Nodes**: Extend the `nodes` and `links` arrays in the `<script>` section of `index.html` following the existing JSON-like structure.
- **Styling**: Modify the CSS variables and Three.js material colors to adjust the visual theme.

## License

This project is for educational and historical research purposes. The underlying data is derived from publicly available historical texts and Wikipedia. Headshot images are sourced from Wikimedia Commons under their respective free licenses.