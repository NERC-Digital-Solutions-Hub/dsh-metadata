# Supporting documentation for data: Mean and variability of topsoil organic carbon concentrations across Great Britain derived at 1 km resolution from an ensemble of eight digital soil maps

## Overview
- Purpose: Create an ensemble view of topsoil organic carbon (SOC) across Great Britain by harmonising eight published maps to a common 1 km grid, enabling analysis of mean values and variability, and identifying drivers of disagreement between maps.
- Context: Part of the UK-SCAPE SOC-D project delivering National Capability, funded by the Natural Environment Research Council (Grant NE/R016429/1).

## Data sources and maps
- Eight primary maps included in the ensemble:
  - Countryside Survey GB maps: CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF
  - ISRIC SoilGrids maps: ISRIC-2017, ISRIC-2020
  - LUCAS map
  - OCTOP map
- Maps originate from diverse methods (pedotransfer rules, upscaling, kriging, machine learning) and cover the top 0–15 cm (with some exceptions in depth coverage).

## Methods and harmonization
- Alignment and harmonization:
  - All maps harmonised to GB extent, 1 km grid, and OSGB:27700 coordinates.
  - ISRIC and LUCAS maps snapped/resampled to the 1 km OS grid; some maps required depth adjustments to obtain 0–15 cm SOC values.
- Depth and unit processing:
  - ISRIC-2017/2020 SOC depths converted to 0–15 cm using depth-specific rules (mean or weighted averages).
  - Unit conversions applied where maps used different units (e.g., %SOC, g/kg, LOI).
- Data quality and range checks:
  - Values corrected to stay within plausible SOC ranges; negative values in CSGB-AIC set to no-data.
  - Maps with no-data cells filtered to avoid misinterpretation.
- Data coverage:
  - Excluded urban/built-up and rocky areas where SOC predictions are unreliable.

## Data structure and file
- File: SOC_map_summaries.tif (single geotiff raster)
- Coverage: Great Britain (excluding Northern Ireland) at 1 km resolution
- Bands (7 total), each representing a specific statistic or annotation:
  1. Mean SOC (g kg-1) across all 8 maps; cells with missing data from any map are set to no-data
  2. Standard deviation (SD) of SOC across the 8 maps
  3. Coefficient of variation (CoV) = SD / mean
  4. Signal-to-noise ratio (SNR) = mean / SD
  5. Most deviant map from the mean at each grid cell (coded 1–13 to indicate which map(s) deviate most)
  6. Greatest deviation from the mean expressed as a percentage difference
  7. Greatest deviation from the mean expressed as the number of SDs exceeded
- Grid and data characteristics:
  - 208,752 grid cells where all eight maps have data
  - Bands 5–7 provide attribution to the map(s) driving disagreement and magnitude of deviations

## Quality control
- Conducted on 19/10/2022 prior to submission:
  - Confirmed identical resolution, extent, and CRS (EPSG:27700)
  - All bands stacked into a single raster; consistent cell size and extent
  - Verified no-data handling ensured 0 g kg-1 values were not misinterpreted as missing
  - SOC values within expected ranges; negative values reset to no-data where appropriate
  - Documented that cells with data from all eight maps were used to compute statistics

## Third-party datasets
- Sources and references for each primary map are provided (including CSGB maps, ISRIC SoilGrids, LUCAS, and OCTOP)
- Links and citations are included for proper attribution and reuse

## Using the data and citation
- Potential uses:
  - Explore spatial agreement and uncertainty across multiple SOC maps
  - Identify where certain maps disproportionately drive variability
  - Support policy, land management, and modelling efforts with an uncertainty-aware SOC baseline
- How to cite:
  - For each map source (CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF, ISRIC-2017, ISRIC-2020, LUCAS, OCTOP)
  - Primary data paper: Feeney et al. 2022 (Sci. Rep.) for background, with DOI provided in the document
- Data product note:
  - The dataset enables self-contained examination of mean SOC and its variability across Great Britain at 1 km resolution, along with per-cell attribution of driving maps and magnitude of deviations.

## Related publications
- Feeney, C. J. et al. Multiple soil map comparison highlights challenges for predicting topsoil organic carbon at national scale. Sci. Rep. 12:1379 (2022) – additional methodological detail and analysis.