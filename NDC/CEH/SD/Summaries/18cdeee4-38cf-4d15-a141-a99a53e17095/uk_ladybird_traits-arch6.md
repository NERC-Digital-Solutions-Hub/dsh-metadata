# Species traits, ecological preferences and distribution metrics for 48 species of ladybird considered resident in the United Kingdom

## Overview
- A compiled dataset detailing traits, ecological preferences, and distribution metrics for 48 UK-resident ladybird species.
- Variables include morphology, habitat and diet preferences, phenology, occupancy trends, and species temperature indices (STIs) for UK and Europe.
- Data sources: published literature, Field Guide to the Ladybirds of Britain and Ireland (Roy & Brown, 2018), UK Ladybird Survey records, iRecord, and GBIF for Europe.
- A detailed data paper will accompany the dataset.
- Four CSV files structure the dataset, with metadata and data provenance captured.

## Data structure and contents
- ladybird_traits.csv
  - 49 rows (header + 48 species) and 74 columns.
  - Contains species-level information: names, traits, ecological preferences, trends, and derived metrics (NA where data are missing).
- metadata.csv
  - Metadata corresponding to the variables described in Table 1 (in CSV format).
- prey_list.csv
  - List of prey species by prey family for calculating diet breadth (number of prey families per ladybird).
- sources.csv
  - List of sources used to compile information (books, papers, websites).
- Variable descriptions and units (Table 1) are also provided in metadata.csv and described in the methods.

## Variables and metrics of interest
- Taxonomic and morphological traits
  - Genus, Species, Common_name, Authority, Tribe, Subfamily
  - Conspicuous vs. Inconspicuous
  - Body_size_min/max (mm)
  - Polymorphism_melanic, Polymorphism_spot
  - UK_native (native vs non-native in UK)
- Record-based metrics
  - n_records, First_yr, Most_recent_yr, nrecs_England/Wales/Scotland/NorthernIreland
  - n_10k (number of 10 km grid cells with records), n_vicecounties
- Occupancy and trends
  - Longterm_trend (1970–2018), LT_trend_lower, LT_trend_upper
  - Shortterm_trend (2009–2018), ST_trend_lower, ST_trend_upper
  - LT_first, LT_last; ST_first, ST_last
  - Notes: some long-term/short-term trends may be missing due to model convergence or data limitations.
- Feeding guild and diet breadth
  - Foodguild_Adelgidae, Aleyrodidae, Aphididae, Coccidae, Diaspididae, Pseudococcidae, Psyllidae, Plants, Fungi, Mites, Other
  - nfood_recs (total feeding records), nfamilies_diet (number of prey families)
  - Foodguild_confidence (low/medium/high)
- Habitat associations
  - Presence in Habitat Type categories (Level 1 IUCN habitats; e.g., Forest_woodland, Shrubland, Native_grassland, Wetlands_inland, Marine_intertidal, Marine_coastal_supratidal, Artificial_terrestrial, Other)
  - n_habitats (total habitats species is present in)
  - n_habitats_weighted (habitats weighted by presence/population intensity)
- Phenology and life history
  - Larvae_first, Larvae_last, Peak_larvae (months; where data available)
  - Adult_first, Adult_last, Peak_adult1, Peak_adult2, Max_month
  - Voltinism_min, Voltinism_max (generations per year)
- Species Temperature Indices (STI)
  - STI_UK_mean, STI_UK_peak (UK-based, all months vs peak month)
  - STI_Europe_mean, STI_Europe_peak (Europe-based, GBIF-derived)
  - STI values rounded to two decimals

## Data sources and collection
- Primary sources: Roy & Brown Field Guide (2018), UK Ladybird Survey and iRecord records, and GBIF European records.
- Temporal scope for records: 1970–2023 (UK records); 1970–2018 for occupancy trends; larval months data extend to 1929–2021 (not all public).
- Spatial data handling:
  - 1 km grid occupancy modelling; 10 km OS grid cells for presence
  - Vice counties for distribution in GB and Ireland
- Data processing and derivation:
  - Traits and preferences derived from literature and records
  - Diet breadth from prey_list with GBIF taxonomy guidance
  - Habitat associations aligned with IUCN Habitat Classification Scheme v3.1
  - STIs computed from WorldClim climate data (1970–2000 baseline) using UK records and GBIF European records
- Data provenance and access:
  - Code and processing pipeline available at https://github.com/CharlieOuthwaite/LadybirdTraits
  - GBIF data require a GBIF account

## Methods and processing details
- Occupancy trends
  - Bayesian occupancy modelling (DRUID framework) to estimate annual occupancy from presence-only records (1970–2021), with trends calculated between first and last converged years (up to 2018 for long-term, 2009–2018 for short-term).
  - First/last years reflect data availability and model convergence; some species have missing trend estimates.
- Traits and records
  - Body size ranges compiled from published sources
  - Melanic and spotted polymorphisms categorized as common, rare, or not present
  - UK native status determined from Roy & Brown (2018)
  - Country-level presence inferred from records within England, Wales, Scotland, Northern Ireland
  - 10-km grid presence derived from overlaying UK records onto OS grid
  - Vice counties counted from predefined GIS layers
- Feeding guilds
  - Prey species identified from literature; prey families assigned using GBIF taxonomy
  - Eleven feeding guild categories populated per species; confidence levels assigned based on the volume of feeding records
- Habitat and phenology
  - IUCN Level 1 habitats used to score presence and weight by relative abundance
  - Larval and adult record timing used to identify monthly first/last/peak occurrences (where data exist)
  - Peak months validated via histogram checks to avoid artefacts from small sample sizes
- Temperature indices
  - UK STI: mean across UK records, and mean for month with most records
  - Europe STI: mean across GBIF European records, with cleaning to remove geospatial errors and unsuitable records

## Spatial and temporal coverage
- Target taxa: 48 resident UK ladybird species
- UK data: 1970–2023 (records); occupancy trends up to 2018
- Europe data: GBIF-derived records from 1970 onward for Europe STI calculation
- Larval data: 1929–2021 (not all species have larval data; not publicly available for some)
- Data quality controls include verification by survey organizers and expert validation of all variables

## Quality control and limitations
- Not all variables calculable for inconspicuous species due to data gaps or recent arrival
- Short-term trend estimates may be missing when occupancy model first-year convergence fails
- Data gaps and biases may arise from uneven sampling effort and recorder activity (notably around 2018 field guide release)
- Data validation steps include cross-checking peaks with histograms and expert review
- Some outputs (notably larval data for certain species) are NA due to limited data

## How Data Support can use this dataset
- Integrate trait, diet, habitat, and occupancy trend information to explore drivers of distribution changes and ecological niches
- Build dashboards or reports that enable end users to self-serve: species profiles with trait/diet/habitat summaries and occupancy trends
- Compare UK-specific STIs with Europe-wide counterparts to assess climate-associated range shifts
- Analyze diet breadth and habitat associations across multiple species to inform conservation or monitoring programs
- Use metadata and sources to ensure reproducibility and facilitate data provenance in analyses

## Access, reproducibility, and next steps
- Four CSV files plus metadata and sources files provide a ready-to-use dataset
- Code and data processing workflow available on GitHub for reproducibility
- A companion data paper will be published to accompany the dataset
- Researchers should note data gaps (e.g., inconspicuous species, incomplete larval data) and trend convergence limitations when analyzing time-series

## References and caveats
- Roy, H.E. & Brown, P.M.J. (2018). Field Guide to the Ladybirds of Great Britain and Ireland.
- Outhwaite et al. (2019); Powney et al. (2019) related occupancy and trend methodologies
- GBIF data and CoordinateCleaner-based cleaning procedures
- Data access requires acknowledgment of UK CEH, iRecord, and GBIF sources as described in the metadata