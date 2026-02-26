# Data access, licensing and citation

- License and access
  - Data are available under the Open Government Licence.
  - Access: https://doi.org/10.5285/28208be4-0163-45e6-912c-2db205126925

- Citation requirements
  - When using the data, cite: Brennan, G.; Creer, S.; Griffith, G. (2020). Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/28208be4-0163-45e6-912c-2db205126925

- Data provenance and collection
  - Data collected by quantitative PCR (qPCR) targeting the ITS2 region of common UK grasses; species include Anthoxanthum odoratum, Arrhenatherum elatius, Cynosurus cristatus, Dactylis glomerata, Lolium perenne, Phleum pratense, Poa pratensis, grass species within Alopecurus/Agrostis, and one degenerate probe.
  - Instrumentation: QuantStudio 6 Flex Real-Time qPCR; copy numbers quantified using standard curves (2 to 2×10^5 copies/µl).
  - Sampling device: Burkard Automatic Multi-Vial Cyclone Samplers (airflow 16.5 L/min) collecting aerial particles onto 1.5 ml vials.
  - Target: only aerial particles originating from plants.

- Timing and location
  - Seasons: grass pollen seasons 2016 and 2017.
  - Dates: 2016 sampling 25 May–28 August; 2017 sampling 5 May–10 September (dates varied by site).
  - Geography: 13 sites across the UK; sites on exposed rooftops (4–6 floors) to sample mixed air flow; avoid vents and sheltered locations; Bangor site included outside Met Office network.

- Sampling strategy and data scope
  - Sites chosen to cover broad geographic variation (heterogeneous soils/land use) and aligned with Met Office UK Pollen Monitoring Network requirements.
  - Sampling unit deployed alongside a seven-day Burkard pollen trap; pollen counts from network used for context.
  - Research sample type: aerial particles (pollen) collected for molecular analysis; Bangor used the same pollen-count methodology.

- Data exclusions and quality control
  - From 1,400 daily aerial samples, 1,210 proceeded to downstream molecular analysis.
  - Exclusions reasons: pollen extraction failed due to heavy rainwater; qPCR efficiency outside acceptable range ( <85% or >115% );
  - Replicate quality: samples with high variability across three technical replicates (>6.95 for SD-based criterion) excluded.
  - Cycle thresholds: amplified outside 10–38 cycles excluded to reduce false positives/negatives.

- Reproducibility and randomization
  - Controls: positive and negative controls used to assess reliability.
  - Randomization: DNA extracts randomized for qPCR on a single plate; randomization applied to 96-well or 384-well plate layouts for data collection.

- Data structure and access
  - Main data file: qPCR_copy_number_abundance_data_aerial_DNA.csv.
  - Table 1 describes column headers (e.g., Site, Target.Name, Start/End dates, number of days pooled, qPCR metrics, sampling metadata, and geographic coordinates).
  - Header details include: QPCR identifiers, site IDs, target species, sampling dates, standard curve metrics (Y-Intercept, R^2, Slope, Efficiency), mean/SD/variance of copy numbers, CT values, and geographic coordinates (Lat, Long).

- Practical notes for data reuse
  - Data are organized to enable end-user self-service analysis (e.g., dashboards, pivot-style exploration) with accompanying metadata.
  - Clear documentation of sampling periods, locations, and quality-filtered data points supports reproducibility and secondary analyses.