# DATA STRUCTURE

- Dataset and format
  - Manure volumes by livestock type and land use for England and Wales
  - Stored as a shapefile: MANURE-GIS_ManureVolumes_EnW.shp

- Data model and schema
  - Each column code encodes three elements:
    - SOURCE.Livestock Sectors (e.g., Beef, Dairy, Pigs, Layers, Sheep, Broilers)
    - SOURCE.Manure/housing (Farmyard manure, Slurry, Direct excreta)
    - DESTINATION.Land Use Type (Grass, Arable Winter, Arable Spring, Arable Summer, etc.; some entries use "-" for unspecified)
  - Units are either kilograms or litres, depending on the manure type
  - Examples by category:
    - Beef
      - B_FYM_Gras: Beef, Farmyard manure, Grass; kilograms
      - B_FYM_AraW: Beef, Farmyard manure, Arable Winter; kilograms
      - B_FYM_AraS: Beef, Farmyard manure, Arable Spring; kilograms
      - B_Slu_Gras: Beef, Slurry, Grass; litres
      - B_Slu_AraS: Beef, Slurry, Arable Spring; litres
      - B_Slu_AraW: Beef, Slurry, Arable Winter; litres
      - B_Grazing: Beef, Direct excreta, destination unspecified; kilograms
    - Dairy
      - D_FYM_Gras, D_FYM_AraW, D_FYM_AraS, D_Slu_Gras, D_Slu_AraS, D_Slu_AraW, D_Grazing
    - Pigs
      - P_FYM_Gras, P_FYM_AraW, P_FYM_AraS, P_Slu_Gras, P_Slu_AraS, P_Slu_AraW
    - Sheep
      - S_FYM_Gras, S_FYM_AraW, S_FYM_AraS, S_Grazing
      - Note: S_Grazing entry includes only the proportion of sheep excreta deposited at grazing on managed grass (excludes rough grazing)
    - Layers (L_)
      - L_FYM_Gras, L_FYM_AraW, L_FYM_AraS, L_FrRngGra (Free Range, destination unspecified)
    - Broilers
      - Bro_FYM_Gras, Bro_FYM_Ar, Bro_FYM__1 (Arable Spring), etc.
    - Other groupings
      - D_S or S_ prefixes indicate dairy or sheep-related entries; various combinations of land-use types and manure/housing

- Purpose and use for environmental monitoring
  - Enables standardized, comparable quantification of manure volumes by livestock type and land-use destination
  - Supports analysis of nutrient flows and potential environmental impacts related to manure application
  - Facilitates generation of outputs such as environmental health indicators, mapped visuals, and policy performance assessments

- Data management and accessibility (how this aligns with the archetype)
  - Data quality processes implied: verify data sources, quality assurance, cleaning, and transformation prior to analysis
  - Outputs are presented in clear formats (reports, maps, charts) and datasets are stored/uploaded to appropriate portals
  - Aims to increase dataset value through integration with additional data and to improve access to underlying data used for outputs

- Notes and caveats
  - The dataset uses discrete land-use categories; some records have destination land-use as "-"
  - The S_Grazing entry explicitly notes scope limitations (only grazing on managed grassland is included; rough grazing excluded)

- Relevance to environmental monitoring challenges
  - Provides a structured basis for combining manure data with other environmental datasets to enhance monitoring value
  - Supports transparent access to the underlying data that underpins final monitoring outputs