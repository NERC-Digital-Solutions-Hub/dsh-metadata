# Experimental design/Sampling regime

- Objective: Describe how soil and related environmental health measures were collected and prepared to support analyses across households and locations.
- Sampling framework:
  - Three fertility zones per household:
    - Home garden: near the house, higher inputs and value crops.
    - Near field: intermediate distance.
    - Far field: owner’s field, furthest from the house.
  - Households and sites:
    - Total households: 72 across 4 kebeles (parishes).
    - Measurement sites: 216 (3 zones × 72 households).
    - Replicates and site diversity:
      - BREAD socioeconomic classes: multiple reps to cover poor, medium, rich; total class reps align with 72 households and 4 kebeles.
      - Soil types: 2 types per kebele area, with replicates to represent variation.
- Data structure:
  - Each fertility zone within each household sampled with multiple replicates, yielding a large, hierarchical dataset (household → kebele → fertility zone → replicate).

# Collection methods

- Positioning and sampling:
  - Random placement within each fertility zone.
  - Within four kebeles (Asore, Lay Arisho, Konicha, 1st Choroko), 18 farms per kebele included.
  - Three soil cores collected from surface (0–20 cm) and subsoil (20–50 cm) per zone.
- Field logistics:
  - Randomly positioned soil cores across areas with differing wealth statuses (poor, medium, rich).
  - Samples stored cool during transport; synchronized arrival to analytical facilities.

# Analytical methods

- Soil carbon and nitrogen:
  - Percent carbon and nitrogen measured by CNS elemental analyzer without ball-milling.
- Soil pH:
  - Measured on 1:5 soil:CaCl2 extracts using a pH meter.
- Soil mineral nitrogen (NO3−, NO2−, NH4+):
  - Mineral N determined via colorimetric methods with standardized reagents and plate-reader measurements.
  - Nitrate/nitrite: prepared standards and absorbance at 540 nm.
  - Ammonium: indophenol method with calibrated standards and spectrophotometry.
- Soil moisture:
  - Measured at sampling and at -10 kPa matric potential (where possible).
  - In some sites (Ethiopia) intact cores were not feasible; disturbed soils were repacked and equilibrated before measurement.
- Soil texture:
  - Silt, sand, clay fractions determined by laser diffraction after organic matter removal and dispersion steps.
- Aggregate stability:
  - Water-stable aggregates measured by wet sieving with a subsequent NaOH treatment to differentiate stable vs unstable fractions.
- Quality and preparation notes:
  - Standardized prep and dispersion protocols, including organic matter removal and careful sample conditioning.
  - Where equipment limitations existed, field adaptations were documented (e.g., disturbed soil prep).

# Data management and files

- Metadata and data structure:
  - Metadata.csv: metadata for the dataset.
  - BREAD-Master_data.csv: sample identifiers for Asore and Lay Arisho.
  - BREAD-Mineral_N_data.csv: soil mineral nitrogen measurements for Asore and Lay Arisho.
  - BREAD-Soil_C_N_and_pH.csv: soil carbon, nitrogen, and pH for Asore and Lay Arisho.
  - BREAD-Soil_moisture.csv: soil moisture measurements for Asore and Lay Arisho.
  - BREAD-Particle_size_analysis.csv: particle size analysis for Asore and Lay Arisho.
  - BREAD_Aggregate_stability.csv: aggregate stability for Asore and Lay Arisho.
  - IPORE-Master_data.csv, IPORE-Mineral_N_data.csv, IPORE-Soil_C_N_and_pH.csv, IPORE-Soil_moisture.csv, etc.: analogous datasets for Konicha and 1st Choroko.
- Data governance and sharing:
  - Datasets are organized into clearly named CSV files with accompanying metadata, enabling reuse, benchmarking, and integration into dashboards or reports.
  - Public sharing of underlying data is acknowledged as a potential barrier in monitoring contexts and should be managed with appropriate governance.

# Notes and limitations for monitoring frameworks

- Field constraints:
  - Equipment limitations in certain locations affected some measurements (e.g., in Ethiopia, intact cores not possible).
- Data quality considerations:
  - Heavy emphasis on randomization, replication, and cross-site comparability to support robust monitoring decisions.
  - Complex preprocessing steps (organic matter removal, dispersion, and calibration) are required to ensure data quality for C, N, mineral N, moisture, texture, and aggregate metrics.
- Relevance to monitoring aims:
  - Methods provide a comprehensive suite of soil health indicators (C, N, pH, mineral N, moisture, texture, aggregate stability) aligned with evaluating environmental health and informing policy/decision-making.
  - Data are structured to enable temporal or spatial comparisons and to support dashboards or stakeholder reporting.