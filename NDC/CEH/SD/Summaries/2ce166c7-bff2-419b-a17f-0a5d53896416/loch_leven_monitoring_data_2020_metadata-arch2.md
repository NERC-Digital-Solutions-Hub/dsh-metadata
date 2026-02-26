# Loch Leven long-term monitoring dataset

- Purpose and scope
  - Describes data from the Loch Leven long-term monitoring programme (started 1968; ongoing at time of writing).
  - Data, sampling/analysis methods, data processing, and output format are documented.
  - Part of UK-SCAPE WP7 LEVEN project; conducted by NERC and later NERC/UK Centre for Ecology & Hydrology.

- Sampling regime and sites
  - Fortnightly sampling generally.
  - Two main sampling sites: Reed Bower (RB) and Sluices (L/Sl8); Reed Bower accessed by boat, Sluices by boat or shore.
  - Occasionally sampling is impossible due to weather, ice, or resource constraints.
  - Site codes referenced in the dataset: Harbour (H), Reed Bower (RB5), Sluices/Outflow (L/Sl8); coordinates provided.

- Measurements and methods
  - In situ measurements: conductivity, pH, temperature; Secchi depth measured at Reed Bower.
  - Water samples collected at each site for laboratory analyses: SRP, TP, TSP (filtered), soluble silicate, total diatom silica, chlorophyll a.
  - Sampling at Reed Bower uses a 0.25 m from bottom integrated sample; Sluices uses a bottle 10 cm below surface.
  - Laboratory analyses include standard nutrient and chlorophyll methods with details referenced (Murphy & Riley 1962; Wetzel & Likens 2000).

- Nutrients and chemistry
  - SRP determined by phosphomolybdate/ascorbic acid method; absorbance at 882 nm.
  - TP measured on unfiltered samples after persulfate digestion; TSP from filtered samples.
  - Procedures align with established limnological methods.

- Weather data
  - Cloud cover, wind direction, and wind force recorded at Reed Bower when possible.
  - Wind force translated to Beaufort scale with a detailed lookup (Table 2).

- Crustacean zooplankton data
  - Densities (ind/L) of multiple crustacean taxa at Reed Bower and Sluices.
  - Taxa include Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus (HB data may vary by site).
  - Sampling: Reed Bower via 4 m net haul (120 µm); Sluices via 30 L surface water through 120 µm net.
  - Preservation in formaldehyde; counts converted to ind/L; counts archived.

- Data processing and quality control
  - Data processed with an import script in R prior to database entry.
  - Wind force: when a range is given (e.g., 4-5), the first value is used.
  - Probe replicate handling: values retained if within Median Absolute Deviation (MAD) of median; pH values transformed for MAD calculations (log10 transformations applied as specified); outputs rounded (pH/DO to 2 decimals; conductivity/DO% and temperatures to 1 decimal).
  - Automated and manual QA checks performed; anomalies investigated and corrected where appropriate.

- Data format and documentation
  - All data stored in a single CSV file.
  - Columns include site conditions, lake chemistry, and crustacean/zooplankton counts with units; missing values marked as NA.
  - Column descriptions (Table 3) provide full determinand, site, and unit details (e.g., Date, Week_of_Year, Wind_Force, Depth_m, Secchi_m, conductivity, pH, TP, SRP, TSP, chla, zooplankton taxa, etc.).

- Data accessibility and use
  - Datasets are stored and uploaded to appropriate data portals for accessibility.
  - Outputs are designed to support standardised formats for comparing environmental health and policy performance over time.

- Key challenges and opportunities
  - Increasing the value of datasets by integrating with other relevant data (avoiding single-use datasets).
  - Enabling broader access to the underlying data used to produce the final outputs for verification and extended analyses.