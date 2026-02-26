# Tc and Se Uptake By Higher Plants - Meta Data

- Overview
  - Describes a radiolabeling uptake study across 61 plant species, each with 5 replicates in 12 cm pots, grown under controlled conditions with supplemental lighting and heating.
  - Focuses on three major clades in the APGIII angiosperm phylogeny (labelled a, b, c in associated files).
  - Radiolabeling with Tc-99 and Se-75, followed by harvest after 48 hours and measurement of radioactivity in plant material.

- Experimental design and material context
  - Randomized block design with species grown together in blocks.
  - Growth media: Levington's F2S peat-based compost with lime and ammonium sulfate; pH ≈ 6.2; targeted nutrient levels (P ≈ 50 mg/L, K ≈ 50 mg/L, nitrate ≈ 10 mg/L).
  - Radiolabeling details: 25 mL solution containing 107 kBq/L of Tc-99 and 95 kBq/L of Se-75 applied to compost surface.
  - Reported mean activity concentrations in compost: Tc-99 ≈ 17.8 kBq/kg; Se-75 ≈ 15.8 kBq/kg.

- Sample processing and measurements
  - Harvest: Above-ground shoot material harvested after 48 hours, then dried.
  - Digestion: 0.1 g of dried tissue digested in 5 mL nitric acid + 5 mL H2O2 until reaction ceased.
  - Counting: Digests counted for gamma emissions (Se-75) and beta emissions (Tc-99) after appropriate preparation (gamma with Se-75, beta with Tc-99).
  - Decay correction: Se-75 counts decay-corrected to the labeling date.

- Data file and variable definitions
  - Data file: TcAndSeUptakeByPlantsData
  - Key columns (examples):
    - Block: indicates species grown together within a randomized block design.
    - CPM1 beta: Counts per minute for beta emissions from Tc-99.
    - CPM1 gamma: Counts per minute for gamma emissions from Se-75.
    - Decay corrected: Se-75 counts per minute decay-corrected to the labeling date.
  - Paragraphs indicate units and correction status; decay corrections use time-stamping relative to labeling.

- Metadata and data model considerations for stewardship
  - Core metadata to capture (beyond column definitions):
    - Species identity and taxonomic details (including clade assignment a/b/c).
    - Replicate IDs, block assignments, and pot identifiers.
    - Experimental conditions: compost composition, pH, nutrient levels, lighting/heating regime.
    - Radiolabeling specifics: activity concentrations, total activity per replicate, labeling date/time.
    - Processing workflow: harvest date, digestion protocol, instruments used, counting method, calibration details.
    - Measurement units: clearly specify counts per minute, activity units (kBq/kg or kBq/kg), and any normalization applied.
  - Data quality considerations:
    - Ensure consistent units across all samples and timepoints.
    - Document decay-correction method and time reference for reproducibility.
    - Capture any data gaps or anomalies in blocks/species to aid future data reuse.
  - Discoverability and reuse:
    - Include descriptive keywords (e.g., plant uptake, Tc-99, Se-75, radiolabeling, randomized block, APGIII clades).
    - Link to related metadata or files (e.g., the jpg file for species sampling and the full species list).
    - Provide dataset provenance, access conditions, and any sharing restrictions.
  - Stewardship actions:
    - Store in a repository with a stable DOI and clear versioning.
    - Maintain a data dictionary or metadata schema aligned with community standards (e.g., ISA-Tab, Ecological Metadata Language) to facilitate interoperability.

- Potential challenges and considerations
  - Incomplete alignment between metadata in the text (descriptions) and data file columns; ensure alignment and fill in any missing fields (e.g., full species names, clade mappings).
  - Interoperability across formats and potential need for standardized identifiers for species and clades.
  - Large but manageable dataset; ensure efficient storage and indexing for discovery across numerous species and replicates.

- End-use implications for data stewards
  - The metadata supports reproducibility of uptake measurements across multiple species and blocks.
  - Clear documentation of counting and decay correction enables cross-study comparisons of radioisotope uptake.
  - Proper governance around updates, versioning, and accessibility will improve long-term usability for researchers studying plant uptake and radiotracer experiments.