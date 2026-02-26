# Supporting documentation for data: Mean and variability of topsoil organic carbon concentrations across Great Britain derived at 1 km resolution from an ensemble of eight digital soil maps

## Overview
- Compares eight published topsoil organic carbon (SOC) maps for Great Britain (GB) to quantify mean, variability, and drivers of disagreement at 1 km resolution.
- Provides a single geotiff with seven data layers summarising ensemble statistics and map-deviation information to support understanding of national-scale SOC predictions and their uncertainty.

## Data sources (the eight primary maps)
- Countryside Survey GB (CSGB) maps derived from: 
  - CSGB-AIC (UKCEH; CS)
  - CSGB-GAMM (UKCEH; CS)
  - CSGB-KRGS (UKCEH; CS)
  - CSGB-MLRF (UKCEH; CS)
- ISRIC SoilGrids-derived maps:
  - ISRIC-2017 (global; 250 m)
  - ISRIC-2020 (global; 250 m)
- LUCAS (ESDAC; Europe; 500 m)
- OCTOP (Europe; 1000 m)
- Depth scope: all maps cover top 0–15 cm (LUCAS 0–20 cm; OCTOP 0–30 cm; others 0–15 cm)

## Data processing and harmonisation
- Maps were harmonised to a common GB extent, 1 km resolution, and a common CRS (EPSG:27700). 
- ISRIC-2017/ISRIC-2020, LUCAS, and OCTOP were snapped to the 1 km OS grid and resampled to 1 km using zonal statistics within ArcGIS and then converted to consistent units/depths where required.
- Depth adjustments: ISRIC-2017 and ISRIC-2020 depths converted to 0–15 cm; other maps already aligned to 0–15 cm (except LUCAS 20 cm and OCTOP 30 cm were adjusted as described).
- Unit conversions:
  - ISRIC maps (SOC in dg/kg) divided by 10 to convert to g/kg.
  - OCTOP (% SOC) multiplied by 10.
  - CSGB-KRGS and CSGB-MLRF (% LOI) multiplied by 5.5 to convert to g/kg (based on regression between LOI and SOC).
- Data quality checks and outlier handling:
  - Negative SOC values reset where necessary (CSGB-AIC adjusted).
  - Cells with insufficient data across all eight maps flagged as no data.
  - Exclusion of urban/built-up, rocky land cover where SOC cannot be reliably predicted.

## Data structure and content
- Dataset name: SOC_map_summaries.tif (single GeoTIFF with 7 bands; GB excluding Northern Ireland; ~1 km grid)
- Band descriptions:
  1) Mean SOC (g/kg) across the eight maps; no-data if any map missing
  2) Standard deviation (SD) of SOC across eight maps
  3) Coefficient of variation (CoV) = SD/Mean
  4) Signal-to-noise ratio (SNR) = Mean/SD
  5) Most deviant map from the mean at each grid cell (coded 1–13; corresponds to which map(s) most diverge)
  6) Greatest deviation from the mean expressed as a percentage difference
  7) Greatest deviation from the mean expressed as the number of SDs exceeded
- Band 5 coding: 1–13, with explicit mapping to maps (including tied cases)
- Maximum grid count: 208,752 cells with SOC predictions from all eight maps
- Notes:
  - If any map missing data for a cell, that cell is set to no data
  - Cells in urban/rocky areas removed from analysis

## Quality control and validation
- QA checks conducted 19/10/2022 prior to submission to EIDC:
  - Ensured identical spatial resolution/extents and CRS across all layers
  - Stacked layers into a single raster; verified cell counts, extents, and coordinate system
  - Confirmed all cells with data exist for all eight maps; no misinterpretation of zeros as no data
  - Verified SOC values fall within expected ranges (0–550 g/kg); corrected anomalies (e.g., negative values, implausible extremes)
  - Documented that 205 ties occurred where two maps were equally deviant; no ties among three or more maps

## Third-party datasets and attribution
- Sources and access details provided for all eight maps (CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF, ISRIC-2017, ISRIC-2020, LUCAS, OCTOP)
- Citations for data and methodological background included; some sources are not publicly released (e.g., certain CSGB maps)
- Guidance on how to cite the derived dataset and individual source maps when used in analyses

## How to use this dataset (analyst perspective)
- Uncertainty assessment:
  - Use CoV (band 3) and SNR (band 4) to identify regions with high disagreement or high agreement among maps
  - High CoV or low SNR indicates substantial inter-map variability; consider deeper investigation or weighting by map performance
- Identifying drivers of disagreement:
  - Band 5 reveals which map(s) most deviate from the ensemble mean at each cell; examine maps contributing to high SD/CoV in target areas
  - Band 6 (percent deviation) and Band 7 (SD-exceeded deviations) quantify magnitude of disagreement
- Data coverage and suitability:
  - Only cells with complete eight-map data are used for summary statistics; many cells may be missing in more data-sparse regions
  - Built-up/urban and rocky areas are excluded from the SOC estimates; use with caution in transitional zones
- Applications:
  - Benchmark SOC predictions for model evaluation or calibration in national-scale land surface/climate studies
  - Inform prioritisation of ground-truth sampling by targeting regions with high map disagreement
  - Support uncertainty-aware policy analyses by incorporating ensemble variability into decision frameworks
- Reproducibility and reuse:
  - The 7-band SOC_map_summaries.tif provides a ready-made summary of ensemble statistics
  - For deeper insights, consult the underlying eight maps and their methodological references listed in the documentation

## Limitations and considerations
- GB-wide analyses exclude Northern Ireland and may not capture local-scale SOC patterns below 1 km resolution
- Variability reflects differences in map methodologies and input datasets; not all sources are equally recent or regionally representative
- Some maps have gaps or data suppression due to sampling or data-sharing constraints
- Depth and resolution differences across source maps necessitated unit and depth adjustments, which introduce additional uncertainties

## Access, usage, and citations
- Dataset is designed for GIS-compatible analysis (GeoTIFF with 7 bands)
- When using the derived dataset, cite the ensemble methodology and individual source maps as provided in the documentation
- Authors and contact for data-related inquiries: Feeney et al., UKCEH (corresponding authors listed in the documentation)