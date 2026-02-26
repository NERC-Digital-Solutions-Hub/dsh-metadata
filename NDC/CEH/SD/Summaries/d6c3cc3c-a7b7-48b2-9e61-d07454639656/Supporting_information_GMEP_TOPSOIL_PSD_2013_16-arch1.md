# GMEP_TOPSOIL_PSD_2013_16.csv

- Aim and context
  - Welsh Government Glastir Monitoring and Evaluation Programme (GMEP) studies soil quality effects to assess Glastir interventions and to quantify baseline status and trends related to climate change, biodiversity, soil and water quality, and woodland expansion.
  - Seeks evidence on drivers of change (land use, climate, pollution) beyond Glastir interventions.

- Survey design and sampling framework
  - 4-year rolling survey (2013–2016) to maximise site coverage while enabling year-on-year monitoring of spatial and temporal trends.
  - Two components: Wider Wales (baseline estimation, national trends) and Targeted Component (Glastir priority areas).
  - Common unit of analysis: 1 km grid; 300 1-km squares sampled over the cycle.
  - Sampling strategy: half squares chosen as Wider Wales; half targeted at Glastir priority areas.
  - Exclusions: squares with >75% urban land or >90% sea.
  - Sample collection within each square: five randomly dispersed soil sampling locations; 15 cm C-core soil cores collected, vegetation surveys co-located.

- Particle size distribution (PSD) focus
  - PSD is a key soil property influencing hydrology, nutrient transport, erosion, soil biota, and productivity.
  - Methods compared: Laser diffraction (LD) vs hydrometer (Gee & Or, 2002).
  - Instruments and materials: Beckman Coulter LS13 320 LD instrument; Calgon (5% Na hexametaphosphate + Na2CO3); platform shaker; organic matter removal via peroxide digest; 63 µm sieve for sand fraction collection.

- Quality assurance and quality control (QA/QC)
  - Adherence to NERC Joint Codes of Practice; inclusion of standard soils (BS1, BS3) in each batch; duplicate samples (1 in 10) to test reproducibility.
  - Instrument calibration, pre-run rinsing, sand flush, and background checks.
  - Cross-check of LD results with sand recovered from sieve; generally good agreement; organics (LOI 40–50%) can cause LD overestimation of sand.
  - Comparison with hydrometer method showed method-related differences; LD tends to align better with newer understanding of clay size; adjustments discussed (e.g., clay/silt cut-offs).
  - Standards and reproducibility tests: Garnet (nominal median size ~13.8 µm) measured as 13.35 ± 0.3 µm; glass beads (~581 µm) measured as 577 ± 26.85 µm.
  - Final LD size-class cut-offs used: Sand 64.61–2000 µm; Silt 2.42–63.41 µm; Clay 0.04–2.41 µm.

- Data quality, comparability, and inter-lab benchmarking
  - LD method validated against hydrometer results for internal standards (BS1, BS3) with differing PSDs; deviations largely within expectations, with method-specific biases acknowledged.
  - Inter-lab comparisons with ADAS and BGS using sandy, clay, and silty soils showed LD results to be accurate, reproducible, and comparable.

- Data structure and metadata
  - Dataset: GMEP_TOPSOIL_PSD_2013_16.csv
  - Key fields (examples):
    - SQ_ID: Unique 1 km square identifier (anonymised)
    - PLOT_TYPE, PLOTNUM, PLOTYEAR: Plot characteristics and sampling year
    - EASTING_10km, NORTHING_10km: Spatial coordinates (OSGB 1936)
    - LC: ITE Land Classification code
    - REPEATED: Repetition indicator (NA if not repeated)
    - BATCH: Batch number (nested within year; 2013–2014 combined in 11 batches)
    - um0.03999 to um2000: Percentage of particles in size bins (µm) with upper-limit columns
    - SAND, SILT, CLAY: Percentages in respective size ranges
    - TOTAL: QA/QC total
  - Purpose of metadata: Enables traceability, reproducibility, and integration with other surveys (e.g., Countryside Survey).

- Implications for analysis and use
  - Enables national and sub-national indicators of soil PSD and its drivers, with integration potential across Wales and GB datasets.
  - Provides a robust, QA/QC’d PSD dataset at 1 km scale suitable for examining links between soil texture, land use, climate, and pollution effects within the Glastir context.
  - Documented methodology and cross-lab benchmarking support data comparability and future harmonisation with external laboratories.

- References and affiliations
  - Key references include foundational PSD methods (hydrometer, pipette), laser diffraction literature, and Glastir/GMEP annual and final reports.
  - CEH (UK) and Bangor University personnel contributed to QA, data processing, and fieldwork, with field teams listed.

- Endnotes
  - The dataset reflects a comprehensive, multi-scale soil monitoring effort (1 km grid) designed to detect spatial and temporal trends and to relate soil quality changes to Glastir interventions and broader environmental drivers.