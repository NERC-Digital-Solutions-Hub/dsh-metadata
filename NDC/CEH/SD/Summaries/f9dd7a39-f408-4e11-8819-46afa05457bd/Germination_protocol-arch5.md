# Germination rates of Eschscholzia californica seeds located within habitats comprising habitats with different floral cover

- Overview
  - Dataset describes germination rates of seeds from Eschscholzia californica plants exposed to habitats with varying floral cover.
  - Collected in June 2015 at the Hillesden estate, Buckinghamshire, UK.
  - Part of a larger experiment on how floral resources affect pollination services to isolated plants.
  - Complete dataset; germination counts derived from 48 field-exposed plants (20 seeds per plant, total 960 seeds).
  - Data stored and interpreted by Evans, T.M.; supporting documentation available.

- Experimental design
  - Experimental arrays: three E. californica plants per array, separated by 1 m, arranged in a triangular formation.
  - 16 arrays across four 100 ha replicate blocks; blocks separated by >500 m.
  - Within each block: four arrays along a 150 m transect crossing the boundary between florally rich and florally poor habitats (two arrays in each habitat type).
  - Central structure includes two habitat types per block (Habitat and Treatment distinctions).

- Collection methods
  - All open flowers removed before field placement; plants left in the field for 16 days to ensure full anthesis and multiple pollination events.
  - Fruits tagged to ensure only period-specific development is analyzed.
  - Post-field, plants collected and stored under controlled glasshouse conditions (day:night ~20°C:15°C; 12:12 h light:dark) until fruit maturation.
  - At maturation, 20 seeds from each of the 48 plants sown into compost and monitored under glasshouse conditions.
  - Germination recorded daily for 30 days; non-germinated seeds tracked up to 90 days as non-viable.
  - Germination success expressed as a ratio of germinated seeds to total seeds sown per plant.

- Data structure and units
  - Single CSV file: Germination_rates_of_Eschscholzia_californica_seeds.csv
  - Key columns:
    - Block: replicate block identifier
    - Experimental_array: array identifier within a block
    - Plant_identification_number: plant ID before field transfer
    - Habitat: habitat category location
    - Treatment: additional experimental treatment descriptor
    - Number_of_seeds_germinated: count per plant
    - Total_number_of_seeds_sown: seeds sown per plant

- Provenance and governance implications for Data Stewards
  - Data is complete and tied to a specific field study; provenance is documented (Evans, T.M.) and linked to broader research on pollination services.
  - File format is CSV with straightforward structure, supporting easy ingestion into data portals and repositories.
  - Metadata considerations for reuse:
    - Capture study location (Hillesden estate), collection date (June 2015), experimental design (arrays, blocks, habitat boundaries), and measurement approach (daily germination over 30 days; 90-day non-viability).
    - Clearly define Habitats and Treatments to ensure cross-dataset consistency.
    - Note sample size details (48 plants, 16 arrays, 4 blocks) and seed counts (20 seeds per plant).
  - Potential data management considerations:
    - Ensure alignment of Habitat and Treatment definitions across related datasets.
    - Maintain traceability to the original publication or dataset descriptors (Evans, T.M.).
    Ensure appropriate citation and any licensing terms are observed.
  - Suggestions for data quality and sharing:
    - Provide versioning and updates if re-analyses or extended data become available.
    - Include a data dictionary or schema documentation to complement the CSV for future reuse.
    - Consider embedding a data provenance line or link to supporting documentation for reproducibility.