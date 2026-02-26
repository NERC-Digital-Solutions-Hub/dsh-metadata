# Earthworm data from Sourhope field experiment site, Scotland, 1999 and 2001 [NERC Soil Biodiversity Programme] H.O. Bishop, I. C. Grieve, J. A. Chudek, & D. W. Hopkins

## Project context and monitoring purpose
- Part of the NERC Soil Biodiversity Thematic Programme (started 1999) focused on intensive study of a large field experiment at Sourhope to understand soil biodiversity and the roles of soil organisms in key ecological processes.
- 24 research projects funded to study soil structure, processes (carbon and nitrogen cycles), and soil biota (across micro-, meso-, and macro-fauna).
- This document describes the earthworm data collected in 1999 and 2001 as part of the programme’s monitoring activities.

## Site description and experimental design
- Location: Sourhope Research Station, southern uplands of Scotland (grid NT8545019630); 2°15W, 55°30N.
- Environment: upland grassland on Brown Forest Soils developed on glacial till; base-poor, damp mineral soils; sheep-grazed until 1998.
- Experimental setup: 30 plots (20 m x 12 m) arranged in five randomized blocks with six treatments.
- Treatments: two main treatments used in this study—unlimed (control) and limed; limed plots received 6 t CaCO3 ha^-1 annually from May 1999 to September 2002 (surface-applied, no incorporation).
- Management: mowing ~once per month May–Sept with cuttings removed; grazing excluded from April 1998.

## Earthworm data collection methods
- Earthworm census: intact soil blocks (42 cm long x 30 cm wide x 25 cm deep) taken from five limed and five unlimed plots in September 1999 and September 2002.
- Extraction: earthworms hand-sorted (preferred over chemical extraction on multi-user plots to avoid contamination).
- Processing: worms refrigerated on damp tissue for 24 hours to void guts, blotted dry, then preserved in 40% ethanol and identified to species using Sims & Gerard (1985) keys.
- Data note: juveniles that could not be identified to species were not included in abundances.

## Data structure and variables
- Data sets: 1011 & 1012 (Baseline and Endpoint earthworm surveys).
- Data file: P2129_ALL_SURVEY.csv (Control and Lime plots at Sourhope).
- Columns and concepts:
  - SUID: unique sampling unit identifier (blocks/main plot/sub-plot/cell, sampling date, project code, sampling unit type, dimensions).
  - BLOCK: block number (1–5).
  - MAIN_PLOT: main plot letter (A–F).
  - SUB_PLOT: sub-plot identifier.
  - CELL_X / CELL_Y: cell grid coordinates.
  - TREATMENT: C = Control, L = Limed.
  - SPECIES: earthworm species (per Sims & Gerard, 1985).
  - ABUNDANCE: total abundance per m^2 (adults and juveniles).
  - TYPE: Baseline (1999 survey) or Endpoint (2002 survey).
- Data are organized to compare baseline vs endpoint earthworm communities under control and limed conditions.

## Data quality, validation and limitations
- Quality control: numeric range checks, data format conformity, and logical integrity checks.
- Data governance: NERC QA procedures applied; however, NERC does not warrant the data’s accuracy or fitness for a specific use and accepts no liability for any use of the data.

## Usage and outputs for environmental monitoring
- Provides standardized, time-based data to monitor soil biota responses to liming and to assess changes in earthworm communities over time.
- Enables analyses of how soil biodiversity relates to soil processes and ecosystem function under different management treatments.
- Datasets are stored and made available through appropriate data portals for reuse and integration with other datasets.

## References and further reading
- Bishop, H. O., Grieve, I. C., Chudek, J. A., & Hopkins, D. W. (2008). Liming upland grassland: the effects on earthworm communities and the chemical characteristics of carbon in casts. European Journal of Soil Science, 59(3), 526-531.
- Scott, R., Bell, J., Kenny, C., Jeffers, J., Buckland, S., & Burt-Smith, G. (2003). Sourhope Field Data Handbook 2003. Supporting Information via EIDC catalogue record.
- Usher, M.B., Sier, A.R., Hornung, M., & Millard, P. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113.
- Sims, R.W., & Gerard, B.M. (1985). Earthworms: keys and notes for the identification and study of the species (Vol. 31). Brill Archive.