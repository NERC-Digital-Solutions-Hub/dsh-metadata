# Loch Leven long-term monitoring dataset

- Purpose and scope
  - Long-term data from Loch Leven, a lowland Scottish lake, collected since 1968 as part of a wider monitoring programme.
  - Aims to document environmental conditions in a consistent format for evaluating environmental health and policy performance over time.
  - Data are processed and presented in standardized outputs (reports, maps, charts) and stored in appropriate data portals.

- Monitoring programme and oversight
  - Sampling and analyses conducted by NERC and UK Centre for Ecology & Hydrology staff.
  - Project context: UK-SCAPE WP7 LEVEN.
  - Emphasis on verification, quality assurance, cleaning, and transformation of established data streams.

- Sampling regime
  - Fortnightly sampling frequency, generally at two sites: Reed Bower and Sluices.
  - Reed Bower: boat-access only; Sluices: boat or shore sampling possible.
  - Data recorded as “Outlet” when sampled without a boat; labeled as “Sluices” for ease of use.
  - Weather and resource constraints can prevent sampling; if boat unsafe, only Sluices may be sampled; extreme cases may prevent both sites.

- Study sites and location details
  - Harbour (Site_H), Reed Bower (Site_RB or RB5), and Sluices/Outflow (Site_L or Sl8).
  - Geographic coordinates provided (UK National Grid epsg:27700) for site locations.
  - Figure and Table references in the original document map site locations.

- Measurements and analyses
  - In situ measurements: conductivity, pH, temperature; Secchi depth measured at Reed Bower.
  - Laboratory analyses on field-collected water samples:
    - Soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP)
    - Soluble reactive silicate and total diatom silica
    - Chlorophyll a
  - Phosphorus methods follow Murphy & Riley (1962) for SRP; TP uses a persulfate digestion per Wetzel & Likens (2000).
  - Chlorophyll a: 400 mL filtered and stored for analysis.
  - Weather observations (cloud cover, wind direction, wind force) recorded at Reed Bower when possible; wind force mapped to Beaufort scale and sea-condition descriptions.

- Sampling and collection specifics
  - Reed Bower: integrated sample collected with a weighted PVC tube to sample the full water column.
  - Sluices: surface water collected with a bottle (10 cm below surface).
  - Replicates: two 2 L water samples per site; sub-samples processed in the laboratory for the various analyses.

- Crustacean & Zooplankton dataset
  - Densities of crustacean zooplankton (ind/L) at Reed Bower and Sluices for multiple taxa (e.g., Daphnia hyalina, Eudiaptomus gracilis, Cyclopidae, Cyclops spp., Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Ceriodaphnia_sp., Polyphemus pediculus, etc.).
  - Zoonplankton data produced from preserved samples, with counting under microscopy and conversion to ind/L.
  - Zero values indicate non-detection at sampling resolution; some values may be NA (missing).
  - As of 2022, column names were updated for consistency; two new taxa added (Ceriodaphnia_sp. and Polyphemus pediculus) at both sites.
  - Reed Bower sampling method: 4 m angled net haul (120 µm); Sluices sampling: 30 L of surface water filtered (120 µm); preservation in 4% formaldehyde.
  - Laboratory processing includes subsampling, species identification to practical taxonomic resolution, and allocation to per-liter densities.

- Data processing and quality assurance
  - Data imported and processed with an R script that applies predefined rules to ensure sensible values.
  - Wind force values: when multiple values like “4-5” appear, the first value is retained.
  - Probe replicates (conductivity, pH, DO, and related temperatures) are screened using Median Absolute Deviation (MAD); outlier rejection depends on replicate count and results are transformed as needed (pH values converted to 10^pH, then logged, averaged, and converted back; rounding applied to two decimals for pH/DO and one decimal for conductivity/temperatures).
  - Inter-calibration: HQ30d replaced by HQ4300; calibration ensured to maintain consistency in measurements.
  - Automated and manual QA checks performed on all data to identify and correct anomalies.
  - Data format: stored as a single CSV file with descriptive column names, units, and site information; missing values marked as NA.

- Data format and column metadata
  - Columns describe determinand, site, units, and conditions; internally standardized in 2023 (abbreviations updated: litres -> L, micrograms -> μg represented as u, degrees symbol -> deg).
  - Ceriodaphnia_sp. added; additional taxa added at the end of the zooplankton dataset.
  - Example column descriptions include date, week of year, water level at Harbour, cloud cover, wind direction and force (Beaufort), depth, Secchi depth, conductivity, temperature, DO, pH, TP/SRP/TSP, chlorophyll a, and zooplankton densities for multiple taxa across sites.
  - The detailed Table 3 provides full column-by-column definitions, site association, and units.

- References and further reading
  - Methods for Physical and Chemical Analysis of Fresh Waters (Golterman et al., 1978)
  - Murphy & Riley (1962) SRP method
  - Wetzel & Likens (2000) Limnological Analyses
  - Additional readings: special Hydrobiologia issue and Scottish Natural Heritage reports
  - Related Loch Leven outputs: 40 years of scientific research (Spears & May, 2012)

- Data accessibility and long-term usefulness
  - Datasets are designed for cross-time comparisons of environmental health and indicators of lake quality.
  - Standardized outputs support monitoring programme scrutiny and policy assessment.
  - Data are stored in a consistent CSV format with clear documentation of measurement methods, processing steps, and taxonomic updates to ensure reproducibility and data integration across time.