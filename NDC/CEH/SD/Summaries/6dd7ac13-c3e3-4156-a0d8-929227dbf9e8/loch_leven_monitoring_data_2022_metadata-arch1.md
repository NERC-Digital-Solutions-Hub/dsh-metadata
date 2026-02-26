# Loch Leven long-term monitoring data

- The dataset comes from Loch Leven, a lowland lake in Scotland, collected as part of a long-term monitoring programme that began in 1968 and continues under the UK-SCAPE WP7 LEVEN project. It describes data, sampling and analysis methods, data processing, and the output format.
- Data produced by staff from former NERC institutions and, more recently, NERC/UKCEH.

## Sampling regime and sites

- Sampling generally occurs fortnightly at two main sites: Reed Bower (RB) and Sluices/Outflow (L/Sl8). A Harbour site (Site_H) is used for reference in the coding scheme.
- Reed Bower is boat-accessible; Sluices can be sampled by boat or from shore. If boat access is not used, data may be recorded as Outlet but referenced as Sluices for ease.
- Occasionally sampling is skipped due to resource constraints, bad weather, or ice cover.
- Measurements can be field-based or laboratory analyses of field-sampled water.

## Measurements, analysis, and site details

- In situ measurements: conductivity, pH, temperature (measured at most sites); Secchi depth measured at Reed Bower only.
- Water samples: two main 2 L duplicates per site. Reed Bower uses a weighted integrated sampler; Sluices uses a bottle held 10 cm below the surface.
- Laboratory analyses (on field-collected samples): soluble reactive phosphorus (SRP), total soluble phosphorus (TSP; filtered and frozen), soluble reactive silicate, total diatom silica, total phosphorus (TP; unfiltered and frozen), chlorophyll a (via filtration).
- Determinands and methods:
  - SRP: Murphy & Riley (1962) method; phosphate forms form phospho-molybdenum blue; absorbance at 882 nm.
  - TP and TSP: digestion of all phosphorus forms to SRP using sulfuric acid and persulphate; method per Wetzel & Likens (2000).
  - Chla: 400 ml filtered through GF/C; filter frozen until analysis.
- Weather data (where possible): cloud cover, wind direction and force (Beaufort scale) recorded at Reed Bower; wind-force lookup table provided.

## Crustacean & zooplankton data

- Two sites (RB and Sl8) with densities (ind/L) for a range of crustacean zooplankton taxa (e.g., Daphnia hyalina, Eudiaptomus gracilis, Cyclopidae, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, etc.).
- Zeros indicate non-recorded taxa in a given sample; NAs indicate missing values.
- As of 2022, column names were updated for consistency, and two new taxa were added at the end (Ceriodaphnia sp. and Polyphemus pediculus).
- Collection methods: RB samples via 4 m angled net haul (120 µm); Sl8 samples via passing 30 L surface water through a 120 µm net; preservation in 4% formaldehyde.
- Lab processing: counts are converted to ind/L; subsamples counted under microscope; specimens identified to the level feasible by preservation and maturity; counts archived after reconstitution.

## Data processing and quality assurance

- An R-based import script processes data before loading into a database; several rules are applied:
  - Wind force: if a range (e.g., 4-5) is provided, the first value is stored.
  - Probe replicate values (conductivity, pH, DO, and related temperatures) are validated using Median Absolute Deviation (MAD); values outside MAD are discarded; pH values are converted to 10^pH for calculation, then back-transformed and averaged; rounding rules apply (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
  - Inter-calibration was performed when HQ4300 replaced HQ30d for the conductivity/condition measurements.
- Both automated and manual checks verify data integrity; anomalies are investigated and corrected as appropriate.

## Data format and column definitions

- Data are stored in a single CSV file with columns describing the determinand, site conditions, lake chemistry, and crustacean/zooplankton counts; missing values are NA.
- Column descriptions (example fields):
  - Date, Week_of_Year: sampling date and week number.
  - Water_Level_cm_Site_H, Depth_m_Site_RB, Secchi_m_Site_RB: site-level physical measurements.
  - Cloud_cover_Eighths_Site_RB, Wind_Direction_Site_RB, Wind_Force_Beaufort_scale_Site_RB: weather conditions.
  - Conductivity_µS/cm_Hach_HQ4300_Site_RB, Temperature_°C_HQ4300_(cond)_Site_RB: water chemistry linked to conductivity measurements.
  - DO_mg/L_Site_RB, DO_%_Site_RB: dissolved oxygen measurements.
  - pH_HQ4300_Site_RB, TP_ugP/l_Site_RB1/L2, SRP_ugP/l_Site_RB1/RB2, TSP_ugP/l_Site_RB1/RB2: phosphorus-related measurements.
  - chla_ug/l_Site_RB1/RB2: chlorophyll a.
  - Zooplankton taxa counts: multiple taxa with per-site ind/L values (e.g., Daphnia_hyalina_ind/L_Site_RB, Cyclops_abyssorum_ind/L_Site_RB, Polyphemus_pediculus_ind/L_Site_RB, etc.).
- Table 3 provides full, detailed mappings of determinands, sites, and units.

## Methods and references

- Core measurement and analysis methods cited:
  - Golterman, Clymo, Ohnstad (1978) for general water analysis methods.
  - Murphy & Riley (1962) for phosphate determination.
  - Wetzel & Likens (2000) for inorganic nutrients analysis.
- Additional readings include Hydrobiologia special issues and Scottish Natural Heritage reports on Loch Leven from 2008–2012 and a 40-year research volume.

## Scope and purpose

- The dataset integrates lake chemistry (nutrients, pH, conductivity, DO, Secchi depth) with biotic data (crustacean zooplankton densities) across two monitoring sites over extended timeframes.
- It is designed for researchers and analysts to identify temporal patterns, correlations between physico-chemical variables and biotic communities, and to support long-term ecological assessments.