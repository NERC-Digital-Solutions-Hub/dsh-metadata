# GMEP TOPSOIL PSD 2013_16

## Overview and aim
- Welsh Government's Glastir Monitoring and Evaluation Programme (GMEP) monitors soil to assess the effectiveness of Glastir management interventions and to quantify soil quality status and trends related to climate, biodiversity, water quality, and woodland expansion.
- The goal is to synthesize and analyse data to understand how drivers (land use, climate, pollution) impact the Welsh environment beyond Glastir actions.

## Survey design and sampling frame
- Adopted a 4-year rolling survey for 2013–2016 to maximise site coverage while tracking year-on-year changes.
- Two components: Wider Wales baseline (national trends) and Targeted component (Glastir priority areas); integrated across components using a common 1 km square unit.
- Sampling frame: 300 x 1 km squares over the cycle.
  - Half randomly sampled within Land Classification strata (for robust national estimates).
  - Half targeted at Glastir priority areas.
- Exclusions: squares with >75% urban land or >90% sea.
- Purpose: enable spatial and temporal analysis and potential integration with the Countryside Survey of Great Britain.

## Field and laboratory methods
- Within each square, soil samples collected from 5 randomly dispersed locations using a 15 cm C-core, co-located with vegetation surveys.
- Samples refrigerated and sent to UKCEH Bangor laboratories for processing.
- Particle Size Distribution (PSD) measured primarily by laser diffraction (Beckman Coulter LS13 320) and validated against hydrometer methods.
- LOI and organic matter removal conducted prior to LD analysis; calibration and quality checks performed (standard soils, internal Bangor standards BS1/BS3, and repeated samples).
- Sand fraction collected with a 63 µm sieve at the end of analysis for cross-checking with LD results.
- Protocol adjustments and QA used to ensure data reliability, including instrument warm-up, alignment, run settings, and duplicate measurements.

## Quality assurance, QA/QC, and method evaluation
- Followed NERC Joint Codes of Practice; included standard soils with each batch; regular instrument calibration and sand flush checks.
- Duplicates (1 in 10 samples) used to assess reproducibility.
- Cross-checks against sieve data to corroborate LD results; high organic matter can slightly bias LD sand estimates, particularly for very organic soils.
- LD vs hydrometer comparison conducted using internal standards (BS1, BS3) to evaluate consistency; observed method-dependent deviations in certain size ranges, but overall LD found accurate and reproducible.
- Adjusted PSD size cut-offs to align LD results with literature: Sand 64.61–2000 µm, Silt 2.42–63.41 µm, Clay 0.04–2.41 µm.
- Inter-lab comparison with ADAS and BGS using multiple soil types demonstrated broad concordance, supporting method reliability and comparability.

## Data structure, metadata, and standards
- Metadata for the dataset (GMEP_TOPSOIL_PSD_2013_16.csv) includes:
  - SQ_ID: anonymised 1 km square identifier
  - PLOT_TYPE, PLOTNUM, PLOTYEAR: sampling plot details
  - EASTING_10km, NORTHING_10km: OSGB coordinates at 10 km resolution
  - LC: ITE Land Classification code
  - REPEATED: indicates if measurement was repeated
  - BATCH: batch number (nested within year; 2013–2014 analyzed together in 11 batches)
  - PSD bins: um0.03999 to um2000 representing particle-size fractions
  - SAND, SILT, CLAY: percentage of particles in defined size ranges
  - TOTAL: QA/QA total for the PSD fractions
- Structure supports integration with GB-wide data and future analyses across surveys.

## Data governance, sharing, and stewardship
- Data management led by UK CEH and Bangor University staff; data QA/QC processes documented and applied.
- Data uploaded to relevant portals; work is documented to support reuse and updates.
- Anonymised 1 km square identifiers protect location privacy while enabling discoverability and cross-study linkage.
- Clear provenance: sampling design, laboratory methods, QA/QC, and cross-method comparisons are documented to support reproducibility and transparency.

## Challenges and considerations for data stewards
- Balancing timely data return from multiple field teams and laboratories.
- Managing heterogeneity across 300 squares and across a 4-year cycle, including potential format differences between methods and labs.
- Ensuring ongoing interoperability with GB datasets (e.g., Countryside Survey) through consistent spatial units and metadata standards.
- Handling the impact of high organic matter on LD measurements and applying validated corrections to ensure comparability.
- Maintaining up-to-date documentation and versioning as methods evolve or re-calibrations occur.

## References and further reading
- Includes foundational methods and comparisons for PSD measurement (laser diffraction vs hydrometer), QA/QC practices, and cross-laboratory benchmarking.
- Key sources cover PSD methodology, land classification, and Glastir Monitoring & Evaluation Programme reporting.

## Acknowledgments
- Involvement across UK CEH, Bangor University, field survey teams, and staff responsible for data management, QA, and sample processing.