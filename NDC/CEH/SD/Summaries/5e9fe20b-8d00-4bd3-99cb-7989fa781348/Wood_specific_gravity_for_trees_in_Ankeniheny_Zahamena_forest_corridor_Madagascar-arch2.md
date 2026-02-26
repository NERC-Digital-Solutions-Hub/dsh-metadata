# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Presents characteristics of sampled trees and measurements of Wood Specific Gravity (WSG) and density at 12% moisture content (D12) from wood cores.
- Analyses conducted by laboratories at UFR Sciences du bois de l'ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo.
- Associated with ESPA Programme and P4GES project.
- DOI provided for dataset access; acknowledgment of UFR Sciences du bois de l’ESSA-forêts and Laboratoire des Radio Isotopes is required for derived products.

## Data Scope and Structure
- Location: Ankeniheny Zahamena forest corridor, Madagascar.
- Project and portals: ESPA (http://www.espa.ac.uk/); P4GES (https://www.p4ges.org).
- Data format: Dataset header information describing variables and measurement context.
- Data availability and attribution: DOI link; dataset usage requires acknowledgment.

## Variables and Measurements
- Day_of_collection: Day wood cores were collected (text string).
- Zone: P4GES Zone code (text string).
- Identification: P4GES wood cores identification (text string).
- Trees_Local_name: Vernacular/local tree name (text string).
- Trees_scientific_name: Scientific name of sampled trees (text string).
- Trees_total_height: Total tree height in meters (numeric); unmeasurable heights may be visually estimated.
- trees_DBH: Diameter at breast height (1.3 m) in centimeters (numeric).
- Trees_PHF_index: Quality indicator of tree form (numeric) covering crown position, crown form, and stem form.
- Remarks: Additional notes (text string).
- Vsat: Saturated volume of the wood core in cubic centimeters (numeric).
- M12: Weight of the wood core at 12% moisture content in grams (numeric).
- V12: Volume of the wood core at 12% moisture content in cubic centimeters (numeric).
- D12: Density at 12% moisture content (calculated as D12 = M12 / V12) (numeric).
- WSG: Wood Specific Gravity, computed as the ratio of anhydrous weight to saturated volume (WSG = M_anhydrous / Vsat) (numeric).

Notes:
- x indicates missing data for any field.

## Methods and Computation
- WSG and D12 derived from core measurements:
  - D12 calculated from M12 and V12 (D12 = M12 / V12).
  - WSG derived from anhydrous weight and saturated volume (WSG = anhydrous weight / Vsat).
- Measurements include both physical dimensions (height, DBH) and quality indicators (PHF index) to support robust tree characterization.

## Data Quality, Provenance, and Compliance
- Data verified, quality assured, cleaned, and transformed using standardized procedures.
- Outputs generated in clear formats (e.g., reports, maps, charts) and stored/uploaded to appropriate data portals.
- Acknowledgement required for products derived from these data (institutional credits specified).
- Clear documentation of field materials/resources and measurement methods to support reproducibility.

## Access, Use, and Linkages
- DOI provided for dataset access; linked to ESPA and P4GES project frameworks.
- Data may be integrated with other environmental monitoring datasets to enhance utility beyond single-use analyses.
- Emphasis on enabling access to underlying data to support broader scrutiny and policy evaluation.

## Considerations for Analysts Monitoring the Environment
- Provides standardized, time-compatible metrics (WSG, D12, DBH, height) for forest health and wood density monitoring.
- Facilitates cross-site and temporal comparisons essential for evaluating environmental health and policy performance.
- Supports data integration with other environmental indicators to improve monitoring value and decision-making.

## Practical Metadata Notes
- Day_of_collection and Zone fields are text-based entries, reflecting field recording practices.
- Missing data indicator: x.