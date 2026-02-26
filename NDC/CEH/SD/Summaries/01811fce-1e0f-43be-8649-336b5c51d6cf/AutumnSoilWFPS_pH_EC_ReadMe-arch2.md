# ReadMe file for AutumnSoilWFPS_pH_EC.csv

## Overview
- Dataset on soil water-filled pore space (WFPS, %), pH, and electrical conductivity (EC) from controlled experimental plots.
- Treatments: Control (no urine), Artificial sheep urine, and Nitrate + glucose (C and N) applied to a humic gleysol in unimproved grazing land.
- Location: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Timeframe: Treatments applied in 2017; sheep excluded from 15/05/17 to avoid confounding effects; samples collected and processed within 24 hours.

## Location and Experimental Context
- Environment: Unimproved grazing land, humic gleysol.
- Plot and sampling: Replicated areas adjacent to greenhouse gas sampling chambers within each plot; soil sampled with an auger.
- Exclusion: Sheep excluded to prevent excretal confounding effects.

## Treatments and Experimental Design
- Treatment groups (n = 4 each):
  - Control: No urine application.
  - ArtUrine: Artificial sheep urine applied in triplicate discrete patches; each patch delivers 1120 kg N ha-1 (200 ml urine per 100 cm2 patch).
  - CandN: Nitrate + glucose treatment; 106 kg N ha-1 and 213 kg C ha-1; 1 L solution applied over a 40 × 40 cm square adjacent to the chamber.
- Application dates:
  - ArtUrine patches prepared/implemented prior to sampling (date not specified beyond overall study timeframe).
  - CandN applied on 25/10/17 (dd/mm/yy).

## Data Collection and Processing
- Sampling method: Soil samples collected from replicated areas near chambers using an auger; processed within 24 hours of collection.
- Parameters measured:
  - WFPS: Calculated as volumetric water content divided by soil porosity.
  - pH and EC: Determined in 1:2.5 soil-to-distilled water suspensions using standard electrodes.

## Computation of Soil Porosity and Measurements
- Porosity calculation: Assumes particle densities of 2.65 g cm-3 for mineral fraction and 1.4 g cm-3 for organic fraction (Rowell, 1994).
- WFPS calculation: WFPS (%) = (volumetric water content) / (porosity) × 100.

## Data Structure and Headers
- Date: Date of soil sample collection (dd/mm/yyyy).
- Days: Days after treatment application.
- Treatment: Categorical (Control, ArtUrine, CandN; abbreviated as ArtUrine and CandN in dataset).
- Plot: Plot identifier.
- WFPS: Soil water-filled pore space (%).
- pH: Soil pH.
- EC: Soil electrical conductivity (µS cm-1).

## References
- Rowell, D.L., 1994. Soil Science: Methods and Applications. Longman Group UK Ltd., London, UK.

## Usage Notes
- Authors must be acknowledged if data are re-used or reproduced.