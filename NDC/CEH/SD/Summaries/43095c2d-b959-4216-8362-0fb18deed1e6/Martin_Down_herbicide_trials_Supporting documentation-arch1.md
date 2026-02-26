# Vegetation survey data for Martin Down Brachypodium pinnatum herbicide control trials

## Brief description
- Botanical field survey data from a replicated trial assessing selective herbicide impacts on tor-grass Brachypodium pinnatum s.l. at Martin Down NNR, England.
- 50 cm × 50 cm quadrats placed in herbicide-treated and control plots.
- Baseline survey in 2012 followed by three surveys in 2013, 2014 and 2015 after repeat treatments.
- Measures include percentage cover of plant species, bare ground, and plant groups (total grasses, total forbs), plus data on plant indicator status and Ellenberg N value.
- Study areas encompassed both sparse B. pinnatum cover (goal: prevent dominance) and dense cover (goal: reduce to allow other calcareous grassland species).
- Data have supported analyses of herbicide impacts on target (B. pinnatum) and non-target groups, as well as community-level analyses (Ellenberg-N weighted cover, DCA).

## Experimental design
- Location: Martin Down, calcareous grassland (two B. pinnatum cover levels: dense and sparse). Dense mean baseline cover ~78%; sparse mean baseline cover ~26%.
- Structure: three experimental blocks; each block contained seven plots (3 m wide × 10 m long) with random assignment of herbicide or management within each block.
- Treatments: five herbicides (plus glyphosate on selected plots) chosen for efficacy against perennial grasses; administered across plots with standardized application protocols.
- Management contrasts:
  - Dense areas: one plot per block treated with glyphosate; others ungrazed to avoid livestock exposure to residues.
  - Sparse areas: equivalent current management was one plot cut and grazed after cutting; remaining plots ungrazed.
- Timing considerations: herbicides applied to actively growing leaves (foliar) in autumn (to target regrowth) except in the third year when delays caused late-spring applications; residual herbicide (propyzamide) applied in winter to maximize root uptake.

## Treatments
- Herbicides included:
  - Propaquizafop (Falcon) – graminicide; foliar, post-emergence; Year 1–3 dates provided.
  - Tepraloxydim (Aramo) – graminicide; foliar, post-emergence; Year 1–3 dates provided.
  - Fluazifop-P-butyl (Fusilade Max) – graminicide; foliar, post-emergence; Year 1–3 dates provided.
  - Cycloxydim (Laser) – graminicide; foliar, post-emergence; Year 1–3 dates provided.
  - Propyzamide (Kerb Flo) – residual, pre- and post-emergence; graminicide and selective broadleaf; Year 1–3 dates provided.
- Glyphosate (Touchdown Quattro) – broad-spectrum; foliar, post-emergence; applied only to plots in dense B. pinnatum areas.
- Application details include product names, active ingredient concentrations, rate (l ha-1), method (foliar vs residual), WSSA group (1, 3, or 9), specificity, and exact application dates across the three years.

## Data collection and sampling
- Monitoring window: July–September for baseline (2012) and for subsequent years (2013–2015).
- Per plot sampling: five 50 cm × 50 cm quadrats placed approximately 2 m apart along a “W”-shaped transect; outermost 50 cm margins avoided to reduce drift risk.
- Within quadrats:
  - 2012 baseline: all plants recorded to species level in quadrats 1, 3, and 4; quadrats 2 and 5 recorded to group level (grasses vs forbs).
  - 2013–2015: similar sampling with species-level recording in the same quadrats; groups used where appropriate.
  - Measurements recorded: percentage cover of B. pinnatum, all vascular plants, and bare ground.
- Data structure: derived totals and groupings (e.g., Total forbs, Total grasses) used to complement species-level data.

## Data structure and file format
- File: a single CSV file containing all observations.
- Key columns and meanings:
  - Brachypodium_initial_cover: initial classification as 'dense' or 'sparse'.
  - Block: Block identifier (Block 1, Block 2, Block 3).
  - Plot_number: Plot identifier within initial cover/block combination (1–42).
  - Quadrat_Number: Quadrat within plot (1–5).
  - Treatment: Herbicide product name (see Table 1 for values).
  - Survey_Date: Date of survey (dd/mm/yyyy).
  - Survey_Year: Year of survey (2012–2015).
  - Abbreviated_name: Original codes for recorded species (mostly abbreviated binomials).
  - Species: Full scientific name for recorded species (where applicable).
  - PC_Cover: Percentage cover for the given species or group.
  - Grass_v_Forb: Classification as 'G' (grass) or 'F' (forb).
  - Ellenberg_N: Ellenberg N fertility tolerance value (as per PLANTATT).
  - Indicator: Indicator status (P = positive, N = negative, A = other/absence) for calcareous grassland condition or disturbance.
- A value of '-' indicates not applicable for that row (e.g., no species-level entry for a given quadrat).

## Variable definitions (glossary)
- Brachypodium_initial_cover: 'dense' or 'sparse' classification of initial B. pinnatum cover.
- Block: experimental block identifier.
- Plot_number: numeric plot identifier within block/initial-cover.
- Quadrat_Number: quadrat index within plot (1–5).
- Treatment: herbicide or management treatment applied to the plot.
- Survey_Date / Survey_Year: date and year of vegetation survey.
- Abbreviated_name: shorthand codes for recorded species.
- Species: full species name (where available).
- PC_Cover: percent cover for the specified species or category.
- Grass_v_Forb: whether the species is a grass (G) or forb (F).
- Ellenberg_N: fertility tolerance value (Ellenberg N).
- Indicator: conservation/land-use indicator status (P, N, or A).

## Use and analysis
- Designed to analyze:
  - Impacts of selective herbicides on target species B. pinnatum and non-target groups (other grasses, forbs, positive/negative indicators, arable indicators).
  - Community-level responses using methods such as Ellenberg-N weighted cover and DCA (detrended correspondence analysis).
- Data can be extrapolated or cross-referenced with product labels and management practices to understand effectiveness and ecological consequences under calcareous grassland management.

## References
- Bobbink, R., den Dubbelden, K., Willems, J.H., 1989. Seasonal dynamics of phytomass and nutrients in chalk grassland. Oikos 55, 216-224.
- English Nature, 2003. The herbicide handbook: Guidance on the use of herbicides on nature conservation sites. English Nature in association with FACT, Peterborough, UK.
- Green, B.H., 1972. The relevance of seral eutrophication and plant competition to the management of successional communities. Biol. Conserv. 4, 378-384.
- Hill, M.O., Preston, C.D., Roy, D., 2004. PLANTATT-attributes of British and Irish plants: status, size, life history, geography and habitats. Centre for Ecology & Hydrology.
- Hurst, A., 1997. Community dominance: An investigation into the competitive mechanisms of Brachypodium pinnatum and possible methods of reducing its dominance on ancient chalk grassland. University of Sussex.
- Hurst, A., John, E., 1999. The effectiveness of glyphosate for controlling Brachypodium pinnatum in chalk grassland. Biol. Conserv. 89, 261-265.
- Natural England, 1999. Chapter 10: Grassland restoration, In The Lowland Grassland Management Handbook (2nd edition). eds A. Crofts, R.G. Jefferson.
- Robertson, H.J., Jefferson, R.G., 2000. Monitoring the condition of lowland grassland SSSIs: I, English Nature's rapid assessment method. English Nature.