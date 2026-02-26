# Experimental design/collection method

- Overview of the study design
  - Four laboratory populations from Belgium, representing two landscape types: woodland (Lauzelle, St. Hubert) and agricultural (Lillois, Hoegaarden).
  - Larvae collected randomly, reared on host plants of Petasites trivialis (P. trivialis) under control or drought-stressed conditions.
  - Equal contribution of each laboratory population to control and drought treatments.
  - Sample sizes: 178 larvae in control and 390 in drought-stressed groups; 3 larvae per plant; monitored through to eclosion; F1 adults weighed and sexed at emergence.
  - On eclosion, a subset of females used for reproductive data collection (100 females: 50 woodland-origin, 50 agricultural-origin).
  - Post-eclosion wing data collected from dead adults via imaging for morphometric analyses.

- Data collected and structure
  - Life history data (Life_history_data.csv)
    - Population, Description (site in Belgium), Landscape ( woodland vs agricultural ), Treatment (drought vs control), ID (individual), Adult_mass (mg), Total_development_time (days), Square_root_Total_devtime, sex (m/f)
  - Female reproductive output (Female_reproductive_output_data.csv)
    - Population, Description, Landscape, Description ( woodland vs agricultural ), Treatment, Description ( drought vs control ), ID, Adult_mass (mg), Mean_egg_size (mm^2), Longevity (days), Number_days_until_1st_egg_laid, Fecundity (total eggs laid), Arcsine_square_root_% Eggs_hatched, %Eggs_hatched
  - Wing data (Wing_data.csv)
    - Population, Description, Landscape, Description, Treatment, Description, ID, Adult_mass (mg), Total_development_time (days), sex, Wing_loading (mg/mm^2), Mean_forewing_Melanin, Mean_FW_aspect_ratio, Total_Wing_area (mm^2)

- Data formats and headers
  - All data stored as CSV spreadsheets
  - Files and headers
    - Life_history_data.csv: headers include Description, Population, Landscape, Treatment, ID, Adult_mass, Total_development_time, Square_root_Total_devtime, sex
    - Female_reproductive_output_data.csv: headers include Population, Description, Landscape, Description, Treatment, Description, ID, Adult_mass, Mean_egg_size, Longevity, Number_days_until_1st_egg_laid, Fecundity, Arcsine_square_root_% Eggs_hatched, %Eggs_hatched
    - Wing_data.csv: headers include Population, Description, Landscape, Description, Treatment, Description, ID, Adult_mass, Total_development_time, sex, Wing_loading, Mean_forewing_Melanin, Mean_FW_aspect_ratio, Total_Wing_area
  - Missing data are represented by empty cells

- Metadata, provenance, and collection details
  - Population origin: site in Belgium with landscape type (woodland vs agricultural)
  - Treatments: drought stress vs control host plant during larval rearing
  - Individual identifiers (ID) linked across datasets
  - Measurements and timing: eclosion date, development time, adult mass at eclosion, reproductive metrics, wing morphology metrics

- Data quality and processing notes
  - Raw data include both life-history metrics and derived fields (e.g., Total_development_time, Square_root_Total_devtime, Arcsine_square_root_% Eggs_hatched)
  - Some rows may have missing data due to mortality or incomplete observations; blank cells denote missing values
  - Wing measurements derived from digital images of wings; specific metrics include wing loading, melanization, aspect ratio, and total wing area

- Governance and reuse considerations for Data Stewards
  - Ensure consistent units across datasets (e.g., Adult_mass in mg, development time in days, wing areas in mm^2, egg sizes in mm^2)
  - Maintain stable IDs to enable cross-dataset joins (Life history, Reproductive output, Wing data)
  - Provide or maintain a data dictionary and metadata file summarizing column definitions, units, and data provenance
  - Address potential data quality concerns: unequal treatment group sizes, missing data due to mortality, and measurement consistency across samples
  - Consider data licensing, access controls, and update plans to support future discovery and reuse
  - Ensure documentation supports discoverability and usability for data users with varying levels of data management maturity

- Practical considerations for data management
  - Publish the three CSV files together with a concise data description and dictionary
  - Include clear notes on sampling design (four populations, two landscapes, two treatments) and randomization
  - Flag any data needed to interpret derived fields (e.g., how Arcsine transformation was computed)
  - Facilitate future integration with other datasets by harmonizing population identifiers and landscape labels across all files