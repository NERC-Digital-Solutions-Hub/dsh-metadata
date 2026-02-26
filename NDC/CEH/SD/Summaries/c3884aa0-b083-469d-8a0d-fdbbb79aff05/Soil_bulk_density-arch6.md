# DATA HEADER INFORMATION for Soil_bulk_density.csv

## Overview
- Records soil bulk density using cylinder samples oven-dried for 24 hours at 105°C.
- Coarse fraction removed via 2 mm sieve; the proportion of coarse fraction is used to adjust the bulk density value.
- Related to ESPA Programme and P4GES Project; acknowledgement required for products derived from these data.

## Data collection and processing
- Samples prepared by drying, sieving to remove coarse material, and adjusting bulk density based on coarse fraction.
- Data likely accompanied by manuals for standard methods.

## Variables and data types
- site_id: Text String
  - Information: P4GES site code
  - Unit: none
- subplot: Categorical
  - Information: Subplot where sampling was done
  - Unit: S1 / S2 / S3 / S4
- Bulk_density: Numeric
  - Information: Soil bulk density value (adjusted)
  - Unit: grams per cubic centimeter (g.cm-3)
- depth: Numeric
  - Information: Depth of the sampled soil layer (from 10 to 100 cm)
  - Unit: centimeters (cm)

## Data provenance and references
- Manuals: Manual_1_Classical_Survey and Manual_3_Laboratory_Works
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Programme: ESPA
- Project: P4GES
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo)

## Usage notes and data quality considerations
- Ensure proper quality assurance and correct application of coarse fraction adjustment.
- Data are depth-specific (10–100 cm) and location-specific (subplot within site).
- When sharing or re-using outputs, include appropriate attribution to ESPA/P4GES and the contributing laboratory.