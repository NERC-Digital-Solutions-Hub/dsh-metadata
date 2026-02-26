# Dataset Summary and contextual information

## Overview
- Data describe Above Ground Carbon Density (ACD) estimated from forest census surveys (1992–2016) in tropical lowland dipterocarp forests of USFR and DVCA, Sabah, Malaysia.
- Three plot networks contribute data: INDFORSUS (A), Pinard & Putz (B), and INFRAPRO/INFAPRO (C).
- Totals: 257 plots, 51,803 tree measurements, across 45.56 ha.
- Data provenance combines multiple projects and restoration contexts, with logging histories and restoration treatments.
- Data quality steps include numeric range checks, formatting checks, and logical integrity checks; analysis and modelling described in Philipson et al. (in press). Code for analysis available at the provided Zenodo DOI.

## Context and experimental design
- Objective: estimate ACD using allometric approaches across a history of logging and restoration within USFR and DVCA.
- Logging history: USFR logged 1972–1993 (tractor or high-lead methods); restoration treatments implemented 1993–2004.
- Plot networks compiled from:
  - A. INDFORSUS: 53 plots (0.1 ha) in areas logged 1981–1993 and unlogged primary forest; 2016 recensus of 20 plots.
  - B. Pinard & Putz: 32 plots (0.08 ha) before logging; recensus in 1996 and 2005; broader nested plots at smaller sizes.
  - C. INFRAPRO/INFAPRO: 205 plots (0.2 ha) across logged areas; recensus in 2010 and seven in 2015.
- Additional data on logging method, coupe, and year of logging provided by Yayasan Sabah Group.
- Data are prepared for integration across networks, with cross-referencing to supporting literature and project documentation.

## Fieldwork protocol and measurements
- Each network used slightly different measurement protocols:
  - A (INDFORSUS): 17.84 m radius plots; all woody plants >20 cm DBH measured; nested circles for smaller rings; DBH measured at 1.3 m unless buttress roots require adjustment.
  - B (Pinard & Putz): All free-standing woody plants ≥20 cm DBH across entire plot; nested subplots with finer DBH ranges (1–19 cm, etc.) at smaller plot areas.
  - C (INFAPRO): Four circles of 0.05 ha (radius 12.62 m); measurements across DBH thresholds with nested plots for smaller DBH classes.
- Allometric approaches rely on DBH at 1.3 m, height (measured or estimated), and wood density.

## Units of recorded values
- Above-ground Carbon Density (ACD): Mg ha^-1.

## Allometric methods and carbon modelling
- Carbon content assumed to be 47% of aboveground biomass (AGB); AGB estimated via allometric equation:
  AGB_est = 0.0673 × (ρ × DBH^2 × H)^0.976
  where DBH in cm, H in m, ρ = wood density (g cm^-3).
- DBH adjustments for POM (point of measurement) when buttresses require raising measurement; use a taper model to estimate  DBH at 1.3 m.
- Height estimation:
  H = 89.53 × [1 − exp(−0.0225 × DBH^0.7383)]
  (three-parameter Weibull-based relationship fitted to data from the study area).
- Wood density sourced from global database; species-level values used when available, otherwise plot average; for 20% cases with no botanical information, plot average density used.
- Individual-tree carbon totals summed per plot to yield ACD (Mg ha^-1); scaling applied for small-tree measurements on nested plots.

## Details of data structure
- For each plot, the following fields are recorded:
  - Plot Identifier
  - Coupe Name
  - Plot identifier (plot network + plot number)
  - Forest/Restoration context (FACE; “Project Scenario”; “Baseline”; “N/A”)
  - LoggingMethod (High lead; Tractor; UnLogged)
  - Year logged
  - YearsSinceLogging
  - MeasureTime (year of census)
  - Dataset (INDFORSUS, FACE, or RIL_PinardLincoln)
  - ACD (Mg ha^-1)
  - Other contextual fields: plot location and forest status (Logged/UnLogged)

## Provenance and references
- Core documentation and methodological details drawn from:
  - Face the Future (INFAPRO) rehabilitation documents (2011)
  - Foody et al. (2001); Foody & Cutler (2003); Tangki & Chappell (2008)
  - Lincoln (2008); Pinard & Putz (1996)
  - Philipson et al. (in press) for carbon modelling and analysis
- Code for data analysis and modelling accessible at: https://doi.org/10.5281/zenodo.3885641

## Practical notes for data stewardship and reuse
- Dataset combines three independently developed plot networks; harmonization across protocols is necessary for cross-network analyses.
- Metadata captures key governance aspects: restoration scenario, logging method, year of logging, and census timing to support data discovery and reuse.
- Data quality controls are explicit and documented; provenance and data lineage are clear, facilitating audit and updates.
- The dataset has a published version (Document version 1.05-06-20); authors and affiliations are provided, with a clear path to supporting analyses and related publications.