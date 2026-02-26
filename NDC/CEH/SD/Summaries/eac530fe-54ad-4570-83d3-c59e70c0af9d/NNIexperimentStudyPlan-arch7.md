# Study Plan:
A large-scale field experiment to quantify the impacts of neonicotinoid (NNI) seed dressings on honeybees in the UK, Germany and Hungary

- Purpose: quantify whether two neonicotinoid seed treatments (clothianidin and thiamethoxam) affect honeybee population growth, mortality and overwintering survival when foraging on oilseed rape.
- Treatments: three levels per site - CONTROL (no NNI), Clothianidin-treated, and Thiamethoxam-treated OSR.
- Scope: field experiment on commercial farms across the UK, Germany and Hungary conducted autumn 2014 with monitoring and harvesting in 2015.

## Spatial design and site context (GIS-relevant aspects)
- Sites and replication:
  - 36 study sites across three countries (UK, Germany, Hungary) arranged into replicate blocks.
  - Each block includes three sites, one per treatment (Control, Clothianidin, Thiamethoxam).
  - Spatial separation: at least 10 km between replicate blocks; within a block, sites separated by a minimum of 3.2 km.
- Landscape and data layers:
  - Landscape homogenization efforts through use of land-cover and major crop data to minimize variation between sites/countries.
  - A surrounding land-cover and flowering resource survey conducted within a 1.5 km radius of each treatment field to map crops, habitat types, flowering resources, hedgerows, woodlands, and other landscape features.
  - Documentation of dominant flowering species (trees, herbs, shrubs) around sites to contextualize forage resources.
- Site size and spatial scale:
  - Each OSR field block area: approximately 45–70 ha to ensure high exposure within treated plots and reduce inter-field foraging on untreated patches.
- Geographic identifiers:
  - Each hive/group has a country code, site index, and unique hive ID for GIS-ready linking of spatial and observational data.

## Treatments and crop management (agronomic GIS context)
- Treatment allocation:
  - Random assignment of field blocks to: CONTROL, Clothianidin-treated, or Thiamethoxam-treated OSR.
  - UK includes additional untreated control sites as residuals to detect potential soil residuals of neonicotinoids.
- Crop and agronomy:
  - Oilseed rape grown with consistent varieties per country (UK Harper; Germany Flyer; Hungary Hybrirock) under Good Agricultural Practice (GAP).
  - Crop density verification planned in spring 2015 (20 random plots per site).
  - Pollen beetle and other pest management timing synchronized across blocks to minimize bee impact and preserve NNI signal; pesticide choices selected to minimize bee risk.
  - Maintenance pesticide applications scheduled within three days of field activities and recorded per site.
- Sowing details:
  - Target seeding rate: 50 seeds per m2.
  - Seed lots used for control and treated plots are from the same batch and variety as appropriate.

## Field design, hive layout and exposure strategy
- Hive deployment:
  - Across all countries, total of 288 hives (6 hives per site × 36 sites) plus reserve/back-up hives for each site.
  - Hives are organized in country-specific overwintering locations to standardize climatic exposure and minimize between-site confounding factors.
- Patches and patch layout:
  - At each site, two hive patches per block centered on the crop area with clear buffers to avoid spray drift (minimum 10 m buffer to patch edge; patches separated by about 100 m in certain setups).
  - For large fields, patches may be centered on field margins/headlands; in UK, site layouts leverage margins to minimize disruption.
- Overwintering plan:
  - All hives within a country overwinter at a single location, with blocks clustered (24 hives per cluster) and clusters separated by ~200 m to reduce robbing; entrances reduced to minimize between-hive robbing.
- Bee management and health:
  - Varroa control regime consistent across all hives (two formic acid applications and one oxalic acid, timing country-dependent).
  - Regular beekeeper checks every 7 days from first exposure through winter; documentation of queen status, swarming, food stores, disease signs, etc.

## Data collection, measurements and endpoints (GIS-ready topics)
- Primary endpoints:
  - Honeybee colony metrics: colony size, growth rate, weight, foraging behavior, brood status, overwinter survival, and pathogen/parasite incidence.
  - Exposure measures: neonicotinoid residues in crop nectar/pollen, stored hive products (honey, pollen, wax), soil, and plant tissues.
  - Foraging landscape context: pollen loads in hives, composition of foraged resources (OSR vs. other flowering resources).
- Temporal sampling windows:
  - Pre-exposure (baseline), during crop flowering (exposure phase), post-exposure, and overwinter periods.
- Spatial data integration:
  - GPS-based hive patch centers recorded with ±2 m accuracy; patch-level and site-level GIS attributes (treatment, country, replicate block).
  - Land-cover and flowering-resource maps linked to site polygons and patch locations for spatial analyses of landscape influences on exposure and effect sizes.
- Disease and residue context:
  - Disease sampling (sites across all three countries) as covariate; pathogen analyses planned with note on power limitations.
  - Residue analyses planned via UKAS-accredited CEH labs; QA/QC procedures outlined.

## Residue sampling design (multiple GIS-ready data layers)
- 6.1: Crop residue sampling in caged-bee tunnels:
  - 36 sites; one hive per site in a tunnel; nectar and pollen collected for residue analysis (two sampling times).
- 6.2: Nectar and pollen sampling from free-flying bees:
  - Three sampling occasions during flowering; approximately 400 bees per site per occasion for nectar and pollen residue analyses.
- 6.3: Stored hive products:
  - Honey, pollen, and wax sampled pre-exposure, post-exposure, and overwintering for residue analyses.
- 6.4: Flowers and leaf material:
  - Tissue sampling from OSR flowers and leaves around peak flowering to corroborate plant-level exposure (archived for potential analysis).
- 6.5: Residue analysis:
  - All samples processed by CEH labs with ongoing QA/QC; data linked to site/hive/treatment identifiers.

## Other measurements and environmental context
- Meteorology:
  - Weather data collected at one site per replicate block (temperature, humidity, rainfall, sunshine) plus use of official weather station data.
- Photographic records:
  - Baseline and periodic photos documenting site conditions, landscape context, crop status, and bee activity.
- Data management:
  - Blind data collection (treatment identities blinded to field workers) to minimize bias; standardized labeling and data capture templates; data stored in an Oracle database with nightly backups.
  - Raw data and data management procedures are designed to produce GIS-ready datasets and reproducible analyses.

## Data management, archiving and accessibility
- Data handling:
  - CEH and Eurofins jointly manage data capture; standardized data formats; 10-year archiving for final reports and peer-reviewed outputs.
  - Archiving of samples and metadata with traceable shipment records and data loggers to verify cold-chain integrity.
- Accessibility:
  - Data sets structured for sponsor access; raw data and study plan distributed to stakeholders; data management plan governs data access and QA processes.

## Timeline and governance
- Timetable:
  - Field setup in 2014; exposure monitoring during 2015 flowering; post-exposure and overwintering phases outlined with specific sampling windows.
- Oversight:
  - Study Director responsible for overall conduct; PIs oversee country-specific components; GLP-compliant practices where applicable; deviations documented and approved.

## Responsibilities and collaboration
- Roles:
  - Eurofins: management of honeybee test colonies and crop trials (Germany and Hungary) and coordination of field operations.
  - CEH: pesticide residue analyses across all sites; crop management in the UK; field mapping and data management oversight.
- Documentation and amendments:
  - Any plan amendments require Study Director approval; deviations logged and justified; confidentiality is not claimed.

## End notes and references
- References and glossary provide standard definitions for experimental terms (sites, replicate blocks, exposure terms, etc.).
- Appendix summarizes terminology and provides example coding schemes for site/hive identifiers and field layouts.

- Overall relevance for GIS Specialists:
  - A rigorously designed, multi-country, large-scale field experiment with explicit spatial structure, landscape-context mapping, and GIS-ready data collection (sites, blocks, patches, GPS coordinates, land-cover attributes, and patch-level exposure data).
  - Emphasizes integration of spatial data with agronomic treatments, hive deployments, and environmental measurements to support spatial analysis of neonicotinoid exposures and bee responses.