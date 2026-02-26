# ReadMe file for AutumnCO2Flux.csv

## Overview
- Quality-assessed CO2/CH4 flux data from soil under three treatments (Control, Artificial sheep urine, Nitrate + glucose) in unimproved grazing land.
- Location: humic gleysol soil, Carneddau mountains, Snowdonia National Park, Wales, UK.
- Data capture focuses on high-frequency flux measurements; not raw gas concentration data.
- Authors must be acknowledged if data are re-used or reproduced.

## Experimental design and site
- Site: unimproved grazing land in the Carneddau mountains, Snowdonia NP, Wales; altitude 556 m a.s.l.; coordinates 53°22'N, 3°95'W.
- Sheep excluded from 15/05/17 to avoid recent excretal confounding.
- Experimental design: randomized block with four replicates per treatment (n = 4 per treatment).
- Treatment application date: 25/10/17.

## Treatments
- Control: no urine application.
- ArtUrine (Artificial sheep urine): applied in triplicate discrete patches inside the chamber; each patch ~200 ml artificial urine over 100 cm2 soil surface; total N application rate per patch equivalent to 1120 kg N ha-1.
- CandN (Nitrate and glucose): 106 kg N ha-1 and 213 kg C ha-1; 1 L solution applied across a 40 × 40 cm square inside the chamber.

## Data collection and instruments
- Monitoring system: automated greenhouse gas monitoring system using LI-COR LI-820.
- Frequency: eight flux measurements per chamber per day; 1 h chamber closure per measurement; four gas samples analyzed per 1 h closure period.
- Calibration: standard analyzed after every fourth gas sample.
- Chamber details: basal area 0.25 m2; chambers 50 cm × 50 cm × 15 cm (L × W × H).
- Monitoring duration: 45 days post-treatment.
- Data type: emissions data from the high-frequency period; not raw gas concentrations.

## Data content and structure
- Data represent quality-assessed flux data (not raw concentrations).
- Data headers:
  - Timestamp: dd/mm/yy hh:mm
  - Days: time in days pre- or post-treatment
  - Columns B–M: CH4 fluxes (units: mg CO2-C m-2 h-1)
  - Column headers encode treatment and chamber/plot numbers (Control, ArtUrine, CandN)

## Quality assurance
- Procedures: inspection of raw data files and GC chromatograms for anomalies; removal of data with anomalies (e.g., gas-peak interference).
- Only data that passed quality checks are included in the provided dataset.

## Metadata and reuse
- Provisions: authors must be acknowledged if the data are reused or reproduced.
- Location, treatments, and time frame clearly documented to enable re-use and integration with related datasets.

## Notes for data users
- Be aware that CH4 flux values are presented as mg CO2-C m-2 h-1 (likely a CO2-C equivalent representation of CH4 flux).
- High-frequency data provide detailed flux patterns post-treatment; consider aggregation or alignment to the treatment timeline for analyses.
- If combining with other datasets, maintain consistency in units, treatment labels, and chamber identifiers.