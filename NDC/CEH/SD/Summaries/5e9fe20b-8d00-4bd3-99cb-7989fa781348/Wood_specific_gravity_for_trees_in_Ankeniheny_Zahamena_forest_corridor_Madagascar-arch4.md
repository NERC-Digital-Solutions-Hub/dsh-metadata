# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Describes measurements of Wood Specific Gravity (WSG) and density at 12% moisture content (D12) from wood cores of sampled trees.
- Analyses conducted by laboratories at UFR Sciences du bois de l'ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo.
- DOI provided: https://doi.org/10.5285/5e9fe20b-8d00-4bd3-99cb-7989fa781348
- Programme ESPA and Project P4GES associated with the work.
- Acknowledgement required for products derived from these data (UFR Sciences du bois de l'ESSA-forêts, Université d'Antananarivo; Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data content and key variables
- Data scope: tree measurements and wood core properties from Ankeniheny-Zahamena forest corridor, Madagascar.
- Key measurements:
  - WSG: Wood Specific Gravity (WSG = anhydrous weight / saturated volume; defined in the notes as WSG = Manhy/Vsat).
  - D12: Density at 12% moisture content (D12 = M12 / V12); where M12 is weight at 12% moisture and V12 is volume at 12% moisture.
- Data fields (with meanings and types):
  - Day_of_collection: Text string indicating day of wood core collection.
  - Zone: P4GES Zone code (text).
  - Identification: Wood cores identification (text).
  - Trees_Local_name: Vernacular/local tree name (text).
  - Trees_scientific_name: Scientific name of sampled trees (text).
  - Trees_total_height: Total tree height (numeric, meters); unmeasured heights may be visually estimated (e.g., ranges provided).
  - trees_DBH: Diameter at breast height (numeric, cm).
  - Trees_PHF_index: Quality of tree form (numeric; P/H/F components).
  - Remarks: Additional remarks (text).
  - Vsat: Saturated volume of the wood core (numeric, cubic centimeters).
  - M12: Weight at 12% moisture content (numeric, grams).
  - V12: Volume at 12% moisture content (numeric, cubic centimeters).
  - D12: Density at 12% moisture content (numeric).
  - WSG: Wood Specific Gravity (numeric).
- Notes on data derivation:
  - WSG is derived from anhydrous weight and saturated volume (WSG = Manhy/Vsat; exact variable name in notes uses Manhy).
  - D12 is derived from M12 and V12 (D12 = M12 / V12).
- Data quality cues:
  - “x” denotes missing data in the dataset.

## Provenance and access
- Collection and analysis location: Ankeniheny-Zahamena forest corridor, Madagascar.
- Analyzing laboratories: UFR Sciences du bois de l'ESSA-forêts, Foresterie et Environnement, Université d'Antananarivo; mention of Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Supporting programs: ESPA Programme; Project P4GES.
- Access and attribution: DOI provided; acknowledgement required for products derived from these data.

## Data quality, structure and constraints
- Data are described by a structured header with variable definitions, units, and data types.
- Some measurements may be estimated when direct measurements were not possible (e.g., tree height).
- Missing data are indicated by “x” in the dataset notes.
- Metadata includes units for numeric fields (e.g., height in meters, DBH in cm, volumes in cubic centimeters, weights in grams).

## Practical guidance for data leaders
- Use for modelling wood density (WSG) and moisture-related density (D12) across species within the forest corridor.
- Helpful for comparative analyses of local vs. scientific names, and for linking tree morphology (DBH, height) with wood properties.
- Ensure proper collaboration with the data producers for updated measurements and metadata, and give appropriate acknowledgment in outputs.
- Consider data gaps due to fragmentation or access limitations when planning broader analyses or integration with other data sources.