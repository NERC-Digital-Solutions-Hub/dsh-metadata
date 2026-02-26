# DATA HEADER information for Lying_dead_wood_carbon_stock.csv

- Overview
  - Describes biomass stock in the lying dead wood pool, including fallen trees sampled along a transect in each plot.
  - DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
  - Programme: ESPA; Project: P4GES
  - Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo
  - References the Winrock International 2005 study used for volume estimation

- Data structure and fields
  - Site_ID
    - Information: P4GES site code
    - Variable Type: Text String
    - Unit: .
    - Field and materials_ressources: .
  - Category
    - Information: Wood density classification
    - Variable Type: Categorical
    - Unit: S (sound) / I (intermediate) / R (rotten)
    - Field and materials_ressources: .
  - Density
    - Information: Density values corresponding to wood category (S, I, R)
    - Variable Type: Numeric
    - Unit: Unitless
    - Field and materials_ressources: .
  - Diameter
    - Information: Diameter of the dead wood trunk in the transect crossing area
    - Variable Type: Numeric
    - Unit: Centimeter (cm)
    - Field and materials_ressources: forester compass
  - Volume
    - Information: Estimated volume of the lying dead wood (based on Winrock International 2005)
    - Variable Type: Numeric
    - Unit: cubic metres (m3)
    - Field and materials_ressources: meter
  - Biomass
    - Information: Biomass stock of lying dead wood
    - Variable Type: Numeric
    - Unit: milligrams per hectare (Mg.ha-1)
    - Field and materials_ressources: .
  - Stock_C
    - Information: Carbon stock of lying dead wood
    - Variable Type: Numeric
    - Unit: milligrams per hectare (Mg.ha-1)
    - Field and materials_ressources: .

- Data provenance and references
  - Data are linked to the Winrock International 2005 study: Impact of logging on carbon stocks of tropical forests: the Republic of Congo case study
  - Online reference: https://www.winrock.org/wp-content/uploads/2016/03/WI-USAID-Logging-Carbon-CongoField-Report-2005.pdf

- Data quality notes
  - Notes indicate “means no data” for missing values
  - Some fields have unclear or placeholder metadata (e.g., Site_ID Unit: .)
  - Data are part of a wider dataset suite and may rely on external methods (e.g., volume estimation method)

- Usage and stewardship implications for Data Leaders
  - Ensure clear metadata for discoverability (field definitions, units, and data types)
  - Verify data suitability and gaps before use, especially regarding missing values
  - Maintain proper attribution and acknowledgments per dataset requirements
  - Track provenance (source references, methods used for density, volume, and biomass calculations)
  - Align with data standards to facilitate integration with broader data systems and cross-network collaboration

- Access points
  - DOI and project links provided (see above)
  - Reference material: Winrock 2005 Congo field report (PDF)