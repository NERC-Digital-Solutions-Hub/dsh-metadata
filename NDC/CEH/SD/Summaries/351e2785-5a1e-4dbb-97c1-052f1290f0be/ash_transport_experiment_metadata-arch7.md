# ash_transport_experiment.csv

## Overview
- Source: Rocky Mountain Research Station Laboratory, US Forest Service, Moscow, ID, USA.
- When: August 2019.
- Purpose: Obtain ash transport rates with runoff after wildfires using laboratory flume experiments.
- Data completeness: Full record with 1296 observations.
- Key variables (map-ready features): ash depth (cm), flow rate (L/min), runoff rate (L/sec), ash transport rate (g/sec), ash concentration (g/L).
- Data contributors: Dr Jonay Neris Tome, Dr Pete Robichaud, Dr Carmen Sánchez-García, Dr Cristina Santín and Prof. Stefan Doerr.

## Experimental design and data structure
- Plot/substrate: 3 m long × 0.15 m wide flumes on an artificial substratum to mimic soil roughness.
- Slope: 17 degrees.
- Treatments: two ash depths (1 cm and 3 cm).
- Replication: 6 replicates per treatment; each replicate includes multiple flow-rate runs.
- Flow-rate treatments: three target flow rates—F1 = 0.25 L/min, F2 = 1 L/min, F3 = 2 L/min (applied in sequence).
- Randomization: flume positions randomized before each replication to distribute flow-rate effects.
- Experimental runs: each replication consists of 3 runs; each run lasts 10 minutes of flow with 1 minute between runs.
- Flume distribution per run: two flumes receive each flow rate per run; the order of flow-rate delivery varies across runs to cover all distributions.
- Replication details: two ash depths × six flow-rate combinations per depth × six replicates per combination × three flow rates per combination = 1296 observations total.

## Data collection and flow-control setup
- Automatic flow regulator: three solenoid valves, three pipes with six exits, each flume receiving one entry per pipe; flow rates set via calibrated orifice disks (TeeJet disks numbers 24, 47, 70) at ~30 psi.
- Run initiation and sampling: samples collected after equilibration, starting when runoff reaches each flume outlet.
- Sample sizes: 500 mL bottles for low/moderate flows; 1 L bottles for high flow.
- Sampling cadence: six runoff samples per flume per run, collected every ~1.5 minutes over 15–20 seconds.

## Protocol and procedures
- Prewetting: rainfall applied to prewet ash; intensity 85 mm/h; duration/depth determined by time to runoff.
- Equilibration: 30 minutes after prewetting before starting runs.
- Run sequencing: three runs per replication; explicit timing and ordering per run, with randomization of flume positions between replications.
- Delayed runoff handling: sampling intervals adjusted for flumes with delayed runoff to synchronize data capture.

## Sample processing and calculations
- Processing steps: drying, weighing, and ash-content calculations for each bottle.
- Beaker workflow:
  - Weigh empty beaker (WB1).
  - Combine sample water and ash, rinse bottle, transfer to beaker.
  - Weigh with contents (WB2); rinse remaining ash into beaker if needed.
  - Dry at 110°C for 24 h; weigh dry ash (WB3).
- Calculations:
  - Ash content (g) = WB3 − WB1.
  - Runoff volume (L) = (WB2 − WB3) / 1000.
- Data interpretation: ash depth, ash concentration, and transport rates derived from sample weights and flow conditions.

## Data quality, scope, and limitations
- Completeness: explicitly labeled as full record.
- Scale and applicability: laboratory flume setup with artificial substratum; results are most applicable to controlled, small-scale conditions and may require careful up-scaling for field contexts.
- Data integration: multiple data components (flow control, sampling, processing, calculations) require careful cleaning and unit normalization for GIS mapping.
- Standards: detailed procedural notes aid reproducibility but highlight potential variability across runs and flumes.

## GIS relevance and how to use in map-based analyses
- Potential map-ready layers:
  - Spatially discretized ash depth (per flume) and ash transport rate (per flume) across runs.
  - Temporal dimension capturing changes across Run 1–Run 3 and replicates.
  - Flow-rate condition identifiers (F1, F2, F3) with associated ash metrics.
- Analytical opportunities:
  - Compare ash transport rates across ash depths and flow rates to model runoff-driven ash mobilization in a spatial context.
  - Assess interaction effects of ash depth and flow rate on transport rate via map-based visualization and spatial statistics.
  - Integrate with other GIS layers (e.g., slope, surface roughness proxies) to explore habitat- or watershed-scale transport implications.
- Practical considerations for GIS work:
  - Ensure unit consistency (e.g., ash depth in cm, flow in L/min, rates in g/s) when joining with spatial attributes.
  - Use flume identifiers and replication/run metadata as spatial-temporal keys to build multi-layer time series maps.
  - Be mindful of the lab-to-field scaling caveats when extrapolating map-based insights to real-world wildfire ash transport.