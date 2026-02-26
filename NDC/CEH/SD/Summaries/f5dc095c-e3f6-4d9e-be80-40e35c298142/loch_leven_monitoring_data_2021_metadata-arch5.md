# Loch Leven long-term monitoring dataset

- Overview
  - Long-running dataset from Loch Leven, a lowland lake in Scotland, collected since 1968 as part of a continuous monitoring programme.
  - Data collection and processing conducted by organisations under the Natural Environment Research Council (NERC) and later the NERC / UK Centre for Ecology & Hydrology.
  - Document describes data, sampling/analysis methods, data processing, and output format; tied to project UK-SCAPE WP7 LEVEN.

- Sampling regime and sites
  - Fortnightly sampling generally; two main sampling sites: Reed Bower (RB) and Sluices (L/Sl8). Harbour (H) and additional RB/L references appear in the dataset naming.
  - Reed Bower is boat-accessible; Sluices can be sampled by boat or from shore/outflow. Occasional sampling gaps due to resources, weather, or ice.
  - When boat use is not possible, only Sluices may be sampled; extreme cases yield no sample.
  - Weather data (cloud cover, wind direction/force) recorded where possible; wind force described using Beaufort scale.

- Measurements and analyses
  - In situ measurements: conductivity, pH, temperature at most sites; Secchi depth measured at Reed Bower.
  - Laboratory analyses on field samples for:
    - Soluble reactive phosphorus (SRP) and total soluble phosphorus (TSP)
    - Soluble reactive silicate and total diatom silica
    - Total phosphorus (TP) and chlorophyll a
  - Methods referenced: Murphy & Riley (1962) for SRP; Wetzel & Likens (2000) for TP/TSP; standard filtration and storage procedures.
  - Duplicate 2 L water samples collected per site; sampling details differ by site (e.g., integrated sample at RB).
  - Crustacean and zooplankton data included (see below).

- Crustacean & zooplankton data
  - Densities (ind/L) for multiple crustacean zooplankton taxa at Reed Bower and Sluices:
    - Examples: Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae (total), Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrophes longimanus, Chydoridae, Polyphemus pediculus, among others.
  - Collection methods:
    - RB: 4 m angled net haul (120 µm mesh).
    - L: 30 L of surface water passed through 120 µm net.
  - Preservation: specimens preserved in 4% formaldehyde.
  - Laboratory processing: subsampling and counting under microscope; identification to species where possible; counts converted to ind/L using factors; samples archived after counting.
  - Zoonoplankton counts include zeros (not detected) and missing values (NA) as appropriate.

- Data processing, QA and governance
  - Import and processing pipeline implemented in R; dataset decisions documented (e.g., wind value handling, replication filtering).
  - Wind force values that appear as ranges (e.g., 4-5) use the first value for database consistency.
  - Probe replicate handling:
    - Measurements from Hach probes (conductivity, pH, DO) are accepted if within Median Absolute Deviation (MAD) from the median; ensures inclusion of limited replicates.
    - pH values converted to 10^pH for MAD/median calculations and then back-transformed; resulting values rounded to 2 decimals (DO and temperature to 1 decimal).
  - Instrument change note:
    - Hach HQ30d replaced by HQ4300 in 2022; for this dataset, HQ30d columns retained to preserve structure; future datasets may switch to HQ4300 with unchanged column order.
  - Quality assurance:
    - Automated and manual checks for data entry errors and out-of-range values; anomalies investigated and corrected where appropriate.

- Data format and metadata
  - Data stored as a single CSV file.
  - Columns include site conditions, lake chemistry, crustacean/zooplankton counts, with explicit units and site identifiers.
  - Missing data represented as NA.
  - Column naming encodes determinand, site, and units; detailed descriptions provided in Table 3 (and accompanying documentation).

- Column descriptions and references
  - Extensive column naming scheme (e.g., date, site, week, water level, cloud cover, wind, depth, conductivity, temperature, DO, pH, TP/SRP, chlorophyll a, and numerous zooplankton/phytoplankton metrics).
  - References for methods and taxonomy provided, including:
    - Methods for water chemistry and analyses (Golterman et al. 1978; Murphy & Riley 1962; Wetzel & Likens 2000).
    - Taxonomic guides for crustacean zooplankton (Dussart & Defaye 1995; Einsle 1996; Flößner & Kraus 1986; Harding & Smith 1974; Scourfield & Harding 1966).

- Caveats and usage notes for data stewards
  - Data cover multiple decades with potential sampling gaps due to weather or logistical constraints.
  - Site IDs and alternative codes exist; careful mapping required when integrating with other datasets.
  - Updates and data lineage are documented (instrument changes, processing rules, QA steps) to support reproducibility and governance.
  - Metadata is comprehensive (unit conventions, site-specific measurements, and determination methods) to facilitate proper data discovery, sharing, and reuse.