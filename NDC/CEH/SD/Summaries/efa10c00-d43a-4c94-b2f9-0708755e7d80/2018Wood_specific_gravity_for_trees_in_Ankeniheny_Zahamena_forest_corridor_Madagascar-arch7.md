# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Presents characteristics of sampled trees and measurements of Wood Specific Gravity (WSG) and density at 12% moisture content (D12) from wood cores.
- Analyses conducted by laboratories at UFR Sciences du bois, Forestry and Environment Department, ESSA-forêts, University of Antananarivo.
- DOI provided; ESPA (P4GES) project referenced; data products require acknowledgment of the UFR Sciences du bois de l'ESSA-forêts and the Laboratoire des Radio Isotopes.
- This is a data header (data dictionary) for a CSV, outlining fields, types, units, and collection context.

## Data provenance and context
- Day_of_collection: Day when wood cores were collected (text).
- Zone: P4GES Zone code (text).
- Identification: P4GES wood core identification (text).
- Trees_Local_name: Vernacular/local name of sampled trees (text).
- Trees_scientific_name: Scientific name of sampled trees (text).
- Trees_total_height: Estimated total tree height (meters; numeric).
- Ttrees_DBH: Diameter at breast height (DBH, 1.30 m) in centimeters (numeric).
- Trees_PHF_index: Tree form quality (P = crown position, H = crown form, F = stem form) (numeric).
- Remarks: Additional notes (text).

## Measured variables and units
- Vsat: Saturated volume of the wood core (cubic centimeters) (numeric). Measured by balance using Archimède water displacement.
- M12: Weight at 12% moisture content (grams) (numeric). Measured by balance.
- V12: Volume at 12% moisture content (cubic centimeters) (numeric). Measured by balance using water displacement.
- Manhy: Anhydrous weight of the wood core (grams) (numeric).
- D12: Density at 12% moisture content (g/cm3) (numeric). D12 = M12 / V12.
- WSG: Wood Specific Gravity (WSG = Manhy / Vsat) (numeric; g/cm3).

## Data fields and metadata details
- Day_of_collection, Zone, Identification, Trees_Local_name, Trees_scientific_name, Trees_total_height, Ttrees_DBH, Trees_PHF_index, Remarks: data type and purpose as described above.
- Field_materials/resources (context): Indicates who collected data (e.g., botanist, forester), and generic laboratory/collection references.
- Notes: "x" denotes missing data.

## Data usage considerations for GIS
- Zone code enables spatial joins to existing GIS zone layers; local names and scientific names assist species-level mapping.
- All numeric measurements (DBH, height, Vsat, M12, V12, Manhy, D12, WSG) support thematic mapping by species, size class, density, or wood properties.
- Derived fields (e.g., D12, WSG) can be calculated if not already present; relationships like WSG = Manhy / Vsat and D12 = M12 / V12 are defined.
- Acknowledgments and provenance should be included in GIS data products and publications.