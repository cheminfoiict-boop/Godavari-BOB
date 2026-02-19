# Godavari Delta Subsidence & Erosion Analysis (2026)

Reproducible workflow for **Figure 1** in the manuscript  
**"Subsidence Outpaces Sea-Level Rise and Amplifies Sediment-Starved Erosion in the Godavari Delta"**  
(submitted / in preparation for *Nature Sustainability*)

## Overview

This repository contains the complete Python / Google Earth Engine workflow used to generate Figure 1, which demonstrates the coupled effects of anthropogenic subsidence and sediment starvation in the Godavari delta (Bay of Bengal, India).

Main outputs:
- True-color Sentinel-2 regional context (panel a)
- High-resolution (~75 m) vertical land motion / subsidence map from point data (panel b)
- NDWI change detection (1990–2025) showing shoreline & mangrove dynamics (panel c)
- Threshold-based integrated vulnerability hotspots (panel d)
- Final vector figure in SVG format

## Repository contents

| File / Folder                              | Description                                                                 |
|--------------------------------------------|-----------------------------------------------------------------------------|
| `Godavari_Delta_Figure1_Workflow.ipynb`    | Main Colab notebook – full workflow (GEE exports, raster processing, SVG assembly) |
| `Figure1_Final_All_Panels_Improved.svg`    | Final vector figure (editable in Adobe Illustrator)                         |
| `README.md`                                | This file                                                                   |
| `LICENSE`                                  | MIT license for code reuse                                                  |

Large TIFF rasters (Sentinel-2 composite, VLM, NDWI change, vulnerability index) are not included due to size limits; they are generated on-the-fly during notebook execution (saved to your Google Drive).

## How to run the workflow

1. Open the notebook in Google Colab (recommended):  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chemoinfoiict-boop/Godavari-BOB/blob/main/Godavari_Delta_Figure1_Workflow.ipynb)

2. Mount your Google Drive (cell will prompt you):  
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
