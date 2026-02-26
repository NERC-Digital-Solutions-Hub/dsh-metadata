# UnknownsUplandLowlandMetabolomics.csv

## Overview
- Project: Uplands-N2O
- Grant number: NE/M015351/1
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Data type: Metabolomics dataset of sheep urine
- Purpose: Untargeted metabolomics profiles to compare urine from sheep at two pasture types (semi-improved and improved)

## Data Description
- Seasons: Autumn
- Samples: 4 from semi-improved site; 4 from improved site (n = 8 total)
- Sample handling: Procedural blanks of ultra-pure water were filtered and blank-corrected; samples were stored at -80 °C
- Shipping: Frozen samples shipped on dry ice to the West Coast Metabolomics Center, UC Davis
- Analysis method: Untargeted primary metabolism analysis using ALEX-CIS GC-TOF-MS (Gerstel Inc., Linthicum, MD)
- Data content: Peak intensity values for all identified compounds from the untargeted analysis
- Data headers: 
  - Sample: sheep ID and urine collection site
  - Season: site, semi-improved or improved pasture
  - Remaining headers: numerical identifiers for unidentified compounds; corresponding peak intensities in rows beneath

## Data Structure and Provenance
- File naming indicates “Unknowns” metabolites across Upland vs. Lowland contexts
- Data derived from untargeted metabolomics; contains intensity values rather than identified compound names for all features
- Provenance includes sample collection at two pasture types in autumn, blank corrections, and centralized analysis at UC Davis

## Data Quality and Metadata Considerations
- Potentially limited metadata for each feature beyond numeric identifiers (unidentified compounds)
- Small sample size (n=8) may limit statistical power and generalizability
- Reuse requires full citation to the original source

## Access, Sharing, and Reuse
- Reuse guidance: If data are reused, ensure it is fully cited
- Data format: CSV with structured headers; accessible for downstream analyses

## Stewardship and Next Steps
- Ensure comprehensive metadata:
  - Clear mapping of Sample IDs to animal identifiers and sites
  - Exact definitions of “semi-improved” vs “improved” pasture and site characteristics
  - Instrument settings, retention times, calibration details, and blank correction methodology
- Link to raw data (e.g., raw GC-TOF-MS files) if available for reproducibility
- Maintain provenance records and versioning; document any reprocessing or normalization steps
- Create a data dictionary for unidentified compound identifiers to aid future interpretation
- Consider data integration with related environmental or phenotypic datasets to enhance usability