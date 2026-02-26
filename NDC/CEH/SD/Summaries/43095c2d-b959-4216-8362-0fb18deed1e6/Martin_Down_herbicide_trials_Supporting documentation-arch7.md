# Vegetation survey data for Martin Down Brachypodium pinnatum herbicide control trials

- Aim
  - Assess selective herbicide impacts on Brachypodium pinnatum and non-target plant groups to manage tor-grass dominance and restore calcareous grassland, using repeated surveys and controlled treatments.

- Study location and context
  - Martin Down National Nature Reserve, England (approximate site coordinates 50.975 N, 1.937 W).

- Experimental design
  - Two initial Brachypodium pinnatum cover levels: dense (mean baseline cover ~78%) and sparse (mean baseline cover ~26%).
  - Three experimental blocks, each containing seven plots (each plot 3 m wide × 10 m long).
  - Within each block, plots randomly assigned to different herbicide treatments or management.
  - Controls: annual late-summer mowing in all plots; dense areas also included a glyphosate plot per block; sparse areas used cut-and-graze or ungrazed controls to avoid widespread sward destruction.
  - Treatments: five herbicides (plus glyphosate in dense areas) chosen for grass control efficacy, applied according to product labels and regulatory permits.
    - Propaquizafop (Falcon) – selective graminicide; foliar, post-emergence.
    - Tepraloxydim (Aramo) – selective graminicide; foliar, post-emergence.
    - Fluazifop-P-butyl (Fusilade Max) – selective graminicide; foliar, post-emergence.
    - Cycloxydim (Laser) – selective graminicide; foliar, post-emergence.
    - Propyzamide (Kerb Flo) – residual, pre- and post-emergence; graminicide and selective broadleaf.
    - Glyphosate (Touchdown Quattro) – broad-spectrum; applied only in dense plots.
  - Application conditions and timing aligned with product labels; autumn applications targeted regrowth, with one-year late-spring applications in Year 3 due to delays; residual propyzamide applied winter for root uptake.

- Data collection and collection methods
  - Timeframe: baseline vegetation survey in 2012 (July–September) before any treatments; subsequent surveys in 2013, 2014, and 2015 (each July–September).
  - Within each plot: five 50 cm × 50 cm quadrats placed at ~2 m intervals along a W-shaped transect; outer 50 cm margins avoided to reduce drift risk.
  - For each quadrat: record percent cover of B. pinnatum, all vascular plants, and bare ground.
  - Recording detail: in quadrats 1, 3, and 4, species-level identifications; quadrats 2 and 5 logged only by group (grass/forb) or other aggregate categories.
  - Additional data collected per observation: species abbreviation codes and full species names; indicators for positive/negative status and Ellenberg N values.

- Data structure and contents
  - One CSV file containing fields such as:
    - Brachypodium_initial_cover (dense or sparse)
    - Block
    - Plot_number
    - Quadrat_Number
    - Treatment (herbicide product name)
    - Survey_Date (dd/mm/yyyy)
    - Survey_Year (2012–2015)
    - Abbreviated_name (codes for species; some groups like 'bare soil', 'Total forbs', 'Total grass excluding Brachy')
    - Species (full scientific binomial for recorded species)
    - PC_Cover (percent cover for the given species/group)
    - Grass_v_Forb (G or F)
    - Ellenberg_N (fertility tolerance value)
    - Indicator (P, N, A indicating positive/negative indicators or arable/disturbance)
  - Note: '-' is used where a field is not applicable to a row entry.

- Data usage and analyses
  - Used to analyze:
    - Impacts of herbicide treatments on target species B. pinnatum.
    - Impacts on non-target groups (other grasses, forbs, positive/negative indicators, arable indicators).
    - Community-level analyses (Ellenberg N-weighted cover, Detrended Correspondence Analysis, or similar ordination).

- GIS and spatial considerations
  - Spatial framework comprises blocks, plots, and quadrats within each plot, enabling map-based visualization of changes over time.
  - Plot dimensions (3 m × 10 m) and quadrat size (50 cm × 50 cm) support creation of GIS layers for temporal vegetation changes.
  - Site-level coordinates provided for the study area; data are conducive to spatial analyses of herbicide effects across dense vs sparse B. pinnatum conditions.

- References and context
  - Foundational guidance and methodologies cited include works on grassland management, herbicide application, and plant trait databases, such as:
    - Bobbink et al. 1989; English Nature 2003; Green 1972; Hill et al. 2004; Hurst & John 1999; Hurst 1997; Natural England 1999; Robertson & Jefferson 2000.

- Notes for GIS integration
  - Ensure alignment of Block/Plot/Quadrat identifiers with any GIS layers representing the transects and plots.
  - Consider time-series analysis across 2012–2015 to map spatial shifts in B. pinnatum and surrounding plant communities under different herbicide regimes.