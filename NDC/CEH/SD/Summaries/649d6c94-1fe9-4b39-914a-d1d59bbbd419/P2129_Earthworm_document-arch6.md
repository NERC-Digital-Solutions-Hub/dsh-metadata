# Earthworm data from Sourhope field experiment site, Scotland, 1999 and 2001 [NERC Soil Biodiversity Programme]

## Aim and scope
- Documents earthworm data collected under the NERC Soil Biodiversity Thematic Programme (1999), focusing on soil biodiversity and ecological roles via an intensive field experiment.
- Part of a broader programme with 24 research projects studying soil structure, processes, and soil biota.

## Site description
- Location: Sourhope Research Station, southern uplands of Scotland; upland, base-poor damp mineral soils.
- Site features: 30 plots (20 m x 12 m) in five randomized blocks with six treatments.
- Treatments: Control (unlimed) vs Limed (CaCO3 6 t ha^-1 annually from 1999–2002).
- Management: Grassland with mowing and removal of cuttings; sheep grazing ceased in 1998.

## Earthworm census and methods
- Sampling: Intact soil blocks (42 cm x 30 cm x 25 cm) collected from five limed and five control plots in Sep 1999 and Sep 2002.
- Processing: Hand-sorting to extract earthworms (preferred to chemical methods due to plot contamination concerns); 24-hour moisture control; gut contents removed; specimens dried and weighed.
- Identification: To species level using Sims & Gerard (1985) keys; juveniles that could not be identified were excluded.
- Data purpose: Baseline (1999) and endpoint (2002) surveys for control and limed plots.

## Data structure and content
- Datasets: 1011 and 1012 (Baseline and Endpoint earthworm surveys).
- Data file: P2129_ALL_SURVEY.csv (comma-separated values).
- Key fields and meanings:
  - SUID: Unique Sampling Unit Identifier (combines block, main plot, sub-plot, cell, date, etc.).
  - SAMPLING_DATE: Date of sampling.
  - BLOCK, MAIN_PLOT, SUB_PLOT: Field layout identifiers.
  - CELL_X, CELL_Y: Cell grid coordinates.
  - TREATMENT: C = Control, L = Limed.
  - SPECIES: Earthworm species (per Gerard & Sims 1985).
  - ABUNDANCE: Total abundance per m^2 (adults and juveniles).
  - TYPE: Baseline or Endpoint.
- Data provenance: Based on Sourhope Field Data Handbook (Scott et al., 2003) and related UK soil biodiversity literature.

## Data access, quality control, and disclaimers
- Quality control: Numeric range checks, format conformity, and logical integrity checks.
- Limitations: While QA processes were applied, data are not guaranteed by NERC for accuracy or fitness for any purpose; no liability for use or outcomes.
- Usage note: Data intended for self-contained analysis and comparison of baseline vs endpoint under different liming treatments.

## References and further reading
- Bishop, H.O. et al. (2008). Liming upland grassland: effects on earthworm communities and carbon casts. Eur J Soil Sci.
- Scott, R. et al. (2003). Sourhope Field Data Handbook (Supporting Information via EIDC).
- Usher, M.B. et al. (2006). Understanding biological diversity in soil: UK Soil Biodiversity Programme. Appl Soil Ecol.
- Sims, R.W. & Gerard, B.M. (1985). Earthworms: keys and notes for identification (Vol. 31). Brill Archive.