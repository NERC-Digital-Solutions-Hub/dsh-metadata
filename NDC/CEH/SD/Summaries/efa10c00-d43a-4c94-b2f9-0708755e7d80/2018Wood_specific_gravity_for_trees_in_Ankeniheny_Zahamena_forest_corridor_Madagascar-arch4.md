# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

- Purpose: This dataset records characteristics of sampled trees and measures Wood Specific Gravity (WSG) and density at 12% moisture content (D12) of wood cores.
- Responsible teams: Analyses conducted by laboratories at UFR Sciences du bois, Forestry and Environment Department, ESSA-forêts, Université d’Antananarivo.
- Reference and access: DOI https://doi.org/10.5285/efa10c00-d43a-4c94-b2f9-0708755e7d80; ESPA Programme and Project P4GES.

## Data scope and metadata

- Dataset focus: Wood core measurements including WSG and D12 for species sampled in the Ankeniheny-Zahamena forest corridor, Madagascar.
- Acknowledgements: Required attribution to UFR Sciences du bois de l’ESSA-forêts, Université d’Antananarivo, and Laboratoire des Radio Isotopes, Université d’Antananarivo for products derived from these data.
- Data access and reuse: Project context provided (ESPA, P4GES); dataset header includes methodological and variable definitions to support data reuse.

## Key variables and measurement details

- Collection metadata
  - Day_of_collection: Text string indicating the day of wood core collection.
  - Zone: Text string (P4GES Zone code).
  - Identification: Text string for wood cores identification.
- Biological identifiers
  - Trees_Local_name: Vernacular/local tree name.
  - Trees_scientific_name: Scientific name.
- Morphometrics
  - Trees_total_height: Numeric, meters; visually estimated total tree height.
  - Ttrees_DBH: Numeric, centimeters; diameter at breast height (1.30 m) from ground.
  - Trees_PHF_index: Numeric; quality of tree form (P: crown position, H: crown form, F: stem form).
- Measured and derived metrics
  - Vsat: Numeric; saturated volume of the wood core (cubic centimeters); measured by balance (Archimedean water displacement).
  - M12: Numeric; weight at 12% moisture content (grams); balance measurements.
  - V12: Numeric; volume at 12% moisture content (cubic centimeters); balance with water displacement.
  - Manhy: Numeric; anhydrous weight of the wood core (grams); balance.
  - D12: Numeric; density at 12% moisture content (g/cm^3); calculated as M12/V12.
  - WSG: Numeric; Wood Specific Gravity (g/cm^3); calculated as Manhy/Vsat.
- Data quality and notes
  - Remarks: Text field for additional notes.
  - Notes: x denotes missing data.
  - Field_materials/resources: Various fields indicate data collection and measurement methods (e.g., balance, Archimedes principle).

## Data governance and quality considerations

- Data types and units are specified for each variable (e.g., height in meters, DBH in cm, volumes in cubic centimeters, weights in grams).
- Some field names show minor inconsistencies (e.g., Ttrees_DBH vs Trees_DBH) which may require harmonization during data integration.
- Missing data is explicitly indicated (x = missing data).
- Metadata provides explicit calculation methods for derived metrics (D12 and WSG).

## Usage considerations for data leaders

- Data stewardship: Clear provenance, measurement methods, and calculation rules support reproducibility and auditability.
- Discoverability and interoperability: Metadata includes variable names, types, units, and data collection context to aid discovery and integration with other data systems.
- Collaboration and standards: While not requiring, awareness of potential sector coordination needs is relevant for broader data ecosystem strengthening and avoiding duplicated effort.  
- Compliance and attribution: Proper acknowledgment of data providers is required for derivative works.