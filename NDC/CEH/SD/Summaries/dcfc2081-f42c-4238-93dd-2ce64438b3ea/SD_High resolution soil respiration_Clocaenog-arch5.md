# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf'

## Overview
- Dataset: 14 columns, 7729 rows
- Context: Clocaenog climate manipulation field experiment with plot-level treatments
  - Treatments mapped to plots: Control (plots 3, 6, 9), Warming (plots 1, 2, 7), Drought (plots 4, 5, 8)
- Measured variables: soil respiration, soil temperature, soil moisture, photosynthetic active radiation (PAR), and air temperature
- Temporal scope: 2013 and 2014 measurement campaigns (Cycle 1-9)
- Data provenance: measurements provided by a Licor instrument using internal software; includes a quality-control flag

## Data structure and key variables
- A (Plot): Factor; describes treatment assignment per plot (1-9); mapping:
  - Control: 3, 6, 9
  - Warming: 1, 2, 7
  - Drought: 4, 5, 8
- B (Climate treatment): Factor; treatment type (control, drought, warming)
- C (Timestamp): dd/mm/yyyy hh:mm; date and time of measurement
- D (Cycle): Factor; 1–9 measurement campaigns during 2013–2014
- E (Date): dd/mm/yyyy
- F (Hour): (not further described)
- G (Month): (not further described)
- H (Year): (not further described)
- I (Soil respiration): µmol CO2 m^-2 s^-1; measured by Licor software
- J (Soil temperature): °C; plot-based soil temperature at 0–5 cm
- K (Soil moisture): m^3 m^-3; plot-based soil moisture at 0–10 cm
- L (Photosynthetic active radiation): µmol photons m^-2 s^-1; one site-based measurement for all plots
- M (Air temperature): °C; plot-scale air temperature at the site
- N (QC flag): Factor; 1 = faulty values (do not use), 0 = values used

## Data collection and processing notes
- I (soil respiration) measurements are provided by Licor using its internal software
- L (PAR) is a single site-based measurement applicable to all plots
- C, E, F, G, and H provide date/time context; ensure consistent time alignment during analyses
- N QC flag indicates data usability; apply QC filtering to exclude flagged values

## Quality, governance, and usage guidance for Data Stewards
- Use the QC flag (N) to identify and filter out faulty measurements
- Maintain clarity on plot-to-treatment mapping (A and B) when aggregating by treatment
- Preserve units and metadata for reproducibility (I: µmol CO2 m^-2 s^-1; J: °C; K: m^3 m^-3; L: µmol photons m^-2 s^-1)
- Be mindful of potential redundancy in time fields (C: Timestamp; E/F/G/H provide date components)
- Document data provenance (Licor source, internal software) and link to the supplementary documentation for context
- Prepare for data ingestion into portals by aligning with standard metadata schemas and ensuring clear versioning and update logs

## Practical considerations for users
- When analyzing treatment effects, use the plot-to-treatment mapping in A and B
- Filter out flagged observations using N before any analyses or sharing
- Use the Cycle field (D) to stratify analyses by measurement campaigns across 2013–2014
- Confirm alignment of date/time fields (C, E, F, G, H) to ensure accurate temporal analyses
- Observe that PAR (L) is site-wide and may not vary by plot in this dataset

## Documentation and access
- This document is a supplement to the primary Clocaenog data series documentation
- Refer to the original supporting documentation for full context and data dictionary details