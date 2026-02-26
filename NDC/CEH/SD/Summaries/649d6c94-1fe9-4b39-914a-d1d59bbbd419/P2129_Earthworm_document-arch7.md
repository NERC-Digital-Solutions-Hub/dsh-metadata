# Earthworm data from Sourhope field experiment site, Scotland, 1999 and 2001 [NERC Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999–) focusing on soil biota diversity and ecological processes.
- This document describes earthworm data collected in 1999 and 2002 from Sourhope, Scotland, for mapping and analysis purposes.

## Site and Experimental Design
- Location: Sourhope Research Station, Scottish Borders (grid reference NT8545019630), upland brown forest soils on a north-facing slope.
- Site layout: 30 plots (20 m x 12 m) across five randomized blocks; two treatments: Control (unlimed) and Limed (6 t CaCO3 ha^-1 annually, 1999–2002).
- Vegetation and land use: Moor grassland; sheep grazed until 1998, fenced off thereafter; grass cut monthly May–Sept with removals.
- Sampling timeframe: Baseline sampling in September 1999 and endpoint sampling in September 2002.

## Data Collected and Structure
- Focus: Earthworm census data from soil blocks removed in each treatment and time point.
- Sampling unit: Blocks of soil (42 cm x 30 cm x 25 cm) removed from five blocks (limed and unlimed).
- Data set identifiers: Datasets 1011 and 1012; file P2129_ALL_SURVEY.csv (Baseline and Endpoint data for Control and Lime plots).
- Data columns (example): 
  - SUID: Unique sampling unit identifier (block/main plot/sub-plot/cell)
  - SAMPLING_DATE: Date of sampling
  - BLOCK: Block number (1–5)
  - MAIN_PLOT: Main plot letter (A–F)
  - SUB_PLOT: Sub-plot
  - CELL_X, CELL_Y: Cell grid coordinates
  - TREATMENT: C = Control, L = Limed
  - SPECIES: Earthworm species (as per Gerard & Sims 1985)
  - ABUNDANCE: Total abundance per m^2 (adults and juveniles)
  - TYPE: Baseline or Endpoint
- Identification: Earthworms identified to species under the Sims & Gerard (1985) key after gut purge.
- Note: Juvenile specimens not speciated and thus not included in species counts.

## Data Collection and Processing Methods
- Sorting: Hand-sorting preferred over chemical extraction to avoid bias and cross-plot contamination on multi-user plots.
- Preservation: Specimens refrigerated briefly to purge guts, then preserved with 40% ethanol before identification.
- Data integrity: Abundant quality control steps described (range checks, formatting, logical integrity).

## Data Quality and Provenance
- Quality assurance steps are implemented, but dataset providers (NERC) do not warrant absolute accuracy or fitness for a specific use.
- Users assume responsibility for the suitability and interpretation of the data.

## GIS and Data Visualization Considerations
- Spatial design supports mapping earthworm distributions by block, treatment, and time (baseline vs endpoint).
- Grid coordinates (CELL_X, CELL_Y) enable spatial plotting within each plot; data can be integrated with soil and vegetation datasets.
- Potential challenges: heterogeneous site conditions, varying resolutions, and grouping by species for habitat analyses.

## References and Further Reading
- Bishop et al. (2008). Liming upland grassland: effects on earthworm communities and carbon in casts. Eur J Soil Sci.
- Scott et al. (2003). Sourhope Field Data Handbook 2003.
- Usher et al. (2006). Understanding biological diversity in soil: UK Soil Biodiversity Programme. Appl Soil Ecol.
- Sims & Gerard (1985). Earthworms: Keys and notes for identification. Brill Archive.