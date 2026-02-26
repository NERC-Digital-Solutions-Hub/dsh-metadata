# ReadMe file for SummerSoilWFPS_pH_EC.csv

## Overview
- Dataset of soil measurements focusing on water-filled pore space (WFPS), pH, and electrical conductivity (EC).
- Treatments: control (no urine), artificial sheep urine, and real sheep urine applied as discrete patches.
- Location: unimproved grazing land on a dystric histosol in the Carneddau mountains, Snowdonia National Park, Wales, UK.
- Purpose aligned with environmental monitoring: provides standardized data to assess soil health responses to urine inputs over time.

## Study site and experimental setup
- Elevation: 556 m above sea level.
- Coordinates: 53°22'N, 3°95'W.
- Soil: dystric histosol (peaty soil under unimproved grazing land).
- Management: sheep excluded from plots from 15/05/2017 to avoid recent excretal effects.
- Plot arrangement: replicated areas adjacent to greenhouse gas sampling chambers in each experimental plot.
- Treatments (n = 4 plots per treatment; real urine treatment n = 3 plots): 
  - Control: no urine application.
  - Artificial sheep urine: patches with 920 kg N ha-1 equivalent per patch.
  - Real sheep urine: patches with 930 kg N ha-1 equivalent per patch.
- Urine patches applied on 24/07/2017.

## Treatments and sampling timeline
- Sampling date reference: dates after treatment application captured in the dataset (Date and Days columns).
- Patch design: discrete patches within plots; 200 ml per patch over 100 cm2 soil surface area per patch.

## Data collected and headers
- Core variables measured: WFPS (%), soil pH, and soil EC (µS cm-1).
- Data columns:
  - Date: date of soil sample collection (dd/mm/yyyy).
  - Days: days after treatment application.
  - Treatment: "Control", "ArtUrine" (artificial urine), or "RealUrine" (real urine).
  - Plot: plot identifier.
  - WFPS: soil water-filled pore space (%).
  - pH: soil pH value.
  - EC: soil electrical conductivity (µS cm-1).

## Methods and calculations
- WFPS calculation: ratio of volumetric water content to soil porosity.
- Porosity: calculated assuming mineral density 2.65 g cm-3 and organic density 1.4 g cm-3 (per Rowell, 1994).
- pH and EC measurement: performed in 1:2.5 soil-to-distilled water suspensions using standard electrodes.
- Processing: soil samples collected via auger and processed within 24 hours of collection.

## Data handling and provenance
- Sample collection: directly adjacent to greenhouse gas sampling chambers; intended to capture immediate soil responses to urine patches.
- Data handling: standard laboratory processing within 24 hours; metadata includes treatment, plot, date, and days-after-treatment.

## Metadata, usage notes, and references
- Acknowledgement: authors must be acknowledged if data are re-used or reproduced.
- Site and methodological reference: Rowell, D.L., 1994. Soil Science: Methods and Applications.
- Reuse considerations for analysts (aligned with monitoring aims):
  - Data structured in a consistent format suitable for time-series analysis of environmental health and policy performance.
  - Opportunities to combine with other datasets to enhance the value of monitoring outputs.
  - Encouraged to provide access to underlying data and upload datasets to appropriate data portals for transparency and long-term stewardship.