# Vegetation survey data for Martin Down Brachypodium pinnatum herbicide control trials

## Overview
- Field study at Martin Down NNR, England, to assess selective herbicide impacts on tor-grass Brachypodium pinnatum s.l. and effects on calcareous grassland.
- Data span baseline (2012) plus three post-treatment surveys (2013, 2014, 2015).
- Measurements include percent cover of B. pinnatum, total vascular plants, bare ground, and plant groups (grasses/forbs), along with indicator status and Ellenberg N values.
- Analyses have been used to examine target and non-target responses and to conduct community-level analyses (Ellenberg-N weighted cover, DCA).

## Experimental design
- Plots established in two B. pinnatum cover contexts: dense (baseline mean cover ~78%) and sparse (baseline mean cover ~26%) within calcareous grassland (NVC CG2).
- For each cover context, three randomized blocks with seven plots per block.
- Treatments: five herbicides (in addition to glyphosate on dense areas) and appropriate control management.
- Controls differ by context:
  - Dense areas: one plot per block treated with glyphosate; other plots left untreated or managed as per protocol.
  - Sparse areas: one plot per block cut and grazed after cutting; remaining plots ungrazed to avoid livestock exposure to residues.
- Herbicides applied as per product labels; treatments timed to maximize efficacy (autumn foliar applications for regrowth; winter residual applications for root uptake where relevant).
- Administrative permit obtained for outside-label field use; drift and weather considerations mitigated through timing and training.

## Data collection methods
- Vegetation surveys conducted July–September in 2012 (baseline), 2013, 2014, and 2015.
- Within each plot, five 50 cm × 50 cm quadrats placed along a W-shaped transect, avoiding outer 50 cm to reduce spray drift risk.
- In quadrats 1, 3, and 4: record all species to species level; in quadrats 2 and 5: record only by group (grasses/forbs) or total groups.
- For each quadrat: record percent cover of B. pinnatum, all vascular plants, and bare ground.
- Additional data per record: Ellenberg N values (fertility tolerance), indicator status (positive/negative for calcareous grassland condition or arable/disturbance), and abbreviated species codes.

## Data structure and variables
- Dataset is a single CSV file with columns including:
  - Brachypodium_initial_cover (dense or sparse)
  - Block (Block 1–3)
  - Plot_number (1–42 within initial cover/block/treatment)
  - Quadrat_Number (1–5)
  - Treatment (herbicide product name)
  - Survey_Date (dd/mm/yyyy)
  - Survey_Year (2012–2015)
  - Abbreviated_name (species codes)
  - Species (full scientific name)
  - PC_Cover (percent cover)
  - Grass_v_Forb (G/F classification)
  - Ellenberg_N (fertility value)
  - Indicator (P/N/A; positive/negative indicators or arable/disturbance)
- '-' denotes not applicable (e.g., certain columns not relevant for some rows).
- Quadrats 1, 3, 4 include species-level data; quadrats 2, 5 provide group-level data.

## Analyses and environmental monitoring relevance
- Enables assessment of herbicide efficacy on target species (B. pinnatum) and impacts on non-target groups (other grasses, forbs, indicator species).
- Supports community-level analyses (e.g., Ellenberg-N weighted cover, detrended correspondence analysis).
- Provides a standardized, temporary dataset suitable for time-series monitoring of habitat condition and management performance on calcareous grassland.

## Access, format, and references
- Data available as a single CSV file with detailed column metadata.
- Key references informing methodology and context include:
  - Bobbink et al. 1989
  - English Nature 2003
  - Green 1972
  - Hill et al. 2004 (PLANTATT)
  - Hurst and John 1999; Hurst 1997
  - Natural England 1999
  - Robertson and Jefferson 2000