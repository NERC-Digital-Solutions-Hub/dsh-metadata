# ReadMe file for AutumnSoilWFPS_pH_EC.csv

## Overview
- Describes soil measurements of water-filled pore space (WFPS), pH, and electrical conductivity (EC) from an environmental study in Wales, UK.
- Experimental plots used control, artificial sheep urine, and nitrate+glucose treatments on a humic gleysol within unimproved grazing land in Snowdonia National Park.
- Sheep were excluded to avoid recent excretal effects; samples processed within 24 hours of collection.

## Location and experimental context
- Site: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Elevation: 556 m above sea level; coordinates provided as 53°22'N, 3°95'W.
- Soil type: humic gleysol.
- Plot setup: replicated areas adjacent to greenhouse gas sampling chambers in each experimental plot.

## Treatments and application details
- Control: no urine application.
- Artificial sheep urine (ArtUrine): applied in triplicate discrete patches per plot; each patch has 1120 kg N ha-1 equivalent; 200 ml of artificial urine per 100 cm2 soil surface area per patch.
- Nitrate + glucose (CandN): applied as 106 kg N ha-1 and 213 kg C ha-1; 1 L of nitrate+glucose solution spread across a 40 × 40 cm square adjacent to the chamber.
- Timing: treatments applied on 25/10/17.

## Sampling, processing, and measurements
- Sampling method: soil samples collected using an auger from replicated areas near the chambers; processed within 24 hours of collection.
- WFPS calculation: ratio of volumetric water content to soil porosity.
- Porosity calculation: based on particle densities of 2.65 g cm-3 (mineral) and 1.4 g cm-3 (organic) as per Rowell 1994.
- pH and EC measurements: conducted in 1:2.5 soil-to-distilled water suspensions using standard electrodes.
- Sheep management: sheep excluded from 15/05/17 to minimize confounding excretal inputs.

## Data structure and variables
- Data headers:
  - Date: date of soil sampling (dd/mm/yyyy)
  - Days: days after treatment application
  - Treatment: which treatment plot received (Control, ArtUrine, CandN)
  - Plot: plot identifier
  - WFPS: soil water-filled pore space (%)
  - pH: soil pH
  - EC: soil electrical conductivity (µS cm-1)
- Treatment codes: ArtUrine = artificial sheep urine; CandN = nitrate and glucose treatment.

## Data provenance, quality, and governance
- Data processing and measurements described as performed within 24 hours of sampling.
- Metadata provided for interpretation and verification (location, soil type, treatment details, and calculation methods).
- Acknowledgement requirement: authors must be acknowledged if data are reused or reproduced.
- References: Rowell, D.L. 1994. Soil Science: Methods and Applications (methods for porosity, general soil analysis referenced).