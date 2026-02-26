# Rationale Contamination of waterbodies in urban areas with FIOs from diffuse and point sources is of significant concern to human health, as well as waterbody quality and ecology, due to the potential for exposure to a large audience of formal and informal recreational users.

## Overview
- Study focus: Examine spatial patterns of fecal indicator organisms (FIOs) and their drivers in water and sediment across urban lakes with variable connectivity in Greater Glasgow, central Scotland.
- Temporal coverage: Sampling conducted in summer (July) and winter (December); all summer sites re-sampled in winter; timing standardized relative to bird activity.
- Primary aim: Map and understand how FIOs distribute across water and sediment and identify contributing factors (bird presence, point sources, hydrology).

## Study areas and contextual data
- Location: Sub-set of lakes within the Greater Glasgow conurbation, spanning rural–urban land cover gradients.
- Site characterization: 6 summer sites; 15 winter sites (including all summer sites); bird surveys conducted for an hour per site.
- Derived physical variables: Altitude, area, catchment size, perimeter, ratio of waterbody to catchment area, shoreline development index (SDI) from the UK Lakes Portal.
- Surrounding land use: 100 m, 500 m, and 2 km buffers around each site using CEH Land Cover Map 2015; land-use classes collapsed into urban, agricultural, and wetland composites.

## Data collected and key variables
- Water chemistry: In situ measurements (conductivity, dissolved oxygen, oxygen saturation, pH, temperature, alkalinity); 500 ml samples filtered for laboratory analysis of major nutrients and metals; chlorophyll a from filters; turbidity measured in the field.
- Sediment analyses: Top 5 cm of lake bed sediment collected; E. coli attached to sediment quantified; other bacteria (total coliform, E. coli) quantified in sediment; assessment for Campylobacter, Enterococci, E. coli (including E. coli O157) using culture-based methods; results reported as CFU per g dry weight.
- Sediment properties: Moisture content and organic content (loss on ignition).
- Water column microbiology: E. coli and other bacteria quantified in water samples; results reported as CFU per 100 ml.
- Metadata and derived metrics: Sample depth, GPS coordinates, distance to shore (including separate distances to islands if present), site size (hectares), perimeter (m), altitude, bird counts and species richness, shoreline diversity index, habitat buffers (%defined habitat within 100 m, 500 m, 2 km), etc.

## Sampling design and data processing
- Sampling framework: Spatially dispersed paired water and sediment samples; maximum 60 cores per lake (largest lake 89 ha); distance to shore calculated for each sample; island considerations for distance.
- Field and lab protocols: Sterilisation of equipment between samples; immediate cooling and processing within specified timeframes; standardized incubation and counting protocols for microbial assays.
- Data management: GPS coordinates recorded; centralised dataset referred to as Sediment_and_water_data_from_Glasgow.csv with explicit field definitions (season, site, sample, coordinates, depth, turbidity, microbial counts, water chemistry, land-use percentages, habitat buffers, and more).

## Spatial analysis and interpretation
- Mapping approach: Kriging used to illustrate spatial patterns of FIOs in water and sediment; identifies hotspots and potential drivers (bird distributions, wastewater inputs).
- Pattern findings: Hotspots present in both water and sediment, yet patterns vary across space and time; hotspots tend to be localised rather than showing broad systematic periodicity.
- Statistical assessment: Semi-variance analyses indicate limited evidence of strong spatial structuring across distance; hotspots do not exhibit consistent spatial decay from a single source.

## Data governance, quality, and provenance
- Quality controls: Sediment cores sterilised between samples; consistent sampling times; cold-chain handling; processing within defined time windows.
- Data sources and provenance: Incorporates pre-existing SEPA data where available (restricted to the summer months and most recent survey year); primary data collected as part of this study with detailed metadata.
- Documentation: Appendix includes a list of major nutrients and metals analyzed; field name descriptions and data dictionary for the Glasgow dataset; references for analytical and spatial methods.

## Appendix and metadata
- Data dictionary: Provides definitions for all fields in Sediment_and_water_data_from_Glasgow.csv (season, site, sample, coordinates, depth, turbidity, E. coli, coliforms, total coliforms, sediment and water CFU counts, and numerous environmental covariates).
- Analytical scope: Major nutrients/metals list; lab instruments referenced; field descriptions for site characteristics and buffers.
- References: Cited sources for statistical software and land cover data.

## Implications and relevance for Data Leaders
- Data assets and reuse: Rich, multi-source dataset linking water/sediment microbiology with physico-chemical, land-use, and biodiversity metrics across multiple sites and seasons; suitable for reproducible spatial modelling and trend analyses.
- Data system needs: Demonstrates importance of integrated data governance across environmental, biological, and geographic data; highlights need for robust metadata, data dictionaries, and standardized processing protocols to enable discoverability and reuse.
- User needs and applicability: Provides actionable insights on spatial hotspots and drivers of FIOs, informing risk assessment, public health advisories, and urban water quality management; supports cross-sector collaboration (environmental agencies, public health, urban planners).
- Challenges illustrated: Spatial and temporal variability; limited broad-scale spatial structuring; data gaps across seasons or sites; necessity for clear provenance and versioning when combining historic SEPA data with new field data.
- Recommendations for data leaders: Invest in standardized metadata schemas, ensure data discoverability across platforms, maintain transparent documentation of sampling designs and lab methods, and foster cross-institution collaboration to reduce data duplication and improve sector coordination.