# Otter Body Found - Liver Tissue Contaminant Data

- Overview
  - Data integrate identifiers from Predatory Bird Monitoring Scheme (CEH Ref) and Cardiff University Otter Project (UWC Ref).
  - Records the month and year an otter body was found, the county (England or Wales), and the animal’s sex and age class.
  - Spatial data captured via X and Y coordinates; supports environmental health monitoring over time.
  - Includes a body condition metric (Condition coefficient K) linked to established ecological methodology.

- Data structure and key fields
  - Identifiers
    - CEH Ref: Unique numeric identifier (Predatory Bird Monitoring Scheme)
    - UWC Ref: Unique numeric identifier (Cardiff University Otter Project)
  - Temporal and location data
    - Month Found: Month otter body was found
    - Year Found: Year otter body was found
    - County: County in England or Wales where found
    - X-coordinate / Y-coordinate: Spatial coordinates
  - Demographics
    - Sex: Female or Male
    - AgeClass: Juvenile, Sub-adult, or Adult
  - Condition
    - Condition coefficient (K): Body condition metric derived from Kruuk & Conroy (1991)
  - Biological/chemical measurements
    - % Dry matter: Percentage of dry mass, determined by drying a 0.5 g liver subsample at 70°C for 48 hours
    - Al, Mn, Fe, Co, Ni, Cu, Zn, Se, Sr, Mo, Cd, Sb, Pb, Hg, Cr, As, V, Ag: Dry weight concentrations in liver tissue (mg/kg)
    - Data status indicators for elements: ND = Non detected; NA = Not analysed
  - Data types and units
    - All element concentrations use mg/kg (dry weight)
    - Some fields have predefined categories (e.g., Sex, AgeClass)

- Data quality, provenance, and outputs
  - Data are sourced from established monitoring schemes; fields are defined to enable verification, quality assurance, cleaning, and standardised transformation.
  - Outputs are designed for clear presentation in reports, maps, and charts.
  - Datasets are stored and uploaded to appropriate data portals to support accessibility and reuse.

- Practical and methodological notes
  - The % Dry matter measurement method is explicitly defined (0.5 g liver subsample dried at 70°C for 48 hours).
  - The Condition coefficient (K) follows Kruuk & Conroy (1991) methodology for otter mortality context.

- Particular challenges and opportunities for analysts
  - Increasing the value of datasets by integrating liver contaminant data with other environmental data sources (avoiding single-use datasets).
  - Facilitating access to underlying data used to create final outputs to enhance transparency and reuse.