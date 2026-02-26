# DATA HEADER INFORMATION for Soil_bulk_density.csv

## Overview
- The dataset records soil bulk density measurements.
- Soil samples were taken in cylinders, oven-dried for 24 hours at 105°C, and passed through a 2 mm sieve to remove coarse fractions (rocks, roots, biomass residues).
- The proportion of coarse fraction is used to adjust (correct) the bulk density value.

## Measurement and processing details
- Coarse fraction correction: proportion of coarse material is applied to adjust bulk density values for consistency.
- Sampling context: depth indicates the soil layer sampled (from 10 to 100 cm).

## Data fields and units
- site_id
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: (none)
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

## Data provenance and references
- Related manuals:
  - Manual_1_ Classical_Survey
  - Manual_3_Laboratory_Works
- DOI reference: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Programme: ESPA (http://www.espa.ac.uk/)
- Project: P4GES (https://www.p4ges.org)

## Acknowledgement and usage constraints
- Acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

## Relevance for monitoring and analysis
- Supports consistent cross-site and temporal monitoring of soil physical properties as part of environmental health indicators.
- Data are prepared to be integrated with standardized formats and outputs (e.g., reports, maps) for policy and health assessments.
- Aligns with aims to verify and quality-assure data, enabling broader data sharing and reuse across monitoring programs.