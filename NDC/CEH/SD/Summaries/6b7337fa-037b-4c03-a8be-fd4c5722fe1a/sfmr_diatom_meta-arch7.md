# Diatom data from the South Fork McKenzie River in Oregon, USA

## Overview
- Monitoring dataset assessing diatom response to wildfire in restored vs. unrestored sites on the South Fork McKenzie River.
- Location: South Fork McKenzie River, Oregon, USA (lat/long provided: 44.17, -122.30).
- Data are organized around two CSV files: (1) SFMR_Diatom_Data with sample-level diatom and site characteristics; (2) a description file detailing key column names for the main data file.
- Sampling occurred post-wildfire (Holiday Farm Fire Sept 2020); data collected in February 2022 (n=10 sites) and September 2021 (n=13 sites).

## Dataset structure and contents
- SFMR_Diatom_Data contains columns for:
  - Status (restored or unrestored); date.coll and year; habitat type (e.g., pool, riffle, off-channel); Season; transect; site.id.
  - Spatial info: leftLon, leftLat, rightLon, rightLat (transect endpoints and coordinates for sampling).
  - Environmental and sampling metrics: AI (autotrophic index), mean.depth (cm), mean.velocity (m/s), rock1.area.cm2, rock2.area.cm2, rock3.area.cm2.
  - Diatom data: genus-level counts for numerous genera (e.g., Tabellaria, Epithemia, Fragilaria, Hannaea, Melosira, Nitzschia, Cocconeis, Gomphonema, Diatoma, Navicula, Achnanthes, Reimeria, Cyclotella, Cymbella, Frustulia, Synedra, Rhicosphenia, Amphora, Caloneis, Surirella, Asterionella, and others).
  - Additional fields include date.coll, year, habitat, transect, and the per-site health/treatment status.
- Data collection details:
  - 23 sites total: 10 sites in February 2022 (5 restored, 5 unrestored) and 13 sites in September 2021 (7 restored, 6 unrestored).
  - Transect labeling: restored zone includes T1 and T2; unrestored zone includes T8, T9, T10, T11 and T8.5.
- Column naming reference file provides descriptions for the main data file’s columns.

## Spatial and temporal coverage
- Post-fire sampling across restored and unrestored reaches of the South Fork McKenzie River.
- Sampling dates: February 2022 and September 2021.
- All sites are within the study area affected by the Holiday Farm Fire (Sept 2020).

## Sampling methodology and measurements
- Periphyton sampling:
  - Three rocks sampled across each transect, composited; transect is the sample unit.
  - At each location, periphyton scrubbed from five cobbles with a toothbrush, rinsed, and composited into a single sample, then split into three subsamples.
  - One subsample preserved in 37% formalin for diatom composition; two subsamples analyzed for chlorophyll a (Chl a) and ash-free dry mass (AFDM).
  - Diatoms counted to genus level; a minimum of 500 diatom valves counted per sample.
- Biomass characterization:
  - Autotrophic index (AI) calculated as the ratio of organic mass per cm2 in periphyton to the mass of chlorophyll a per cm2 in periphyton.
  - Proportion of algae biomass characterized as % Chl a within periphyton AFDM.
- Quality control: diatoms sampled and counted following standard laboratory procedures; robustness ensured with the 500-valve minimum per sample.

## Data use and GIS relevance
- Provides spatially explicit data for mapping restored vs. unrestored sites, transect locations, and periphyton metrics.
- Enables analysis of diatom community composition by genus across habitat types (pool, riffle, off-channel) and environmental context (depth, velocity, rock surface area).
- Useful for overlaying with wildfire impact data, post-fire recovery assessments, and restoration effectiveness evaluations.

## Notes and methodology references
- Collection and analysis align with standard methods for periphyton and diatom routine sampling (e.g., Baird et al. 2017; Kelly et al. 1998).
- Data include explicit metadata on sampling dates, habitat, transects, and site identifiers to support reproducibility and GIS-driven analyses.