# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagasca r.csv

## Overview
- This dataset records characteristics of sampled trees and measurements of Wood Specific Gravity (WSG) and density at 12% moisture content (D12) for wood cores.
- Analyses were performed by laboratories at UFR Sciences du bois, Forestry and Environment Department, ESSA-forêts, Université d’Antananarivo.
- Associated with ESPA Programme and the P4GES project. DOI provided for data traceability.
- Acknowledgement of the UFR Sciences du bois and related labs is required for products derived from these data.

## Data content and key variables
- Day_of_collection: Day when wood cores were collected (text).
- Zone: P4GES Zone code (text).
- Identification: P4GES wood cores identification (text).
- Trees_Local_name: Vernacular/local name of sampled trees (text).
- Trees_scientific_name: Scientific name of sampled trees (text).
- Trees_total_height: Estimated total tree height from ground (meters; numeric).
- Ttrees_DBH: Diameter at breast height (1.3 m) (centimeters; numeric).
- Trees_PHF_index: Quality of tree form (numeric; relates to P: crown position, H: crown form, F: stem form).
- Remarks: Additional remarks (text).

- Vsat: Saturated volume of the wood core (cubic centimeters; numeric). Measured by Archimedes principle using water displacement.
- M12: Weight at 12% moisture content of the wood core (grams; numeric).
- V12: Volume at 12% moisture content (cubic centimeters; numeric). Measured by water displacement method.
- Manhy: Anhydrous weight of the wood core (grams; numeric).
- D12: Density at 12% moisture content (grams per cubic centimeter; numeric). D12 = M12 / V12.
- WSG: Wood Specific Gravity of the species (grams per cubic centimeter; numeric). WSG = Manhy / Vsat.

Notes:
- x indicates missing data.

## Data provenance and usage constraints
- Source institutions and laboratories: UFR Sciences du bois, ESSA-forêts, Université d’Antananarivo.
- DOI and project references (ESPA, P4GES) enable data traceability and reuse.
- Data products derived from these data require formal acknowledgement of the contributing Malagasy institutions.
- Data management practices emphasize storing and uploading datasets to appropriate portals for broader access.

## Methods and measurement notes
- Core sampling context: wood cores from sampled trees within the Ankeniheny-Zahamena forest corridor (Madagascar).
- Measurement methods:
  - Vsat: Saturated volume via water displacement (Archimedes principle).
  - M12: Mass at 12% moisture content (balanced measurement).
  - V12: Volume at 12% moisture content (water displacement).
- Derived metrics:
  - D12 = M12 / V12 (density at 12% moisture).
  - WSG = Manhy / Vsat (wood specific gravity).
- Units are specified for each variable to support standardized comparisons across datasets and time.

## Practical considerations for analysts
- Use standardized variables and units to enable time-series comparisons of WSG and D12 across species and zones.
- Leverage the provenance information (DOI, ESPA/P4GES) to cite data properly and to access metadata.
- Account for missing data denoted by x when performing analyses or aggregations.
- Consider linking these core measurements with auxiliary environmental or ecological datasets to increase the value of the monitoring dataset.