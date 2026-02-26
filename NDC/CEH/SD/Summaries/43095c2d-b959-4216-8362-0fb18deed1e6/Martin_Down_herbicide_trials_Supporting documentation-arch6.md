# Vegetation survey data for Martin Down Brachypodium pinnatum herbicide control trials

## Brief description
- Botanical field survey dataset from trials on selective herbicide impacts on Brachypodium pinnatum in calcareous grassland at Martin Down NNR, England.
- Data collected in 50 cm x 50 cm quadrats within plots treated with herbicides or controls, including a baseline survey in 2012 and follow-ups in 2013, 2014, and 2015.
- Variables include percentage cover of plant species, bare ground, plant groups (total grasses, total forbs), plant indicator status, and Ellenberg N values.
- Covers both dense and sparse B. pinnatum scenarios, aiming to manage B. pinnatum dominance and restore calcareous grassland diversity.
- Used to analyze herbicide effects on target and non-target groups and for community-level analyses (Ellenberg-N weighted cover, DCA).

## Experimental design
- Location: Martin Down (50.975 N, 1.937 W) on calcareous grassland with two baseline B. pinnatum cover levels: dense (mean baseline cover 78%) and sparse (mean baseline cover 26%).
- Three experimental blocks per baseline type, each block containing seven plots (3 m wide x 10 m long per plot).
- Within each block, plots randomly assigned to one of five herbicides or a control management.
- Management for controls differed by baseline: dense areas used one plot with glyphosate; sparse areas used one plot that was cut and grazed post-cut; remaining plots remained ungrazed.
- Herbicides (five active products; glyphosate included in dense areas) chosen for efficacy against perennial grasses; Administrative Trials Permit obtained for off-label use.
- Application timing aligned with product labels, aiming for active growth and regrowth post-cutting; a residual herbicide applied in winter for root uptake.
- In years 2–3, one year's timing shifted due to operational issues; dates are provided in Table 1 of the source.

## Collection methods
- Vegetation monitored July–September in 2012 (baseline), 2013, 2014, and 2015.
- Within each plot, five 50 cm x 50 cm quadrats placed approximately every 2 m along a W-shaped transect, avoiding the outer 50 cm to minimize spray drift.
- In quadrats 1, 3, and 4, all plants recorded to species level; in quadrats 2 and 5, only group-level data (grasses vs. forbs) recorded.
- For each quadrat, recorded percentage cover of B. pinnatum, all vascular plants, and bare ground.

## Data structure and content
- Dataset is a single CSV file with the following columns:
  - Brachypodium_initial_cover (dense or sparse)
  - Block (Block 1, Block 2, Block 3)
  - Plot_number (1–42, unique per initial cover/block/treatment)
  - Quadrat_Number (1–5)
  - Treatment (herbicide product name; table 1 details)
  - Survey_Date (date)
  - Survey_Year (2012–2015)
  - Abbreviated_name (codes for species; includes some groups)
  - Species (full scientific binomial)
  - PC_Cover (percent cover for the species/group)
  - Grass_v_Forb (G or F)
  - Ellenberg_N (soil fertility tolerance)
  - Indicator (P, N, or A for positive/negative indicators or arable/disturbance)
- A value of '-' indicates non-applicable entries (e.g., species without indicator status).
- Table 1 (not reproduced here) lists herbicides used, including product name, active ingredient, MAPP number, concentration, application rate, method (foliar or residual), timing (pre- or post-emergence), WSSA group, and year-by-year application dates.

## Data usage and aims
- Enables analysis of herbicide impacts on target species B. pinnatum and non-target groups (other grasses, forbs, indicators).
- Supports community-level analyses such as Ellenberg-N weighted cover and DCA.
- Provides opportunities to assess management effectiveness in different B. pinnatum baseline conditions and to compare across years.

## References (contextual)
- Bibliographic sources relating to herbicide use, grassland management, and plant trait data used for interpretation (e.g., PLANTATT, various herbicide handbooks and studies cited in the original description).