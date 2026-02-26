# FIO Sampling and Analysis in Glasgow Lakes

## Aim and Scope
- Examine spatial patterns of fecal indicator organisms (FIOs) and their drivers in water and sediment across urban lakes.
- Address implications for human health, waterbody quality, and ecology in a context of variable connectivity to vectors.

## Study Areas and Context
- Subset of lakes in the Greater Glasgow conurbation (central Scotland) across a rural-urban gradient.
- Seasonal sampling: summer (July) with 6 sites; winter (December) with 15 sites (including all summer sites).
- Bird surveys conducted for an hour at each site, coordinated with sampling times (3 hours after sunrise for consistency with bird activity and UAV exposure).
- Derived physical variables: altitude, area, catchment size, perimeter, waterbody-to-catchment ratio, shoreline development index from UK Lakes Portal.
- Land use around each waterbody assessed within 100 m, 500 m, and 2 km buffers using CEH Land Cover Map 2015, with composites to reduce categories (urban, agricultural, wetland).

## Data Collected and Measurements
- Water chemistry in situ: conductivity, dissolved oxygen, oxygen saturation, pH, temperature, alkalinity (via Hach HQ40d and HI-755).
- Lab analyses on 500 ml subsamples: major nutrients and metals; chlorophyll a from filters.
- Turbidity: measured in the field.
- Existing SEPA data retained for summer months when available.
- Bird metrics: numbers, species, and activity recorded at each site.
- Derived GIS metrics: distance to shore, distance to islands, shoreline development index, etc.
- Sediment and water sampling coordination across lakes, with a total of 770 unique sample points (water and sediment from each point).

## FIO Sampling and Analysis
- Sediment: gravity core sampling; top 5 cm analyzed; sediment sterilization between samples.
- Sediment processing: detachment of E. coli from sediment particles, enumeration of total coliforms and E. coli on MLGA plates; additional testing for Campylobacter, Enterococci, E. coli O157 using enrichment protocols; results presented as CFU per g dry weight.
- Sediment characteristics: moisture content (drying at 60°C) and organic content (loss on ignition at 550°C).
- Water column: surface-proximal sampling (~30 cm depth); bacteria enumerated after filtration and plating (CFU per 100 mL) on MLGA plates; incubation at 37°C.
- Subsample handling and incubation protocols adhered to standard microbiological methods (as detailed in Appendix).

## Spatial Analysis and Outputs
- Generated maps of FIO spatial patterns at the waterbody scale using kriging in R.
- Identified hotspots of FIOs in both sediment and water; patterns linked to bird distributions and point sources like wastewater treatment plants.
- Spatial structure analysis (semi-variance) showed clear FIO hotspots but limited evidence for strong, consistent spatial structuring or periodicity; hotspot influence appears largely local to each lake and not uniformly patterned across lakes or seasons.
- Example site contrasts provided (e.g., Strathclyde Loch and Bardowie Loch) to illustrate spatial patterns.

## Data Structure and Appendix
- Major nutrients and metals measured per 500 ml subsample (instrumentation and determinants listed).
- Data file fields (Sediment_and_water_data_from_Glasgow.csv) include:
  - season, site, sample, coordinates (x, y), depth, turbidity
  - water column: E. coli (waterecoli), coliforms, total coliforms
  - sediment: E. coli (elec), Enterococci, Campylobacter (campy)
  - distances, shoreline metrics, land-use buffers (100m, 500m, 2k)
  - habitat percentages (Acid grassland, Arable, Improved grassland, Suburban, Urban, Woodland, Freshwater) at 100m, 500m, 2k buffers
  - site morphology: Perimeter, Size (ha), Altitude, Shoreline Diversity Index (SDI), Shade, NearestNeighbor, Inflow, Outflow
  - additional metadata fields for coordinates and buffer definitions
- Appendix also details the data field descriptions and the laboratory methods used for nutrient and metal determinations.

## References
- R Core Team (2018). R: A language and environment for statistical computing.
- Rowland et al. (2017). Land Cover Map 2015 (GB). NERC Environmental Information Data Centre.

## Implications for Monitoring and Data Use
- Uses standardized data collection and well-documented laboratory protocols suitable for integration with other environmental datasets.
- Produces spatial outputs (kriging maps) and statistical assessments that support monitoring of FIO risk hotspots and the influence of birds and point sources.
- Emphasizes data quality assurance, reproducibility, and the potential for uploading curated datasets to monitoring portals to enhance data accessibility and reuse.