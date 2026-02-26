# ash_transport_experiment.csv

## Overview
- Data file documenting an ash transport by runoff laboratory experiment conducted to obtain ash transport rates after wildfires.
- Where: Rocky Mountain Research Station Laboratory, US Forest Service, Moscow, ID, USA.
- When: August 2019.
- Who: Dr Jonay Neris Tome, Dr Pete Robichaud, Dr Carmen Sánchez-García, Dr Cristina Santín, and Prof. Stefan Doerr.
- Completeness: Full record.
- Key variables: ash depth (cm), flow rate (L/min), runoff rate (L/sec), ash transport rate (g/sec), ash concentration (g/L).
- Observations: 1,296.
- Purpose for monitoring: generating quantitative measures of ash movement under controlled flow scenarios to inform environmental impact assessments and management decisions.

## Experimental design and data structure
- Experimental setup:
  - Plot size: 3 m long × 0.15 m wide.
  - Slope: 17 degrees.
  - Substratum: artificial roughened substratum to mimic soil.
  - Ash depths evaluated: 1 cm and 3 cm.
- Flow rates (three levels):
  - F1 = 0.25 L/min
  - F2 = 1 L/min
  - F3 = 2 L/min
- Replication and runs:
  - Each replicate: 3 runs.
  - Each run: 10 minutes of flow.
  - Each run involves two flumes for each flow rate; distribution of flow rates across flumes randomized per run.
  - Per ash depth, there are 6 replicates, with 6 replicates per flow-rate combination per ash depth.
- Observations and data structure:
  - Features include: ash depth (cm), flow rate (L/min), runoff rate (L/sec), ash transport rate (g/sec), ash concentration (g/L).
  - Total observations: 1,296.
- Data collection context:
  - An automatic flow regulator controls flow rates via three solenoid valves and calibrated orifice disks to standardize flow rates across flumes.

## Data collection protocol
- Equilibration: samples equilibrate 30 minutes after prewetting.
- Sampling schedule:
  - Each run lasts 10 minutes with runoff samples collected every 1.5 minutes (6 samples per run).
  - Bottles used: 500 mL for low and moderate flows; 1 L for high flow.
  - Initial samples for delayed runoff are collected more quickly to synchronize with other flumes.
- Run sequence:
  - Run 1: flows in a defined sequence (with randomization between runs)
  - Run 2: different sequence
  - Run 3: again randomized sequence
- Pre-run preparation:
  - Ash depth application at 1 cm and 3 cm.
  - Flow sequences are permuted to ensure random distribution of flow rates among flumes.

## Sample processing and calculations
- Sample processing (drying and weighing):
  - Use 500 mL and 1 L beakers to dry and determine runoff volume and ash content.
  - Steps include taring beakers, transferring samples, rinsing bottles, drying at 110°C for 24 hours, and final weighing.
- Calculations:
  - Ash content (g) = WB3 − WB1 (dry mass difference).
  - Runoff volume (L) = (WB2 − WB3) / 1000.
- Derived metrics:
  - Ash transport rate (g/sec) and ash concentration (g/L) are collected as features, enabling assessment of how ash moves under different flow conditions and depths.

## Data governance, quality and accessibility considerations
- Data provenance:
  - Clear authorship, institutional affiliation, and date for reproducibility.
  - Detailed experimental design, including dimensions, slope, substratum, ash depths, and flow-rate configurations.
- Metadata and standardization:
  - Comprehensive metadata present in the data file (units, definitions, and replication structure), facilitating use across monitoring and policy contexts.
  - Potential governance actions for monitoring frameworks:
    - Ensure metadata completeness and consistency across related datasets.
    - Promote open access to underlying data and protocols to support transparency and replication.
    - Maintain alignment between data collection methods and data management standards (quality assurance, cleaning, transformation, and documentation).
    - Mitigate barriers such as data silos and ensure timely sharing of datasets and protocols for reuse in policy evaluation and future decision-making.