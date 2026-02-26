# UplandLowlandMetabolomics.csv

## Overview
- Project: Uplands-N2O
- Grant number: NE/M015351/1
- Authors: Karina A Marsden; Lucy Lush; Jon A Holmberg; Mick J Whelan; Andrew J King; Rory P Wilson; Alice F Charteris; Laura M Cardenas; Davey L Jones; Dave R Chadwick
- Data description: Metabolomics profile data from sheep urine, collected in autumn from semi-improved and improved pastures (n = 4 per site)

## Data Collection and Processing
- Sample collection and preparation:
  - Urine samples syringe-filtered (< 0.2 μm) and flash-frozen
  - Procedural blanks (ultra-pure water) filtered and blank-corrected
- Storage and shipment:
  - Frozen at -80 °C, shipped on dry ice to West Coast Metabolomics Center, UC Davis
- Analytical method:
  - Untargeted primary metabolism analysis using ALEX-CIS GC-TOF-MS (Gerstel Inc.)
- Data generation:
  - Peak intensity values for all identified compounds in the untargeted analysis

## Data Content and Structure
- Data contents:
  - Peak intensity values for identified metabolites
- Data headers:
  - Sample: sheep ID and site of urine collection
  - Site: semi-improved or improved pasture
  - Other headers: identified compounds; subsequent rows contain corresponding peak intensities

## Provenance, Citation, and Access
- Reuse guidance:
  - If data are reused, ensure full citation
- Provenance:
  - Data produced by the listed authors under the specified grant
  - Data description includes collection, processing, and analysis steps as described above

## Implications for Data Strategy and Leadership
- Metadata and discoverability:
  - Clear labeling of Sample and Site aids interoperability and cross-study comparisons
  - Documentation of blank correction and analytical method supports reproducibility
- Data quality and governance:
  - Blank correction and untargeted approach imply attention to background signals and compound identification quality
- Use in broader data ecosystems:
  - Dataset suitable for comparative analyses of metabolomic profiles across pasture types
  - Aligns with data-leadership goals to understand collaborations, provenance, and reuse potential across networks
- Considerations for future data management:
  - Ensure explicit metadata standards (e.g., controlled vocabularies for sample sites, compound identifiers)
  - Maintain traceability of sample IDs and site metadata to support meta-analyses and data integration