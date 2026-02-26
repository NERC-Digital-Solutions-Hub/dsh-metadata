# Experimental design/Sampling regime

- Study context and targets
  - Protocol describes sampling of soil properties (pore water conductivity, volumetric water content, and soil temperature) across Ethiopian households in Konicha and 1st Choroko.
  - Three fertility zones per household: Home (near the house, higher management/input), Near (between home and far), Far (furthest from house, more extensive production).
  - Measurements collected at multiple depths (0–5 cm, 5–10 cm, 10–15 cm) and across seven months (January–July).

- Sampling design and replication
  - Measurements positioned randomly within each fertility zone.
  - Sampling accounts for wealth status (poor, medium, rich) and two kebeles; extended to multiple soil types.
  - Replication structure
    - Fertility zones per household: 3
    - Replicates per zone: 3 to 6 (depending on configuration)
    - Overall site and sample counts scale across three configurations:
      - Configuration 1: 36 households, 2 kebeles, 2 soil types, 108 measurement sites, 3 replicates per zone, 324 samples
      - Configuration 2: 36 households, 2 kebeles, 2 soil types, 108 measurement sites, 3 replicates per zone, 324 samples
      - Configuration 3: 72 households, 4 kebeles, 4 soil types, 216 measurement sites, 6 replicates per zone, 648 samples

- Data collection methods
  - Three fertility zones sampled per household with random placement.
  - Field measurements conducted at specified depths using the W.E.T sensor, with strict field procedures and calibration steps.
  - Data captured include household and geography identifiers, zone, depth, replicate, and monthly readings.

- Equipment and calibration
  - Primary instrument: W.E.T soil sensor (soil water content, electrical conductivity, and temperature).
  - Soil water content calibration
    - Two-point calibration using damp and dry soil cores.
    - Steps to derive b0 and b1 parameters; enter custom soil type (Custom 1) into the sensor for field readings.
  - Pore water conductivity calibration
    - Involves preparing soil-water mixtures, equilibrating, and recording EC and permittivity values to compute ECp, then entering soil parameters into the sensor (Custom 1).
  - Field calibration workflow includes enabling Custom 1 soil type and verifying parameter entries before measurements.

- Quality control and data integrity
  - Randomized, triplicate sampling to address spatial variability.
  - Periodic sensor checks in saline solution; operation by two experienced soil scientists.
  - Data upload via tablet with pre-defined input variables to minimize mislabeling and data loss.
  - Sample labeling rigor and loss rate noted (less than 5% due to label eligibility issues).
  - Laboratory analyses conducted at University of Aberdeen with standard SOPs; regular calibration of sensors; distribution of data checked for normality.

- Data files and schema
  - IPORE-Soil EC.csv
    - Columns include: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, and monthly pore water conductivity values (January–July).
  - IPORE-Soil water.csv
    - Columns include: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, and monthly volumetric water content values (January–July).
  - IPORE-Soil temperature.csv
    - Columns include: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, and monthly soil temperature values (January–July).
  - All datasets include identifiers for household, kebele, fertility zone, depth range, replicate, and month-specific measurements.

- Data governance and usability notes (Data Leaders perspective)
  - Clear dimensional structure (household, kebele, zone, depth, replicate, month) supports end-to-end data governance, provenance, and reproducibility.
  - Metadata elements embedded in the data files (location, zone, depth, replicate) enable cross-site comparability and stratified analysis.
  - QA/QC processes and documentation of calibration procedures enhance data quality and reliability for downstream analytics, policy work, and partner collaborations.
  - Potential limitations noted include labeling losses and the need for consistent cross-site equipment calibration; data normalization and standardization procedures are described to address these issues.