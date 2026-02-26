# ash_transport_experiment.csv

## Overview
- Purpose: Experimental data to obtain ash transport rates by runoff after wildfires, using laboratory flume experiments.
- Location and time: Rocky Mountain Research Station Laboratory, US Forest Service, Moscow, ID, USA; August 2019.
- Contributors: Dr Jonay Neris Tome, Dr Pete Robichaud, Dr Carmen Sánchez-García, Dr Cristina Santín and Prof. Stefan Doerr.
- Completeness: Full record.
- Data role: Provides ash depth, flow rate, runoff rate, ash transport rate, and ash concentration to assess environmental transport processes and support monitoring over time.

## Data and Measurements
- Features captured: 
  - Ash depth (cm)
  - Flow rate (L/min)
  - Runoff rate (L/sec)
  - Ash transport rate (g/sec)
  - Ash concentration (g/L)
- Observations: 1296 data points.
- Treatments: Two ash depths (1 cm and 3 cm) and three flow rates (0.25, 1, and 2 L/min).

## Experimental Design and Treatments
- Setup: 3 m long x 0.15 m wide flumes with a 17° slope; artificial substratum to mimic soil roughness.
- Prewatering: Prewetting with rainfall to precondition ash; rainfall intensity and duration determined by time to runoff.
- Flow regime: Three flow rates applied in sequence per run (F1 = 0.25 L/min, F2 = 1 L/min, F3 = 2 L/min).
- Runs and replication:
  - Each replication includes 3 runs, each run 10 minutes of flow.
  - Between runs: 1-minute delay.
  - Per run: two flumes receive each flow rate; distribution of flows across flumes varied to cover all permutations.
  - Replication: 6 replicates per combination (ash depth × flow rate combination), with six replicates per flow-rate combination.
- Automation: Automatic flow regulator with 3 solenoid valves, 3 input pipes, and 6 exits per pipe to supply each of 6 flumes; flow rates controlled by calibrated orifice disks (Teejet numbers 24, 47, 70) at 30 psi.

## Sampling Protocol
- Equilibration: 30 minutes after prewetting.
- Run structure: Start run 1; repeat for runs 2 and 3.
- Runoff sampling: Collect runoff at flume outlets; 6 samples per flume per run.
- Sample volumes: 500 ml bottles for low/moderate flows; 1 L bottles for high flow.
- Sampling cadence: Every 1.5 minutes for 15–20 seconds per sample; adjust intervals for delayed runoff to synchronize with other flumes.
  
## Sample Processing and Calculations
- Processing: Dry and weigh runoff contents to determine volume and ash content.
- Step sequence:
  - Weigh empty beaker (WB1)
  - Combine bottle contents into beaker, rinse bottle with sample water into beaker
  - Weigh beaker with wet ash (WB2)
  - Rinse remaining ash into beaker if needed
  - Dry beakers at 110°C for 24 hours and cool
  - Weigh beaker with dry ash (WB3)
- Calculations:
  - Ash content (g) = WB3 − WB1
  - Runoff volume (L) = (WB2 − WB3) / 1000

## Data Management and Access
- Data handling: Standardized collection, processing, and calculation steps to ensure consistency.
- Data storage: Datasets stored and uploaded to appropriate data portals or repositories.

## Relevance for Environmental Monitoring
- The dataset provides controlled measurements of ash transport under varying ash depths and runoff rates, enabling analysis of transport dynamics after wildfires.
- Structured design facilitates integration with other hydrological or post-fire datasets to enhance monitoring and policy evaluation over time.