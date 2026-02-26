# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Dataset provides wood-specific gravity (WSG) and density at 12% moisture content (D12) for wood cores sampled in the Ankeniheny-Zahamena forest corridor, Madagascar.
- Analyses conducted by laboratories at UFR Sciences du bois, ESSA-forêts, University of Antananarivo.
- Includes key tree measurements and core-by-core properties to support forestry and environmental monitoring.

## Source, provenance, and access
- DOI: https://doi.org/10.5285/efa10c00-d43a-4c94-b2f9-0708755e7d80
- Programme: ESPA; Project: P4GES
- Acknowledgement required for products derived from these data (UFR Sciences du bois de l'ESSA-forêts, Université d’Antananarivo, and related laboratories).
- Data sharing and openness are emphasized, though some barriers may exist around metadata completeness and dataset sharing.

## Data content and variables
- Day_of_collection: Day of collection of wood cores (text string).
- Zone: P4GES Zone code (text string).
- Identification: Wood cores identification (text string).
- Trees_Local_name: Vernacular/local tree name (text string).
- Trees_scientific_name: Scientific name (text string).
- Trees_total_height: Estimated total tree height (meters).
- Ttrees_DBH: Diameter at breast height (cm).
- Trees_PHF_index: Quality index for tree form (P/H/F components; numeric).
- Remarks: Additional remarks (text string).
- Vsat: Saturated volume of the sample (cm3).
- M12: Weight at 12% moisture content (g).
- V12: Volume at 12% moisture content (cm3).
- Manhy: Anhydrous weight of the sample (g).
- D12: Density at 12% moisture content (g/cm3).
- WSG: Wood Specific Gravity (WSG = Manhy/Vsat) (numeric; typical units g/cm3 or dimensionless per method).

- Notes:
  - Data values use balance and water displacement (Archimedes principle) for volume/weight measurements.
  - D12 is derived as M12/V12; WSG is derived as Manhy/Vsat.
  - “x = missing data” indicates gaps in the dataset.

## Measurement methods and data lineage
- Vsat: Saturated volume measured by balance (water displacement method) for wood cores.
- M12: Mass at 12% moisture (grams) measured by balance.
- V12: Volume at 12% moisture (cm3) measured by water displacement.
- Manhy: Od hydrous (dry) mass (grams).
- D12: Calculated density at 12% moisture (g/cm3) from M12/V12.
- WSG: Calculated wood specific gravity from Manhy/Vsat.
- Total_height and DBH are field estimations (height visually estimated; DBH measured at 1.30 m).

## Metadata quality, governance, and accessibility considerations
- Metadata completeness varies; some fields indicate text or unstandardized entries (e.g., Day_of_collection as text, zone codes as strings).
- Metadata gaps can impede rapid verification of data suitability for policy monitoring.
- Data governance practices should ensure clear provenance, transformation steps, and consistent units.
- Public sharing of underlying data is encouraged but may require adherence to attribution and data-use standards.
- The dataset is associated with a recognized project and has a DOI to support traceability.

## Relevance for monitoring frameworks and policy evaluation
- Provides species- and site-specific wood density information critical for forest carbon stock assessments and timber property evaluations.
- Enables comparisons of wood quality across zones and species, supporting policy decisions on management strategies and resource allocation.
- The dataset’s structure—variables for localization, tree metrics, and core-based wood properties—facilitates integration into dashboards and reports assessing forest health, carbon, and biomass dynamics.
- Highlights governance needs for data timeliness, interoperability, and transparent data sharing to improve evidence-informed decision-making.

## Practical considerations for use
- Assess metadata adequacy before integration; standardize field names and units where possible.
- Confirm data provenance and attribution requirements (acknowledgement to data providers).
- Anticipate data transformation needs (e.g., parsing text fields, converting height estimates to standardized units).
- Monitor for missing data and document any imputation or exclusion in monitoring outputs.