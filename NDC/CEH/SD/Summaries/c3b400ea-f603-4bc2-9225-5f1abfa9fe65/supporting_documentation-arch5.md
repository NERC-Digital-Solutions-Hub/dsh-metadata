# Supporting documentation for data: Mean and variability of topsoil organic carbon concentrations across Great Britain derived at 1 km resolution from an ensemble of eight digital soil maps

## Overview
- Purpose: Document the dataset summarising topsoil organic carbon (SOC) concentrations across Great Britain (GB) at 1 km resolution, derived from an ensemble of eight published digital soil maps.
- Context: Part of the UK-SCAPE SOC-D project delivering National Capability; aims to support understanding of soil carbon at national scale and its use in land surface/climate modelling.
- Scope: GB (excluding Northern Ireland); maps harmonised to a common grid and extent; data produced to enable assessment of agreement and disagreement among map products.

## Data content and structure
- Dataset file: SOC_map_summaries.tif
- Spatial coverage and resolution: GB at 1 km resolution; excludes urban/rocky land covers where predictions are unreliable.
- Bands (7 total) and meaning:
  1) Mean SOC (g kg-1) across the 8 maps; cells with missing data in any map are set to no data.
  2) Standard deviation (SD) of SOC across the 8 maps.
  3) Coefficient of variation (CoV) = SD/Mean.
  4) Signal-to-noise ratio (SNR) = Mean/SD (inverse of CoV).
  5) Most deviant map from the mean at each grid cell (coded 1–13; some ties).
  6) Greatest deviation from the mean expressed as a percentage difference.
  7) Greatest deviation from the mean expressed as the number of SDs exceeded (relative to band 2).
- Units and value ranges:
  - SOC in g kg-1; typical range 0–550 g kg-1.
  - Band 5–7 provide metadata on which map drives disagreement and the magnitude of deviations.
- Data accessibility: Intended for GIS use; the dataset is designed to support quick assessment of map agreement and outliers.

## Data generation and harmonisation
- Source maps (the 8 primary maps):
  - CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF (Countryside Survey-derived)
  - ISRIC-2017, ISRIC-2020 (SoilGrids)
  - LUCAS (European soil dataset)
  - OCTOP (Europe-wide soil carbon dataset)
- Depth coverage and processing:
  - Most maps cover the top 15 cm; LUCAS is 20 cm; OCTOP is 30 cm.
  - SOC values converted to 0–15 cm where necessary (ISRIC-2017 via depth band weighting; ISRIC-2020 via weighted average of 0–5 cm and 5–15 cm bands).
- Harmonisation steps:
  - All maps aligned to GB extent, 1 km grid, CRS EPSG:27700 (OSGB 1936 / British National Grid).
  - Snap/align ISRIC, LUCAS, and OCTOP to the 1 km GB OS grid to ensure exact alignment with Countryside Survey maps.
  - Where required, simple translations used to snap grids (no resampling within grid cells that could distort data).
- Data preparation:
  - 0 g kg-1 values are not treated as missing unless explicitly flagged; negative SOC values in CSGB-AIC are set to no data.
  - Unit adjustments applied to ensure consistent units across maps (e.g., ISRIC and OCTOP adjustments; some maps converted from % to g kg-1 or vice versa using established conversions).

## Quality control and validation
- Pre-submission checks (as of 19 Oct 2022):
  - All layers have identical resolution/extent and CRS (EPSG:27700).
  - Bands stacked into a single raster; GIS-ready with consistent cell counts and extents.
  - Data completeness: analyses restricted to cells with data from all 8 maps; no data handling clearly distinguished from zero-value predictions.
  - Value checks: SOC values constrained to plausible ranges (0–550 g kg-1); negative values reset to no data when applicable.
  - Documentation of outliers: identification of most deviant maps per cell; 205 ties observed across 5 map-pair combinations.
- Data integrity:
  - Bands 5 (“Most deviant map”) encoded 1–13; ties documented (e.g., ISRIC-2020 & OCTOP tied, etc.).
  - Summary statistics (mean, SD, CoV, SNR) reflect inter-map variability and agreement across the ensemble.

## Third-party datasets and provenance
- Source maps and access/links:
  - CSGB-AIC and CSGB-GAMM maps from EIDC with DOIs.
  - CSGB-KRGS map supplied privately due to concerns about reverse-engineering precise sampling locations.
  - CSGB-MLRF map (unpublished at the time) with anticipated availability later on EIDC.
  - LUCAS and OCTOP maps from ESDAC (ESDB) sources.
  - SoilGrids maps (ISRIC) from ISRIC (version 1.0 and 2.0).
- Usage and citations:
  - If using the derived SOC_map_summaries dataset, cite the primary source maps as listed (CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF, ISRIC-2017, ISRIC-2020, LUCAS, OCTOP) with their respective references.
  - Key referenced publications for background and methods are provided (e.g., Sci. Rep. 2022 paper on multiple soil map comparison) and should be cited where relevant.

## Governance, access, and licensing considerations
- Data governance:
  - Dataset represents a synthesis of eight maps; uses a transparent, auditable workflow with explicit handling of data compatibility and data gaps.
  - Documentation includes detailed methodology, quality checks, and data structure metadata for reproducibility.
- Access restrictions:
  - Some third-party maps (e.g., CSGB-KRGS) have access limitations due to sensitivities around precise sampling locations.
- Maintenance and updates:
  - Version dated 09/12/2022; described as a harmonised ensemble snapshot rather than a continuously updated product.
- How to cite and reuse:
  - Users should cite the 8 primary maps individually as well as the SOC_map_summaries.tif dataset when deriving analyses or figures.
  - Provide attribution to all contributing maps and the primary method publication for background context.

## Implications for data stewardship
- Encourages adoption of harmonisation and interoperability practices when combining diverse map products.
- Highlights the importance of documenting data lineage, transformation steps, and quality checks to support reuse and governance.
- Demonstrates a practical approach to revealing map-level uncertainties and drivers of disagreement, aiding transparent data discovery and interpretation.
- Underlines data access considerations and the need to respect restrictions on sensitive third-party datasets.