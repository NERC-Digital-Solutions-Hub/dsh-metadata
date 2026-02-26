# Supporting documentation for data:
Mean and variability of topsoil organic carbon concentrations across Great Britain derived at 1 km resolution from an ensemble of eight digital soil maps

## Aim and scope
- Presents a dataset of topsoil organic carbon (SOC) summaries across Great Britain (GB) at 1 km resolution.
- Builds from an ensemble of eight published digital soil maps to compare predictions and quantify inter-map variability.
- Excludes Northern Ireland; built-up, rocky inland/coastal areas removed due to lack of soil data for reliable predictions.
- Enables assessment of agreement/disagreement among maps and identification of drivers of differences.

## Data sources and maps (the eight primary maps)
- Countryside Survey GB: AIC (CSGB-AIC)
- Countryside Survey GB: GAMM (CSGB-GAMM)
- Countryside Survey GB: KRGS (CSGB-KRGS)
- Countryside Survey GB: MLRF (CSGB-MLRF)
- ISRIC SoilGrids 2017 (ISRIC-2017)
- ISRIC SoilGrids 2020 (ISRIC-2020)
- LUCAS soil carbon map (LUCAS)
- OCTOP (OCTOP)
- Each map uses different underlying datasets and methodologies (e.g., machine learning, kriging) and covers the topsoil in varying depths.

## Harmonisation and preprocessing
- All maps harmonised to GB extent, 1 km grid, and OSGB (EPSG:27700).
- Depth alignment: ISRIC maps converted to 0–15 cm; ISRIC-2017 uses 0,5,15 cm layers; ISRIC-2020 uses 0–5 and 5–15 cm with weighted averaging.
- Unit conversions applied to place all maps in g kg−1 SOC:
  - ISRIC maps converted from dg kg−1 by dividing by 10.
  - OCTOP from % SOC by multiplying by 10.
  - CS maps (LOI%) converted to g kg−1 using established regression (×5.5).
- Outliers and physical limits addressed:
  - LUCAS and OCTOP values above ~55% SOC capped at 550 g kg−1.
  - CSGB-AIC negative SOC values removed (set as no data where appropriate).
  - Cells with insufficient data (missing any map) set to no data for mean computation.

## Calculations and data produced
- For cells with complete data from all eight maps (n = 208,752):
  - Mean SOC (g kg−1)
  - Standard deviation (SD) of SOC (g kg−1)
  - Coefficient of variation (CoV = SD/Mean)
  - Signal-to-noise ratio (SNR = Mean/SD)
  - Most deviant map from the mean (per cell; coded 1–13, with ties possible)
  - Greatest deviation from the mean expressed as a percentage (band 6)
  - Greatest deviation from the mean expressed as the number of SDs exceeded (band 7)

## Dataset structure and access
- File: SOC_map_summaries.tif (single geotiff)
- 7 bands at 1 km resolution across GB (excluding NI):
  1. Mean SOC
  2. SD
  3. CoV
  4. SNR
  5. Most deviant map from the mean (codes 1–13)
  6. Greatest deviation from mean as a % (band 6)
  7. Greatest deviation from mean as number of SDs exceeded (band 7)
- Metadata includes: units, interpretation, and relationship to the eight primary maps.

## Quality control and data integrity
- Checks performed 19/10/2022 prior to submission:
  - Consistent resolution, extent, and CRS (EPSG:27700) across all maps.
  - All bands stacked into a single raster; 1 km grid cells aligned with OSGB grid.
  - Verified no misinterpretation of zero-values as missing data; corrected negatives in CSGB-AIC to no data where appropriate.
  - SOC values constrained to plausible ranges (0–550 g kg−1 for means; SDs consistent with data).
  - 7-band data structure verified; no data left blank for cells with complete eight-map data.
- Exclusions acknowledged: urban/built-up and rocky areas not included due to lack of soil data for predictions.

## Third-party datasets and provenance
- AIC, GAMM, KRGS, MLRF maps sourced from EIDC or provided by data custodians (with access restrictions noted for some maps).
- LUCAS (ESDAC), OCTOP (ESDB), SoilGrids (ISRIC) with public references.
- Detailed citations provided for each contributor and the underlying maps (including DOIs and project reports).

## Usage, attribution, and citation
- Derived dataset intended to accompany the eight primary SOC maps for national-scale comparison and uncertainty analysis.
- When using the dataset, cite the corresponding primary maps and data providers as specified (CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF, ISRIC-2017, ISRIC-2020, LUCAS, OCTOP), and refer to the Sci. Rep. 2022 paper for context.
- Version date: 09/12/2022
- Lead contact: Christopher Feeney (corresponding author for data) at UKCEH

## Authorship and funding
- Authors: Christopher Feeney, Jack Cosby, David Robinson, Amy Thomas, Bridget Emmett, Pete Henrys (UKCEH)
- Funded under UK-SCAPE SOC-D project delivering National Capability; grant NE/R016429/1 from the Natural Environment Research Council.