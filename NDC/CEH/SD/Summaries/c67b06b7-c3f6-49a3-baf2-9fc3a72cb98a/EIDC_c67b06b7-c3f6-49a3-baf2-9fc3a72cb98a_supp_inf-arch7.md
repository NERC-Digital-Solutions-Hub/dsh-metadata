# Overview

- A vegetation survey in Sabah, Malaysian Borneo, sampled living vegetation across 18 sites (14 fragmented RSPO oil palm-set as conservation set-asides; 4 large contiguous forest sites) during July–November 2017.
- Total: 49 plots in 18 sites, using a nested plot design (30 m radius main plots with 20 m and 5 m subplots) to capture trees, lianas, ground vegetation, coarse woody debris, and habitat/landscape variables.
- Data are provided in six CSV files and are designed for map-based, spatial analyses and landscape-scale comparisons.

## Data files and key contents

- CWD.csv: coarse woody debris (≥10 cm) measurements with diameter, length/height, decay class, and subplot context.
- lianas.csv: diameter at breast height (dbh) for lianas ≥10 cm entering tree crowns and associated tree information.
- seedlings_groundveg.csv: ground vegetation and tree seedlings within eight 1x1 m quadrats per plot; includes morphospecies codes and native/exotic status.
- sites_habitat.csv: plot-level habitat and landscape context, including coordinates, elevation, disturbance history, forest type, fragmentation status, fragmentation dates, and extensive canopy/landscape metrics.
- soil.csv: soil chemical and physical properties (pH, phosphorus, nitrogen, carbon, moisture, C:N ratios) for each plot.
- trees.csv: individual tree/palm stems with dbh, height (where measured), taxonomic identification, lianas per stem, and subplot context.

## Spatial design and sampling framework

- Study footprint: 18 sites across Eastern Sabah (maximum site distance ~192 km apart; ≥1.5 km between sites to reduce spatial autocorrelation).
- Plot configuration: in fragmented sites, 2–3 circular plots per site (30 m radius; 0.28 ha per plot) with first plot 25 m from forest edge and subsequent plots ≥25 m from edges; in continuous forest sites, 2–3 plots arranged to sample interior conditions.
- Nested sampling: in each 30 m plot:
  - main plot: trees/palms ≥25 cm dbh (30 m radius)
  - 20 m subplot: trees/palms 10–25 cm dbh
  - 5 m subplot: trees 2–10 cm dbh
  - eight 1x1 m quadrats for ground vegetation and seedlings (located 25 m from plot center on random bearings)
- Fragmentation metrics (landscape context):
  - UAV-derived land cover within buffers (0.1–2 km) around each plot to quantify surrounding forest vs. oil palm
  - Forest area, edge index (forest–oil palm boundary cells per forest area), distance to nearest forest–oil palm edge, and time since fragmentation
  - Comparisons also calculated for continuous forest plots using Google Earth imagery

## Measurements and data collection details

- Living trees and palms: dbh measurements by size class and crown height estimates; species identification in field, with herbarium verification for unidentified specimens.
- Coarse woody debris: size-classified (≥25 cm and 10–25 cm), decay class (1–5), and orientation (fallen, standing, hanging); length/height measurements and boundary handling described.
- Lianas: dbh of lianas ≥10 cm that entered crowns of recorded trees; linked to associated tree stem data.
- Ground vegetation: eight 1x1 m quadrats per plot; morphospecies coded, with native/exotic status, and voucher details.
- Habitat/topography: leaf litter depth, canopy cover from densiometer readings (four directions), GPS-based coordinates and elevation, and slope in four directions.
- Soil: eight parameters (pH, total and available P, total N, total C, organic C, C:N ratios) from five soil cores per plot; standard sample processing and analysis.
- Data identifiers and structure: Site_name, Site_plot_code, dates, and standardized coding schemes (e.g., F a P b) to link datasets.

## Data quality and processing notes

- Protocols mostly follow established methods and are described with references (e.g., RAINFOR, standard forest carbon protocols).
- Height estimates obtained by eye were cross-validated with a subset using a clinometer; consistent observer practices applied per variable.
- Biodiversity analyses should exclude palms and lianas (not identified) from species diversity metrics; ground vegetation morphospecies were identified to genus/species where possible.
- Forest cover derived from densiometer readings: canopy cover = 100 − (Forest_cover readings × 1.04).

## GIS-relevant use and integration guidance

- Spatial data readiness:
  - Plot-level coordinates (Latitude, Longitude, Elevation, Slope) enable mapping and integration with other spatial layers.
  - Site_plot_code and Site_name provide linkages across all six CSV files.
  - Distances and fragmentation metrics (Nearest_edge_m, ForArea_buffer X m, ForEdge_buffer X m, ForEdge_buffer X m_index) facilitate landscape-scale analyses at multiple spatial scales (100–2000 m buffers).
- Landscape context:
  - Use UAV-derived land cover within buffers to classify plots as surrounded by forest vs. oil palm and to quantify edge density and boundary proximity.
  - Time-since-fragmentation data allow temporal analyses of fragmentation impact when combined with habitat measurements.
- Canopy and forest structure:
  - Canopy/forest cover can be computed from densiometer data for spatial modelling of light and vegetation structure.
  - Slope and elevation can be used to model microclimate and habitat suitability across plots.
- Data integration opportunities:
  - Combine soil properties, CWD, liana load, and tree metrics with canopy/land cover maps for biodiversity and carbon stock assessments.
  - Framework supports map-based data products for policy briefings, conservation planning, and stakeholder-facing visualisations.

## Endnotes and caveats

- Biodiversity analyses should exclude lianas and palms (not identified) to avoid biased diversity estimates.
- Some height data and precise species identifications are incomplete; use height models or imputation where appropriate and document exclusions.
- Data capture occurred across a broad Southeast Asian landscape; ensure alignment of coordinate reference systems when integrating with external GIS datasets.

## References (methodological context)

- Standard methods for tropical forest plots and biomass estimation cited, including RAINFOR field manuals and related vegetation measurement protocols; documentation provides data-specific methodological details and references for background techniques.