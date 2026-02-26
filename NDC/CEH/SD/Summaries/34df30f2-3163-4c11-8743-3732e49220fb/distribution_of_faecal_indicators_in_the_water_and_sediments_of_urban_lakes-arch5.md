# Rationale

## Aim and scope
- Investigates contamination of urban waterbodies by fecal indicator organisms (FIOs) from diffuse and point sources.
- Aims to examine spatial patterns of FIOs in water and sediment across lakes in urban Scotland, where connectivity to vectors varies over space and time.
- Contextualized within human health, waterbody quality, and ecology due to recreational exposure risk.

## Study areas and sampling design
- Sub-set of lakes in the Greater Glasgow conurbation, spanning a rural-urban land-cover gradient.
- Sampling seasons: summer (July) with 6 sites; winter (December) with 15 sites (including all summer sites).
- Consistent sampling time: 3 hours after sunrise to align with bird activity and UAV exposure.
- Bird surveys conducted at each site for an hour (numbers, identity, activity).
- Physical variables derived for each waterbody using the UK Lakes Portal (altitude, area, catchment size, perimeter, waterbody-to-catchment ratio, shoreline development index).
- Land use around each waterbody quantified within 100 m, 500 m, and 2 km buffers using CEH Land Cover Map 2015; 21 classes collapsed into broader groups (urban, agricultural, wetland).
- Land-use proportions calculated within each buffer and catchment.

## Sampling methodology
- Spatially dispersed paired water and sediment samples collected from each lake; up to 60 sediment cores per lake (dependent on lake size; largest lake 89 ha).
- At every sampling point: water depth recorded; GPS coordinates captured; distance to shore calculated (with special handling for islands using QGIS).

## Sediment sampling and analysis
- Sediment collected with a gravity corer, top 5 cm stored cold and processed promptly.
- E. coli attached to sediment particles detached with PBS; enumerated on MLGA plates after incubation.
- For certain bacteria (Campylobacter, I. enterococci, E. coli 0157, E. coli) three subsamples pooled to form a composite (1 g); incubated in LB broth and then plated for CFU enumeration after specified incubation steps.
- Results expressed as CFU per g of oven-dried soil; moisture and organic content determined via drying and LOI at high temperature.

## Water sampling and analysis
- Water samples collected ~30 cm below surface prior to sediment sampling.
- Filtration of three volumes (100 ml, 10 ml, 1 ml) onto MLGA plates; plates incubated and colonies counted after 24 h.
- Bacterial counts expressed as CFU per 100 ml water.

## Data processing, outputs, and interpretation
- Spatial mapping of FIOs via kriging to identify hotspots in water and sediment.
- Semi-variance analysis used to assess spatial structure (independence) of FIO concentrations.
- Findings indicate hotspots linked to bird activity and point sources (e.g., wastewater treatment plants), with patterns varying within and between water bodies.
- Generally limited evidence for strong, consistent spatial structuring across lakes; hotspots appear localized and do not show clear periodicity.
- Example site maps provided for Strathclyde Loch and Bardowie Loch (winter) and correlograms for winter and summer water column E. coli.

## Appendix and metadata
- Appendix lists major nutrients and metals derived from each 500 ml water subsample (specific instruments and determinants noted).
- Field name descriptions for Sediment_and_water_data_from_Glasgow.csv provided, detailing:
  - Seasonal, site, sample identifiers; coordinates (British National Grid); depth, turbidity.
  - Water column metrics: E. coli (waterecoli), coliforms, total coliforms, various dissolved ions and nutrients (Ca, K, Mg, Na, TP, OC, TN, NO3, PO4, NO2, SO4, Fl, Cl, etc.).
  - Sediment metrics: E. coli in sediment (noenrich, ecolised), Enterococci, Campylobacter; organic matter (LOI); sediment moisture content; distance metrics to shore and islands; habitat buffers (100 m/500 m/2 k) for various land-use classes.
  - Site characteristics: number of birds, bird species richness, site perimeter, size, altitude, shoreline diversity index, shade, nearest neighboring water body; inflow/outflow status.
  - Central coordinates for water chemistry measurements.
- Data sources and references:
  - R Core Team (2018) for R software.
  - Rowland et al. (2017) for Land Cover Map 2015 (GB).

## Data governance and stewardship considerations
- Data are spatially explicit, multi-entity collected across lakes, with standardized timing, sampling, and laboratory protocols.
- Metadata-rich file structure and a field-name dictionary facilitate discoverability, interpretation, and reuse.
- Portal and coordinate systems (British National Grid) support interoperability and integration with GIS workflows.
- Documentation includes explicit unit definitions, infection metrics (CFU counts), and methods, supporting quality assurance, provenance tracking, and reuse for governance and decision-making.