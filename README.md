# Godavari Delta Subsidence & Erosion Analysis (2026)

Reproducible workflow for the manuscript  
**Subsidence Outpaces Sea-Level Rise and Amplifies Sediment-Starved Erosion in the Godavari Delta, India**  
(target: *Nature Sustainability*)

## Overview

This repository contains the complete Google Colab workflow used to generate Figure 1 and Supplementary Figure S1, including:
- Google Earth Engine exports (Sentinel-2 true-color, NDWI change 1990–2025, temporal NDWI split 2000–2010 vs 2015–2025)
- High-resolution vertical land motion rasterization (Godavari from Ohenhen CSV)
- Threshold-based vulnerability hotspot index
- Quantitative area calculations (vulnerability zones, coastal retreat)
- Temporal vulnerability change analysis
- Comparative layers for Cauvery (1 km subsidence placeholder + NDWI change)
- SVG figure assembly

## Key files

- `Godavari_Cauvery_Comparison_Workflow_2026-02-20.ipynb` — main notebook (temporal split, stats, Supp Fig S1, Cauvery layers)
- `Figure1_Final_All_Panels_Improved.svg` — main manuscript figure
- `Supp_Fig_S1_Godavari_vs_Cauvery.svg` — comparative supplementary figure (Godavari vs Cauvery)

Large TIFF rasters (~75–300 MB) are generated on-the-fly and saved to Google Drive (not included in repo due to size).

## How to run

1. Open the notebook in Google Colab:  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chemoinfoiict-boop/Godavari-BOB/blob/main/Godavari_Cauvery_Comparison_Workflow_2026-02-20.ipynb)

2. Mount Google Drive (prompt appears):  
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
