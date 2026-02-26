# Data file: ash_transport_experiment.csv

## Overview
- Source: Rocky Mountain Research Station Laboratory, US Forest Service, Moscow, ID, USA
- When: August 2019
- Why: Obtain ash transport rates with runoff after wildfires
- Who: Dr Jonay Neris Tome, Dr Pete Robichaud, Dr Carmen Sánchez-García, Dr Cristina Santín, Prof. Stefan Doerr
- Completeness: Full record
- Methodology: Experimental flume setup with controlled ash depths and flow rates (see below)

## Data details
- Observations: 1296
- Features (variables):
  - ash depth (cm)
  - flow rate (L/min)
  - runoff rate (L/sec)
  - ash transport rate (g/sec)
  - ash concentration (g/L)
- Treatments:
  - ash depths: 1 cm and 3 cm
  - flow rates: 0.25, 1, 2 L/min
- Replication structure:
  - 2 ash depths
  - 6 flow-rate combinations per ash depth
  - 6 replicates per combination
  - 3 flow-rate runs per replicate
  - 6 samples (bottles) per flow rate
- Periodicity: Not applicable (NA)

## Experimental design
- Plot/substratum: 3 m long x 0.15 m wide plot; artificial substratum to simulate soil roughness
- Slope: 17 degrees
- Ash application: two depths (1 cm and 3 cm)
- Flow rates (F1, F2, F3): 0.25, 1, 2 L/min
- Replicates/runs: Each replicate has 3 runs; each run lasts 10 minutes with a 1-minute delay between runs
- Flow-rate distribution: Each run involves all three flow rates distributed across two flumes per flow rate; order randomized per run and per replication
- Randomization: Flume positions rearranged before each replication

## Automatic flow control
- System: 3 solenoid valves, controlled by a datalogger
- Piping: 1 m PVC pipe per valve with 6 exits to 6 flumes
- Flow-rate control: Orifice disks calibrated for 0.25, 1, 2 L/min (TeeJet disks 24, 47, 70) at ~30 psi

## Protocol (data collection)
- Equilibration: 30 minutes after prewetting
- Run procedure: Start run 1, collect runoff samples from flume outlets
- Sampling per flume/run: 6 runoff samples
  - Bottle sizes: 500 mL (low/moderate flow) and 1 L (high flow)
  - Sampling timing: As soon as runoff reaches outlet; every 1.5 minutes for 15–20 seconds (6 samples total)
  - Delays: Shorter initial intervals for flumes with delayed runoff to catch up
- Repetition: Steps repeated for runs 2 and 3; steps repeated for each replication

## Sample processing
- Containers: 500 mL and 1 L beakers
- Steps:
  - Weigh empty beaker (WB1)
  - Combine bottle contents into beaker; rinse bottle to recover ash
  - Weigh beaker with contents (WB2)
  - Rinse remaining ash into beaker with deionized water if needed
  - Dry beakers at 110°C for 24 h; cool
  - Weigh dry ash (WB3)

## Calculations
- Ash content (g) = WB3 − WB1
- Runoff volume (L) = (WB2 − WB3) / 1000

## Data use and takeaways
- Enables analysis of relationships between ash depth, flow rate, and ash transport rate/concentration
- Supports creation of dashboards or reports for self-serve data exploration
- Can be integrated with other wildfire runoff datasets for broader comparative analyses
- Documented methodology and replication structure support reproducibility and quality assessment

## Data quality considerations
- Full record availability; detailed metadata on experimental conditions
- Complex, multi-step sampling and processing; careful unit consistency needed during integration
- Randomized flow-rate distribution aids in reducing systematic bias across flumes and runs