# Vegetation survey data for Martin Down Brachypodium pinnatum herbicide control trials

## Overview
- Vegetation data from a botanical field survey examining selective herbicide impacts on Brachypodium pinnatum (tor-grass) control at Martin Down NNR, England.
- Experimental setup: 50 cm × 50 cm quadrats within herbicide-treated and control plots in a replicated design, with a baseline survey in 2012 and follow-up surveys in 2013, 2014, and 2015.
- Data types: percentage cover of plant species, bare ground, and plant groups (total grasses, total forbs); includes plant indicator status and Ellenberg N values.
- Purpose: analyze herbicide effects on B. pinnatum and non-target groups, plus community-level analyses (e.g., Ellenberg-N weighted cover, DCA).

## Experimental design
- Site: Martin Down calcareous grassland with two initial B. pinnatum cover levels — “dense” (mean baseline cover ≈ 78%) and “sparse” (≈ 26%).
- Structure: 3 blocks; each block contains 7 plots (3 m wide × 10 m long). Within each block, plots receive different herbicide or management treatment at random.
- Treatments:
  - Five herbicides (six when including glyphosate) selected for perennial grass control; detailed in a comprehensive table with active ingredients, products, MAPP numbers, concentrations, rates, application methods, action groups, and timing.
  - Controls: annual cut in late summer (July–August) with a mechanical mower.
  - Dense areas: one plot per block treated with glyphosate; sparse areas: one plot cut and grazed after cutting; remaining plots ungrazed.
- Management constraints: cutting, grazing, and public access timing guided herbicide applications to maximize efficacy and minimize drift and exposure; all foliar herbicides applied to actively growing leaves (autumn generally), with a late-spring exception in year 3 due to delays; residual propyzamide applied in winter.
- Permits: Administrative Trials Permit from the GB Chemicals Regulation Division for off-label herbicide use.

## Data collection methods
- Monitoring window: July–September 2012 (baseline), 2013, 2014, 2015.
- Within-plot sampling: five 50 cm × 50 cm quadrats per plot, positioned along a W-shaped transect (~2 m between quadrats); outermost 50 cm margins excluded to reduce spray drift risk.
- Within quadrats:
  - Quadrat 1, 3, 4: all plants recorded to species level.
  - Quadrat 2, 5: recording by group level only (grasses vs. forbs) and total cover.
  - Recorded data per quadrat: B. pinnatum cover, all vascular plants, bare ground.
- Time and funding constraints limited species-level recording to three of the five quadrats.

## Data structure and content
- Data format: a single .csv file.
- Key columns and meanings:
  - Brachypodium_initial_cover: initial cover category (“dense” or “sparse”).
  - Block: Block identification (Block 1, Block 2, Block 3).
  - Plot_number: plot number within block and treatment combination.
  - Quadrat_Number: quadrat position within plot (1–5).
  - Treatment: herbicide/product name (reference table 1 for values).
  - Survey_Date: date of survey (dd/mm/yyyy).
  - Survey_Year: year of survey (2012–2015).
  - Abbreviated_name: coded species identifiers (or groups like bare soil, Total forbs, Total grass excluding Brachypodium).
  - Species: full scientific binomial; for some rows, values are '-' if not applicable.
  - PC_Cover: percent cover for the given species/group.
  - Grass_v_Forb: classification as G (grass) or F (forb).
  - Ellenberg_N: fertility tolerance value (from PLANTATT, 2–8).
  - Indicator: status as P (positive), N (negative), or A (arable/disturbance).
- Notation: '-' indicates not applicable for that row entry.
- Data scope: includes both species-level and group-level data; integrates baseline year with 2013–2015 follow-ups.

## Location and temporal coverage
- Site: Martin Down NNR, coordinates 50.975 N, 1.937 W.
- Temporal scope: baseline in 2012; subsequent surveys in 2013, 2014, and 2015.

## References and supporting sources
- Bobbink et al. 1989; English Nature 2003; Green 1972; Hill et al. 2004; Hurst 1997; Hurst & John 1999; Natural England 1999; Robertson & Jefferson 2000.