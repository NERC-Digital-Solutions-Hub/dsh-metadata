# Persistence and UV exposure of Salmonella Typhimurium on plastic and glass with virulence assessment in Galleria mellonella

- Purpose and scope
  - Evaluate the ability of a clinically relevant Salmonella Typhimurium strain to colonise and persist on plastic waste (LDPE) and glass, and to withstand environmentally relevant UV exposure.
  - Assess virulence of recovered bacteria using the Galleria mellonella infection model.
  - Align with UKRI NERC grants on microbial hitchhikers in the plastisphere and related environmental studies.

- Experimental design and conditions
  - Materials: glass and LDPE plastic.
  - Photoperiod and UV exposure: 4 h white light; 4 h UV (UV index 8); 4 h white light; 12 h darkness.
  - Temperature: continuously monitored and controlled; data logged every hour.
  - Sampling schedule: 1, 2, 3, 6, 8, 10, 14, and 21 days after inoculation (DAI) for persistence; virulence assessed in Galleria over 72 hours.
  - Inoculation and environments: strains inoculated on materials in nutrient-rich and surface water conditions; UV exposure applied via bespoke frames and controlled lighting.

- Data and variables collected
  - Five CSV data files:
    - Persistence_Salmonella_UV_exposure.csv: persistence levels on plastic and glass under UV exposure, including dry, submerged, and surrounding water conditions.
    - Concentration_killing_curve_Galleria_control.csv: virulence levels in the Galleria mellonella model using a dilution series of Salmonella Typhimurium D23580.
    - Virulence_in_Galleria_mellonella_model.csv: virulence of D23580 recovered from PE and glass after exposure.
    - Temperature_logger_data.csv: temperature records throughout the study.
    - Linear_decline_analysis.csv: die-off rates and related metrics.
  - Key variables encoded in the datasets:
    - Material (Plastic/Glass), Condition (Dry/Submerged/water), UV (UV/No_UV), Time (Days or Hours), Concentration (CFU/ml), Survival (%), replication data, and derived metrics (R-squared, Gradient, K Day-1, D-value).

- Analytical approaches
  - Die-off analysis: log-linear regression on log10-transformed CFU data to derive die-off constant k (per day) and decimal reduction times (t90).
  - Statistical testing: ANOVA to assess effects of treatment factors; Holm-Šídák post-hoc tests for multiple comparisons.
  - Multivariate analysis: two- and three-way ANOVAs (strain, temperature, material) using SPSS v28 to explore combined effects.
  - Virulence assessment: Galleria survival data used to evaluate pathogenicity across doses and after recovery from surfaces.
  - Validation and verification: confirmatory PCR targeting ttr gene for Salmonella identity; routine calibration of plate reader and PCR thermocycler.

- Quality control and data integrity
  - Biological triplicates for key experiments.
  - Replicates maintained in controlled laboratory conditions; temperatures and lighting strictly regulated.
  - Data completeness noted with missing entries marked as ND.
  - Strain verification performed via PCR.

- Data provenance and collection context
  - Location: Scotland, UK.
  - Timeframe: February to August 2024.
  - Experimental workflow: surface inoculation on glass and PE; exposure to a defined UV regime; periodic sampling with bacterial enumeration; parallel virulence testing in Galleria mellonella.
  - Galleria assays included negative PBS controls to account for handling mortality.

- Relevance for environmental monitoring and policy
  - Provides standardized, QA-backed datasets on pathogen persistence on environmental plastics and glass under UV stress, with virulence context.
  - Supports monitoring and risk assessment of microbial hitchhikers in the environment and informs management strategies around plastic waste and UV exposure scenarios.
  - Data structure and documentation facilitate integration into monitoring portals and broader environmental health analyses.

- Completeness and metadata notes
  - Datasets are structured with explicit metadata for materials, conditions, timepoints, and replicates.
  - Documentation includes detailed column descriptions and data units; missing data flagged as ND.

- Related references and context
  - Contextual findings linked to prior work by Ormsby and collaborators on persistence and virulence of environmental microbes on plastic waste and under UV stress.