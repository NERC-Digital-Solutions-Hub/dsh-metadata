# Data file: ash_transport_experiment.csv

- What it is: A laboratory experiment dataset describing ash transport by runoff using flumes to obtain ash transport rates after wildfires, produced by Rocky Mountain Research Station Laboratory, US Forest Service (Moscow, ID, USA) in August 2019.
- Authors: Dr Jonay Neris Tome, Dr Pete Robichaud, Dr Carmen Sánchez-García, Dr Cristina Santín, and Prof. Stefan Doerr.
- Completeness: Full record.
- Key variables (features): ash depth (cm), flow rate (L/min), runoff rate (L/sec), ash transport rate (g/sec), ash concentration (g/L).
- Treatments: Two ash depths (1 cm and 3 cm) and three flow rates (F1 = 0.25 L/min, F2 = 1 L/min, F3 = 2 L/min).
- Replication and observations: 2 ash depths × 6 flow-rate combinations per depth × 6 replicates per combination × 3 flow rates per combination × 6 samples (bottles) per flow rate, totaling 1296 observations.
- Methodological scope: Laboratory flume experiments with artificial substratum to simulate soil roughness; prewetting with rainfall; 3 runs per replication; each run 10 minutes of flow; randomized flume/flow-rate distribution before each replication.
- Data collection cadence: runoff samples collected every 1.5 minutes for 15–20 seconds per sample, with adjustments for delayed runoff.
- Derived calculations: 
  - Ash content (g) = WB3 − WB1
  - Runoff volume (L) = (WB2 − WB3) / 1000
- Documentation and processing: Detailed protocols for sample processing (drying, weighing, and ash content calculation) and for sample labeling and tracking (beaker and bottle IDs).

## Experimental design and data collection

- Experimental setup
  - Plot size: 3 m long × 0.15 m wide
  - Slope: 17 degrees
  - Substratum: artificial substrate to mimic soil roughness
  - Ash depths: 1 cm and 3 cm
  - Runoff flow rates: F1 (0.25 L/min), F2 (1 L/min), F3 (2 L/min)
  - Replications: 6 replicates per flow-rate combination; 3 runs per replicate
  - Randomization: flume positions and flow-rate distribution randomized at the start of each replication
- Flow control system
  - Automatic regulator with 3 solenoid valves feeding 3 pipes (1 m each), each with 6 exits to 6 flumes
  - Flow rates set via calibrated orifice disks (Teejet: 24 for F1, 47 for F2, 70 for F3) at 30 psi
- Run and sampling protocol
  - Equilibration: 30 minutes after prewetting
  - Sampling: 6 runoff samples per flume per run
  - Sample volumes: 500 mL for low/moderate flows; 1 L for high flow
  - Timing: samples collected as flow reaches outlet, every 1.5 minutes, 15–20 seconds per sample
  - Run structure: 3 runs per replication; the 3 runs use shuffled flow-rate sequences
- Pre-wetting and rainfall
  - Prewetting with rainfall intensity 85 mm/h
  - Rainfall depth/duration determined by time to runoff

## Data processing and calculations

- Sample handling
  - Use 500 mL or 1 L beakers to dry, weigh, and determine ash content and runoff volume
  - Weighing steps: WB1 (empty beaker), WB2 (beaker with sample), WB3 (dry ash content)
  - Post-processing: rinse bottles to ensure all ash is transferred to the beaker; dry at 110°C for 24 h; weigh final dry ash
- Calculations and units
  - Ash content and runoff volumes calculated from measured weights
  - Units for key measurements: ash depth (cm), flow rate (L/min), runoff rate (L/sec), ash transport rate (g/sec), ash concentration (g/L)

## Data governance and reuse considerations for Data Stewards

- Provenance and accountability
  - Clear authorship, institutional affiliation, and date (August 2019) documented
  - Full methodological detail provided, enabling reproducibility and auditing
- Metadata and discoverability
  - Dataset should be catalogued with variables, units, experimental design (depths, flow rates, replicates), and processing steps
  - Include protocol references for sampling, processing, and calculations to support re-use
- Data quality and stewardship
  - The dataset is flagged as a full-record dataset with defined QA/processing steps; ensure consistent unit usage and validation of weight-based calculations across the dataset
  - Capture any data provenance notes (e.g., versioned protocol, any deviations during runs) in metadata
- Usability and interoperability
  - Align with data standards for experimental measurements (clearly specify units and variable definitions)
  - Document mathematical formulas used to derive ash content and runoff volume for transparency and reuse in meta-analyses
- Storage, sharing, and updates
  - Prepare for uploading to data portals and catalogues; ensure data remains discoverable and citable
  - If updates occur (e.g., revised measurements or corrected weights), maintain versioning and changelog within metadata

## Practical implications for data users

- Enables analysis of ash transport rates as a function of ash depth and hydraulic forcing
- Supports modeling of post-fire ash redistribution in runoff scenarios under controlled conditions
- Useful for comparative studies with field data or other lab-based flume experiments, given explicit experimental design and processing details