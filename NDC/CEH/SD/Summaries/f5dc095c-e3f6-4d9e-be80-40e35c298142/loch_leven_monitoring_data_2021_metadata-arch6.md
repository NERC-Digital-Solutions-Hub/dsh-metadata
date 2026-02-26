# Abstract

- This document describes the Loch Leven long-term monitoring dataset (Scotland, UK), collected from 1968 onward as part of the NERC / UK Centre for Ecology & Hydrology programme, under project UK-SCAPE WP7 LEVEN.
- It details the nature of the data, sampling and analysis methods, data processing techniques, and the format of the output file.

## Overview of the dataset and aims

- Purpose: to document long-term lake monitoring data enabling trend analysis and data products for exploration and use by others.
- Coverage: lake chemistry (water quality), physical conditions, and crustacean zooplankton across two monitoring sites.
- Output: a single CSV file with comprehensive metadata, determinands, units, and site information; designed for self-serve data use.

## Sampling regime and sites

- Sampling frequency: generally fortnightly.
- Sites: two main sampling sites per occasion - Reed Bower (RB) and Sluices/Outflow (L). Harbour (H) is represented in site coding in the dataset.
- Accessibility: RB requires boat; L can be sampled by boat or from shore. Some sampling occasions may sample only L or neither site due to weather, ice, or resource constraints.
- Sampling details:
  - In situ measurements at each site; Secchi depth measured at RB.
  - When not in the field, samples are collected for laboratory analyses and later processed.

## Measurements and analyses

- In situ measurements: conductivity, pH, and temperature (hand-held probes); Secchi depth measured at RB for water clarity.
- Water sampling and laboratory analyses:
  - Duplicate 2 L samples per site (RB: integrated sample with a weighted PVC tube; L: bottle 10 cm below surface).
  - Analyses include soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP), soluble silica (silicate), total diatom silica, chlorophyll a; some parameters are filtered/frozen for later analysis.
  - SRP method: Murphy & Riley (1962); TP/TSP methods: Wetzel & Likens (2000).
- Weather data: cloud cover, wind direction, wind force (Beaufort scale) recorded at RB when possible.

## Crustacean & zooplankton dataset

- Focus: densities of crustacean zooplankton at RB and L, measured as individuals per litre (ind/L) for multiple taxa (e.g., Daphnia hyalina, Eudiaptomus spp., Cyclopidae, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, etc.).
- Sample collection:
  - RB: 4 m angled net haul (mesh 120 µm).
  - L: filtration of 30 L surface water through a 120 µm net.
- Laboratory processing: subsampling, identification and counting under a microscope; counts converted to ind/L using appropriate factors; samples preserved in 4% formaldehyde and archived.

## Data processing

- Import and normalization: an R script processes data before database entry, applying consistent rules.
- Wind force handling: when multiple values appear (e.g., "4-5"), the first value is used.
- Replicate data handling (conductivity, pH, DO, and corresponding temperatures):
  - Values within Median ± MAD are retained; outliers are discarded unless only 1–2 replicates exist.
  - pH values are converted to 10^pH for median/MAD calculations, then back-transformed; means are rounded to 2 decimals; conductivity, DO%, and temperatures rounded to 1 decimal.
- Probe changes: HQ30d (old model) vs HQ4300 (new model) for Hach probes; for this dataset, HQ30d columns are used to avoid changing structure; future datasets may switch to HQ4300.

## Quality assurance

- Automated and manual checks performed on all data.
- Any unusual values are investigated and corrected where appropriate.

## Format and structure of stored data

- Storage format: a single comma-separated values (CSV) file.
- Columns: include siteConditions, lake chemistry, crustacean/zooplankton counts, with units and site information.
- Missing data: represented as NA (Not Available).

## Column descriptions and core reference

- Columns cover:
  - Date, Site, Week_of_Year (date and week)
  - Water_Level_cm (Harbour/H), Cloud_cover_Eighths (RB), Wind_Direction (RB), Wind_Force_Beaufort_scale (RB)
  - Depth_m (RB), Secchi_m (RB)
  - Conductivity_µS/cm (RB, L), Temperature_°C (for conductivity measurements)
  - Dissolved Oxygen (DO_mg/L, DO_% , Temperature_°C) (RB, L)
  - pH (RB, L) and Temperature for pH measurements
  - TP_ugP/l, SRP_ugP/l, TSP_ugP/l (site-specific replicates)
  - Chlorophyll a (chla_ug/l)
  - Zooplankton densities for multiple taxa (e.g., Daphnia hyalina, Eudiaptomus gracilis, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, etc.)
- Table 3 (detailed column descriptions) serves as the core reference for what each column represents, including determinand, site, and units.

## References and additional reading

- Method references for analyses:
  - Golterman, H.L., Clymo, R.S., Ohnstad, M.A.M. (1978). Methods for Physical and Chemical Analysis of Fresh Waters.
  - Murphy, J. & Riley, J.P. (1962). A modified single solution method for phosphate in natural waters.
  - Wetzel, R.G. & Likens, G.E. (2000). Inorganic nutrients: nitrogen, phosphorus and other nutrients. Limnological Analyses.
- Further reading and project context:
  - Dudley et al. (2012). Water quality monitoring at Loch Leven 2008-2010.
  - Spears & May (eds.) (2012). Loch Leven: 40 years of scientific research.
- Data processing and QA methods documented within the dataset description.

## Project and availability

- Data generated under project UK-SCAPE WP7 LEVEN.
- Collaboration and data curation involve staff from NERC and CEH, with long-term maintenance of the Loch Leven monitoring record.