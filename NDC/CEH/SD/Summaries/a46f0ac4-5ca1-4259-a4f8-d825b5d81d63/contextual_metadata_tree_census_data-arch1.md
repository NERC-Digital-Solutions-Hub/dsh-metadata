# Tree census and Above Ground Biomass variation in permanent monitoring plots along an altitudinal and forest perturbation gradient in Andean ecosystems in Colombia, 2017-2020

- Purpose and scope
  - Aims to investigate factors influencing forest change across altitudinal and perturbation gradients and to evaluate forest composition.
  - Part of the BioResilience project, a transdisciplinary study on forest ecosystem resilience after Colombia’s postconflict period.
  - Data collection timeframe: 2017–2020.

- Study design and sampling frame
  - 27 permanent forest plots, each 0.5 ha, distributed along three altitude bands: lowlands (0–1200 m), midlands (1200–2200 m), highlands (2200–3200 m).
  - Forest perturbation gradient with three levels: low, medium, high disturbance/recovery.
  - 3 plots per level of perturbation within each altitude category, totaling 27 plots.
  - Locations cover five sites across Colombia: Quinchas (lowlands), Pedro Palo and Encino (midlands), Encenillo and Martos (highlands).

- Data collected per plot
  - Tree measurements: diameter (D) in mm and height (m) for sampled trees.
  - Above Ground Biomass (AGB) in Mg calculated for each tree.
  - Taxonomy: species (binomial name) and family (APG III standard).
  - Metadata: disturbance gradient, elevation category, and a plot code.
  - Amount of data: 5225 individuals (lowlands), 9338 (midlands), 11824 (highlands) measured.

- Measurement protocols
  - Diameter measured at 1.3 m (POM) using a yellow-marked point; DBH ≥ 5 cm targeted.
  - Height measured on ten stems per plot with a hypsometer; remaining heights calibrated from these measurements.
  - Recruits labeled systematically; multi-stems labeled with a main stem and branch suffixes.
  - Botanical material collected for morphospecies identification; one specimen per morphospecies per disturbance gradient identified by a specialist (CAV) to ensure consistent taxonomy.

- Data collection and management
  - Plot locations and relocation data captured with GPS; plots subdivided into 10 × 10 m subplots with permanent markers.
  - Field data recorded using ForestPlots.net field formats.
  - Data and metadata subject to calibration steps and quality control, including external review for structure, completeness, and consistency.
  - Data provenance and discoverability emphasized; datasets and metadata are tracked and prepared for portal upload.

- Biomass estimation and data transformation
  - Above Ground Biomass (AGB) estimated using pantropical allometric models (Chave et al. 2014) via the computeAGB function in R (BIOMASS package).
  - Tree height estimated using the retrieveH function (Feldpausch et al. 2012).
  - Transformation categories (High, Mid, Low) describe disturbance level and recovery stage.

- Dataset structure and access
  - Primary dataset: a single CSV file titled plot_data_nerc.csv with eight columns: Family, Species, Diameter (D), Height, Transformation, Above Ground Biomass (AGB), Altitude, plot.id.
  - Units: D in millimeters; Height in meters; AGB in megagrams (Mg).
  - D ranges from 50 to 1634 mm; Height from 1 to 40 m; AGB from 0.001 to 21.164 Mg.

- Data quality, calibration, and validation
  - Calibration and accuracy checks performed on instruments and measurements.
  - External validation of metadata and database structure to ensure accuracy, completeness, and consistency.
  - Taxonomic identifications centralized to a single authority to minimize bias in diversity measurements.

- Context and references
  - Supported by the UK Natural Environment Research Council (NE/R017980/1).
  - Grounded in related literature on pantropical biomass estimation and Andean forest ecology.

- Potential uses for analysts
  - Analyze correlations between altitude, disturbance, and forest structure/biomass.
  - Develop predictive models of AGB across gradients and over time.
  - Inform resilience assessments and management decisions within Andean forest ecosystems.
  - Ensure reproducibility and data sharing through documented datasets and metadata.