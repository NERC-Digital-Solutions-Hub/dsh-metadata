# DATA HEADER INFORMATION for Soil_bulk_density.csv

## Overview
- This dataset records soil bulk density measurements. Samples were oven-dried for 24 hours at 105°C and passed through a 2 mm sieve to remove coarse fractions; the proportion of coarse fraction is used to adjust the bulk density value.

## Data collection and processing
- Programme and project context: ESPA Programme; Project P4GES.
- Related manuals: Manual_1_Classical_Survey and Manual_3_Laboratory_Works.
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo (required for products derived from these data).

## Dataset structure and fields
- site_id
  - Information: P4GES site code
  - Variable type: Text string
  - Unit: (not specified)
- subplot
  - Information: subplot where sampling was done
  - Variable type: Categorical
  - Unit: S1 / S2 / S3 / S4
- Bulk_density
  - Information: Soil bulk density value
  - Variable type: Numeric
  - Unit: Grams per cubic centimeter (g.cm-3)
- depth
  - Information: depth of the sampled soil layer (from 10 to 100 cm)
  - Variable type: Numeric
  - Unit: Centimeter (cm)

## Data provenance and usage rights
- Data origin: P4GES project sites; specific site and depth ranges documented.
- Acknowledgement and DOI references provided for traceability.
- Emphasis on transparent data handling, including the need to share underlying data where appropriate.

## Relevance to monitoring and governance
- Provides a concrete environmental health metric (soil bulk density) relevant to soil structure and land management policy evaluation.
- Methodology supports standardization across monitoring initiatives (oven-drying, sieving, coarse fraction adjustment), aiding comparability.
- Clear metadata and unit definitions facilitate data integration into dashboards, reports, or policy evaluations.

## Considerations for monitoring frameworks
- Metadata completeness and data provenance are essential for data quality and trust.
- Data governance implications: sharing underlying data publicly may be a barrier; ensure data management standards are upheld at source.
- Timeliness and accessibility: ensure data can be retrieved and transformed without excessive barriers, given potential silo challenges.