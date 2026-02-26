# DATA HEADER information for Lying_dead_wood_carbon_stock.csv

- Overview
  - Describes biomass stock in the lying dead wood pool, including fallen trees sampled along transects within each plot.
  - Acknowledge related materials and projects: ESPA programme and P4GES project.
  - See also the manual reference: Manual 1_Classical_Survey.

- Data structure and key variables
  - Site_ID
    - Information: P4GES site code
    - Type: Text/String
  - Category
    - Wood density classification
    - Type: Categorical
    - Categories: S (sound), I (intermediate), R (rotten)
    - Density value associated with each category (see Density)
  - Density
    - Corresponding density values by wood category (S, I, R)
    - Type: Numeric
    - Unit: Unitless
  - Diameter
    - Diameter of the dead wood trunk in the transect crossing area
    - Type: Numeric
    - Unit: Centimeters (cm)
  - Volume
    - Estimated volume of lying dead wood
    - Type: Numeric
    - Unit: Cubic metres (m3)
  - Biomass
    - Biomass stock of lying dead wood
    - Type: Numeric
    - Unit: Milligrams per hectare (Mg.ha-1)
  - Stock_C
    - Carbon stock of lying dead wood
    - Type: Numeric
    - Unit: Milligrams per hectare (Mg.ha-1)

- Data provenance and references
  - DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
  - Programme: ESPA
  - Project: P4GES
  - Acknowledgement: Required for products derived from these data to Credit Laboratoire des Radio Isotopes, Université d'Antananarivo
  - References: Winrock International 2005. Impact of logging on carbon stocks of tropical forests: the republic of Congo case study. (link provided in notes)

- Notes and data quality
  - Notes: "means no data" (missing data indicator)
  - Data formatting and unit details may require careful interpretation (e.g., Biomass and Stock_C units as stated)

- Usage considerations
  - Data can be used to assess lying dead wood biomass and carbon stock across plots, with transect-based sampling.
  - Outputs derived from these data should include appropriate acknowledgments and citations as specified.