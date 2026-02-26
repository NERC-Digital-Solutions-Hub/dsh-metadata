# Data file: ash_transport_experiment.csv

- What it is: A dataset describing laboratory measurements of ash transport by runoff from controlled flume experiments conducted in August 2019 at Rocky Mountain Research Station Laboratory, US Forest Service, Moscow, ID, USA.
- Authors and purpose: Produced to obtain ash transport rates with runoff after wildfires; associated with researchers Jonay Neris Tome, Pete Robichaud, Carmen Sánchez-García, Cristina Santín, and Stefan Doerr.

## Data content and structure

- Observations: 1296 data points.
- Key variables (features):
  - Ash depth (cm)
  - Flow rate (L/min) and corresponding runoff rate (L/sec)
  - Ash transport rate (g/sec)
  - Ash concentration (g/L)
- Experimental factors:
  - Ash depths: 1 cm and 3 cm
  - Flow rates: 0.25, 1, and 2 L/min
- Experimental blocks and replication:
  - 2 ash depths
  - 6 flow-rate combinations per ash depth
  - 6 replicates per flow-rate combination
  - 3 flow rates per combination
  - 6 bottles/samples per flow rate
- Data collection granularity: For each run, six runoff samples per flume were collected at intervals of 1.5 minutes over 15–20 seconds per sample.

## Experimental design

- Physical setup:
  - Flumes: 3 m long, 0.15 m wide
  - Substratum: Artificial substrate simulating soil roughness (glued sand and gravel)
  - Slope: 17 degrees
- Treatments:
  - Ash depths: 1 cm and 3 cm
  - Runoff flow rates: Fixed at 0.25 (F1), 1 (F2), 2 L/min (F3)
- Randomization and replication:
  - Flume positions randomized between runs to distribute flow rates
  - Each replication includes 3 runs; each run uses all three flow rates in a varied order
  - Each run includes two flumes receiving each flow rate, with different flow-rate distribution per run

## Data collection protocol

- Automatic flow control:
  - A flow regulator with three solenoid valves and three pipes delivering flow to six flumes
  - Orifice disks calibrated for specific flow rates to achieve F1, F2, F3 at ~30 psi
- Sampling procedure:
  - Pre-run equilibration: 30 minutes after prewetting
  - Run duration: 10 minutes per run
  - Sample collection: runoff samples from each flume outlet
  - Sample sizes: 500 ml bottles for low/moderate flow, 1 L bottles for high flow
  - Sampling cadence: six samples per run, every ~1.5 minutes
  - Adjustments: shorter intervals for flumes with delayed runoff to maintain timing parity

## Sample processing and calculations

- Processing steps:
  - Drying and weighing: use 500 ml and 1 L beakers
  - Weighing sequence: initial beaker weight (WB1), post-sample weight (WB2) including water and ash, final dry weight (WB3)
  - Rinse and combine: rinse bottles to collect all ash; combine with beaker contents
  - Drying: 110°C for 24 hours, then reweigh (WB3)
- Calculations:
  - Ash content (g) = WB3 − WB1
  - Runoff volume (L) = (WB2 − WB3) / 1000
- Data provenance: full record of measurements and derived quantities enabling calculation of ash transport metrics per observation

## Data management and accessibility

- Completeness: Full record present
- Metadata and traceability: Data collected under a documented protocol; authors and experimental conditions explicitly stated
- Potential for reuse: Datasets and derived metrics suitable for modeling ash transport as a function of ash depth, flow rate, and runoff characteristics

## Potential analyses and applications

- Correlations and predictive modeling:
  - Analyze how ash depth and flow rate influence ash transport rate and ash concentration
  - Develop regression or mechanistic models to predict ash transport under different runoff conditions
- Scale-up considerations:
  - Use lab results to inform field-scale predictions of ash transport after wildfires
  - Compare lab-derived relationships with field-observed data, accounting for substrate and slope differences
- Data quality and comparability:
  - Ensure consistent data handling across ash depths and flow-rate combinations
  - Leverage complete sampling sequence (six samples per run) to assess temporal dynamics of runoff transport

## Key considerations and challenges for analysts

- Experimental context vs. real-world: lab flume conditions with artificial substrata; results may require validation for field scenarios
- Data structure complexity: multiple nested factors (ash depth, flow rate, replicate, run) requiring careful modeling design
- Sampling cadence: uniform 1.5-minute intervals with occasional adjustments for delayed runoff
- Documentation: comprehensive methodology aids reproducibility and data integration with other datasets in the domain of post-fire sediment and ash transport research