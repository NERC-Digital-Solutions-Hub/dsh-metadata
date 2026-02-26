# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

- Overview
  - Describes characteristics of sampled trees and measurements of Wood Specific Gravity (WSG) and density at 12% moisture content (D12) from wood cores.
  - Analyses conducted by laboratories at UFR Sciences du bois de l'ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo.
  - DOI and project context: DOI link provided; ESPA Programme and P4GES project referenced.
  - Acknowledgement required for products derived from these data (UFR Université d’Antananarivo and Laboratoire des Radio Isotopes).

- Data provenance and collection context
  - Day_of_collection: day when wood cores were collected (text string).
  - Zone: P4GES Zone code (text string) used to geolocate or group samples spatially.
  - Identification: code/name identifying each wood core sample.
  - Trees_Local_name: vernacular/local name of sampled trees.
  - Trees_scientific_name: scientific name of sampled trees.
  - Trees_total_height: measured total tree height (meters); visual estimation noted when exact measurement unavailable.
  - trees_DBH: Diameter at breast height (cm).
  - Trees_PHF_index: quality assessment of tree form (P, H, F components) as a numeric index.
  - Remarks: any additional notes.

- Measured variables and formats (per sample)
  - Vsat: Saturated volume of the wood core (cubic centimeters); measured via balance (Archimedes principle).
  - M12: Weight of the sample at 12% moisture content (grams); balance measurement.
  - V12: Volume at 12% moisture content of the wood core (cubic centimeters); balance measurement.
  - D12: Density at 12% moisture content; calculated as D12 = M12 / V12 (unitless; derived from M12 and V12).
  - WSG: Wood Specific Gravity of the species; derived as WSG = Mhy / Vsat (dimensionless; derived from Mhy and Vsat).
  - Notes on data: a missing data placeholder used is "x" (data may be incomplete for some fields).

- Data structure and units
  - Day_of_collection, Zone, Identification, Trees_Local_name, Trees_scientific_name: text fields.
  - Trees_total_height: numeric (meters).
  - trees_DBH: numeric (centimeters).
  - Trees_PHF_index: numeric (no unit).
  - Vsat, M12, V12: numeric (cubic centimeters or grams as noted).
  - D12, WSG: numeric (unitless).

- Data use and GIS relevance
  - The dataset provides per-tree core measurements that can be linked to spatial features via Zone or Identification for map-based visualisations.
  - WSG and D12 allow modeling wood properties across species and locations.
  - Height, DBH, and PHF_index enable assessment of tree form and structure across the forest corridor.
  - Data quality notes (missing values) should be considered when aggregating or joining with spatial layers.

- Notes for data users
  - A related manual exists: Manual 4_Wood_Specific_Gravity.
  - Proper acknowledgment is required when using products derived from these data.
  - If data are incomplete (indicated by x), treat fields as missing during analysis and GIS joins.