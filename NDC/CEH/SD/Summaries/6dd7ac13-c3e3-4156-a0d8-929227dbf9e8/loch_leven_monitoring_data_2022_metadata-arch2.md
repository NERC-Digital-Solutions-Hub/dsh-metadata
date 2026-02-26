# Loch Leven long-term monitoring dataset

- Aim of the dataset
  - Provide a consistent, time-series view of Loch Leven’s environmental health to support scrutiny of environmental health and policy performance over time.
  - Support standardised outputs suitable for analysis and comparison across periods and outputs (reports, maps, charts).
  - Ensure data are verifiable, quality-assured, and stored in accessible data portals/datasets.

- Who contributes and how the data are gathered
  - Collected as part of Loch Leven’s long-term monitoring programme (ongoing since 1968), with recent work by NERC/UK Centre for Ecology & Hydrology.
  - Data cover a combination of water chemistry, physical parameters, and crustacean zooplankton densities.
  - Sampling occurs fortnightly at two main sites (Reed Bower and Sluices/Outflow); Harbour data are referenced via site codes as needed.
  - Sampling may be disrupted by weather, ice, or resource constraints; when boats are unusable, only Sluices may be sampled (or neither site on extreme occasions).

- Sites and site coding
  - Harbour (Site_H), Reed Bower (Site_RB or RB5), Sluices/Outflow (Site_L or Sl8).
  - Site coordinates provided (UK National Grid EPSG:27700) for Harbour, Reed Bower, and Sluices.
  - Data columns encode site and determinand (e.g., water level, Secchi depth, conductivity, pH, temperature, DO, TP, SRP, chla, zooplankton counts).

- Measurements, measurements regime, and methods
  - In situ measurements: conductivity, pH, temperature, Secchi depth (Secchi depth measured at Reed Bower; other sites typically measured in situ as field conditions allow).
  - Water sampling: duplicate 2 L samples from each site; Reed Bower uses a weighted tube to sample the whole water column; Sluices uses a bottle 10 cm below the surface.
  - Laboratory analyses (from field samples): soluble reactive phosphorus (SRP), total soluble phosphorus (TSP, filtered and frozen), soluble reactive silicate, total diatom silica, total phosphorus (TP, unfiltered and frozen), chlorophyll a (via filtration and freezing).
  - Determinands include: SRP (µg/L), TP (µg/L), TSP (µg/L), chlorophyll a (µg/L), dissolved oxygen (DO, mg/L and %), pH, various temperature measurements, and conductivity (µS/cm).
  - Weather observations (when possible) include cloud cover, wind direction, and wind force (Beaufort scale); wind force values map to wind speeds and sea-state descriptions.

- Crustacean & Zooplankton dataset
  - Densities of crustacean zooplankton from Reed Bower and Sluices, reported as numbers per litre (ind/L).
  - Taxa include Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, and others (with 2022 additions for Ceriodaphnia sp. and Polyphemus pediculus).
  - Sampling, preservation, identification, and counting procedures described; counts converted to ind/L; samples preserved in formaldehyde and later counted under microscope.

- Data processing and quality assurance
  - Processing performed with an R-based import script that standardises handling of data before database entry.
  - Wind force: when a range is given (e.g., 4-5), the first value is used.
  - Probe replicate values (conductivity, pH, DO, and related temperatures): values are included if they fall within Median ± MAD; this preserves use where replicates are limited; pH values are transformed to 10^pH for median/MAD calculation, then back to log scale and rounded to two decimals; other measurements rounded to 1 decimal (conductivity, DO %, temperatures) or two decimals as noted.
  - Inter-calibration: HQ30d replaced by HQ4300 for the Hach probe with inter-calibration to maintain consistency; column names updated to HQ4300 while order remains unchanged.
  - Automated and manual QA checks identify out-of-range or anomalous values; flagged values are investigated and corrected as appropriate.

- Data format and storage
  - Data stored in a single comma-separated values (CSV) file.
  - Columns include site conditions, lake chemistry, and crustacean/zooplankton counts with units and site information.
  - Missing data are marked as NA.
  - Column naming conventions: descriptive, indicating date, site, determinand, units, and other contextual details.

- Column descriptions and structure
  - Core schema includes: date, site, week-of-year, water level, cloud cover, wind direction and force, depth, Secchi depth; conductivity, temperature for conductivity measurements; DO (mg/L and %), DO temperature; pH and pH temperature; TP, SRP, TSP; chlorophyll a (chla); zooplankton taxa counts per site (ind/L) with corresponding metadata for each taxon (e.g., Cyclopidae total, Cyclops abyssorum, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, etc.).
  - For each determinand, the table provides description, site, and units; some replicates are noted (RB1, RB2, L1, L2) and correspond to replicate measurements or related dataset fields.

- Temporal scope and historical context
  - Long-running program dating back to 1968; documentation covers data collection, processing, and output generation across decades.
  - The 2022 dataset includes minor column-name updates for consistency and the addition of two new taxa; core data structure and order of columns remain stable.

- References and further reading
  - Methods references for analytical procedures (e.g., Murphy & Riley 1962 for SRP, Wetzel & Likens 2000 for TP/TSP).
  - Additional information and reports on Loch Leven include historical hydrobiological literature and SNH commissioned reports.
  - Zooplankton taxonomic references used for identification keys and procedures.