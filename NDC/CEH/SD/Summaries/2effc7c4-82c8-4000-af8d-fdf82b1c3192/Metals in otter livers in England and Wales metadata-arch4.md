# Liver tissue chemical concentrations in otter samples

- Overview
  - The dataset captures otter liver tissue analyses with identifiers from two projects:
    - CEH Ref: Unique numeric identifier from the Predatory Bird Monitoring Scheme
    - UWC Ref: Unique numeric identifier from the Cardiff University Otter Project
  - Key sample metadata includes when and where the otter body was found, demographic details, body condition, location coordinates, and detailed chemical analyses of liver tissue.

- Dataset schema (primary fields and definitions)
  - Month Found: Month in which the otter body was found
  - Year Found: Year in which the otter body was found
  - County: County in England or Wales where the otter was found
  - Sex: Female or Male
  - AgeClass: Juvenile, Sub-adult, or Adult
  - Condition coefficient (K): Body condition coefficient calculated per Kruuk & Conroy (1991)
  - X-coordinate: Spatial X coordinate
  - Y-coordinate: Spatial Y coordinate
  - % Dry matter: Percentage of mass that is dry matter, determined by drying a 0.5 gram subsample of the liver at 70 degrees Celsius for 48 hours
  - Element concentrations (dry weight, mg/kg) and related details:
    - Al, Mn, Fe, Co, Ni, Cu, Zn, Se, Sr, Mo, Cd, Sb, Pb, Hg, Cr, As, V, Ag
    - For each element: definition as dry weight concentration in liver tissue; units = mg/kg
    - Classes for elements: ND - Non detected; NA - Not analysed

- Data quality and metadata notes
  - Each field includes a explicit definition, units, and potential value classes (e.g., ND/NA for chemical measurements)
  - Spatial coordinates and location data support mapping and regional analyses
  - The dataset documents the method for % Dry matter measurement, ensuring reproducibility
  - There may be missing or non-detected data (ND) across several element measurements

- How this data supports data leadership goals
  - End-to-end data view: captures identifiers, temporal, spatial, demographic, and analytical data in a single schema
  - Alignment with user needs: enables researchers and policy colleagues to assess environmental exposure and liver chemistry across otter populations
  - Data discoverability and governance: clearly defined fields and units improve data discoverability, reuse, and integration with other datasets (e.g., broader ecological or contaminant data)
  - Data quality and iteration: explicit definitions and measurement methods facilitate validation, updates, and methodological transparency

- Practical considerations for data leaders
  - Data integration: potential to link CEH Ref and UWC Ref with additional datasets (e.g., population data, habitat data, other tissue analyses)
  - Gaps and limitations: presence of ND/NA values indicates incomplete data for some elements; plan for imputation or targeted data collection if needed
  - Standardization: ensure consistent units and metadata across related datasets to support cross-study comparisons
  - Access and collaboration: coordinate between Predatory Bird Monitoring Scheme and Cardiff University Otter Project to maintain data currency and enable broader community use

- End notes
  - The collection is focused on liver tissue chemistry with a comprehensive set of elemental concentrations, enabling environmental exposure assessment in otters and informing related ecological or conservation analyses.