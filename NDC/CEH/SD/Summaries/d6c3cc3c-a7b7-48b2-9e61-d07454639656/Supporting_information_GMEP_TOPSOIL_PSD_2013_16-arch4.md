# Glastir Monitoring & Evaluation Programme

- Purpose and scope
  - Welsh Government AES monitoring since the 1990s, with Glastir focusing on soil quality and its relation to climate, biodiversity, soil and water quality, and woodland expansion.
  - GMEP aims to collect evidence on the status and trends of soil quality and to assess how Glastir interventions interact with drivers of change (land use, climate, pollution).
  - Uses a 4-year rolling survey to maximize site coverage and detect spatial and temporal changes cost-effectively; two components: Wider Wales (baseline and national trends) and Targeted (Glastir-priority areas); integrates data across metrics with a common 1km square unit.

- Sampling design and locations
  - Total of 300 1km squares sampled over the 4-year cycle; half randomly sampled within Land Classification strata (G Britain-based) and half targeted at Glastir priority areas.
  - Exclusion criteria: squares with >75% urban land or >90% sea excluded.
  - Sampling within squares: five predetermined random locations for soil sampling when possible.

- Field and sample collection
  - Soil samples collected using a black plastic core (C-core), 15 cm long, from locations co-incident with vegetation surveys.
  - Samples refrigerated and shipped to UK Centre for Ecology & Hydrology (CEH) Bangor laboratories within a few days.

- Particle size distribution (PSD) measurement
  - PSD is a fundamental soil property influencing hydrology, nutrient availability, erosion, and soil biota.
  - Methods used: laser diffraction (LD) with Beckman Coulter LS13 320 and traditional hydrometer method (Gee and Or, 2002) for comparison.
  - Calibration and standards: multiple reference soils and internal Bangor standards (BS1, BS3); duplicate samples used for reproducibility checks.
  - Quality assurance and control:
    - Adherence to NERC Joint Codes of Practice.
    - Regular instrument calibration, cleaning, and sand flush tests.
    - Sand fraction measured with a 63 µm sieve for cross-checks; high organic matter can affect LD results.
  - Data comparison and interpretation:
    - LD generally aligns with hydrometer results but shows differences in clay fractions, especially at lower particle sizes.
    - Consideration of adjusting clay/silt cut-offs (e.g., using 8 µm for clay-silt boundary) to better align methods.
    - Validation with standards (Garnet ~13.8 µm; Glass beads ~581 µm) confirms LD accuracy, particularly in the low size range.

- Final PSD definitions and data quality
  - Final LD cut-offs used:
    - Sand: 64.61 – 2000 µm
    - Silt: 2.42 – 63.41 µm
    - Clay: 0.04 – 2.41 µm
  - Data accuracy and reproducibility demonstrated through internal standards and cross-lab comparisons (ADAS, BGS, Bangor).

- Data structure and metadata
  - File: GMEP_TOPSOIL_PSD_2013_16.csv
  - Key fields include: SQ_ID (anonymized 1km square), PLOT_TYPE, PLOTNUM, PLOTYEAR, EASTING_10km, NORTHING_10km, LC (Land Classification), REPEATED, BATCH, and PSD size-bin percentages (SAND, SILT, CLAY) with TOT.
  - Metadata documents the sampling design, QA/QC procedures, and the relationships between measurements and site attributes.

- Data comparability and cross-lab benchmarking
  - PSD results compared with ADAS and BGS laboratories using shared standard soils; LD-based results shown to be accurate and reproducible and comparable to other labs.
  - Observed method-dependent differences in clay fraction emphasize the need for consistent data processing and potential methodological adjustments.

- Stakeholders, teams, and governance
  - UK CEH staff across multiple roles (database management, QA, lab management, data analysis, field coordination).
  - Bangor University staff and field survey teams contributing to sampling, processing, and data collection.
  - Emphasis on data management, QA/QC, and deriving national and sub-national indicators for Welsh environment monitoring.

- References and further reading
  - Foundational literature on PSD methods, LD vs hydrometer comparisons, and the Glastir Monitoring & Evaluation Programme reports and standards.