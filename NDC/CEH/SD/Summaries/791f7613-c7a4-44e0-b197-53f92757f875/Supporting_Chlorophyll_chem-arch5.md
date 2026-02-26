# BLEL_Chlorophyll_chem.csv

## Overview
- Supporting information for the dataset BLEL_Chlorophyll_chem.csv.
- Collected by Emma Gray for the project NEC05744.
- Purpose: chemical analysis of chlorophyll a as an indicator of phytoplankton biomass.
- Location: Blelham Tarn, Lake District, NW England; monitoring buoy at the lake’s deepest point (14.5 m).
- Timeframe: sampling conducted in 2016 and 2017.
- Sampling details: water samples (lake: 500 mL; streams: 1000 mL) collected at metre intervals from 1 m to 10 m in 2016, and 0.5 m then 1 m to 9 m in 2017 (lake only), plus samples from three inflows and the outflow.
- Sample processing: samples filtered immediately after collection through GF/C filter paper, filter papers frozen, and analyses performed within a month using the method described by Talling (1974).
- Measurement: chlorophyll a extracted with methanol and quantified with a spectrophotometer.
- Wavelengths: 750 nm for background turbidity (A750) and 665 nm for chlorophyll a absorbance (A665).
- Calculation: Chlorophyll a concentration = (13.9 × A_corr665 × 1/d) × (v/V), where A_corr665 = A665 − A750; d is cuvette path-length (cm); V is filtered sample volume (mL); v is extract volume (mL); 13.9 approximates the reciprocal of the specific absorption coefficient at 665 nm for this solvent.
- Data structure: Date (dd/mm/yyyy), Depth (m) ranging from -1 (surface) to -10 (deepest measurement), Chlorophyll a (µg/L).

## Sampling and Analysis Protocol
- Filter: 5.5 cm GF/C filter paper; samples filtered and filter papers frozen.
- Analysis window: analyses conducted within one month of collection.
- Extraction: methanol extraction of chlorophyll a.
- Spectrophotometry: absorbance measured at 750 nm (A750) and 665 nm (A665) for background correction and chlorophyll signal, respectively.

## Data Structure and Fields
- Date: format dd/mm/yyyy.
- Depth: vertical sampling depth in meters, encoded as negative values from -1 to -10 (with -1 being the topmost measurement).
- Chlorophyll a: concentration in micrograms per liter (µg/L).

## Location and Context
- Study site: Blelham Tarn, with the monitoring buoy at the deepest point in the lake.
- Figure referenced for bathymetric context.
- References for methods and depth context: Ramsbottom (1976) depth charts and Talling (1974) pigment measurement procedures.

## References
- Ramsbottom, A. (1976). Depth charts of the Cumbrian lakes. Freshwater Biological Association.
- Talling, J.F. (1974). Photosynthetic pigments. In: Methods for Measuring Primary Productivity in Aquatic Environments.

## Data Governance Considerations for Data Stewards
- Metadata completeness: ensure date format, depth units, and chlorophyll units are consistent across records.
- Method provenance: document extraction, filtration, freezing, and analysis steps with citation to Talling (1974) and Ramsbottom (1976) for reproducibility.
- Units and calculations: preserve the explicit calculation formula and parameter meanings (A665, A750, d, V, v) to enable replication.
- Data provenance: clearly associate data with the collector (Emma Gray) and project NEC05744.
- Accessibility and discoverability: ensure the dataset includes location context (lake vs. inflows/outflow), depth interval details, and sampling years for proper filtering.
- Quality assurance: note potential variability due to different sample volumes (lake vs. streams) and sampling intervals between years; validate consistency of depth indexing and data entries.

## Quality and Limitations
- Temporal and depth sampling varied between 2016 and 2017 (depth interval adjustments in 2017).
- Different water volumes used for lake vs. streams may affect comparability; ensure portal metadata captures this distinction.
- The description is sufficient for reproducibility but may require access to the original figure (Figure 1) and cited references for full methodological replication.