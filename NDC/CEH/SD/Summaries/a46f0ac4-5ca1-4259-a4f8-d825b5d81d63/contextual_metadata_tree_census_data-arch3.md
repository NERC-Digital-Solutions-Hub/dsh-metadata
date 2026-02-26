# Tree census and Above Ground Biomass variation in permanent monitoring plots along an altitudinal and forest perturbation gradient in Andean ecosystems in Colombia, 2017-2020

- Aim and scope
  - Establish and describe a long-term monitoring dataset to investigate factors driving forest change across an altitudinal and disturbance gradient in Colombian Andean ecosystems.
  - Part of the BioResilience project, aimed at understanding forest resilience after Colombia’s postconflict period.
  - Funded by the UK Natural Environment Research Council (NE/R017980/1).

- Study design and locations
  - 27 permanent forest plots (0.5 ha each) along a three-level altitude gradient: lowlands (0–1200 m), midlands (1200–2200 m), highlands (2200–3200 m).
  - Disturbance gradient: low, medium, high perturbation with three plots per level.
  - Locations span Quinchas (lowlands), Encino and Pedro Palo (midlands), Encenillo and Martos (highlands) with precise geographic and climatic context provided.

- Plot establishment and measurement protocol
  - Plots subdivided into 10 x 10 m subplots; GPS coordinates recorded for relocatability; plot corners marked with orange tubes and subplot corners with PVC markers.
  - Measurements conducted between 2017 and 2020; systematic stem numbering and labeling for multi-stemmed individuals.
  - Censuses included all woody stems with DBH ≥ 5 cm; recruits labeled relative to nearby trees.
  - Optimum measurement point (POM) fixed at 1.3 m; yellow paint used to mark POM on trees.

- Taxonomy, measurement, and biomass estimation
  - For each tree: diameter at POM, total height (measured on ten stems per plot using a hypsometer), species identification (morphospecies in field; voucher specimens collected for taxonomic verification by CAV).
  - Above Ground Biomass (AGB) estimated using pantropical allometric models (Chave et al. 2014) via the BIOMASS package in R; height estimates calibrated with retrieved height methods (Feldpausch et al. 2012).
  - Species names follow APG III; disturbance gradient and plot code captured as metadata.

- Data collection and management tools
  - Field data recorded using ForestPlots.net field formats.
  - Equipment list includes pruners, pruning shears, bags, markers, tree tags, nails, hammer, diametric tape, data worksheets, and yellow paint for POM marking.
  - Specimens identified by a recognized taxonomic authority to ensure consistency and reduce bias in diversity assessments.

- Data structure and content
  - Primary dataset stored as a single CSV file named plot_data_nerc.csv.
  - Eight columns: Family, Species, Diameter (D), Height, Transformation, Above Ground Biomass (AGB), Altitude, plot.id.
  - Variables include range and unit details: D (mm; 5 cm to 1634 mm), Height (m; 1–40 m), AGB (Mg; 0.001–21.164 Mg); altitude categories and plot identifiers provided.

- Data quality assurance and governance
  - Calibration steps and equipment preparation performed prior to measurements to ensure accuracy.
  - Comprehensive quality control, including external review of database structure, completeness, data typing, and absence of duplicates; metadata validation to ensure accuracy and consistency.
  - Emphasis on traceability, standardization, and reliability to support informed interpretation and policy-relevant conclusions.

- Data processing and analytical approach
  - AGB calculated with pantropical models (Chave et al. 2014); height estimated using established retrieval methods (Feldpausch et al. 2012).
  - Data prepared to support analyses of forest change and biomass variation across gradients, enabling assessments of ecosystem resilience in postconflict contexts.

- Context and references
  - BioResilience project background and related ecological and methodological references underpin the study design and biomass estimation approach (e.g., Chave et al. 2014; Feldpausch et al. 2012; local ecological surveys and region-specific sources cited).

- Implications for monitoring framework practice
  - Demonstrates a robust, gradient-based monitoring framework with standardized plot design, transparent measurement protocols, and rigorous QA.
  - Highlights the importance of metadata-rich datasets, open-format data (ForestPlots.net formats), taxonomic verification, and reproducible biomass calculations for informing policy, management decisions, and future monitoring cycles.
  - Provides a replicable template for long-term forest monitoring in heterogeneous landscapes, including clear data structure, documentation, and data governance practices.