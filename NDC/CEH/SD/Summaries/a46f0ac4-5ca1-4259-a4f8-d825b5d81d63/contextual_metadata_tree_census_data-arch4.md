# Tree census and Above Ground Biomass variation in permanent monitoring plots along an altitudinal and forest perturbation gradient in Andean ecosystems in Colombia, 2017-2020

- Overview
  - Dataset collected from 2017 to 2020 across 27 permanent forest plots (0.5 ha each) in five locations along an altitudinal gradient (lowland, mid-elevation, highland) and a forest perturbation gradient (low, medium, high) in Andean Colombia.
  - Variables include tree diameter (DBH), height, species (APG III nomenclature), family, Above Ground Biomass (AGB), perturbation level, altitude, and plot code.
  - Objective: investigate factors shaping forest change across gradients and evaluate forest composition; part of the BioResilience transdisciplinary project on forest ecosystem resilience post-conflict; funded by UK NERC (NE/R017980/1).

- Study design and scope
  - 27 permanent plots (0.5 ha each) distributed across three altitude bands: lowlands (0–1200 m), midlands (1200–2200 m), highlands (2200–3200 m).
  - Perturbation gradient categories: low (>30 years since last perturbation), medium (20–30 years), high (<20 years).
  - Three plots per perturbation level within each altitude band.

- Location details and gradients
  - Lowlands: Serranía de las Quinchas (Puerto Boyacá, Boyacá) with plots in Reserva Natural de las Aves el Paujil and nearby private properties.
  - Midlands: Reserva biológica Cachalú (Encino and Charala, Santander) and Tenasucá de Pedro Palo in Catalamonte, Cundinamarca.
  - Highlands: Reserva Biológica El Encenillo (Guasca, Cundinamarca) and Martos (Guatavita, Cundinamarca).
  - Site descriptions include climate and vegetation context (temperature ranges, rainfall, forest types) and associated references.

- Plot establishment and measurement protocol
  - 27 plots of 0.5 ha each, divided into 10 x 10 m subplots; GPS coordinates recorded for relocation; subplots marked with yellow rope and PVC markers.
  - Timing: field campaigns conducted between 2017 and 2020 (specific months per site noted).
  - Tree census procedures: systematic stem numbering, labeling for multi-stemmed individuals and recruits; census conducted per plot.

- Measurements and calculations
  - Measurements: diameter at the correct measurement point (POM) at 1.3 m; DBH ≥ 5 cm measured; ten stems per plot measured for height to calibrate manual estimates; morphospecies identified in the field; one specimen per morphospecies per location collected for taxonomic verification by CAV.
  - Height estimation: calibrated using field measurements and Hypsometer-based methods; AGB estimated using pantropical allometric models (Chave et al., 2014) via the BIOMASS package in R; height retrieval using Feldpausch et al. (2012).
  - Data recorded with ForestPlots.net field formats.

- Data structure and content
  - Primary data file: plot_data_nerc.csv
  - Eight columns: Family, Species, Diameter (D in mm), Height (m), Transformation (High/Low/Mid), Above Ground Biomass (AGB in Mg), Altitude, plot.id.
  - Diameter values range roughly 50–1634 mm; Height 1–40 m; AGB range 0.001–21.164 Mg.
  - Taxonomic identification aims for consistency via CAV verification; data include disturbance gradient and plot metadata.

- Quality control and data management
  - Rigorous quality control focusing on accuracy, completeness, and consistency of data and metadata.
  - External review of databases and metadata to check structure, missing values, data typing, and duplication.
  - Documentation includes data transformation details and unit specifications to enable reproducibility.

- Fieldwork equipment and workflow
  - Key tools: pole pruners, pruning shears, bags for botanical material, masking tape, indelible markers, tree tags and nails, hammer, diametric tapes, data worksheets, and yellow paint for POM marking.
  - Calibration and data integrity steps: equipment preparation, accuracy verification, and standardized measurement protocols.

- Access and references
  - Data generated under the BioResilience project; references provided for methods and site contexts (Chave et al. 2014; Feldpausch et al. 2012; and regional ecological references).
  - Data collection and computation workflows align with established tropical forest biomass estimation practices.