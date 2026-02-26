# DATA HEADER INFORMATION for Wood_specific_gravity_for_trees_in_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

- Overview
  - Dataset provides characteristics of sampled trees and measurements of Wood Specific Gravity (WSG) and density at 12% moisture content (D12) from wood cores.
  - Analyses conducted by laboratories at UFR Sciences du bois, ESSA-forêts, Université d’Antananarivo.
  - Associated with ESPA programme and the P4GES project; DOI and acknowledgements included.

- Provenance and context
  - Location: Ankeniheny-Zahamena forest corridor, Madagascar.
  - Programme: ESPA (P4GES project).
  - Access and acknowledgement: Acknowledgement of the contributing laboratories required for derived products.

- Data content and structure
  - Variables included (with purpose, type, and units):
    - Day_of_collection: day of collection; text string.
    - Zone: P4GES Zone code; text string.
    - Identification: wood cores identification; text string.
    - Trees_Local_name: vernacular/local tree name; text string.
    - Trees_scientific_name: scientific name; text string.
    - Trees_total_height: total tree height (ground to top); numeric; meters.
    - Ttrees_DBH: diameter at breast height (1.30 m); numeric; centimeters.
    - Trees_PHF_index: quality of tree form (P/H/F components); numeric.
    - Remarks: additional notes; text string.
    - Vsat: saturated volume of the wood core; numeric; cubic centimeters.
    - M12: weight at 12% moisture content; numeric; grams.
    - V12: volume at 12% moisture content; numeric; cubic centimeters.
    - Manhy: anhydrous weight of the wood core; numeric; grams.
    - D12: density at 12% moisture content; numeric; g/cm3.
    - WSG: Wood Specific Gravity (WSG = Manhy/Vsat); numeric; g/cm3.
  - Notes on measurements:
    - WSG is derived as Manhy divided by Vsat.
    - Vsat and other measurements obtained via balance and Archimedes’ principle (water displacement).

- Measurement details and units
  - Height: meters.
  - DBH: centimeters.
  - Volumes: cubic centimeters.
  - Weights: grams.
  - D12 and WSG: g/cm3.
  - Data collection and processing notes are described in accompanying Notes and Manuals (e.g., Day_of_collection as text, x = missing data).

- Data collection and processing notes
  - Analyses performed in specified laboratories; methods referenced in related manuals (e.g., Manual 4_Wood_Specific_Gravity).
  - Data may require cleaning and standardization when integrating with other datasets (scale and format variations possible).

- Data quality, gaps, and caveats
  - x indicates missing data for certain fields.
  - Potential challenges include local-scale data availability, access to datasets across platforms, and consistency across species and sites.
  - Data may require careful handling of units and scale when conducting cross-dataset analyses.

- Usage, access, and provenance references
  - DOI: https://doi.org/10.5285/efa10c00-d43a-4c94-b2f9-0708755e7d80
  - Programme: ESPA; Project: P4GES
  - Data and metadata intended to be discoverable via appropriate data portals; users should acknowledge ESSA-forêts and University of Antananarivo as per data usage notes.