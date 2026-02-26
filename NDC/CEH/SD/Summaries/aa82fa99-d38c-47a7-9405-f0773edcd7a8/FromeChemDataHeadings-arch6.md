# Column header/Determinand

- Overview
  - Defines a data schema for river/water quality measurements, aligning each column with a determinand (determinant) that has a standardized preferred label and ontology URI, plus a corresponding units label and units URI.
  - Intended to support consistent data interpretation, interoperability, and the ability to build self-serve data products.

- Data schema highlights
  - Core columns include:
    - Sampling Date and Sampling Time
    - Physical and chemical determinations such as: Average daily river flow, Temperature, pH, Electrical conductivity, Gran alkalinity, Dissolved nitrate, Dissolved reactive silicon, Total Phosphorus, Total dissolved phosphorus, Soluble reactive phosphorus, Dissolved chloride, Dissolved sulfate, Dissolved sodium, Dissolved potassium, Dissolved magnesium, Dissolved calcium, Suspended solids, Dissolved ammonium.
  - For each determinand there are:
    - Determinand preferred label
    - Determinand URI
    - Units preferred label
    - Units URI
  - Some entries indicate "No units" where appropriate; others specify units such as:
    - Flow: m3/s (and formatting hints like hh:mm)
    - Temperature: deg C (degrees Celsius)
    - pH: no units
    - Electrical conductivity: µS cm-1 (units at 25°C)
    - Gran alkalinity: mEq L-1
    - Nutrients and inorg. species: mg L-1 or µg L-1 (e.g., mg NO3-N, mg Si L-1, Total dissolved P, Dissolved Cl, Dissolved SO4, Dissolved Na, Dissolved K, Dissolved Mg, Dissolved Ca, Dissolved NH4)
  - Ontology/standardization references:
    - Each determinand and its units include a preferred label and a URI from the Onto.nerc CAST vocabulary (e.g., Temperature, pH, Electrical conductivity, Gran alkalinity, Total dissolved phosphorus, Dissolved Cl, Dissolved Na, etc.).
    - Units also have labels and URIs (e.g., degrees Celsius, µS cm-1, micrograms per litre, milligrams per litre, etc.).

- Ontology and standardization benefits
  - Enables consistent interpretation across datasets and systems.
  - Facilitates data merging, cross-system querying, and the creation of reusable data products.
  - Supports clear provenance and makes outputs easier to summarize for diverse audiences.

- Data quality and preparation considerations
  - Some fields show no units or mixed formatting; standardization may be needed during cleaning.
  - Data may originate from multiple formats and systems; alignment to the ontology URIs will aid integration.
  - Time-related fields (Sampling Date/Time) may require careful handling for temporal analyses and self-serve dashboards.

- How this supports the Data Support archetype
  - Provides a ready-to-use, ontology-aligned schema to search, combine, and analyse a broad set of water-chemistry measurements.
  - Enables creation of dashboards, pivot tables, and reports that end users can self-serve from.
  - Supports sharing early prototypes and gathering feedback to refine data products.
  - Offers a foundation for advocating better, more consistent data creation and capture across systems.

- Practical next steps for use
  - Map existing datasets to the determinand labels and URIs, and standardize units where needed.
  - Build self-serve dashboards and reports using the standardized fields.
  - Validate data quality by checking for missing units, inconsistent formatting, and alignment with the CAST ontology.
  - Share first prototypes with stakeholders, collect feedback, and iterate on data products and documentation.