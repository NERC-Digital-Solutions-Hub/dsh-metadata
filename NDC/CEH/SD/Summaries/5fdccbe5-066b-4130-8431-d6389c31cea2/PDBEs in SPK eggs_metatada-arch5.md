# EXPERIMENTAL SECTION

- Context and purpose
  - PBMS (Predatory Bird Monitoring Scheme) in the UK archived failed/abandoned sparrowhawk eggs for PBDE analysis.
  - Study focused on long temporal coverage (1985–2007) within a small geographic area: eastern England near the Welsh border (within ~250 km).
  - Sampling design required 3–5 eggs per year from different nests; when multiple eggs from a nest were present, one was chosen at random due to unknown laying order.

- Sample collection and initial processing
  - Measured egg weight, length, and breadth; shells washed, air-dried, reweighed; contents homogenised and stored at -20°C until analysis.
  - Egg homogenates prepared for PBDE analysis; sample selection prioritized temporal breadth and geographic concentration.

- PBDE analysis methodology
  - Gas Chromatography–Mass Spectrometry (GC-MS) with specified column and standards; 27 PBDE congeners analyzed (tri- to octa-BDEs, including 17, 28, 32, 35, 37, 47, 49, 51, 66, 71, 75, 77, 85, 99, 100, 118, 119, 126, 128, 138, 153, 154, 166, 183, 190, 196, 197).
  - Instrument detection limits (LoD) ranged from 2.5 pg/μl to 12.5 pg/μl depending on congener; egg-level LoD varied (e.g., 0.063–0.316 pg/g wet weight).
  - Five procedural blanks per batch; blank corrections applied; recoveries for 13128 C12-labelled congeners 28, 47, 99, 100, 153, 154, 183 averaged 73.4–95.6%.
  - Quality control (QC) standard run with five PBDEs across 2.5–250 pg/μl; batches passed QC if concentrations were within ±10% of expected values.
  - Identification of three additional potential octa-BDEs (201, 202, 203) based on distinctive mass fragments; semi-quantified using calibration curves for BDEs 196 and 197 due to lack of specific calibrants.

- Data processing and normalization
  - Results presented on a wet weight basis and desiccation-corrected using total egg weight/volume ratio.
  - Egg volume estimated via V = 0.51 × L^2 (L = length, B = breadth); damaged eggs used mean volume/weight ratio from undamaged eggs when possible.
  - Shell index calculated as shell weight (mg) / (shell length × breadth in mm).
  - Below-LoD values:
    - For congeners with less than 20% below-LoD across eggs, interpolate values; for those with more than 20%, no analyses conducted on those datasets.
    - ΣPBDE calculated as the sum of detected congeners, with below-LoD concentrations set to zero for the sum.
  - Data distributions were skewed; Box-Cox transformations applied to congeners and ΣPBDE to meet normality assumptions for analyses.

- Statistical analyses and modeling
  - Associations between ΣPBDEs, individual congeners, and shell index assessed via Pearson’s rank correlation.
  - Temporal trends analyzed with linear, polynomial (second order), or split-line regressions.
  - Relationships with time, land-use, human population density, and eggshell thickness modeled using linear or polynomial regression.
  - Model suitability assessed using Akaike Information Criterion (AIC).
  - Shell index analyses performed only on samples with reliably calculable shell indices (undamaged eggs).

- Metadata, provenance, and data quality considerations
  - Documentation includes sampling year, nest identity, geographic region, egg measurements, storage conditions, extraction/analysis procedures, calibration standards, and QC results.
  - Acknowledges damaged/missing data (e.g., some eggs damaged, volume data unavailable for some eggs) and uses conservative imputation strategies where feasible.
  - Notes the need to interpret certain data (e.g., semi-quantified octa-BDEs) with caution due to calibration limitations.

- Data governance and archiving implications
  - Study exemplifies data stewardship: archived samples with traceable analytical methods, detailed QA/QC, and transparent handling of non-detects.
  - Emphasizes importance of robust metadata (sampling context, measurement methods, QA criteria) to enable reuse, replication, and integration with broader datasets (e.g., temporal trends, land-use, and population covariates).