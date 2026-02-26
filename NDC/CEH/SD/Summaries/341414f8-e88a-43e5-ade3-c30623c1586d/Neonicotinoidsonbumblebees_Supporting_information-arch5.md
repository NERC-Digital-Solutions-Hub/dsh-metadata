# The number and individual weight of bumblebees (Bombus terrestris audax) from nests containing neonicotinoids in Wester Ross, UK

## Overview
- Provides experimental data on bumblebee (Bombus terrestris audax) mass from nests exposed to neonicotinoid-containing pesticides in Wester Ross, Highlands, Scotland.
- Two separate experiments with untreated and pesticide-treated groups (chlorpyrifos and/or imidacloprid) conducted in field conditions.
- Dataset consists of two CSV files with individual bee weights (mg) recorded after laboratory processing.

## Experimental design and data collection
- Housing and field setup
  - Bees housed in nests (3 nests per box) with entrances at two ends and one in the middle.
  - Tripols (experimental units) assigned to treatment groups; approximately 1 m spacing between Tripols to confine orientation errors within a treatment.
  - Colonies placed in sheltered wilderness/enriched grassland habitat; low baseline pesticide exposure in the Highlands.
- Treatments and exposure
  - 1500 ml sugar syrup provided per colony, either untreated or containing pesticide.
  - Two experiments:
    - Experiment 1: untreated, chlorpyrifos (150 nM), and chlorpyrifos (150 nM) with imidacloprid (10 nM).
    - Experiment 2: untreated, imidacloprid (10 nM) with chlorpyrifos (150 nM), and imidacloprid (10 nM) alone.
  - Order: UT, single treatment, double treatment to minimize local effects.
- Field period and assessment
  - Field exposure: 28 to 48 days depending on experiment (dates given in document).
  - Final day: bee entrance gates set to allow entries only; after ~5 hours, colonies returned to lab for assessment.
  - Lab assessment metrics: colony mass change, total live bees, average bee mass, number of healthy brood cells, overall nest condition.
  - Individual bees weighed after CO2 anesthesia; bees weighed and then sacrificed in ice-cold detergent-containing water to prevent awakening.
- Data recording
  - Bee masses recorded at start and end of the experiment (excluding the sugar syrup provided).
  - Final mass measurements used to populate the datasets.

## Data records and structure
- Files
  - Neonicotinoidsonbumblebees_Experiment1.csv
  - Neonicotinoidsonbumblebees_Experiment2.csv
- Columns and rows
  - Columns: Colony number and treatment.
  - Rows: Bee mass measurements (mg), ordered by mass.
  - Unit: milligrams (mg).

## Data quality and provenance
- Quality control
  - Double-checking: one person reads the weight aloud; a second person records the weight to ensure accuracy.
  - Recorders were blinded to treatment group to avoid bias.
- Provenance and documentation
  - Dataset is accompanied by narrative methodology (this document) and references a broader study (Moffat et al 2015, In Press).
  - Data structure is consistent across the two experiments.

## Metadata considerations for data stewardship
- Recommended metadata elements
  - Study name, species (Bombus terrestris audax), site location (Wester Ross, The Highlands, Scotland), habitat type.
  - Experimental design details: number of nests per box, Tripol arrangement, treatment concentrations, and order of treatments.
  - Timing: exact start and end dates for each experiment, duration of field exposure.
  - Measurement protocol: instrument type, measurement procedure, units (mg), handling/anaesthesia method (CO2).
  - Data processing: any transformations, quality checks, or exclusion criteria applied to measurements.
  - Limitations and contextual notes: background low environmental pesticide use, potential confounders (foraging behavior, exposure duration).
- Data documentation
  - Ensure clear mapping of columns (e.g., colony_id, treatment_code) and a codebook for treatment nomenclature.
  - Include links to related publications (Moffat et al. 2015) and dataset-level README or data dictionary.

## Storage, sharing, and governance
- File formats
  - Use plain CSV files for interoperability; preserve original column order and data types.
- Discoverability and reuse
  - Provide dataset-level metadata describing scope, methods, units, and limitations to facilitate discovery and reuse by researchers and data systems.
  - Include versioning and timestamps; note the two-experiment structure and any updates or corrections.
- Access considerations
  - No obvious confidentiality concerns; ensure that the metadata clearly communicates experimental conditions and contexts to enable reproducibility.
- Documentation and traceability
  - Maintain a dataset-level README or metadata file detailing data collection procedures, QC steps, and any data processing performed beyond record-keeping.