# Earthworm data from Sourhope field experiment site, Scotland, 1999 and 2001 [NERC Soil Biodiversity Programme] H.O. Bishop, I. C. Grieve, J. A. Chudek, & D. W. Hopkins

## Purpose and context
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biota diversity and functional roles in key ecological processes.
- This document describes earthworm data collected in the Sourhope field experiment (Scotland) during 1999 and 2001, as part of the programme’s broader soil biodiversity studies.

## Site and experimental design
- Location: Sourhope Research Station, southern uplands of Scotland; upland grassland on Brown Forest Soils with variability across the site.
- Experimental setup: 30 plots (20 m x 12 m) arranged in five randomized blocks with six treatments; treatments include unlimed and limed plots.
- Liming regime: 6 t CaCO3 ha^-1 applied annually from 1999 to 2002 (surface application, no incorporation).
- Management: Heather grassland typical of British uplands; grazing excluded in 1998; mowing 1 per month May–Sept with cuttings removed.

## Earthworm census and methods
- Sampling unit: intact soil blocks (42 cm long x 30 cm wide x 25 cm deep) collected from five limed and five unlimed plots in Sep 1999 and Sep 2002.
- Extraction: hand-sorting (preferred over chemical extracts to avoid bias); worms kept on damp tissue, guts voided, dried, weighed.
- Identification: killed in 40% ethanol and identified to species using Sims & Gerard (1985) key.
- Data coverage: juveniles that could not be identified to species excluded from abundance counts.

## Data structure and content
- Datasets: 1011 & 1012 (Baseline and Endpoint earthworm surveys).
- File format: CSV (P2129_ALL_SURVEY.csv) with fields including:
  - SUID: unique sampling unit identifier (block/main plot/sub-plot/cell and sampling date)
  - BLOCK: block number (1–5)
  - MAIN_PLOT: main plot letter (A–F)
  - SUB_PLOT: sub-plot designation
  - CELL_X / CELL_Y: cell grid coordinates
  - TREATMENT: C = Control, L = Limed
  - SPECIES: earthworm species (as per Gerard & Sims, 1985)
  - ABUNDANCE: total abundance per m^2 (adults and juveniles)
  - TYPE: Baseline or Endpoint (baseline Sep 1999; endpoint Sep 2002)
  - SAMPLING_DATE: date of sampling
- Purpose of data: enable comparison of earthworm communities between limed vs control treatments over time.

## Quality control and governance
- Quality assurance steps included numeric range checks, formatting validation, and logical integrity checks.
- Data provenance and use: NERC provides QA but does not warrant accuracy or fitness for a specific use; no liability for losses or damages from data use.
- Data sharing and metadata: highlights that underlying data should be shared appropriately; potential barriers include metadata completeness and data format transformations; emphasizes data governance and openness considerations.

## References and related resources
- Related scientific publications and data resources cited, including: 
  - Bishop et al. (2008) on liming effects on earthworms and carbon characteristics
  - Sourhope Field Data Handbook (Scott et al., 2003)
  - Usher et al. (2006) on UK Soil Biodiversity Programme
  - Sims & Gerard (1985) earthworm identification keys

## Relevance for monitoring frameworks
- Demonstrates a structured, well-documented approach to baseline vs endpoint monitoring under a treatment (liming) with explicit spatial design (blocks, plots, cells) and species-level data.
- Illustrates key monitoring framework challenges and mitigations, including:
  - Importance of detailed metadata and consistent data formats
  - Data accessibility and sharing while maintaining quality
  - Handling of unidentifiable juvenile specimens and treatment-specific sampling considerations
  - Need for robust governance to ensure data quality, timeliness, and ongoing usefulness for policy-relevant monitoring and decision-making