# Dataset Summary and contextual information

- Aim of the dataset
  - Provides Above-ground Carbon Density (ACD) estimates derived from tropical forest census surveys (1992–2016) to support monitoring, evaluation, and policy decisions related to forest carbon dynamics, restoration, and logging impacts in Sabah, Malaysia.

- Context and experimental design
  - Study area: Ulu Segama Forest Reserve (USFR) and Danum Valley Conservation Area (DVCA), Sabah, Malaysia; mixed globally logged and unlogged tropical lowland dipterocarp forest.
  - Logging history: USFR includes coupes logged 1972–1993 by tractor or high-lead methods; restoration treatments (climber cutting, tree planting) applied 1993–2004 in selected patches.
  - Plot networks (three independent datasets):
    - A. INDFORSUS: 0.1 ha plots (radius ~17.84 m) with measurements for trees ≥20 cm DBH; nested circles for smaller trees.
    - B. Pinard & Putz (1992): 0.08 ha plots with full plot measurements for ≥20 cm DBH; nested subplots for smaller DBH classes.
    - C. INFRAPRO (INFAPRO): four 0.05 ha circles (total ~0.2 ha) arranged in a cross; different DBH measurement intensities across circles.
  - Additional metadata: logging method, coupe, and year of logging provided by Yayasan Sabah; restoration scenario (FACE) and baseline/unlogged references recorded.
  - QC and data handling: numeric range checks, formatting checks, and logical integrity checks performed; data analysis and modelling described by Philipson et al. with code available on Zenodo.

- Fieldwork protocol and measurements
  - Network A (INDFORSUS): plots with a 17.84 m radius; measure all free-standing woody plants ≥20 cm DBH (and smaller classes in nested circles); DBH measured at 1.3 m unless buttress roots require adjustment.
  - Network B (Pinard & Putz): measures all trees ≥20 cm DBH across entire plot; nested subplots for 10–19 cm, 5–9 cm, and 1–5 cm DBH.
  - Network C (INFAPRO): four circles of 0.05 ha; DBH ≥20 cm measured in all circles; additional DBH classes measured in nested circles within the cross layout.
  - Units: Above-ground Carbon Density (ACD) reported in Mg ha−1.

- Allometric methods and carbon modelling
  - Carbon content assumed as 47% of aboveground biomass (AGB).
  - AGB estimated from DBH, tree height, and wood density using allometric equations (specific functional form provided in the dataset documentation).
  - Adjustments for measurement method when necessary:
    - DBH at 1.3 m (or equivalent via taper model for POM measurements) to standardize height measurement.
    - Height estimated with a three-parameter Weibull-based model when not measured directly.
  - Wood density values drawn from global databases; species-level values used when available; otherwise plot-average values applied.
  - The carbon calculation aggregates individual tree carbon to plot-level ACD (Mg ha−1); small-tree contributions on nested plots scaled to reported plot totals.

- Data structure and content
  - For each plot, key fields include:
    - Plot identifiers and network (INDFORSUS, FACE, or RIL_PinardLincoln)
    - Coupe name and logging information (LoggingMethod, Year logged, Forest status)
    - ACD (Mg ha−1) and FACE restoration scenario
    - YearsSinceLogging and MeasureTime (year of census)
    - Dataset name and related metadata
  - Data captures both restoration scenarios and logging history to enable comparisons between baseline, restored, logged, and unlogged conditions.

- Data quality, governance, and accessibility
  - Quality control applied at data collection and integration stages (range checks, formatting, logical integrity).
  - Clear metadata on plot-level attributes supports traceability and verification; however, the three networks were developed independently, presenting harmonization challenges for cross-network analyses.
  - Data sharing and governance emphasize transparency and openness, with dissemination of outputs and underlying data where appropriate; analysis code for ACD modelling is publicly accessible (Zenodo: https://doi.org/10.5281/zenodo.3885641).
  - References and provenance underpinning the dataset include multiple foundational studies and project documents (Face the Future INFAPRO; Foody et al.; Pinard & Putz; Lincoln; Philipson et al., in press).

- Relevance for monitoring frameworks
  - Enables long-term monitoring of carbon dynamics in selectively logged and restored tropical forests.
  - Supports policy evaluation of restoration programs and logging practices by providing consistent ACD estimates over time and across restoration scenarios.
  - Highlights the importance of harmonized protocols, metadata quality, and transparent data governance for reliable environmental health monitoring.