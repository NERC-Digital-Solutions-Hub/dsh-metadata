# The germination rates of seeds from Eschscholzia californica plants located within habitats comprising habitats with different floral cover

- Overview
  - Dataset detailing germination rates of Eschscholzia californica seeds from field-exposed plants across habitats with different floral cover.
  - Collected in June 2015 at the Hillesden estate, Buckinghamshire, UK; part of a larger experiment on how floral resources influence pollination services to isolated plants.
  - Data collected and interpreted by Evans, T.M.; supporting documentation exists.

- Experimental design
  - 16 experimental arrays across four 100-hectare replicate blocks, each block >500 m apart.
  - Each array comprises three E. californica plants (1 m apart) arranged in a triangular formation.
  - At the center of each block, four arrays spaced along a 150 m transect across the boundary between a florally rich wildflower patch and florally poor bare/fallow/grazed grassland (two arrays in rich habitat, two in poor habitat).

- Collection methods and timeline
  - All open flowers removed prior to field placement; plants remained in the field for 16 days to allow full anthesis and multiple pollination events.
  - After 16 days, fruits were tagged to ensure only period-specific development was analyzed.
  - In controlled glasshouse conditions, 20 seeds from each of the 48 plants were sown; germination was recorded daily for 30 days. Seeds not germinating by 90 days were recorded as non-viable.
  - Germination success expressed as the ratio of germinated seeds to total sown seeds per plant.

- Data structure and units
  - Single CSV: Germination_rates_of_Eschscholzia_californica_seeds.csv
  - Key columns:
    - Block: replicate block ID (one of four blocks)
    - Experimental_array: array ID within a block
    - Plant_identification_number: plant ID prior to field transfer
    - Habitat: florally rich vs florally poor location
    - Treatment: associated condition (series within habitat)
    - Number_of_seeds_germinated: germinated seeds per plant
    - Total_number_of_seeds_sown: seeds sown per plant

- Provenance, completeness, and documentation
  - Dataset is complete as reported; part of a larger study on floral resources and pollination services.
  - Collected and interpreted by Evans, T.M.; supporting documentation exists to contextualize methods and design.

- Relevance for data leadership and governance
  - Demonstrates clear provenance and a well-documented experimental design suitable for cross-study integration.
  - Metadata elements (Block, Habitat, Treatment, experimental layout) support data discoverability, filtering, and reuse in policy or partner networks.
  - Provides a well-defined data schema and units, enabling reproducibility and secondary analyses (e.g., comparing germination rates across habitats or linking to pollination outcomes).

- Considerations and limitations
  - Study restricted to 48 plants across four blocks at a single site and time frame (2015), which may affect generalizability.
  - The exact interpretation of "Treatment" is tied to habitat condition and should be cross-checked with supplementary documentation.
  - Data are bounded by the 90-day non-viability rule and 30-day germination window; longer-term viability not captured.