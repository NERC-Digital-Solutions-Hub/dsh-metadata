# Dataset Summary and contextual information

- Overview
  - Focus: Above Ground Carbon Density (ACD) estimated from tropical forest census surveys (1992–2016) in Sabah, Malaysia (Ulu Segama Forest Reserve and Danum Valley Conservation Area).
  - Plot networks: three independent networks contributed data:
    - INDFORSUS: 53 plots (0.1 ha each); logged 1981–1993; some plots relocated and recensus in 2016.
    - Pinard & Putz (1996): 32 plots (0.08 ha) plus nested plots for smaller DBH classes.
    - INFRAPRO / INFAPRO (Face the Future): 205 plots across four circles (0.05 ha total per cross) with nested measurements.
  - Scale: 257 plots, 51,803 individual tree measurements across 45.56 ha; total data across multiple years and restoration scenarios.
  - Data products: ACD per plot (Mg ha^-1); associated metadata on restoration scenario, logging method, and timing.

- Data sources and networks
  - Three plot networks were developed independently, each with its own field protocol and measurement details.
  - Data include logging method (High lead, Tractor) or unlogged, year logged, and forest restoration scenario (baseline, project scenario, or unlogged).

- Field measurements and protocols
  - ACD derived from measurements of free-standing woody plants above 20 cm DBH (and related nested measurement schemes for smaller DBH classes) with 1.3 m height reference.
  - Each network used slightly different plot geometries and measurement radii:
    - INDFORSUS: 17.84 m radius plots; concentric circles with radii 12.61 m and 2 m for nested measurements.
    - Pinard & Putz: nested plots with 400 m^2, 100 m^2, and 25 m^2 areas for different DBH classes.
    - INFAPRO: four circles (0.05 ha total) arranged in a cross; additional nested circles for smaller DBHs.
  - Measurements include DBH at 1.3 m (or adjusted when buttress roots required), tree height (directly measured for many trees or estimated for the rest), and species identity where possible.

- Allometric methods and carbon modelling
  - Carbon content assumed as 47% of aboveground biomass (AGB).
  - AGB estimated using allometric equation: AGB_est = 0.0673 × (ρ × DBH^2 × H)^0.976, where DBH is in cm, H in m, and ρ is wood density (g cm^-3).
  - DBH adjustments: when DBH_POM is measured above 1.3 m, a taper model is used to estimate DBH at 1.3 m.
  - Height estimation: for trees without direct height, a three-parameter Weibull-based equation H = 89.53 × (1 − exp(−0.0225 × DBH^0.7383)) was used, calibrated with available measurements.
  - Wood density: sourced from global wood density database; if species-level density missing, plot-level average used or nearest taxon average assigned; carbon contents summed per plot to yield ACD (Mg ha^-1).

- Data structure and content
  - For each plot, the following fields are recorded:
    - Plot Identifier, Coupe Name, Plot identifier (plot network + plot number), Dataset (INDFORSUS, FACE, or Pinard-Lincoln)
    - ACD (Mg ha^-1)
    - FACE (restoration scenario: 'Project Scenario', 'Baseline', or 'N/A' for unlogged)
    - LoggingMethod ('High lead', 'Tractor', 'UnLogged')
    - Year logged
    - Forest (Logged/UnLogged)
    - YearsSinceLogging
    - MeasureTime (year of census)
  - Data lineage and version: Document version 1.05-06-20; references to data management and reproducibility.

- Quality control, data management, and reuse
  - Quality control steps included numeric range checks, formatting checks, and logical integrity tests.
  - Data analysis and modelling described by Philipson et al. (in press); code and workflow access provided via Zenodo: https://doi.org/10.5281/zenodo.3885641
  - The dataset integrates three networks with harmonized ACD calculations, enabling cross-network comparisons and temporal analyses of carbon density in response to logging and restoration.
  - Potential considerations for data leaders: heterogeneity in measurement protocols across networks; attention needed for metadata harmonization and documentation to support consistent downstream analytics and governance.

- References
  - Face the Future (INFAPRO), 2011; Foody et al., 2001; Foody & Cutler, 2003; Tangki & Chappell, 2008; Pinard & Putz, 1996; Lincoln, 2008; Philipson et al. (in press); additional methodological sources for allometric equations and wood density databases.