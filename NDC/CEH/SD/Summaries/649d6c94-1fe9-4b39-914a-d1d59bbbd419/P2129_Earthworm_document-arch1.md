# Earthworm data from Sourhope field experiment site, Scotland, 1999 and 2001 [NERC Soil Biodiversity Programme] H.O. Bishop, I. C. Grieve, J. A. Chudek, & D. W. Hopkins

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999–2002), which studied soil biodiversity and the functional roles of soil organisms across 24 research projects.
- This document describes earthworm data collected at Sourhope field site (Scottish Borders) in 1999 (baseline) and 2002 (endpoint) as part of a liming experiment.
- Objectives relevant to analysts: quantify earthworm communities under different soil management (limed vs control) to assess productivity, diversity, and potential links to soil processes.

## Site and experimental design
- Location: Sourhope Research Station, southern uplands of Scotland (grid NT8545019630), north-facing slope on Brown Forest Soils developed on glacial till.
- Vegetation: upland grassland typical of base-poor, damp mineral soils; pasture historically grazed by sheep until 1998.
- Experimental setup: 30 plots (20 m x 12 m) arranged in five randomized blocks.
- Treatments: Limed vs Control (unlimed). Limed plots received 6 t CaCO3 ha^-1 annually from May 1999 to Sept 2002, applied to soil surface with no incorporation.
- Management: grass mown ~monthly May–Sept with cuttings removed; grazing ceased in 1998 due to fencing.

## Earthworm data collection and processing
- Sampling design: intact blocks of soil (42 cm long x 30 cm wide x 25 cm deep) were removed from five limed and five unlimed plots in Sep 1999 and Sep 2002.
- Extraction method: hand-sorting used to maximize detection and avoid chemical extraction biases; worms kept on damp tissue for 24 h to void gut contents.
- Preservation and identification: worms killed in 40% ethanol and identified to species level using Sims & Gerard (1985) keys.
- Data scope: abundances include adults and juveniles; juvenile abundances that could not be identified to species were not included.

## Data structure and contents
- Data sets: 1011 & 1012 (Baseline and Endpoint earthworm surveys).
- File: P2129_ALL_SURVEY.csv (CSV format).
- Core columns:
  - SUID: unique sampling unit identifier (block/main-plot/sub-plot/cell details)
  - SAMPLING_DATE: date of sampling
  - BLOCK: block number (1–5)
  - MAIN_PLOT: main plot label (A–F)
  - SUB_PLOT: sub-plot designation
  - CELL_X, CELL_Y: cell grid coordinates
  - TREATMENT: C = Control, L = Limed
  - SPECIES: earthworm species (per Gerard & Sims, 1985)
  - ABUNDANCE: total abundance per m^2 (adults and juveniles)
  - TYPE: Baseline ( Sept 1999 sampling) or Endpoint ( Sept 2002 sampling)
- Important notes:
  - Abundances are per m^2; juveniles not identifiable to species excluded from SPECIES/ABUNDANCE breakdown.
  - Data are tied to the Sourhope field experiment’s liming treatment and sampling dates.

## Data quality, limitations, and usage notes
- Quality control: numeric range checks, formatting checks, and logical integrity checks performed.
- Limitations:
  - Despite QA procedures, data are not warranted for accuracy or fitness for any particular use; no liability assumed for data use or interpretation.
  - Potential scale-related gaps and variability inherent to field data (site- and treatment-level factors).
- Practical use for analysts:
  - Assess impact of liming on earthworm species composition, abundances, and potential links to soil processes.
  - Compare Baseline vs Endpoint communities within treatments and across treatments.
  - Integrate with other soil biodiversity data from the programme for multivariate analyses.

## References and further reading
- Bishop, H. O., Grieve, I. C., Chudek, J. A., & Hopkins, D. W. (2008). Liming upland grassland: the effects on earthworm communities and the chemical characteristics of carbon in casts. European Journal of Soil Science, 59(3), 526-531. doi: 10.1111/j.1365-2389.2007.01009.x
- Scott, R., Bell, J., Kenny, C., Jeffers, J., Buckland, S., & Burt-Smith, G. (2003). Sourhope Field Data Handbook 2003. Supporting Information via EIDC catalogue record.
- Usher, M. B., Sier, A. R., Hornung, M., & Millard, P. (2006). Understanding biological diversity in soil: the UK’s Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113.
- Sims, R. W., & Gerard, B. M. (1985). Earthworms: Keys and Notes for the Identification and Study of the Species (Vol. 31). Brill Archive.