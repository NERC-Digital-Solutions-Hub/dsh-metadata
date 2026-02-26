# ReadMe file for AutumnSoilWFPS_pH_EC.csv

## Overview
- Dataset provides soil % water-filled pore space (WFPS), pH, and electrical conductivity (EC) measured under three treatments applied to a humic gleysol in Snowdonia National Park, Wales, UK.
- Treatments: Control (no urine), Artificial sheep urine (art Urine) applied in discrete patches, and Nitrate + glucose (CandN) treatment.
- Sampling occurred on unimproved grazing land near greenhouse gas sampling chambers; sheep were excluded from 15/05/17 to avoid confounding excreta effects.
- Sampling location details: Carneddau mountains, Snowdonia National Park, at ~556 m altitude; coordinates provided in the ReadMe.
- Data headers include Date, Days after treatment, Treatment, Plot, WFPS, pH, and EC (units specified below).
- Authors must be acknowledged if data are reused or reproduced.

## Experimental design
- Treatments (n = 4 replicates):
  - Control: no urine application.
  - Artificial sheep urine: applied in triplicate discrete patches (each patch with 1120 kg N ha-1; 200 ml artificial urine over 100 cm2 soil surface per patch).
  - C and N: nitrate and glucose treatment applied at 106 kg N ha-1 and 213 kg C ha-1; 1 L solution applied across a 40 × 40 cm area adjacent to the chamber.
- Treatment application dates:
  - Art Urine: patches applied (date not explicitly stated in the ReadMe snippet for urine patches).
  - CandN: applied on 25/10/17 (dd/mm/yy).
- Sampling approach: soils were sampled from replicated areas adjacent to the greenhouse gas sampling chambers using an auger and processed within 24 hours of collection.
- Replication: there are four treatment replicates (n = 4) across plots (exact plot structure implied by the data file).

## Measurements and variables
- WFPS: percent soil water-filled pore space (calculated as volumetric water content divided by soil porosity).
- pH: soil pH measured from 1:2.5 soil-to-distilled water suspensions using standard electrodes.
- EC: soil electrical conductivity measured from 1:2.5 soil-to-distilled water suspensions; unit is µS cm-1.
- Date: date of soil sampling (format dd/mm/yyyy).
- Days: days after treatment application.
- Treatment: one of Control, ArtUrine (Artificial sheep urine), CandN (Nitrate and glucose).
- Plot: identifier for the plot from which samples were taken.
- Porosity calculation: assumed particle densities of 2.65 g cm-3 (minerals) and 1.4 g cm-3 (organic fraction), per Rowell (1994).

## Data structure and metadata
- Data headers: Date, Days, Treatment, Plot, WFPS, pH, EC.
- WFPS expressed as a percentage; EC expressed in microSiemens per centimeter (µS cm-1).
- Location and environmental context described to support data interpretation and reproducibility.
- Reference for calculation method and methods: Rowell, D.L., 1994. Soil Science: Methods and Applications.

## Usage notes and potential data products
- Potential data products:
  - Time-series dashboards showing WFPS, pH, and EC by treatment and plot over days after treatment.
  - Comparative analyses of WFPS response to urine vs. nitrate+glucose vs. control.
  - Integration with greenhouse gas measurements from the same plots for holistic soil–gas studies.
  - QA/QA workflow to ensure date formats, treatment labels, and plot identifiers are consistent across datasets.
- Data preparation considerations:
  - Ensure consistent date parsing and calculation of Days after treatment.
  - Verify porosity assumptions if combining with other soil properties.
  - Acknowledge data authors when reusing; follow any required citation.

## References
- Rowell, D.L., 1994. Soil Science: Methods and Applications. Longman Group UK Ltd.

## Cautions
- The ReadMe notes a potential discrepancy: Treatments described as (n = 4) but only three treatment categories are listed. When merging datasets, confirm replication structure and plot-level details from the accompanying data file to avoid misinterpretation.