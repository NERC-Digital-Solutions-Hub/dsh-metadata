# Site description

- Long-term alpine research site established in Gunnison National Forest, Colorado (38.978725°N, 107.042104°W) at ~3540 m a.s.l. on a southeast-facing ridgeline with ~20% slope and a barren substrate (Mancos shale downslope; quartz monzonite porphyry upslope). Bedrock within 5–10 cm; loose weathered gravel layer; 0–10% perennial vegetation cover during short summer season. Snow typically falls October–melting June–July; avalanches rare; strong W–E winds common.
- Experimental design: 50 permanent 2 × 2 m plots arranged 5 × 10 on a grid along the ridge axis (~40° heading) with 2 × 2 m buffer between plots; site footprint ~18 × 38 m.

## Data assets and scope

- Census data (2014–2017; n = 4 years)
  - Every year, all individuals within each plot mapped to the nearest centimeter and tagged.
  - Species identifications validated with RMBL Herbarium vouchers; one unidentifiable seedling recorded as Indet indet.
  - Demographic data per individual: size (max length/height), recruitment status (seedling or clonal), fecundity (mature floral structures), dormancy/death status; tag removal if no aboveground growth for >2 consecutive years.
  - Spatial delineation challenges for grasses/sedges; individuals considered separate if ground-level stems >3 cm apart; notes on connected perennials.
- Microenvironmental data (2 m resolution, kriged to 10 cm resolution within plots)
  - Substrate surface temperature (iButton loggers, every 20 minutes; medians used).
  - Local slope, elevation, and aspect (derived).
  - Disturbance proxy: distance from a historic eastern trail (Euclidean distance).
  - Soil moisture: shallow (3.8 cm) in July 2015; deep moisture to 10 cm in July 2016.
  - Soil texture fractions by dry sieving; soil chemical properties (23 samples): Cu, Fe, K, Mn, P, Zn, nitrate/nitrogen, organic matter, pH, electrical conductivity.
  - Hardness/fragility proxy: soil penetration energy density (MJ m^-3) measured July 2015.
- Macroenvironmental data
  - Annual climate data (2013–2017) from Billy Barr weather station (~4.5 km away): total precipitation January–July.
- Functional trait data (collected adjacent to plots to avoid disturbance)
  - Belowground and aboveground metrics: height, width, root depth/length/volume, root tissue density; fine-root length vs dry mass; specific root length (mm g^-1); root traits via microscopy (AMF and DSE prevalence).
  - Leaf traits: leaf lamina thickness, fresh mass, area, aspect ratio; specific leaf area; leaf dry matter content; leaf carbon and nitrogen concentrations; leaf δ13C and δ15N.
  - Tissue partitioning: biomass fractions (leaves, stems, coarse/fine roots); root and stem dry matter content.
  - Photosynthetic capacity: per-mass rate (LiCor 6400XT) under standardized conditions; adjustments for leaf area where needed.
  - Fruit/seed data (end of 2015 season): fruit counts, seeds per fruit, fertile vs aborted seeds; mean seed mass.
- Metadata and documentation
  - Voucher specimens stored in RMBL Herbarium; permanent tagging system; clear documentation of sampling times, instruments, and protocols.
  
## Data processing and summarization

- Microenvironment summarization
  - Kriged 10 cm grids across plots; PCA on standardized variables; retention of components with eigenvalues > 1; generation of predicted scores for each grid cell.
- Realized niches
  - Species presence/absence on the 10 cm grid; each individual treated as a circle with diameter equal to its maximum vegetative width; niche centroids derived from median microenvironment PCA scores for cells where the species is present.
- Vital rates
  - Definitions: recruitment (new seedling or vegetative propagule in a year), growth rate (change in vegetative length between years), mortality (death in a year), fecundity (number of floral structures in a year).
- Trait data processing
  - Species means calculated; missing data (68 of 540 observations) imputed via multiple imputation by chained equations.
  - PCA on standardized trait data; components retained with eigenvalues > 1; predicted scores assigned per species.
- Trait neighborhoods
  - Species-level: pairwise trait differentiation using absolute difference and hierarchical difference metrics.
  - Individual-level: crowding coefficient within 50 cm radius, weighting by neighbor size and distance; intra- and interspecific neighbor calculations.
  - Mean trait difference: size-weighted mean neighbor trait value minus focal trait value.
  - Mean trait hierarchy: size-weighted mean neighbor trait value relative to focal species trait; zero if not higher.
  - All approaches incorporate neighbor size (s_k) and rely on species-mean trait values where necessary.

## Data management and quality considerations

- Data completeness
  - Mostly comprehensive census and trait measurements; a small portion of observations missing (68/540) addressed via imputation.
- Identification and sampling challenges
  - Delineation difficulties for grasses/sedges; strict criteria used to separate individuals; some recruits and dormant individuals carefully tracked.
- Reproducibility and provenance
  - Detailed measurement protocols, instrument models, and sampling timing documented; vouchers linked to specimens; spatial coordinates to enable replication and cross-site comparisons.

## Implications for Data Leaders (data strategy and governance)

- Data scope and integration
  - Rich, multi-faceted dataset combining census demographics, micro- and macroenvironmental variables, and functional traits across time; strong potential for integrative analyses linking environment, plant traits, and population dynamics.
- Data quality, discoverability, and reuse
  - Well-documented methods enable reuse and cross-site comparison; kriging-derived microenvironment maps and realized niches provide reusable geospatial products.
  - Gaps (missing data) addressed with transparent imputation; consistent metadata facilitates discovery and downstream analyses.
- Collaboration and stewardship
  - Herbarium vouchers and long-term plot data support cross-network collaboration; potential for co-ownership of data products, sharing of microenvironment rasters, and standardized trait metrics.
- Opportunities for application
  - Use in trait-based ecological modeling, community assembly studies, and responses to climate variation; development of data products (e.g., microenvironment maps, niche centroids) for stakeholders and modelers.
- Considerations for future data strategy
  - Maintain and expand metadata for longitudinal analyses; ensure standardization of units and thresholds for cross-site integration; plan for ongoing data updates and versioning; explore scalable data sharing mechanisms to support broader communities of practice.