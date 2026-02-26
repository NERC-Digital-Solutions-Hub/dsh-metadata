DATA HEADER information for Sapling_carbon_stock.csv

- Overview
  - The dataset records the carbon stock of a regenerating tree cluster.
  - Associated with ESPA programme and P4GES project; requires acknowledgement to Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from the data.
  - Provides field definitions, data types, and units for key measurements used to assess sapling biomass and carbon stock.

- Key variables and definitions
  - site_ID: P4GES site code; text string; no unit specified.
  - Number_saplings: number of trees with diameter < 5 cm and height > 1.3 m counted within a 2 m radius circle; numeric.
  - Number_collected_saplings: number of saplings collected from among the population inside the 2 m radius circle; numeric.
  - Fresh_weight_total: total fresh weight of collected saplings; grams; numeric.
  - Fresh_weight_sample: weight of the field-collected sapling sample used for biomass analysis; grams; numeric.
  - Dry_weight_sample: dried weight of the subsample after oven drying (stabilized); grams; numeric.
  - Dry_weight_collected_saplings: total dry weight of all collected saplings after oven drying; grams; numeric.
  - Biomass: biomass stock of saplings; units indicated as milligrams per hectare (Mg.ha-1); numeric.
  - Stock_C: carbon stock of saplings; units indicated as milligrams per hectare (Mg.ha-1); numeric.

- Measurements and units
  - Fresh_weight_total, Fresh_weight_sample, Dry_weight_sample, Dry_weight_collected_saplings: grams.
  - Biomass, Stock_C: milligrams per hectare (noting the header text uses Mg.ha-1, which typically denotes megagrams per hectare; potential terminology inconsistency to be clarified).

- Methodological notes
  - Saplings are defined by diameter and height criteria and are counted within a 2 m radius circle around each site.
  - Biomass and carbon stock are derived metrics from collected saplings, with weights measured and processed (fresh and dry weights) prior to calculating stock values.

- Data quality, gaps, and governance
  - Notes field indicates “means no data” for any unspecified entries.
  - Data may require transformation or metadata augmentation to ensure interoperability across datasets.
  - Requires data provenance acknowledgment and adherence to data sharing and governance standards.

- Data provenance and usage considerations
  - Source programs: ESPA (Environmental SPectrum for Sustainability) and Project P4GES.
  - Acknowledgement requirement for works derived from these data.
  - Ensure consistent metadata and dataset provenance when integrating with monitoring frameworks or reporting dashboards.