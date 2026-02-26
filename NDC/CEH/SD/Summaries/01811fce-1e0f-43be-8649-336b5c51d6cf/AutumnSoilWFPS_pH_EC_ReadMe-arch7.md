# ReadMe file for AutumnSoilWFPS_pH_EC.csv

## Overview
- Dataset of soil properties: water-filled pore space (WFPS), pH, and electrical conductivity (EC).
- Treatments: control (no urine), artificial sheep urine, and nitrate plus glucose (C and N) applied to plots in unimproved grazing land.
- Location: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m above sea level; 53°22'N, 3°95'W).
- Sampling context: plots fenced to exclude sheep from 15/05/2017; samples collected adjacent to greenhouse gas sampling chambers using an auger and processed within 24 hours.

## Location and sampling context
- Terrain: unimproved grazing land in Snowdonia National Park.
- Plot/ref: sampling taken from replicated areas adjacent to each experimental chamber.
- Elevation and coordinates: 556 m a.s.l.; 53°22'N, 3°95'W.

## Experimental design and treatments
- Treatments (n = 4): 
  - Control: no urine application.
  - Artificial sheep urine: applied in triplicate discrete patches; each patch ≈1120 kg N ha-1, 200 ml artificial urine over 100 cm2 per patch.
  - C and N (Nitrate and glucose): 106 kg N ha-1 and 213 kg C ha-1; 1 L solution applied across a 40 × 40 cm square adjacent to the chamber.
- Application timing: 25/10/2017 (dd/mm/yy).
- Sheep exclusion: from 15/05/2017 to minimize confounding effects.

## Measurements and lab methods
- WFPS calculation: ratio of volumetric water content to soil porosity; porosity computed using particle densities 2.65 g/cm3 (mineral) and 1.4 g/cm3 (organic) per Rowell (1994).
- pH and EC measurements: performed in 1:2.5 soil-to-distilled water suspensions using standard electrodes.

## Data structure and headers
- Date: date of soil sample collection (dd/mm/yyyy).
- Days: days after treatment application.
- Treatment: treatment type per plot ('Control', 'ArtUrine', 'CandN').
- Plot: plot identifier.
- WFPS: percent soil water-filled pore space.
- pH: soil pH value.
- EC: soil electrical conductivity (µS cm-1).

## Temporal and sampling details
- Sampling occurred after treatments were applied, with data including the “Days” since application to capture temporal changes in soil moisture and chemistry.
- Treatments include both patch-based urine applications and a broader nitrate+glucose treatment, reflecting spatially varied input patterns.

## Data provenance and usage notes
- Authors must be acknowledged if data are reused or reproduced.
- Data suitable for GIS-based visualization of spatial and temporal variation in soil moisture, pH, and EC.
- Encourages integration with other spatial datasets for landscape-scale interpretation.
- Data processing and methods documented to enable reproducibility and cross-study comparisons.

## References
- Rowell, D.L., 1994. Soil Science: Methods and Applications. Longman Group UK Ltd., London, UK.