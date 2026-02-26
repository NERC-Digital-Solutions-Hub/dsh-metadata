# Loch Leven long-term monitoring dataset

- Overview: Data from Loch Leven, a lowland Scottish lake, collected as part of a long-term monitoring programme since 1968. The dataset documents sampling methods, measurements, processing, and output formats. Managed under project UK-SCAPE WP7 LEVEN and compiled by NERC / UK Centre for Ecology & Hydrology staff over time.

- Sampling regime and sites:
  - Fortnightly sampling at two main sites: Reed Bower (RB) and Sluices/Outflow (L). Reed Bower accessible by boat; Sluices accessible by boat or from shore.
  - Occasionally sampling is missed due to resource limits, weather, or ice; when boat use is unsafe, only Sluices may be sampled, and in extreme cases neither site is sampled.
  - Site codes used in data: Harbour (Site_H), Reed Bower (Site_RB), Sluices (Site_L); geographic coordinates provided (UK National Grid epsg:27700).

- Measurements and analyses:
  - In situ measurements: conductivity, pH, temperature, and Secchi depth (Secchi measured at Reed Bower only).
  - Water samples collected as duplicates (2 L per site) with site-specific collection methods; laboratory analyses performed on filtered or unfiltered subsamples.
  - Determinands and methods:
    - Nutrients: soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP) with appropriate digestion/filtration steps.
    - Chlorophyll a: measured by filtering 400 mL and storing filters frozen until analysis.
    - Other parameters: conductivity, pH, temperature for respective measurements.
  - Analytical methods referenced (e.g., Murphy & Riley 1962 for SRP; Wetzel & Likens 2000 for TP).

- Weather and site conditions:
  - Weather data (cloud cover, wind) recorded at Reed Bower when possible; wind force linked to Beaufort scale with a lookup table.
  - Depth, Secchi depth, and other site conditions recorded; water level relative to harbour wall also documented.

- Crustacean & Zooplankton data:
  - Densities (ind/L) of multiple crustacean zooplankton taxa collected at RB and L.
  - Taxa include Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Ceriodaphnia sp., Polyphemus pediculus, and others.
  - Zoonplastic preserved in 4% formaldehyde; counting conducted under light microscopy; counts converted to ind/L; samples generally identified to species level when possible.
  - 2022 dataset updates: some column names adjusted for consistency; two new taxa added (Ceriodaphnia sp. and Polyphemus pediculus) at both sites.

- Data processing and quality assurance:
  - Data processed with an R import script that handles:
    - Wind value formatting: uses first value in ranges like "4-5".
    - Probe replicates: replicate measurements validated by Median Absolute Deviation (MAD); outlier rejection applied conservatively to preserve small sample sizes; pH values converted to 10^pH for processing, then back to pH scale; values rounded (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
    - Calibration update: HQ30d replaced by HQ4300; inter-calibration performed to maintain consistency.
  - Automated and manual QA checks performed on all data; unusual values investigated and corrected as needed.

- Data format, storage, and metadata:
  - Output format: a single CSV file containing all data with columns detailing determinands, site conditions, lake chemistry, and crustacean/zooplankton counts; missing values marked as NA.
  - Column naming and descriptions: comprehensive metadata describing determinand, site, and units; 2023 update standardized terminology (e.g., litres to L, micrograms to µ, degrees to deg) and added Ceriodaphnia_sp. Columns aligned to encoding-friendly formats.
  - Core reference tables (Table 3) provide detailed descriptions of every column, including date, week, site, environmental conditions, and all measured constituents.

- Governance, provenance, and updates:
  - Dataset provenance traces to the Loch Leven long-term monitoring programme with documented sampling, storage, and laboratory methods.
  - Versioning and schema updates implemented (notably 2022–2023) to improve consistency and include new taxa; changes are reflected in column headers and documentation while maintaining overall data structure.
  - Documentation includes references for analytical methods and suggested further reading, supporting reproducibility and traceability.

- References and supporting materials:
  - Method references: Golterman et al. (1978), Murphy & Riley (1962), Wetzel & Likens (2000).
  - Additional reading: Hydrobiologia special issues and SNH reports on Loch Leven research.
  - Zooplankton identification keys cited for taxa included in the dataset.