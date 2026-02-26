# DATA HEADER information for Sapling_carbon_stock.csv

- Overview
  - Dataset records the carbon stock of regenerating tree clusters.
  - Part of ESPA Programme with P4GES project; DOI provided.
  - Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

- Data schema and key fields
  - site_ID
    - Information: P4GES site code
    - Variable type: Text
    - Unit: .
  - Number_saplings
    - Information: number of trees with diameter < 5 cm and height > 1.3 m counted in a 2 m radius circle
    - Variable type: Numeric
    - Unit: .
  - Number_collected_saplings
    - Information: number of sapling trees collected among the population inside the 2 m radius circle
    - Variable type: Numeric
    - Unit: .
  - Fresh_weight_total
    - Information: weight of all collected saplings
    - Variable type: Numeric
    - Unit: grams
  - Fresh_weight_sample
    - Information: weight of the sample among the collected saplings (biomass analysis)
    - Variable type: Numeric
    - Unit: grams
  - Dry_weight_sample
    - Information: weight of subsample after oven drying (stabilized dry weight)
    - Variable type: Numeric
    - Unit: grams
  - Dry_weight_collected_saplings
    - Information: weight of all collected saplings after oven drying
    - Variable type: Numeric
    - Unit: grams
  - Biomass
    - Information: Biomass stock of sapling
    - Variable type: Numeric
    - Unit: milligrams per hectare (Mg.ha-1)
  - Stock_C
    - Information: Carbon stock of sapling
    - Variable type: Numeric
    - Unit: milligrams per hectare (Mg.ha-1)

- Data notes and quality considerations
  - Notes field indicates: "means no data" (missing data indicator)
  - Some text contains minor inconsistencies (e.g., radius and unit descriptions) to be clarified during data cleaning

- Data provenance and usage considerations
  - Source program/project: ESPA (P4GES)
  - Site codes correspond to P4GES sites
  - Data may require integration with other datasets to enhance analyses (e.g., site characteristics, temporal data)

- Potential data products and end-user applications (Data Support perspective)
  - Self-serve dashboards or pivot tables to summarize by site, carbon stock (Stock_C), and biomass (Biomass)
  - Calculations to compare biomass vs. carbon stock across sites or over time
  - Data quality reports highlighting missing values indicated by the Notes field
  - Documentation for users on data provenance, units, and data cleaning steps
  - Guidance materials to help end users interpret sapling biomass and carbon stock measurements

- Access and attribution
  - Ensure acknowledgement of ESPA P4GES and Laboratoire des Radio Isotopes, Université d'Antananarivo for derived products
  - Include DOI and project details when sharing outputs or dashboards