# Rationale Contamination of waterbodies in urban areas with FIOs from diffuse and point sources is of significant concern to human health, as well as waterbody quality and ecology, due to the potential for exposure to a large audience of formal and informal recreational users.

## Aim and scope
- Examine spatial patterns of fecal indicator organisms (FIOs) and their drivers in water and sediment across lakes in an urban environment.
- Assess how connectivity to multiple vectors varies spatially and temporally.
- Support data-informed understanding and potential public health and ecological implications.

## Study areas and contextual information
- Location: Greater Glasgow conurbation, central Scotland; rural–urban land cover gradient.
- Sampling timeline: Summer (July) with 6 sites; Winter (December) with 15 sites (including all summer sites).
- Sampling consistency: Samples collected 3 hours after sunrise; bird surveys conducted for an hour at each site.
- Physical variables (derived from UK Lakes Portal): altitude, area, catchment size, perimeter, ratio of waterbody to catchment area, shoreline development index.
- Water chemistry (in situ): conductivity, dissolved oxygen, oxygen saturation, pH, temperature, alkalinity (Hach HQ40d, Hanna HI-755); 500 ml subsample filtered for lab analysis of major nutrients and metals; chlorophyll a from filters.
- Existing data: Where available, SEPA summer data used for consistency.
- Land use around waterbodies: 100 m, 500 m, and 2 km buffers using CEH Land Cover Map 2015, with 21 classes collapsed into composites (urban, agricultural, wetland). Land use proportions calculated within each buffer/catchment.

## FIO sampling and analysis
- Spatially dispersed paired water and sediment samples per lake; number of cores per lake scaled to lake size (max 60 for largest lake, 89 ha).
- For each sample point: water depth recorded; GPS coordinates captured; distance to shore calculated via GIS (QGIS); distance to island considered if applicable.

## Sediment sampling
- Gravity corer used to extract lake bed sediment; top 5 cm stored separately and kept at 4°C.
- E. coli in sediment: detachment in PBS, enumeration on MLGA agar to count CFU per g (sediment dw).
- Bacteria testing in sediment: three subsamples pooled per time/position; samples enriched in LB broth and incubated to test for Campylobacter, I. enterococci, and E. coli including 0157; CFU per g dw reported after incubation.
- Sediment moisture and organic content: moisture by weight loss after drying; organic content by LOI (550°C).

## Water sampling
- Water samples before sediment sampling; collected ~30 cm below surface.
- Filtration approach: two volumes (100 ml, 10 ml, 1 ml) filtered and plated on MLGA agar; incubated at 37°C for 24 h; results reported as CFU per 100 ml.

## Indicative results and interpretation
- Spatial maps (kriging in R) show FIO hotspots in both sediment and water.
- Hotspots linked to bird presence and point sources (e.g., wastewater treatment plants); patterns variable across time and within lakes.
- Spatial structuring analysis (semi-variance) indicates hotspots are relatively localized with limited evidence of strong, consistent spatial decay; no uniform periodicity observed.
- Example site pairings: Strathclyde Loch and Bardowie Loch illustrate differing hotspot patterns and seasonal dynamics.

## Appendix and data documentation
- Appendix lists major nutrients and metals measured in each 500 ml water subsample.
- Field name descriptions for Sediment_and_water_data_from_Glasgow.csv, including:
  - season, site, sample, x, y, depth, turbidity
  - waterecoli, coliform, totcolif, noenrich, ecolised, entero, campy
  - island_dist, loi (organic matter), DO2, pH, Temperature, EC, Ca, K, Mg, Na
  - TP, OC, TN, Fl, Cl, NO3, PO4, SO4
  - no_birds, bird_sp, Perimeter_m, Size_ha, Altitude, SDI, Shade, NearestNeighbour
  - Inflow, Outflow, Eastings_c, Northings_c
  - Landscape habitat percentages within 100 m, 500 m, and 2k buffers (Acid grassland, Arable, Improved grassland, Suburban, Urban, Woodland, Freshwater, and Sub_Urb)
- Geographic references: coordinates in British National Grid; distance metrics to shore and islands.
- References for data sources and methods: R (R Core Team 2018) and Land Cover Map 2015 (Rowland et al. 2017).

## Data support and reuse considerations
- The dataset enables spatial analysis of FIO distribution and drivers across urban lakes, with integrated environmental, land-use, and avian context.
- Facilitates cross-site comparisons and replication of kriging and spatial-structure analyses; supports linking microbial indicators with bird activity and point-source inputs.
- Ensure consistent units and coordinate reference (British National Grid) when merging with other datasets.
- Suitable as a template for end-to-end data pipelines: field collection, lab analysis, GIS integration, and spatial statistical analysis.