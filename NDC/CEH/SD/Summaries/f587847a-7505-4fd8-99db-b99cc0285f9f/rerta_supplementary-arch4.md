# Nitrous oxide and methane fluxes from different riparian restoration treatments in Oil Palm plantations in Riau, Indonesia 2019-2021

- Objective and context
  - Assesses greenhouse gas fluxes (N2O, CH4, CO2) across four riparian buffer treatments in oil palm plantations to guide growers and policymakers on environmental impacts.
  - Builds on concerns about oil palm expansion driving deforestation, biodiversity loss, and emissions; riparian buffers are regulatory and certification considerations, with growing interest in their ecosystem-service benefits.

- Experimental design and data collected
  - Project: Riparian Ecosystem Restoration in Tropical Agriculture (RERTA), within BEFTA collaboration (Cambridge University; SMARTRI).
  - Sites: Two RERTA sites (Kandista 2016; Ujung Tanjung 2019); this study conducted at Ujung Tanjung.
  - Four treatments in 50 x 400 m zones on both river sides:
    1) Immature oil palm – no restoration; replanting to river margin
    2) Mature oil palm – no restoration; 50 m buffer maintained
    3) Native trees – enrichment planting with forest trees in 50 m buffer; mature oil palm removed
    4) Mature oil palm and native trees – enrichment planting with forest trees; mature oil palm maintained
  - Replication: 6 replicates per treatment; 16 chambers in surrounding plantation.
  - Temporal scope: January 2019 to September 2021, with breaks for felling/replanting (Apr–Oct 2019) and Covid-19 (Jan–Jun 2021).
  - Data collected: Nitrous oxide (N2O), methane (CH4), and carbon dioxide (CO2) fluxes; soil moisture; chamber metadata.

- Field collection and laboratory methods
  - Chamber setup: 40 cm diameter collars installed 7 cm deep; lids seal chambers with draft excluders; sampling via 0, 15, 30, 45 minutes over 45-minute incubations.
  - Gas analysis: 100 mL samples analyzed by gas chromatography at UKCEH Edinburgh (μECD for N2O; FID for CH4 and CO2).
  - Environmental covariates: volumetric soil moisture measured around chambers using Theta probe at 7 cm depth.
  - Permits: Indonesian Foreign Research Permits (RISTEK) linked to project operations across years.

- Calibration, data processing, and quality control
  - Calibration: four-point calibration with mixed gas standards (CH4, CO2, N2O) run after about every 20 samples.
  - Flux calculation: RCFlux R package fit six models (linear, quadratic, asymptotic, HMR, best-fit) and selected the best-fitting model per chamber; fluxes expressed as μmol m^-2 s^-1 with 95% CIs.
  - Quality control: visual inspection of regression plots; data flagged as invalid only if clearly unreliable; most flux estimates derived from linear or HMR models.
  - Outputs and data structure:
    - rerta_ghg_rcflux.csv: flux estimates for each chamber (1–40) across sampling occasions; includes multiple model fluxes, best-fit method, confidence intervals, adjusted R², year, date, chamber details, location (east/west), plot type, treatment zone, and soil moisture.
    - rerta_chambers.csv: detailed metadata for the 40 chambers (RERTA_code, position, plot, treatment zone, treatment, planting date, installation date, latitude, longitude, elevation, etc.).
  - Data fields and units: comprehensive data dictionary provided within the CSVs to describe each variable (e.g., gasName, flux_linear, ci95lo_linear, adjr2_linear, bestFitMethod, date_installed, soil_moisture, diameter_cm, area_m2, etc.).

- Data governance, accessibility, and provenance
  - Data provenance documented via multi-year field program and permits; data linked to specific RERTA treatment zones and dates.
  - Spans two experimental sites with standardized protocols to enable cross-site comparisons.
  - Data products are structured for reuse (per-chamber and per-measurement records) and include metadata to support discoverability and reproducibility.

- Implications for data strategy and practice
  - Demonstrates end-to-end data lifecycle: from field sampling and lab analysis to model-based flux estimation and data curation.
  - Highlights the need for detailed metadata to enable understanding of treatment effects, spatial configuration, and temporal dynamics.
  - Aligns with data-leadership priorities: documenting data availability, ensuring data quality and traceability, and providing data structures that support user-friendly access for policy analysis and management decisions.

- Key takeaways for data systems in environmental management
  - Longitudinal, multi-treatment field experiments require robust data governance (permits, site metadata, replication records) to support policy-relevant analyses.
  - Use of standardized processing (RCFlux) and clear data dictionaries enhances comparability and reuse across researchers and decision-makers.
  - Data gaps or interruptions (e.g., pandemic-related breaks) should be explicitly captured to maintain transparency in trend interpretation and model confidence.