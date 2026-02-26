# DATA HEADER INFORMATION for Soil_bulk_density.csv

- What it records
  - Soil bulk density measurements, with samples oven-dried (24 h at 105°C) and sieved to remove coarse fractions (rocks, roots, biomass). The proportion of coarse fraction is used to adjust the bulk density value.

- Data collection and processing context
  - Related manuals: Manual_1_Classical_Survey and Manual_3_Laboratory_Works
  - Programme: ESPA; Project: P4GES
  - Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo)

- Data provenance and references
  - DOIs/links provided:
    - DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
    - ESPA: http://www.espa.ac.uk/
    - P4GES: https://www.p4ges.org

- Data schema (columns)
  - site_id
    - Information: P4GES site code
    - Type: Text String
    - Unit: (not specified)
  - subplot
    - Information: subplot where sampling was done
    - Type: Categorical
    - Unit: S1 / S2 / S3 / S4
  - Bulk_density
    - Information: Soil bulk density value
    - Type: Numeric
    - Unit: Grams per cubic centimeter (g.cm-3)
  - depth
    - Information: depth of the sampled soil layer
    - Type: Numeric
    - Unit: Centimeter (cm)
    - Range: 10 to 100 cm

- How the data can be used (analytical perspective)
  - Analyze spatial variation in bulk density across sites and subplots
  - Examine depth-dependent changes in bulk density (10–100 cm)
  - Combine with other soil properties to model soil structure and carbon storage
  - Ensure reproducibility by referencing the manuals and acknowledging data sources

- Usage and discoverability notes
  - Data are associated with P4GES/ESPA projects; proper citation and acknowledgment are advised for derived analyses
  - Metadata explicitly describes each field to support data harmonization and cross-study comparisons