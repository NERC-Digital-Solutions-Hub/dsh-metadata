# DATA HEADER INFORMATION for Soil_bulk_density.csv

- Purpose and processing
  - Records soil bulk density.
  - Method: soil samples from a cylinder were oven-dried for 24 hours at 105°C.
  - Coarse fraction (rocks, roots, biomass residues) removed by passing through a 2 mm sieve.
  - Proportion of coarse fraction used to adjust the bulk density value.
  - Related manuals and project context: Manual_1_Classical_Survey and Manual_3_Laboratory_Works; ESPA Programme; Project P4GES.
  - Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

- Data provenance and references
  - Programme: ESPA (http://www.espa.ac.uk/)
  - Project: P4GES (https://www.p4ges.org)
  - DOI for referenced manuals: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
  - Acknowledgement for outputs linked to the data.

- Data schema (fields, types, units)
  - site_id
    - Information: P4GES site code
    - Variable Type: Text String
    - Unit: (none)
  - subplot
    - Information: subplot where sampling was done
    - Variable Type: Categorical
    - Unit: S1 / S2 / S3 / S4
  - Bulk_density
    - Information: Soil bulk density value
    - Variable Type: Numeric
    - Unit: g.cm-3
  - depth
    - Information: depth of the sampled soil layer (from 10 to 100 cm)
    - Variable Type: Numeric
    - Unit: cm

- Data quality and management considerations
  - Explicit units and variable types help ensure consistent interpretation and discovery.
  - Depth range provided (10–100 cm) defines the sampling interval for the bulk density measurements.
  - Metadata links to processing steps (oven-drying, sieving, coarse fraction adjustment) to support traceability and reproducibility.

- Practical notes for data leadership
  - Data is linked to a broader data ecosystem (ESPA, P4GES) with clear provenance and acknowledgement requirements.
  - Ensure discoverability by maintaining clear field definitions, units, and category values (e.g., subplot S1–S4).
  - Leverage the referenced manuals and project context to inform data stewardship, validation, and potential integration with related soil datasets.