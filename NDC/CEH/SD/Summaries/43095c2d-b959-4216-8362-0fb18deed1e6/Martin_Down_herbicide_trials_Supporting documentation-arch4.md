# Vegetation survey data for Martin Down Brachypodium pinnatum herbicide control trials

## Overview
- Vegetation data from botanical field surveys of selective herbicide trials aimed at controlling Brachypodium pinnatum s.l. on calcareous grassland at Martin Down NNR, England.
- Study design includes 50 cm × 50 cm quadrats in herbicide-treated and control plots, with a baseline survey in 2012 and follow-up surveys in 2013, 2014, and 2015.
- Recorded measurements include percent cover of plant species, bare ground, and plant groups (total grasses, total forbs), plus indicator status and Ellenberg N values.
- Data support analyses of herbicide impacts on target (B. pinnatum) and non-target groups, as well as community-level analyses (Ellenberg-N weighted cover, DCA).

## Experimental design
- Site: Martin Down calcareous grassland with two B. pinnatum cover levels: dense (mean baseline cover ~78%) and sparse (mean baseline cover ~26%).
- Structure: 3 blocks; each block contains 7 plots. Each plot assigned a different herbicide or management treatment at random.
- Treatments: five herbicides (six including glyphosate) selected for efficacy against perennial grasses; administered after securing an Administrative Trials Permit.
- Application method: uniform spray across plots using an AZO handheld sprayer; trained personnel on favorable weather and ground conditions.
- Controls and management: 
  - Dense areas: one plot per block received glyphosate; other plots ungrazed.
  - Sparse areas: one plot per block received a cut-and-graze treatment; other plots ungrazed.
  - All plots otherwise ungrazed to avoid livestock exposure to herbicides.
- Timing: foliar herbicides applied autumn to target regrowth after cutting; in year 3 some late-spring applications occurred due to delays; residual herbicide (propyzamide) applied in winter.
- Herbicide details: detailed product names, active concentrations, application rates, methods (foliar vs residual), timing (pre-/post-emergence), WSSA group classification, and application dates across years.

## Data collection and methods
- Monitoring periods: July–September 2012 (baseline), 2013, 2014, 2015.
- Plot sampling: five 50 cm × 50 cm quadrats per plot positioned along a W-shaped transect, avoiding outer 50 cm to minimize drift risk.
- Within quadrats:
  - Record percent cover of B. pinnatum, all vascular plants, and bare ground.
  - For quadrats 1, 3, and 4: identify and record at species level.
  - For quadrats 2 and 5: record percent cover at group level (grasses and forbs) only.
- Data captured include abbreviations for species, Ellenberg N values, and indicator status.

## Data structure and fields
- Dataset: a single CSV file.
- Key columns:
  - Brachypodium_initial_cover: initial cover category ('dense' or 'sparse').
  - Block: Block identifier (e.g., 'Block 1', 'Block 2', 'Block 3').
  - Plot_number: Plot number within block (1–42 across combinations).
  - Quadrat_Number: Quadrat number within plot (1–5).
  - Treatment: Herbicide or management treatment name (refs to Table 1 for values).
  - Survey_Date: Date of survey (dd/mm/yyyy).
  - Survey_Year: Year of survey (2012–2015).
  - Abbreviated_name: Original species codes (mostly abbreviated binomials) plus groups ('bare soil', 'Total forbs', 'Total grass excluding Brachypodium').
  - Species: Full scientific binomial for recorded species.
  - PC_Cover: Percentage cover for the species/group.
  - Grass_v_Forb: Classification as 'G' (grass) or 'F' (forb).
  - Ellenberg_N: Ellenberg N fertility value (2–8).
  - Indicator: Status as positive ('P'), negative ('N'), or arable/disturbance ('A').
- Notes: '-' indicates not applicable for a given row.

## Data use and analyses
- Enables assessment of herbicide impacts on target species (B. pinnatum) and non-target groups (other grasses, forbs, positive/negative indicators, arable indicators).
- Supports community-level analyses such as Ellenberg-N weighted cover and DCA (detrended correspondence analysis).

## Data quality, limitations, and metadata notes
- Recording scope varied: three quadrats per plot were recorded to species level, while others were recorded to group level due to time/funding constraints.
- Mixed data granularity (species-level and group-level) with some fields not applicable (denoted by '-').

## References
- Bobbink et al. 1989; English Nature 2003; Green 1972; Hill et al. 2004; Hurst 1997; Hurst & John 1999; Natural England 1999; Robertson & Jefferson 2000.