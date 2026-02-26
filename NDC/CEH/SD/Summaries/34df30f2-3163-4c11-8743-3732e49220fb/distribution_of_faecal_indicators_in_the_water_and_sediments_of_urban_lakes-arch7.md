# Rationale Contamination of waterbodies in urban areas with FIOs from diffuse and point sources

- Aim and scope
  - Examine spatial patterns of faecal indicator organisms (FIOs) and their drivers in water and sediment across urban lakes with variable connectivity to multiple vectors (birds, point sources, etc.).
  - Focus on an urban-subset within Greater Glasgow, Scotland, to understand spatial and temporal variability.

- Study areas and contextual information
  - Sub-set of lakes along a rural-urban gradient in the Greater Glasgow conurbation.
  - Sites surveyed in summer (July; 6 sites) and winter (December; 15 sites; includes all summer sites).
  - Bird surveys conducted for an hour at each site; sampling timed to ~3 hours after sunrise for consistency with bird activity and UAV exposure.
  - Physical variables sourced from the UK Lakes Portal: altitude, area, catchment size, perimeter, ratio of waterbody to catchment area, shoreline development index (SDI).
  - Water chemistry: in situ measurements (conductivity, dissolved oxygen, oxygen saturation, pH, temperature, alkalinity); major nutrients and metals analyzed in lab; chlorophyll a from sediment filters.
  - Land use: 100 m, 500 m, and 2 km buffers around each waterbody using CEH Land Cover Map 2015 (LCM2015); 21 land cover classes aggregated into urban, agricultural, and wetland composites.

- FIO sampling and analysis overview
  - Spatially dispersed paired water and sediment samples per lake; up to 60 sediment cores for the largest lake (89 ha).
  - A total of 770 unique sample points; GPS coordinates recorded; distance to shore calculated in GIS (QGIS).
  - Island considerations: distance to shore calculated both to nearest shoreline (including island) and to outer shoreline excluding the island.

- Sediment sampling and analyses
  - Sediment collected with a gravity corer; top 5 cm stored under cold conditions.
  - E. coli detached from sediment and quantified with MLGA plates; total coliforms and E. coli enumerated.
  - Pathogen/indicator testing: Campylobacter, Enterococci, and E. coli 0157 using multiple subsamples pooled for CFU per gram of oven-dried soil.
  - Moisture content (loss on drying) and organic content (loss on ignition) measured for sediment.

- Water sampling and analyses
  - Water samples collected ~30 cm below surface prior to sediment sampling; stored at 4°C; processed within 6 hours.
  - E. coli and other indicators quantified by filtering water samples in multiple volumes onto MLGA agar; results reported as CFU per 100 ml.

- Indicative results and interpretation
  - Spatial mapping (kriging in R) generated to illustrate FIO patterns in water and sediment; hotspots identified in both matrices.
  - Hotspots appear linked to bird distributions and potential point sources (e.g., wastewater treatment plants) but exhibit spatial and temporal variability within lakes.
  - Semivariogram-based semi-variance analyses show limited evidence for strong, broad spatial structuring; hotspots are relatively localized with no consistent periodicity.

- GIS and data processing methods (relevant for map-based data products)
  - Location and environmental data integrated via GIS: sample coordinates (British National Grid), distance-to-shore metrics, and land-use buffers.
  - Data sources linked: Lakes Portal-derived physical variables, LCM2015 land cover, bird counts, batch lab results.
  - Mapping outputs include hotspot maps for FIOs in water and sediment, and spatial structure diagnostics (correlograms).

- Appendix and data dictionary highlights
  - Appendix provides a comprehensive list of major nutrients and metals analyzed per 500 ml water subsample.
  - Data dictionary for Sediment_and_water_data_from_Glasgow.csv includes fields such as:
    - season, site, sample, x, y, depth, turbidity, waterecoli, coliform, totcolif, noenrich, ecolised, entero, campy
    - island_dist, 100Acid_grassland, 500Urban, 2kWoodland, Altitude, SDI, and habitat buffers (100, 500, 2k) with percentages
    - coordinates for central water chemistry sample and various habitat-related metrics
  - Additional fields cover hydrological connectivity (inflow/outflow), shore proximity, and surrounding landscape metrics.

- References
  - R Core Team (2018). R: A language and environment for statistical computing.
  - Rowland et al. (2017). Land Cover Map 2015 (25 m raster, GB). NERC Data Centre.