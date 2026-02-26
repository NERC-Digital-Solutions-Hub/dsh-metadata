# This document is a supplement to the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf' Details of data structure to ' HF_NW_herbage_yield.csv '

## Overview
- Presents the HF_NW_herbage_yield.csv dataset (7 columns, 96 rows) containing herbage yield measurements from a grassland fertiliser trial conducted in 2016 at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research).
- Purpose: provide a structured, plot-level yield dataset suitable for map-based visualization and spatial analysis.
- Main measurement: dry weight yield of grass (tonnes per hectare).

## Data structure (columns)
- Date: Date of grass cut
- Site: HF or NW indicating trial location (HF = Henfaes, NW = North Wyke)
- N_app: 1, 2, or 3 denoting fertiliser applications; 1st & 2nd applications at 90 kg ha-1, 3rd application at 60 kg ha-1
- Block: 1–4, blocking factor of the randomised design
- Plot: 1–16, the harvested plot; plot size 2 m × 6 m
- Treatment: AN (ammonium nitrate), U (urea), IU (inhibited urea, AgroInhib), C (0 N control)
- Dry_tonnes_ha: yield in tonnes per hectare (dry matter)

## Spatial and GIS relevance
- Spatial keywords: two sites (HF, NW) and plot-level observations (1–16 per block)
- Suitable for creating map-based visuals: yield by site, by treatment, by N_app, and by block/plot
- Can be joined with site/plot boundary shapefiles to produce field-level yield maps and to assess spatial patterns of management impact

## Data quality and integration considerations
- Designed for integration with GIS workflows: plot-level observations within a block-randomised design
- Requires alignment with spatial boundaries for HF and NW plots; ensure consistent plot identifiers across GIS layers
- Date field may require standard date parsing; ensure consistent date formats
- Data completeness and consistency with the referenced supporting documentation should be verified prior to analysis

## How this supports GIS workflows
- Enables creation of thematic maps showing yield variation across sites, treatments, and fertiliser levels
- Supports spatial comparisons of management effects (e.g., fertiliser type, application rate) within and between sites
- Facilitates overlay with environmental layers (soil type, topography) to explore drivers of yield differences

## Source and references
- Dataset: HF_NW_herbage_yield.csv (7 columns, 96 rows)
- Supplemental to: Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf