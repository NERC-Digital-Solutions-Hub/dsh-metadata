# Rationale

- Contamination of urban waterbodies by fecal indicator organisms (FIOs) poses health risks to recreational users and affects waterbody quality and ecology.
- The dataset investigates spatial patterns of FIOs and their drivers in water and sediment across lakes in an urban environment with variable connectivity to vectors (birds, point sources).

## Study areas and contextual information

- Subset of lakes in the Greater Glasgow conurbation, spanning a rural-urban land cover gradient.
- Sampling occasions: summer (July; 6 sites) and winter (December; 15 sites; includes all summer sites).
- Standardized sampling timing: all samples 3 hours after sunrise to align with bird activity and UAV exposure; one-hour bird surveys recording numbers, identity, and activity.
- Derived physical variables from the UK Lakes Portal: altitude, area, catchment size, perimeter, ratio of waterbody to catchment area, shoreline development index (SDI) indicating shoreline shape complexity.
- Water chemistry: in situ measurements (conductivity, dissolved oxygen, oxygen saturation, pH, temperature, alkalinity) plus lab analysis of major nutrients and metals from 500 ml subsamples; chlorophyll a from sediment filters; turbidity via turbidity meter.
- Use of pre-existing SEPA data for summer months when available.
- Land use around each waterbody: proportion within 100 m, 500 m, and 2 km buffers using CEH Land Cover Map 2015; 21 classes simplified into composites (urban, agricultural, wetland) for surrounding buffers and catchments.

## FIO sampling and analysis

- Spatially dispersed paired water and sediment samples collected from each lake; up to 60 cores for the largest lake (89 ha).
- For each sample point: water depth recorded; GPS coordinates captured; distance to shore calculated (including separate calculations for islands where relevant).
- Sediment sampling: gravity corer used; top 5 cm of sediment collected and stored cold; sterilization between samples.
- E. coli in sediments detached with PBS, then enumerated on MLGA plates; additional testing for total coliforms and E. coli in sediment.
- Bacteria testing in sediment: three subsamples pooled per time/position; prepared in LB broth and incubated; CFU counts reported per g of oven-dried soil.
- Water column testing: three volumes (100 ml, 10 ml, 1 ml) filtered onto MLGA plates; CFU per 100 ml reported after incubation.
- Additional sediment analyses: moisture content (loss on drying at 60°C), organic content (loss on ignition at 550°C).

## Sediment sampling

- Sediment cores collected to assess bacterial abundance and presence; processing includes detachment, enrichment, and plating to determine CFU per g dry weight for E. coli, total coliforms, Enterococci, Campylobacter, and related indicators.
- Inoculated and incubated plates used to quantify target organisms; results expressed as CFU per g dry weight.

## Water sampling

- Water samples collected before sediment sampling, about 30 cm below the surface.
- Filtration of three volumes (100 ml, 10 ml, 1 ml) through 0.45 μm membranes onto MLGA agar; plates incubated and counted after 24 hours.
- Bacterial counts reported as CFU per 100 ml of water.

## Indicative results and interpretation

- Spatial mapping of FIOs using kriging in R to show hotspots at waterbody scale in both sediment and water.
- Hotspots appear related to bird distributions and point sources (e.g., wastewater treatment plants); patterns vary temporally and spatially within waterbodies.
- Semi-variance analysis used to assess spatial structuring; although clear hotspots exist, there is limited evidence of strong, consistent spatial autocorrelation with distance from hotspots, indicating localized and variable patterns across lakes.

## Appendix

- Major nutrients and metals measured per 500 ml water subsample (detailed analyte list and instruments).
- Field name descriptions for Glasgow.csv, outlining the structure and meaning of each variable (season, site, sample, coordinates, depth, turbidity, E. coli metrics, sediment and water chemistry, bird counts, land-use buffers, shoreline metrics, habitat percentages, etc.).
- Dataset metadata includes coordinates in British National Grid, sample IDs, and descriptions for each field.

## References

- R Core Team (2018). R: A language and environment for statistical computing.
- Rowland et al. (2017). Land Cover Map 2015 (GB). NERC Environmental Information Data Centre.