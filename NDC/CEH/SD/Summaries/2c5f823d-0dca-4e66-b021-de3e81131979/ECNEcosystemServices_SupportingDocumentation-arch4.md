# Data availability and citation

- Overview
  - The Environmental Change Network (ECN) is the UK's long-term environmental monitoring and research programme, regularly measuring air, soil, water, and various biota to track environmental change.
  - The dataset "Ecosystem services variables from the UK Environmental Change Network (ECN)" uses the Millennium Ecosystem Assessment (MA) framework to define ecosystem services and create variables for cross-site comparison.
  - The dataset supports analysis and comparison of ecosystem services delivered by 11 ECN sites, and is linked to a publication in Environmetrics (2011) comparing services across sites.

- Data sources and boundary definitions
  - Data sources comprise three types: (i) standard ECN protocol data, (ii) site-manager data from other sources, and (iii) expert knowledge from site managers.
  - Site selection and boundaries are central: boundaries are defined primarily by land ownership/land management, aligned with decision-making units; some sites align with ECN site boundaries or whole basins. Boundary decisions affect which data are included for each site.
  - Eleven ECN sites (ALI, CAI, DRA, GLE, MOO, NOR, POR, ROT, SNO, SOU, WYT) with a combined total area of 11,262 ha; site boundary characteristics include features like land management, land ownership, water basins, and ECN site boundaries.

- Variables and selection process
  - A January 2010 workshop standardized the selection and definitions of variables to ensure consistent environmental and biodiversity measurements over time and space; single-year data (commonly 2009) or year-averages were used to minimize temporal variability; area-dependent variables were scaled by site area.
  - Variables span a comprehensive suite of ecosystem services, including categories such as:
    - Food (e.g., meat production, vegetables, fruits, eggs, cereals, provisioning categories)
    - Fibre and materials (e.g., wool, wood, hydropower)
    - Genetic resources and biochemicals
    - Ornamental, cultural, aesthetic, educational, and spiritual values
    - Regulatory services (air quality, climate, water regulation, erosion control, disease regulation, pest control, pollination)
    - Natural and other hazards, cultural diversity, ecotourism, and social relations
  - Variables include diverse units (tonnes per hectare, yes/no, counts, MWh, etc.) and are designed to be area-scaled. The dataset contains a large number of variables (as defined in the accompanying tables).

- Dataset format and structure
  - The dataset was originally created in Excel 2007 and has been converted to a CSV format for long-term storage.
  - Table 3 structure (conceptually) maps service types to variable definitions and site-specific data columns; each site code (ALI, CAI, DRA, etc.) holds the corresponding variable measurements.
  - Columns include Service type, Variable, Units, Variable_ID, Variable_Number, and site-specific data.

- References and usage
  - Foundational framework: Millennium Ecosystem Assessment (2005) Ecosystems and human well-being.
  - Analyses: The dataset underpins the paper “A comparison of ecosystem services delivered by 11 long-term monitoring sites in the UK Environmental Change Network” (Environmetrics, 2011).
  - Access and citation: The dataset is documented with a DOI link for data availability and citation (https://doi.org/10.5285/2c5f823d-0dca-4e66b021-de3e81131979).

- Implications for data leaders
  - Demonstrates the importance of standardized data protocols and cross-site comparability through MA-based variable definitions.
  - Highlights the need for clear boundary definitions to ensure consistent data inclusion and interpretation across sites.
  - Shows the value of combining protocol data, site-manager inputs, and expert knowledge to build rich, multi-faceted dataset products.
  - Emphasizes data discoverability and long-term storage by transitioning from Excel to CSV with explicit metadata (variable numbers, IDs, site codes) to facilitate reuse.
  - Illustrates how a well-structured, multi-source dataset can support strategic analyses and inform policy or management decisions across a network of partners.