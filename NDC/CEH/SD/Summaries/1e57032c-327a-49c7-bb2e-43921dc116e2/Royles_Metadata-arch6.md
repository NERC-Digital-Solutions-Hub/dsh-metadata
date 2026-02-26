# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements.

- Study aims and scope
  - Investigates moss physiology and stable isotope ecology to model spatial and temporal climatic signals.
  - Focuses on field measurements and dark-adapted PAM fluorescence to link moss physiology with climate data.

- Field sites and taxa
  - Dersingham Bog (52.83° N, 0.48° E): bog heathland; multiple moss species including Aulacomnium palustre, Dicranum scoparium, Sphagnum spp.
  - Brandon Country Park (52.43° N, 0.62° E): heathland; Pleurozium schreberi, Polytrichastum formosum.
  - Wicken Fen: shaded woodland and fen habitats; species such as Brachythecium rutabulum, Calliergonella cuspidate, Kindbergia praelonga.
  - Targeting a range of moss lifeforms and growth conditions to provide analogues for palaeoclimate work.
  - Voucher specimens verified by bryologists; field permissions obtained from landowners/managers.

- Sampling design and field procedures
  - Fieldwork approximately monthly from April 2017 to September 2018.
  - On each visit: three samples per target species (each ~2 x 2 x 2 cm) collected and stored separately.
  - Chlorophyll fluorescence measurements (in the field from June 2017 onward) using Walz MINI-PAM II:
    - Three measurements per sample in light.
    - Samples dark-adapted for at least 30 minutes, then three additional measurements in the dark.
    - Calculated metrics: fluorescence yield (Φ), non-photochemical quenching (NPQ), and electron transport rate (ETR = 0.84 × PAR × 0.5 × Φ; units μmol electrons m^-2 s^-1).
  - Water content and tissue analyses:
    - Fresh sample weighed (≈0.3 g) and dried at 70°C to determine field relative water content (RWC = (Fresh − Dry) / Dry; expressed as proportion of dry mass).
    - Dry moss subjected to standard cellulose extraction (Soxhlet) and water extraction by cryogenic vacuum distillation.
    - Fresh water samples collected at each site; precipitation collected near the study area center.
  - Enzymatic and biochemical analyses (selected samples):
    - Enzymatic, photo-spectrophotometric sucrose content analysis (standard procedures).

- Isotope and chemical analyses (highlights)
  - Water isotopes (fresh moss distillates and water samples): δD and δ18O determined at Lancaster Environment Centre.
  - δD: measured by Isoprime100 IRMS after glass-wool filtration; precision ±1‰.
  - δ18O: measured by Isoprime100 IRMS after pyrolysis; precision ±0.5‰.
  - Oxygen isotopes: measured at Godwin Laboratory (Cambridge) using EA-IRMS with calibration to V-SMOW; precision better than 0.4‰.
  - Carbon isotopes: δ13C measured at Godwin Laboratory with calibration to IAEA standards; precision better than 0.1‰.
  - Standards and traceability: VSMOW, IAEA reference materials, and lab-specific in-house TAP standards; all linked to VSMOW-GISP scale.

- Datasets and data structure
  - Four CSV datasets:
    - Royles_Field_data_by_time
      - Captures: sample metadata, measurement types (RWC, C13, O18), chlorophyll fluorescence session data, location, species, collection date, and notes.
      - Key fields include: Location, Species, Session, Month/Date, RWC, C13, O18, Sphagnum flag, and descriptions.
    - Royles_RWC_and_Isotope_data
      - Contains sample-cellulose and reference numbers, wet/dry weights, dry tube information, isotopic percentages and ratios (δ13C, δ18O).
    - Royles_Sample_Number_Key
      - Mapping between sample reference numbers, collection date, location, species, herbarium notes (if applicable).
    - Royles_Water_Samples
      - Water sample details: date, location, type (fresh water or leaf distillate), source, and δ18O and δD values.
  - Data capture notes
    - All isotope analyses performed in duplicates per sample.
    - Measurements linked to standardized references with inter-laboratory calibration where applicable.

- Data quality, standards, and provenance
  - Replicates: duplicates for isotope measurements; triplicate field measurements per sample for fluorescence metrics.
  - Calibration and standards:
    - δD and δ18O calibrated to VSMOW/GISP scales with IAEA-standardized inter-laboratory standards.
    - Carbon isotopes calibrated using IAEA reference materials.
  - Documented references for methods (e.g., cellulose extraction technique, water extraction times, and fluorescence calculations) cited for reproducibility.

- Temporal and spatial coverage
  - Timeframe: April 2017 – September 2018 (monthly field visits).
  - Sites: Dersingham Bog, Brandon Country Park, Wicken Fen; multiple microhabitats (bog heathland, heathland, shaded woodland, fen).
  - Species coverage includes a mix of bryophytes typical of bogs, heathlands, and fen/moss communities.

- Potential uses and insights
  - Integrating moss physiological responses (PAM fluorescence metrics) with water content and isotope data to model climate-driven signals.
  - Cross-site comparisons of isotope signatures (δD, δ18O, δ13C) in relation to habitat, moisture status, and photosynthetic performance.
  - Establishing baselines for palaeoclimate proxy work using modern analogs and validating isotopic and physiological relationships.
  - Data products suitable for self-service exploration (e.g., dashboards or pivot-style analyses) and for informing future sampling strategies.

- References and methodological sources
  - Methodological foundations for cellulose batch processing and isotopic analyses:
    - Loader et al. (1997)
    - Stitt et al. (1989)
    - West et al. (2006)
  - Instrumentation and analysis platforms:
    - Walz MINI-PAM II for chlorophyll fluorescence
    - Isoprime100 IRMS and Thermo Delta V EA-IRMS for isotope measurements

- Access and reuse considerations
  - Datasets are organized for straightforward data integration and reuse, with explicit field names and units.
  - Careful attention to field metadata (location, date, species, sampling session) facilitates temporal and spatial trend analyses.