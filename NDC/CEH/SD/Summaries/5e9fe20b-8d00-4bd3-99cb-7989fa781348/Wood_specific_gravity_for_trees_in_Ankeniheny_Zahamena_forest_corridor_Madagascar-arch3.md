# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Records wood core measurements to derive Wood Specific Gravity (WSG) and density at 12% moisture content (D12) for trees sampled in the Ankeniheny-Zahamena forest corridor, Madagascar.
- Analyses conducted by laboratories at UFR Sciences du bois de l'ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo.
- Associated program/project: ESPA and P4GES (DOI provided).
- Acknowledgement of the UFR Sciences du bois de l'ESSA-forêts and related laboratory is required for products derived from these data.

## Data fields and measurements included
- Day_of_collection: Day of collection of wood cores (text string).
- Zone: P4GES Zone code (text string).
- Identification: P4GES wood cores identification (text string).
- Trees_Local_name: Vernacular/local name of the sampled trees (text string).
- Trees_scientific_name: Scientific name of the sampled trees (text string).
- Trees_total_height: Measured total tree height (meters); if not measured, height recorded as a visual estimate.
- trees_DBH: Diameter at breast height (cm) (numeric).
- Trees_PHF_index: Quality of tree form (P: crown position, H: crown form, F: stem form) (numeric).
- Remarks: Free-text remarks (text string).
- Vsat: Saturated volume of the sample (wood core) in cubic centimeters (numeric).
- M12: Weight at 12% moisture content of the sample (wood core) in grams (numeric).
- V12: Volume at 12% moisture content of the sample (wood core) in cubic centimeters (numeric).
- D12: Density at 12% moisture content (D12 = M12 / V12) (numeric; unitless).
- WSG: Wood Specific Gravity of the species (WSG = M_anhydrous / Vsat) (numeric; unitless).
- Notes: x = missing data (indication of missing entries).

## Data provenance and methods
- Source and location details linked to the Ankeniheny-Zahamena forest corridor study area.
- Analytical methods:
  - Vsat measured using balance with Archimede principle.
  - M12 and V12 determined via balance measurements.
  - D12 calculated as M12 divided by V12.
  - WSG calculated as the anhydrous mass divided by the saturated volume (WSG = M_anhydrous / Vsat).
- Dataset supported by ESPA and Project P4GES with explicit data provision from the University of Antananarivo.

## Data governance, usage, and acknowledgements
- Derived products must acknowledge the UFR Sciences du bois de l'ESSA-forêts, Université d'Antananarivo, and related laboratories.
- Data sharing and use should credit the DOI and project context (ESPA/P4GES).
- Metadata completeness and clarity are emphasized; note there may be missing values (as indicated by “x = missing data”).

## Relevance for monitoring and policy
- Provides species- and sample-level wood density and volume metrics critical for forest carbon stock estimation and timber quality assessments.
- Enables monitoring of forest health and wood properties across species within the corridor, informing policy decisions and conservation planning.