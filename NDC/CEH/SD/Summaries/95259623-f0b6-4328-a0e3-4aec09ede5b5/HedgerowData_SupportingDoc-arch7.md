# Biodiversity and structural data from hedgerow management and rejuvenation experiments in England, 2005-2016

- Overview
  - A comprehensive dataset from three long-running hedgerow experiments in England (2005–2016), focused on how cutting regimes and rejuvenation affect hedgerow biodiversity and structure.
  - Aims include assessing effects of simple cutting regimes on wildlife habitat and food resources, and testing practical, low-cost hedgerow restoration options suitable for large-scale management under ELS/HLS.
  - Five field sites across England (e.g., Monks Wood, Marsh Gibbon, Woburn, Waddesdon, Yarcombe) with hedge plots organized for factorial treatment applications and rejuvenation treatments.
  - Data collection spanned vegetation, flowers, berries, pollinators, invertebrates, and hedge structure, with both baseline and repeated measures.

- Experimental designs and sites
  - Experiment 1 (2006–2014)
    - Randomised plot experiment on four hedgerows planted in 1961 at Monks Wood.
    - 32 contiguous plots of 15 m length; factorial treatments of cutting frequency (annual, every 2 years, every 3 years) and cutting timing (autumn vs winter).
    - Two unmanaged controls monitored (hedges not cut in 15+ years).
    - Cutting: tractor-mounted flail cutter; otherwise, standard hedgerow maintenance. Yearly cutting cycle summarized in accompanying data.
  - Experiment 2 (2010–2016)
    - Randomised block design across four field sites to test effects on basal flora species richness.
    - Treatments (2×2×3): Time of cutting (Autumn vs Late Winter), Intensity (Standard vs Incremental), Frequency (Annual, Biennial, Triennial).
    - Full factorial with three replicates per treatment per site; hedge sections 15–20 m long.
    - Winter cutting not applied at one site (WB) due to site constraints.
  - Experiment 3 (2010–2013 rejuvenation and post-management)
    - Rejuvenation applied to 24 m hedge plots (various techniques) to restore hedgerows.
    - Rejuvenation treatments (12 replicates across sites): Midlands hedge-laying, Conservation hedge-laying, Wildlife hedging, Circular saw reshaping, Coppicing, Control.
    - Post-rejuvenation management in a split-plot design (autumn 2011–2013) with varying cutting frequencies (annual, every 2–3 years, or uncut).
    - Five field sites; some sites had restrictions (e.g., CB not all treatments applyable due to hedge maturity).

- Data collected and structure
  - Vegetation and baseline data
    - BaselineSpecies.csv: species present, cover, and depth within hedges; unique ID by experiment, site, plot, aspect, visit year, species.
    - BaselineParameters.csv: non-species hedge parameters (height, multiple width points, gap metrics, adjacent land, historic management, ditch info, field margins).
  - Vegetation and structure measures
    - Flowers.csv and Dimensions.csv: annual flower production and hedge dimensions (height/width) per replicate, used to convert to per-hedge-length metrics.
    - Gap.csv and Structure.csv: hedge gaps and overall hedge coverage derived from photo analysis; height/width context across height classes and photo years.
  - Berry resources
    - Berries.csv: counts and weights (total, subsamples) by species, per plot and year.
    - BerriesQuadrats.csv: quadrat-level berry counts and proportions for specific species.
  - Pollinators and plant-pollinator interactions
    - Pollinators.csv and related files (PollinatorsFieldMarginFlowers.csv, PollinatorsFlowersCounts.csv, PollinatorsFlowersQuadrats.csv, PollinatorsHedgeFlowers.csv): timed pollinator observations, taxa, temperature/visibility context, and matching plant species data.
    - Field-margin flowering data and quadrat-level flowering interactions across time.
  - Invertebrates
    - Invertebrates.csv and InvertebratesWeight.csv: counts and weights by taxa, collected via beating or guttering methods.
    - InvertebrateEggSurveys.csv: Lepidoptera eggs for select species.
  - Hedgerow regrowth and recovery (Experiment 3 focus)
    - ShootCount.csv and ShootMeasurements.csv: shoot counts and growth metrics post-rejuvenation.
    - RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv: multi-faceted data on aerial regrowth, branch regrowth, leaves, seedlings, stools, and biomass weights.
  - Recording and data integrity
    - Data collected on standardized paper sheets, transcribed to Excel, then loaded into an Oracle database.
    - Quality control included standardized protocols, expert review of species lists, and anomaly checks during entry/import.
    - Historic/pre-2010 data present for Experiment 1; missing values attributed to surveyor omissions or post-upload corrections.

- Treatment codes and data organization
  - Treatments coded in a consolidated table (1–25) reflecting combinations of frequency, timing, intensity, rejuvenation type, and cut patterns (e.g., annual standard autumn cut; hedgelaying variations; control-uncut; etc.).
  - Experiment and site identifiers, hedge plots, aspect, and visit dates are used to link records across datasets.
  - File structure includes: BaselineSpecies.csv, BaselineParameters.csv, Flowers.csv, Dimensions.csv, Berries.csv, BerriesQuadrats.csv, Pollinators.csv, PollinatorsFieldMarginFlowers.csv, PollinatorsFlowersCounts.csv, PollinatorsFlowersQuadrats.csv, PollinatorsHedgeFlowers.csv, Invertebrates.csv, InvertebratesWeight.csv, InvertebrateEggSurveys.csv, Gap.csv, Structure.csv, ShootCount.csv, ShootMeasurements.csv, RegrowthAerial.csv, RegrowthBranch.csv, RegrowthLeaves.csv, RegrowthSeedlings.csv, RegrowthShoots.csv, RegrowthStool.csv, RegrowthTotals.csv, RegrowthWeight.csv.

- Data accessibility and provenance
  - Data collected under Defra project BD2114 and managed by UKCEH; funding acknowledged.
  - All data exports referenced with date stamps (January–February 2020) and are prepared for integration into GIS workflows via plot-centric identifiers and year-by-year attributes.

- How this supports GIS and data-product development
  - Provides spatially explicit hedge plots with consistent IDs across experiments and years, enabling map-based visualization of hedge management regimes and biodiversity outcomes.
  - Rich attribute layers: hedge height/width, gap metrics, canopy structure, and rejuvenation treatments, enabling hedgerow health and connectivity mapping.
  - Temporal dimension: multi-year data allow time-series visualization of management effects on vegetation, pollinators, invertebrates, and regrowth.
  - Multi-taxon biodiversity data (plants, berries, pollinators, invertebrates) support species distribution modeling and habitat suitability mapping.
  - Data quality notes and clear provenance aid in reproducible GIS analyses and data standardization for map products.

- Additional notes
  - Historic data exist for Experiment 1 with imperfect date resolution; most records have visit year and date fields where available.
  - Anomalies (e.g., 2014 MG site cutting error) are documented and may affect specific time-series at that site.