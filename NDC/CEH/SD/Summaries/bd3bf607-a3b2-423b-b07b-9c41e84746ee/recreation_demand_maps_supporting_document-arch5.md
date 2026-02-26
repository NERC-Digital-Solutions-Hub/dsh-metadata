# Predicted recreation demand across the UK

## Overview
- Maps predicted local recreation demand (a proxy for cultural ecosystem services) at 250 m resolution across the UK.
- Demand is modeled as the total number of projected visits to a target grid cell, based on a bespoke version of the universal law of human mobility.
- Outputs are spatial rasters representing estimated visits per 250 m grid cell under different visit frequencies and with/without attractiveness adjustments.

## Data inputs and structure
- Population density: WorldPop 2020 unconstrained density (≈75 m) regridded to 250 m for UK sources.
- Travel distance: combination of long-range cost-weighted distance (2.5 km scale) along roads (OpenStreetMap) and short-range Euclidean distance to nearest road.
- Road speeds and cost-weights: speeds by road type (from Statista 2015) converted to per-cell cost weights; remote cells assigned high weight to reflect walking.
- Attractiveness: based on UK terrestrial protected areas (UNEP-WCMC 2022) using IUCN categories II–V to define attractiveness; higher protection generally more attractive. Attractiveness scaled so II = 1, III–V = scaled values, and No Status = 0.2.
- Urban areas: target cells removed to focus on wider landscape; urban cells still used as potential sources.
- Outputs: six raster datasets in TIFF format, each 250 m resolution, British National Grid (EPSG 27700), 0.9996 scale factor, 2854 x 5200 grid:
  - Weekly_250m_NonUrban_Attrac.tif
  - Weekly_250m_NonUrban_NoAttrac.tif
  - Monthly_250m_NonUrban_Attrac.tif
  - Monthly_250m_NonUrban_NoAttrac.tif
  - Yearly_250m_NonUrban_Attrac.tif
  - Yearly_250m_NonUrban_NoAttrac.tif
- Reproducibility: calculations performed in ArcGIS Pro v2.9.0 and Matlab v7.14.0.739; code available at github.com/dhooftman72/RecreationalValue.

## Methodology (key points)
- Core equation (Demand_i): attractiveness of target cell i multiplied by the sum over all source cells j of [Population_j / (Frequency_ij × TravelDistance_ij)^α], with α = 2.17 (following Schläpfer et al., 2021).
- Frequency scenarios: visits per year (1), per month (12), and per week (52) to reflect three plausible engagement levels.
- Attractiveness integration: applied via a weighted factor based on protected-area status; datasets include both with attractiveness (Attrac) and without (NoAttrac) for comparison.
- Distance calculations:
  - Long-range distance: 2.5 km gridded cost-weighted distance using road networks (GB) and offshore connections; based on OpenStreetMap data.
  - Short-range distance: Euclidean distance to nearest road within a 250 m cell.
- Urban filtering: target cells in urban areas removed using the 2020 UKCEH Land Cover Map to avoid urban bias.
- Thresholding: calculated visit densities below 1 per km² are rounded down to zero (value 0 denotes effectively <0.5 visits per km²).
- Parameter data sources and assumptions: population density (WorldPop 2020), travel speeds by road type (Statista 2015), protected areas (UNEP-WCMC 2022); frequency assumptions made where visit data are unavailable.

## Data outputs and interpretation
- Outputs express the estimated number of visits per 250 m grid cell for a given frequency (weekly, monthly, yearly) under two conditions (with and without attractiveness).
- The approach provides a coarse but scalable view of recreation demand across non-urban UK landscapes, useful for evaluating CES supply-demand balance and informing planning decisions.

## Reproducibility, provenance and quality control
- Data sources are peer-reviewed or widely accepted (WorldPop, UK Land Cover Map, UNEP-WCMC protected areas, OpenStreetMap).
- Full internal team review and external peer review completed for publication.
- Data processing and transformation steps are documented, with scripts and maps generated as part of the study; the underlying code is available on GitHub.
- Outputs are standardized in TIFF rasters with explicit metadata (description includes frequency, attract/NoAttrac, and urban exclusion).

## Governance, stewardship and reuse considerations for Data Stewards
- Metadata and cataloging
  - Include: data title, purpose, spatial extent, resolution (250 m), projection (EPSG 27700), units (visits per grid cell), frequency definitions (weekly/monthly/yearly), attractiveness adjustment status, urban filter, input data sources, α value (2.17), and date of generation.
  - Link to source datasets (WorldPop 2020, UKCEH Land Cover Map 2020, UNEP-WCMC Protected Areas, OSM road network) with version/date stamps.
  - Document the methodology and any assumptions (e.g., visit frequencies, distance calculations, attractiveness weights by IUCN category).
- Versioning and updates
  - The current outputs are based on 2020 land cover and associated inputs; establish a schedule for updating inputs (e.g., population grids, protected-area status, road networks) and re-running the model.
  - Maintain versioned releases of all six rasters and update notes describing changes in inputs or parameters.
- Access, licensing and reuse
  - Ensure licensing enables reuse in research and planning contexts; clearly state permissions and any restrictions.
  - Provide clear provenance links to all input data and to the code used for reproduction.
- Data quality and validation
  - Maintain traceability from input data to outputs; preserve intermediate datasets where feasible to aid auditing.
  - Acknowledge the limitations: model-based predictions, assumptions about visit frequency, sensitivity to input data quality, and potential changes in road networks or protected-area designations.
- Storage and discoverability
  - Store rasters with descriptive filenames (as used in the study) and centralized metadata records in the data catalog.
  - Ensure discoverability by linking to the corresponding publication and GitHub repository for reproducibility.

## Practical implications and cautions for use
- Useful for understanding spatial patterns of potential outdoor recreation demand and for informing CES-related planning and governance decisions.
- Should be interpreted as model-informed estimates rather than exact counts; the attractiveness component relies on protected-area designations and is subject to policy and land-management changes.
- Computationally intensive to reproduce fully; rely on provided rasters for immediate use, or re-run with updated inputs if needed.