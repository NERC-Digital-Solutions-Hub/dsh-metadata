# Data file: ash_transport_experiment.csv

## Overview
- Location and date: Rocky Mountain Research Station Laboratory, US Forest Service, Moscow, ID, USA; August 2019.
- Purpose: Obtain ash transport rates with runoff after wildfires using controlled laboratory flume experiments.
- Method: Laboratory experiments with flumes under controlled ash depths and flow rates.
- Data completeness: Full record.
- Observations: 1296 data points.
- Key data features: ash depth (cm), flow rate (L/min), runoff rate (L/sec), ash transport rate (g/sec), ash concentration (g/L).
- Team/contacts: Dr Jonay Neris Tome, Dr Pete Robichaud, Dr Carmen Sánchez-García, Dr Cristina Santín, Prof. Stefan Doerr.
- Context: Data intended to support understanding of ash transport by overland runoff following wildfires.

## Data structure and metadata
- Experimental factors:
  - Ash depths: 1 cm and 3 cm.
  - Flow rates: 0.25 L/min (F1), 1 L/min (F2), 2 L/min (F3).
- Experimental design:
  - Substratum: artificial substrate to simulate soil roughness.
  - Plot/experimental setup: flume dimensions 3 m long x 0.15 m wide; slope 17°.
  - Prewetting: ash prewet with rainfall equivalent (85 mm/h) to initiate runoff.
- Replication and runs:
  - Replicates: 2 ash depths x multiple flow-rate combinations per depth with replication (specifics: 6 flow-rate combinations per ash depth; 6 replicates per combination; 3 flow rates per combination; 6 samples per flow rate).
  - Runs per replication: 3 runs per replication; each run lasts 10 minutes with a 1-minute delay between runs.
  - Flume distribution: each run includes two flumes per flow rate; flow-rate distribution across flumes varied per run to ensure randomization.
- Observations per run:
  - 6 runoff samples collected per flume per run.
  - Sample collection volumes: 500 mL bottles for low/moderate flows; 1 L bottles for high flow.
- Data attributes:
  - Run protocol and timing (sampling every ~1.5 minutes for 15–20 seconds per sample).
  - Sample processing and calculation steps define how ash content and runoff volume are derived.

## Experimental design details
- Physical layout:
  - Plot size: 3 m long x 0.15 m wide.
  - Slope: 17 degrees.
- Treatments:
  - Ash depths: 1 cm and 3 cm.
  - Runoff conditions: three flow rates (0.25, 1, 2 L/min).
- Replication and sampling plan:
  - Two ash depths with six flow-rate distributions per depth.
  - Six replicates per flow-rate distribution.
  - Three flow-rate levels applied per distribution.
  - Six samples (bottles) collected per flow rate per distribution.

## Automatic flow regulation
- Automated system with three solenoid valves tied to a main water supply.
- Each flume receives water from one of three pipes (one entry per pipe per flume), with flow rates controlled by calibrated orifice disks (TeeJet disks 24, 47, 70) at 30 psi.
- Objective: precise, repeatable delivery of F1, F2, F3 flow rates across flumes.

## Protocol and sampling procedure
- Pre-run equilibration: 30 minutes after prewetting.
- Run sequence: start Run 1, collect runoff samples from flume outlets.
- Sampling specifics:
  - Six runoff samples per flume per run.
  - Bottle sizing: 500 mL for low/moderate flows; 1 L for high flow.
  - Sampling cadence: every 1.5 minutes for 15–20 seconds ( adjusts for delayed runoff if necessary).
- Repetition:
  - Steps repeated for Run 2 and Run 3.
  - Steps repeated for each replication.

## Sample processing
- Drying and weighing:
  - Use 500 mL and 1 L beakers to dry runoff samples and determine volumes and ash content.
  - Weigh empty beaker (WB1), then weigh beaker with sample after transfer and rinsing (WB2), then weigh after drying ash (WB3).
- Processing steps:
  - Combine sample and rinse water into the beaker; rinse bottles to recover all ash.
  - Dry at 110°C for 24 hours; cool and reweigh to determine dry ash mass.

## Calculations
- Ash content (g): WB3 − WB1.
- Runoff volume (L): (WB2 − WB3) / 1000.
- The dataset uses these computations to derive ash transport metrics for each observation.