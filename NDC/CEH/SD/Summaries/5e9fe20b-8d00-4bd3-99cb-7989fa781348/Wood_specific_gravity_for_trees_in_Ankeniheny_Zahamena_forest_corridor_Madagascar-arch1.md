# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- This dataset contains characteristics of sampled trees and measurements of Wood Specific Gravity (WSG) and density at 12% moisture content (D12) from wood cores.
- Analyses were conducted by laboratories at UFR Sciences du bois de l'ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo.
- DOI and project context: DOI link provided; Programme ESPA; Project P4GES.
- Acknowledgement required for products derived from these data (UFR Sciences du bois de l'ESSA-forêts, Université d'Antananarivo and Laboratoire des Radio Isotopes).

## Data provenance and context
- Location: Ankeniheny-Zahamena forest corridor, Madagascar.
- Data produced under ESPA/P4GES framework; dataset and header specify zone codes and identifiers for traceability.
- Day_of_collection is recorded as a text string; other collection metadata accompany biological measurements.

## Variables and data types (high-level)
- Day_of_collection: Text string (date/period of wood core collection).
- Zone: Text string (P4GES zone code).
- Identification: Text string (P4GES wood cores identification).
- Trees_Local_name: Text string (vernacular/local tree name).
- Trees_scientific_name: Text string (scientific name of sampled trees).
- Trees_total_height: Numeric (meters; some values are visual estimates when precise height could not be measured).
- trees_DBH: Numeric (centimeters; diameter at breast height, 1.3 m from ground).
- Trees_PHF_index: Numeric (quality index for tree form: crown position, crown form, stem form).
- Remarks: Text string (additional notes).
- Vsat: Numeric (saturated volume of the wood core in cubic centimeters).
- M12: Numeric (weight of the wood core at 12% moisture content, in grams).
- V12: Numeric (volume of the wood core at 12% moisture content, in cubic centimeters).
- D12: Numeric (density at 12% moisture content; D12 = M12 / V12; units specified as gram/volume-like in metadata, but derived as density).
- WSG: Numeric (wood specific gravity; WSG = Mhy / Vsat; derived from anhydrous weight and saturated volume; exact formula given in metadata).

## Measurement methods
- Wood cores sampled and analyzed to derive:
  - Vsat (saturated volume) via balance (Archimedes principle) or related methods.
  - M12 (mass) at 12% moisture via balance.
  - V12 (volume) at 12% moisture via balance (Archimedes principle).
  - D12 computed as D12 = M12 / V12.
  - WSG computed as WSG = Mhy / Vsat (as specified in notes).
- Units are provided per variable (e.g., height in meters, DBH in cm, volumes in cm^3, masses in g).

## Data quality and notes
- Notes indicate x represents missing data.
- Some fields have ambiguous unit specifications in the header (e.g., D12 units listed as gram/unitless); the derived definitions indicate density/volume relationships.
- Data may require integration with other datasets due to local zone codes and identification fields.

## Practical considerations for analysis
- Ensure consistent handling of missing values (noted as x in the header).
- Cross-check that derived variables (D12, WSG) use the stated formulas when validating results.
- Be mindful of height measurements that are visual estimates rather than precise measurements.
- Consider provenance and acknowledgments requirements when using or publishing analyses based on these data.