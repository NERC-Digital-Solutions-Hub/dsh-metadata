# Supporting documentation for data: Mean and variability of topsoil organic carbon concentrations across Great Britain derived at 1 km resolution from an ensemble of eight digital soil maps

## Overview
- Presents a harmonised, 1 km resolution ensemble of eight GB topsoil organic carbon (SOC) maps.
- Produces per-grid-cell statistics (mean, variability) to assess agreement among maps and support soil and carbon-climate monitoring.
- Part of the UK-SCAPE SOC-D project, funded by the Natural Environment Research Council (Grant NE/R016429/1).

## Data scope and purpose for monitoring
- Geographic coverage: Great Britain (excluding Northern Ireland).
- Resolution: 1 km gridded data; 208,752 grid cells with complete eight-map coverage.
- Objective: quantify mean SOC and its variability across maps to aid environmental monitoring, model input, and policy-relevant assessments of soil carbon.

## Data sources and harmonisation
- Eight primary SOC maps used:
  - CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF (Countryside Survey GB data)
  - ISRIC-2017, ISRIC-2020 (SoilGrids)
  - LUCAS (Europe; ESDAC)
  - OCTOP (Europe; ESDAC)
- Maps originally use different depths; harmonised to GB extent, 1 km resolution, and OSGB1936 grid.
- ISRIC, LUCAS, and OCTOP data snapped/resampled to the GB 1 km grid; some maps required depth-adjustment to 0–15 cm.

## Depth handling and unit conversions
- Depth alignment to 0–15 cm across maps:
  - ISRIC-2017: uses 0, 5, 15 cm layers; mean for 0–15 cm via trapezium rule.
  - ISRIC-2020: uses 0–5 cm and 5–15 cm; weighted average for 0–15 cm.
  - LUCAS and OCTOP: converted to 0–15 cm using available specifications.
- Unit conversions:
  - ISRIC maps converted to g kg−1 (from dg kg−1) by dividing by 10.
  - OCTOP converted from % SOC to g kg−1 by multiplying by 10.
  - CSGB maps converted from LOI to SOC using a regression factor (5.5× LOI) to obtain g kg−1.
- Data cleaned to avoid physically impossible values (e.g., capped at ~550 g kg−1; negative SOC values reset to no data where needed).

## Quality control and data integrity
- QA performed on 19 Oct 2022:
  - Ensured identical resolution, extent, and CRS (EPSG:27700) across all maps.
  - All eight maps exist for each grid cell considered (no data handling for missing maps at a cell level).
  - Out-of-range SOC values corrected; CSGB-AIC negatives set to no-data where applicable.
  - Reported ranges: Mean SOC 19.2–479.3 g kg−1; SD 2.8–239.8 g kg−1.
- Grid metadata: 1 km OS grid, 591 × 1026 cells, OSGB 1936 British National Grid extents.

## Data structure and interpretation
- Deliverable: a single GeoTIFF file SOC_map_summaries.tif with seven bands, covering GB at 1 km resolution.
- Band descriptions:
  1) Mean SOC (g kg−1) across the 8 maps; cells with any missing map are no-data.
  2) Standard deviation (g kg−1) across the 8 maps.
  3) Coefficient of variation (CoV) = SD/Mean.
  4) Signal-to-noise ratio (SNR) = Mean/SD (inverse of CoV).
  5) Most deviant map from the mean at each grid cell (coded 1–13; includes ties).
  6) Greatest deviation from the mean expressed as a percentage difference.
  7) Greatest deviation from the mean expressed as the number of SDs exceeded.
- Band 5 coding: integers 1–13; mapping provided to identify which map(s) are most deviant. Some cells show ties (e.g., ISRIC-2020 vs OCTOP; multiple tied pairs).

## Most deviant map identification
- The “Most deviant map” band flags which of the eight primary maps most diverges from the ensemble mean at each cell.
- In cases of ties, multiple maps may be reported as equally deviant (e.g., ISRIC-2020 & OCTOP tied).

## Third-party datasets and provenance
- CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF, LUCAS, OCTOP, ISRIC-2017, ISRIC-2020 referenced with source links.
- Some maps have access restrictions (e.g., CSGB-KRGS restricted due to potential reverse engineering of sampling points).
- Citations recommended for using the derived data, corresponding to each map source.

## How this supports monitoring and use
- Provides standardized, transparent metrics to compare national-scale SOC predictions and their uncertainty.
- Enables assessment of spatial agreement and drivers of disagreement across multiple map products.
- Useful for calibrating and validating soil carbon in land-surface models and for policy-relevant monitoring of soil carbon stocks over time.
- Encourages data reuse and cross-map analyses by documenting data structure, QA steps, and metadata.

## Documentation, versioning, and authors
- Version date: 09/12/2022.
- Authors: Christopher Feeney, Jack Cosby, David Robinson, Amy Thomas, Bridget Emmett, Pete Henrys (UKCEH).
- Data collection/generation context: UK-SCAPE SOC-D project; National Capability; funded by NERC (Grant NE/R016429/1).
- Suggested citations for derived datasets and underlying maps provided within the document.