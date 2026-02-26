# Lolium and Trifolium solardomes ozone exposure experiment

- Objective
  - Assess the effects of ozone exposure on two pasture species, Lolium perenne and Trifolium repens, in monoculture versus mixed swards.
  - Measure biomass production, tissue composition, and photosynthetic function to understand ozone tolerance and interspecific interactions.

- Experimental design and treatments
  - Four solardomes used in a randomized block design; two additional domes as controls with charcoal-filtered air.
  - Ozone treatments include: constant 30 ppb (control), and two higher-exposure regimes with episodic peaks up to 80–100 ppb, plus a rural-like episodic profile (O3(30+peaks)).
  - Continuous ozone monitoring in each dome every 30 minutes.
  - Exposures lasted 12 weeks, with two harvest periods: weeks 1–6 and weeks 7–12.

- Plant material and cultivation
  - Plants derived from turf samples of pasture near Edinburgh; randomised across competition treatments.
  - Each pot contained 12 plants: 4 central plants (T. repens) surrounded by 8 L. perenne.
  - For each dome/treatment, three pots of L. perenne monoculture, three pots of T. repens monoculture, and three pots of a L. perenne + T. repens mixture.

- Data collected and data structure
  - Biomass data
    - Harvested at two time points; plants dried to constant weight to determine dry biomass per pot.
    - Data file: Lolium_and_Trifolium_solardomes_biomass_data.csv (16 rows, 6 columns) with columns: Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight (g per pot, cutting height 7 cm), standard error.
  - Canopy and tissue distribution
    - Partitioned biomass by canopy position and by plant part (e.g., for clover: stolons, flowers, leaves; for ryegrass: leaves and stems).
    - Data files: Lolium_and_Trifolium_solardomes_clover_distribution_data.csv (28 rows, 6 columns) and Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv (32 rows, 6 columns).
  - Physiological measurements
    - Leaf-level photosynthetic characterization using A-Ci and AQ curves to derive photosynthetic parameters.
    - Measurements taken on representative leaves across ages, with at least six leaves per measurement day.
    - Data file: Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv (220 rows, 7 columns) with columns: Species, Leaf number, weeks since start of exposure, Treatment, dome.pot, Ci (ppm), A corrected for leaf area (umol m-2 s-1).
  - Analytical details
    - A-Ci curves analyzed with Farquhar et al. model; Jmax estimated from the asymptote of the A-Ci curve (Ci > 500 ppm) using the Stirling et al. method.
    - Vcmax inferred from the initial slope of A vs Ci (Ci up to 300 ppm).
    - Measurements performed with a CIRAS I system under 1000 µmol m-2 s-1 PAR, CO2 steps from 0 to 2000 ppm.

- Data processing and analysis
  - Data are averaged to solardome means prior to analysis.
  - Statistical approaches:
    - One-way ANOVA (Minitab) to test ozone effects on Jmax (no monoculture vs mixture comparison in this analysis).
    - GLM regression to compare A vs Ci relationships between treatments.
    - Genstat (split-plot and split-split-plot ANOVA) with main factor as ozone treatment and subplot as monoculture vs mixture.
    - Canopy position included as a sub-sub plot for biomass partitioning.
  - Outputs support both identification of ozone effects on physiological performance and the influence of competition regime on biomass allocation and photosynthesis.

- Datasets and file structure
  - Lolium_and_Trifolium_solardomes_ACi_Curve_data.csv: 220 rows, 7 columns (Species, Leaf number, weeks since start of exposure, Treatment, dome.pot, Ci, A corrected for leaf area).
  - Lolium_and_Trifolium_solardomes_biomass_data.csv: 16 rows, 6 columns (Harvest, Species, Monoculture or mixture, Ozone treatment, dry weight (g per pot, cutting height 7 cm), standard error).
  - Lolium_and_Trifolium_solardomes_clover_distribution_data.csv: 28 rows, 6 columns (Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error).
  - Lolium_and_Trifolium_solardomes_Lolium_distribution_data.csv: 32 rows, 6 columns (Harvest, Monoculture or mixture, part of canopy, Ozone treatment, Dry weight per pot (g), standard error).

- Practical implications for data use
  - Data support for exploring how ozone affects growth, tissue allocation, and photosynthetic capacity in single-species vs mixed swards.
  - Rich, multi-level dataset enabling self-serve analyses, comparison of A-Ci derived parameters (Jmax, Vcmax) under ozone stress, and assessment of interspecific interactions under atmospheric changes.
  - Clear documentation of data structure facilitates reuse, replication, or integration into broader analyses of ozone physiology in pasture species.