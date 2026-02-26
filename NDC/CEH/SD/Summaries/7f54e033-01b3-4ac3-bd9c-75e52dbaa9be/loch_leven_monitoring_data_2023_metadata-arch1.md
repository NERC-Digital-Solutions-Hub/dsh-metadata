# Abstract

- Loch Leven long-term monitoring dataset (started 1968; ongoing at time of writing) collected and analyzed by NERC and UKCEH staff under project UK-SCAPE WP7 LEVEN.
- Document describes data nature, sampling/analysis methods, data processing, and output format of the dataset.
- Data cover lake chemistry and crustacean/zooplankton metrics collected as part of a continuous monitoring programme.

## Sampling regime and sites

- Fortnightly sampling with two main sites per occasion: Reed Bower (RB) and Sluices/Outflow (L/Sl8); Harbour (H) referenced in data via site codes.
- Reed Bower accessible only by boat; Sluices can be sampled by boat or from shore/outlet.
- Sampling may be halted by resource constraints, bad weather, ice; at times only one site or none can be visited.
- Site coordinates and IDs provided; site names include Harbour (H), Reed Bower (RB5), Sluices/Outflow (L/Sl8).

## Measurements and analyses conducted in situ and in the lab

- In situ measurements: conductivity, pH, temperature (via handheld probes); Secchi depth measured at Reed Bower.
- Water samples collected as duplicates from each site for laboratory analyses: SRP, TP (unfiltered; digested for all phosphorus forms), TSP (filtered), soluble silicate, total diatom silica, chlorophyll a (via filtration).
- Determination methods: Murphy & Riley (SRP); Wetzel & Likens (TP/TSP) with digestion steps; standard references provided.
- Weather observations: cloud cover, wind direction, wind force (as available); wind force linked to Beaufort scale with a lookup table.
- Data formats: outputs stored as CSV with site, date, determinands, units, and metadata.

## Crustacean and zooplankton data

- Densities of crustacean zooplankton recorded from Reed Bower and Sluices; taxa include Daphnia, Eudiaptomus, Cyclopidae, Cyclops spp., Bosmina, Leptodora, Bythotrephes, Chydoridae, Ceriodaphnia, Polyphemus pediculus, among others (as of 2022/2023).
- Data express individuals per litre (ind/L); zeros indicate non-recorded presence at sampling/analytical resolution; NAs indicate missing values.
- Sampling: RB via 4 m net haul (120 µm); L via filtration of 30 L surface water (120 µm); samples preserved in 4% formaldehyde.
- Lab processing: subsampling with precise counts under microscope; counts converted to ind/L; specimens archived.
- Taxa updated over time (e.g., Ceriodaphnia sp. added; Polyphemus pediculus added).

## Data processing and quality assurance

- Data ingested with an R import script applying sensible defaults and rules.
- Wind force: when ranges (e.g., 4-5) appear, the first value is used.
- Probe replicates (conductivity, pH, DO, and related temperatures): values kept if within Median ± MAD; extreme cases retained when only 1–2 replicates exist.
- pH values converted to 10^pH for MAD calculations, then transformed back; means computed and values rounded (pH/DO to 2 dp; conductivity/DO% and temperatures to 1 dp).
- Interim inter-calibration: HQ30d replaced by HQ4300; inter-calibration performed to maintain consistency.
- Quality assurance: automated and manual checks for data entry errors and out-of-range values; anomalies investigated and corrected as needed.

## Data format, structure, and column details

- Data stored in a single CSV file with columns describing determinands, sites, conditions, lake chemistry, and crustacean/zooplankton counts; missing values marked NA.
- 2023 updates: column naming made internally consistent and encoding-friendly (e.g., litres → L, µ → u, ° → deg); Ceriodaphnia_sp. added; additional taxa included at dataset end.
- Column descriptors (example): Date, Week_of_Year, Water_Level_cm at Harbour (H), Cloud_cover_Eighths at Reed Bower (RB), Wind_Direction at Reed Bower, Depth_m at Reed Bower, Secchi depth at Reed Bower, Conductivity at RB and L (HQ4300), Temperature corresponding to conductivity, DO measurements (mg/L and %), pH, pH-related temperatures, TP/SRP/TSP (with replicates), chlorophyll a, and densities for multiple zooplankton taxa (RB and L sites).

## References and further reading

- Methodological foundations for water chemistry analyses (Golterman et al., Murphy & Riley, Wetzel & Likens).
- Related reporting and long-term Loch Leven work: Hydrobiologia special issues and Scottish Natural Heritage reports (e.g., Dudley et al. 2012; Spears & May 2012).