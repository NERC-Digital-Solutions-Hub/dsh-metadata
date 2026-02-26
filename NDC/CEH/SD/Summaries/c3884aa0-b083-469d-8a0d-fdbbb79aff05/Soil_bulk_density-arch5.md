# DATA HEADER INFORMATION for Soil_bulk_density.csv

## Overview
- This dataset records soil bulk density, including methodology to adjust for coarse fraction.
- Soil samples were oven-dried at 105°C for 24 hours and sieved through a 2 mm sieve to remove coarse material; the proportion of coarse fraction is used to adjust the bulk density value.

## Data provenance and context
- Programme: ESPA.
- Project: P4GES.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data fields, types, and units
- site_id
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: (none specified)
- subplot
  - Information: subplot where the sampling was done
  - Variable Type: Categorical
  - Unit: S1 / S2 / S3 / S4
- Bulk_density
  - Information: Soil bulk density value
  - Variable Type: Numeric
  - Unit: Grams per cubic centimeter (g.cm-3)
- depth
  - Information: depth of the sampled soil layer (from 10 to 100 cm)
  - Variable Type: Numeric
  - Unit: Centimeter (cm)

## Methodology details
- Bulk density is determined after oven-drying soil samples at 105°C for 24 hours.
- Coarse fraction ( rocks/roots/biomass residues) removed using a 2 mm sieve; the proportion of coarse fraction is used to adjust bulk density.

## Documentation and references
- Manual_1_ Classical_Survey
- Manual_3_Laboratory_Works
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05

## Data governance and sharing considerations
- Data should be uploaded to relevant portals and catalogued with the accompanying metadata.
- Ensure proper data lineage, versioning, and documentation of any transformations (cleaning, adjustments for coarse fraction).
- Maintain alignment with standards for metadata completeness (source, methods, units, variable definitions) to support discovery and reuse.

## Acknowledgments and usage restrictions
- Acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.
- Respect sharing limitations and disclose any embargoes or proprietary constraints as applicable.

## Challenges and considerations for Data Stewards
- Ensuring timely data submission from contributors.
- Achieving metadata completeness and consistency across datasets (especially variable definitions and units).
- Handling diverse data systems and formats when integrating with catalogs and portals.
- Managing large datasets and ensuring interoperability with existing soil datasets.