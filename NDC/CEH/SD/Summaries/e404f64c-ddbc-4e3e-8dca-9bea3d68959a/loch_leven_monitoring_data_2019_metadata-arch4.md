# Loch Leven long-term monitoring dataset (UK-SCAPE WP7 LEVEN)

## Overview
- Long-term data collection from Loch Leven, a lowland lake in Scotland, initiated in 1968 and ongoing.
- Collected under the UK-SCAPE WP7 LEVEN project, with involvement from NERC and the UK Centre for Ecology & Hydrology.
- Datasets described include lake chemistry (conductivity, pH, temperature, Secchi depth, nutrients, chlorophyll a) and crustacean zooplankton densities, gathered as part of a sustained monitoring programme.

## Data scope and structure
- Sampling regime: fortnightly visits to two main sites per occasion.
  - Reed Bower (RB) site visited by boat; Sluices (L) site accessible by boat or shore.
  - At times, sampling may be limited by weather, ice, or resources; if boats unusable, only Sluices sampled or neither site sampled.
- Sites and identifiers:
  - Harbour (H), Reed Bower (RB/RB5), Sluices/Outflow (L/Sl8); coordinates are provided (UK National Grid, epsg:27700).
- Data types:
  - Water chemistry (in situ measurements and lab analyses) and crustacean zooplankton densities (ind/L) from two sites.
  - Weather observations (cloud cover, wind direction and force) recorded when possible.

## Measurements and methods
- In situ measurements:
  - Conductivity, pH, temperature measured with hand-held probes; Secchi depth measured at Reed Bower.
- Water sampling and laboratory analyses:
  - Duplicate 2 L samples collected per site.
  - Reed Bower: integrated column sample using a weighted PVC tube; Sluices: bottle sampled 10 cm below surface.
  - Laboratory analyses include:
    - Soluble reactive phosphorus (SRP) and total soluble phosphorus (TSP) after filtration and storage.
    - Total phosphorus (TP) from unfiltered samples after persulfate digestion; method aligned with Wetzel & Likens (2000).
    - Chlorophyll a analysis via filtration of 400 mL samples.
    - Additional storage and handling details for filtered/unfiltered samples.
- Other measurements:
  - Weather conditions recorded when possible; wind force described using a detailed Beaufort-based scale.

## Crustacean & zooplankton data
- Densities (ind/L) of various crustacean zooplankton taxa recorded at Reed Bower and Sluices.
- Sampling and preservation:
  - Reed Bower: 4 m angled net haul (120 µm mesh).
  - Sluices: 30 L surface water passed through a 120 µm net.
  - Samples preserved in 4% formaldehyde; later lab processing includes sub-sampling and counting under a microscope.
- Taxa counted (examples): Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus.
- Data handling:
  - Counts converted to ind/L; four sub-samples counted; identification to species level where practical; zeros indicate non-detection within subsample; NAs indicate missing values.
- Laboratory processing references provided for taxonomic identification.

## Data processing and quality assurance
- Data processing:
  - An R-based import script was used to ingest data into the database.
  - Decisions include handling wind force values (e.g., “4-5” uses the first value) and probe replicate values.
  - Replicates for conductivity, pH, dissolved oxygen (DO) and related temperatures are screened using Median Absolute Deviation (MAD); transformations applied for pH (log10) during MAD/median calculations; final values rounded to 2 dp (pH/DO) or 1 dp (conductivity and temperatures).
- Quality assurance:
  - Automated and manual checks for data entry errors and out-of-range values; anomalies investigated and corrected as appropriate.
- Data format and storage:
  - All data stored in a single CSV file.
  - Columns describe determinands, sites, units, and related metadata; missing readings marked as NA.

## Column structure and reference information
- Column naming convention:
  - Includes date, week, weather, site conditions, lake chemistry measurements, and crustacean/zooplankton counts.
  - Examples: depth, Secchi depth, conductivity, various temperatures, dissolved oxygen (mg/L and %), pH, TP/SRP/TSP, chlorophyll a, and taxa densities (ind/L) per site.
- Column descriptions:
  - Table 3 provides detailed descriptions of each column, including determinand, site, units, and interpretation.
- Sites and determinands:
  - Sampled determinands span physical/chemical water quality metrics (e.g., conductivity, pH, temperature, DO, Secchi depth), nutrients (SRP, TP, TSP), chlorophyll a, and a comprehensive suite of zooplankton taxa densities.
- Data completeness and format:
  - Missing values represented as NA to align with common data standards.
  - Data are organized by site and replicates (e.g., RB1, RB2; L1, L2) for replicated measurements.

## References and further reading
- Methodological foundations and historical references for analyses and sampling procedures (e.g., Murphy & Riley 1962 for SRP; Wetzel & Likens 2000 for TP; Golterman et al. 1978; Dussart & Defaye 1995; etc.).
- Additional information and context available in related Hydrobiologia issues and Scottish Natural Heritage reports.