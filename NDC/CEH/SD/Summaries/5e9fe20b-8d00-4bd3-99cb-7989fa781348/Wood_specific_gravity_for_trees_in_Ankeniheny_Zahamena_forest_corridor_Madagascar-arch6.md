# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Dataset of wood specific gravity (WSG) and density at 12% moisture content (D12) from wood cores sampled in the Ankeniheny-Zahamena forest corridor, Madagascar.
- Analyses conducted by laboratories at UFR Sciences du bois de l'ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo.
- DOI provided for the dataset.
- Associated with ESPA (programme) and the P4GES project.
- Acknowledgement required for outputs derived from these data (UFR Sciences du bois de l’ESSA-forêts and Laboratoire des Radio Isotopes, Université d’Antananarivo).

## Key variables and fields
- Day_of_collection: Text string; day the wood cores were collected.
- Zone: Text string; P4GES zone code.
- Identification: Text string; P4GES wood cores identifier.
- Trees_Local_name: Text string; vernacular/local tree name.
- Trees_scientific_name: Text string; scientific name of the sampled tree.
- Trees_total_height: Numeric; total tree height in meters (some values are visually estimated when height could not be measured).
- trees_DBH: Numeric; diameter at breast height (1.3 m) in centimeters.
- Trees_PHF_index: Numeric; quality of tree form (P, H, F components).
- Remarks: Text string; any additional notes.
- Vsat: Numeric; saturated volume of the wood core in cubic centimeters (cm3) measured by balance using Archimède principle.
- M12: Numeric; weight of the wood core at 12% moisture content in grams.
- V12: Numeric; volume of the wood core at 12% moisture content in cm3.
- D12: Numeric; density at 12% moisture content (calculated as M12/V12).
- WSG: Numeric; wood specific gravity (calculated as anhydrous mass divided by Vsat; WSG = M_anhydrous / Vsat).
- Notes: Includes data quality cues (e.g., x = missing data).

## Measurements, calculations, and units
- Units:
  - Height: meters (Trees_total_height)
  - DBH: centimeters (trees_DBH)
  - Volumes: cubic centimeters (Vsat, V12)
  - Weights: grams (M12)
  - WSG and D12: dimensionless (calculated values)
- Calculations:
  - D12 = M12 / V12
  - WSG = M_anhydrous / Vsat
- Methods:
  - Vsat determined via balance using Archimède principle.
  - Height sometimes visually estimated when not measured.

## Data provenance and usage rights
- Source labs: UFR Sciences du bois de l’ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo.
- Project context: ESPA and P4GES program.
- DOI available for dataset; proper acknowledgement of UFR Sciences du bois de l’ESSA-forêts and the Laboratoire des Radio Isotopes (Université d’Antananarivo) is required for products derived from these data.

## Data quality, gaps, and notes
- x indicates missing data.
- Some fields (e.g., Day_of_collection) are text strings; others are numeric.
- Height data may be incomplete or visually estimated when exact measurement was not possible.
- Data may be in patchy formats or have variable completeness across records; users should verify field completeness before analysis.
- Cross-field consistency (e.g., D12 via M12/V12 and WSG via M_anhydrous/Vsat) should be checked during usage.

## How this supports data use (for data work and dashboards)
- Provides a structured metadata foundation to enable data discovery, cleaning, and integration with species information and forest inventory datasets.
- Supports building self-service analyses and dashboards to explore wood density and related metrics by species, zone, and tree size (height, DBH).
- Facilitates cross-referencing local and scientific names, along with collection metadata (zone, day, remarks) for richer context.
- Clear provenance and usage rights aid in proper data sharing and attribution, aligning with data governance and reproducibility goals.