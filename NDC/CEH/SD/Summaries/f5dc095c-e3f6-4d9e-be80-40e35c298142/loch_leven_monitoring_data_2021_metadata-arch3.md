# Abstract

- This dataset documents data from Loch Leven, a lowland Scottish lake, collected as part of a long-term monitoring programme that began in 1968 and continues under the UK Centre for Ecology & Hydrology, funded by NERC. It forms part of the UK-SCAPE WP7 LEVEN project.
- The documentation covers the nature of the data, sampling and analysis methods, data processing techniques, and output formats to enable reuse and interpretation.

- Sampling regime and sites
  - Fortnightly sampling with two main sites per occasion: Reed Bower (RB) and Sluices (L). Reed Bower is boat-accessible; Sluices can be sampled by boat or from shore.
  - Data labeled as Outlet when not using the boat at Sluices; dataset standardizes references as Sluices (L/Sl8) for ease.
  - Primary monitoring sites correspond to Harbour (H), Reed Bower (RB/RB5), and Sluices/Outflow (L/Sl8); coordinates provided (UK National Grid epsg:27700).
  - Sampling can be interrupted by weather, ice, resource limits. Secchi depth measured at Reed Bower; conductivity, pH, temperature measured in situ; water samples collected at each site for laboratory analyses.

- Measurements, sampling, and analyses
  - In situ measurements: conductivity, pH, temperature at most sites; Secchi depth at Reed Bower as a measure of water clarity.
  - Water sampling: two 2 L duplicates per site; Reed Bower uses an integrated sample from near the lake bottom, Sluices uses a bottle 10 cm below surface.
  - Laboratory analyses (on returned samples): soluble reactive phosphorus (SRP), total soluble phosphorus (TSP; filtered and frozen), soluble reactive silicate, total diatom silica, total phosphorus (TP; unfiltered and frozen), chlorophyll a (via filtration and freezing).
  - Analytical methods: SRP via Murphy & Riley (1962); TP via persulfate digestion with Wetzel & Likens (2000) protocol; chla via standard chlorophyll method.
  - Weather conditions (cloud cover, wind direction, wind force) recorded at Reed Bower when possible; wind force linked to Beaufort scale and sea-conditions descriptions.

- Crustacean and zooplankton component
  - Densities (individuals per litre) of crustacean zooplankton taxa collected at Reed Bower and Sluices, counting species where possible.
  - Taxa include Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae (total), Cyclops abyssorum, Cyclops vicinus, Cyclopod nauplii, Bosmina longirostris, Leptodora kindti, Bythotrophes longimanus, Chydoridae, Polyphemus pediculus.
  - Sampling and preservation: Reed Bower uses a 4 m net (120 µm); Sluices uses 30 L surface water passed through a 120 µm net. Samples preserved in 4% formaldehyde.
  - Laboratory processing: subsampling and counting under a microscope; identification to species where possible; counts converted to ind/L; four subsamples counted per sample; samples archived after counting.

- Data processing, quality assurance, and processing decisions
  - An R-based import script processes data before database entry with explicit handling rules:
    - Wind force: when presented as a range (e.g., 4-5), the first value is used.
    - Probe replicate values: values are retained if they fall within Median ± MAD; approach preserves small sample sizes while filtering outliers.
    - pH handling: pH values converted to 10^pH for MAD calculations, then transformed back; final reported values are rounded to 2 decimals; DO concentration and temperature rounded to 1 decimal; other variables rounded as appropriate.
    - Inter-calibration note: HQ30d sensors used historically; new HQ4300 model introduced; dataset retains HQ30d column naming to preserve structure; future datasets will reflect HQ4300 in column names without altering column order.
  - Automated and manual quality checks ensure data entry accuracy and value ranges; anomalies are investigated and corrected where appropriate.

- Format, storage, and metadata
  - Data stored in a single CSV file with columns describing the determinand, site conditions, lake chemistry, and crustacean/zooplankton counts; missing data marked as NA.
  - Column naming convention encodes determinand, site, and units (example: Date, Site, Week_of_Year, Water_Level_cm_Site_H, Conductivity_µS/cm_Hach_HQ30d_Site_RB, etc.).
  - Detailed column descriptions (Table 3) provide descriptions for each column, including date, site, week, weather, depth, Secchi depth, conductivity, temperature, dissolved oxygen, pH, phosphorus fractions (TP, SRP, TSP), chlorophyll a, and zooplankton counts/densities.

- References and further reading
  - Method references for analyses: Golterman et al. (1978); Murphy & Riley (1962); Wetzel & Likens (2000).
  - Additional readings include Hydrobiologia issues and reports on Loch Leven monitoring and long-term research (e.g., Dudley et al. 2012; Spears & May 2012).

- Implications for monitoring framework design
  - Demonstrates comprehensive long-term data collection across physical, chemical, and biological indicators with clearly documented methods, quality control, and data processing rules.
  - Highlights importance of metadata completeness (site identifiers, coordinates, measurement methods, units) and transparent data processing decisions to support reproducibility.
  - Provides a model for balancing field practicality (fortnightly sampling, two sites) with robust laboratory analyses and zooplankton biodiversity assessment.
  - Underlines governance aspects relevant to monitoring frameworks: data provenance, standardized formatting (CSV with explicit column metadata), and automated QA workflows to maintain data quality over decades.