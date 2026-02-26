# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Dataset presents Wood Specific Gravity (WSG) and density at 12% moisture content (D12) for wood cores sampled from trees in the Ankeniheny-Zahamena forest corridor, Madagascar.
- Analyses were conducted by laboratories at UFR Sciences du bois de l'ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo.
- DOI: https://doi.org/10.5285/5e9fe20b-8d00-4bd3-99cb-7989fa781348
- Programs and projects: ESPA and P4GES.
- Acknowledgement of the UFR Sciences du bois de l'ESSA-forêts, Université d'Antananarivo and the Laboratoire des Radio Isotopes is required for products derived from these data.

## Data content and variables
- The dataset covers measurements of:
  - Day_of_collection: Day of collection of wood cores (Text String).
  - Zone: P4GES Zone code (Text String).
  - Identification: P4GES wood cores identification (Text String).
  - Trees_Local_name: Vernacular/local name of sampled trees (Text String).
  - Trees_scientific_name: Scientific name of sampled trees (Text String).
  - Trees_total_height: Total tree height (Numeric, meters); some heights are estimated when not measured.
  - trees_DBH: Diameter at breast height (1.3 m) (Numeric, centimeters).
  - Trees_PHF_index: Quality of trees form (Numeric; P: crown position, H: crown form, F: stem form).
  - Remarks: Additional remarks (Text String).
  - Vsat: Saturated volume of the wood core (Numeric, cubic centimeters).
  - M12: Weight at 12% moisture content of the sample (Numeric, grams).
  - V12: Volume at 12% moisture content of the sample (Numeric, cubic centimeters).
  - D12: Density at 12% moisture content (Numeric; computed as D12 = M12 / V12).
  - WSG: Wood Specific Gravity (Numeric; defined as the wood’s anhydrous weight divided by the saturated volume; WSG is unitless).
- Note: “Notes: x = missing data” indicates missing values in the dataset.

## Standards, provenance, and documentation
- Reference to Manual 4_Wood_Specific_Gravity for methodology and definitions.
- Data use requires proper acknowledgment to the contributing institutions.
- DOI and programmatic context (ESPA, P4GES) support traceability and attribution.
- Metadata fields include units and field_materials/resources where applicable.

## Quality, limitations, and data handling
- Height data include visual estimates when precise measurements are unavailable.
- Presence of missing data is indicated by the convention “x = missing data,” which data stewards should handle in quality checks and documentation.
- The dataset employs standard measurement approaches (e.g., balance for masses, Archimedean principle for volumes) and clearly defined variable types and units to facilitate interoperability.

## Data access, usage, and governance
- DOI provided for citation and access fidelity.
- Data use requires acknowledgement of the contributing labs and institutions.
- Data should be uploaded to appropriate portals and catalogued within data holdings; updates should be managed to maintain currency and discoverability.
- Acknowledge any products derived from the data to the UFR Sciences du bois de l'ESSA-forêts, Université d'Antananarivo, and the Laboratoire des Radio Isotopes.

## Stewardship considerations for Data Stewards
- Ensure metadata completeness and consistency with Manual 4_Wood_Specific_Gravity and the dataset’s variable definitions.
- Verify units, data types, and computed fields (e.g., D12, WSG) align with documentation and standard practices.
- Enforce proper acknowledgment language and track citations to the DOI and program references.
- Maintain provenance by linking field collection details (Day_of_collection, Zone, Identification) with laboratory analyses (Vsat, M12, V12, D12, WSG).
- Manage data quality issues, including handling of missing values and clearly documenting any estimations or proxies used for height measurements.
- Support interoperability across systems and formats, and provide guidance to data creators on metadata requirements and data sharing constraints.