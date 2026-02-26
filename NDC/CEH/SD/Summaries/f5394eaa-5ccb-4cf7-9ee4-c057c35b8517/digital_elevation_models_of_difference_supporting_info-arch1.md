# Digital elevation models of difference (DoD) for Chamoli avalanche, Uttarakhand, India

- The DoD data are raster (.tif) digital elevation models of difference that quantify vertical (z) topographic change between two dates. They are intended for use in GIS analyses to assess landscape change, supporting analyses and modelling.

## Overview and purpose
- Created to support analysis of landscape change following the 7 February 2021 avalanche-debris flow in Chamoli District, Uttarakhand, India.
- Also supports numerical modelling with CAESAR-Lisflood.
- Useful for identifying erosion (negative changes) and deposition (positive changes) between DEM pairs.

## Spatial and temporal coverage
- Spatial extent described by bounding box in WGS 84 / UTM Zone 44:
  - Top left: 352312 m E, 3385209 m N
  - Lower right: 384787 m E, 3358896 m N
- Raw DEMs were generated between 10 February 2021 and 27 April 2022; DoDs were created in a rolling sequence within this period.
- DoDs represent differences between two DEM dates; file naming encodes the period spanned by each DoD.

## Data creation and interpretation
- DoDs created in QGIS (versions 3.18 and 3.24) using Raster Calculator.
- For each DEM pair, the later DEM minus the earlier DEM; negative values = surface lowering (erosion), positive values = surface gain (deposition).
- Project Principal Investigator (PI) authored all DoDs.

## Data completeness and reproducibility
- The dataset contains all DoDs generated as part of this research.
- Additional DoDs could be generated using other input DEM combinations from the broader data collection; the methodology is described to enable replication.
- The dataset includes guidance to estimate significant change thresholds (as described in section 5).

## Data quality and handling of gaps
- DoDs reproduce holes/data gaps present in input DEMs (caused by photogrammetric reconstruction issues due to cloud cover, occlusion, or large view-angle offsets).
- To determine statistically significant change thresholds for each DoD, 16 stable hillside areas adjacent to the valley floor were analyzed using Pléaides orthophotos; standard deviations within these areas were used to estimate a two-sigma DoD uncertainty.
- Reported two-sigma uncertainties per DoD:
  - ±1.11 m (Sept 2015 – 10 Feb 2021 DoD)
  - ±0.91 m (10 Feb 2021 – 06 Jun 2021 DoD)
  - ±0.61 m (06 Jun 2021 – 25 Dec 2021 DoD)
  - ±1.14 m (10 Feb 2021 – 25 Dec 2021 DoD)
  - ±1.06 m (10 Feb 2021 – 27 Jan 2022 DoD)
- DoD values exceeding the relevant threshold are considered statistically significant.
- Stable area polygons used for this assessment are provided with the dataset.

## Dataset structure and contents
- Key DoD files:
  - 1509_composite_210210_DoD.tif
  - 210210_210606_DoD.tif
  - 210606_211225_DoD.tif
  - 210210_211225_DoD.tif
  - 210210_220127_DoD.tif
- Stability reference:
  - stable_areas.shp (plus auxiliary files: .cpg, .dbf, .prf, .qmd, .shx)
- File naming conventions:
  - DoD filenames follow YY-MM-DD, where the two dates indicate the period spanned by the DoD.
  - The September 2015 DEM is a composite; “1509” denotes September 2015.

## How to use and interpret
- Use GIS tools to view raster DoDs and interpret negative (erosion) versus positive (deposition) changes.
- Compare DoDs across periods to identify spatial patterns of landscape change related to the avalanche-debris flow.
- Apply the two-sigma thresholds to assess statistical significance of observed changes.
- Leverage the stable areas and metadata to contextualize uncertainty and to reproduce threshold calculations if needed.