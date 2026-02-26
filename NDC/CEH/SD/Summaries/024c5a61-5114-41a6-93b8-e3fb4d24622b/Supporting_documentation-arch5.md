# Experimental design/Sampling regime:

## Scope and sampling framework
- Within each household, three fertility zones are sampled: home (near house, higher inputs), near (between home and far), and far (farther from house, more extensive production).
- Study spans four kebeles (parishes): Asore, Lay Arisho, Konicha, and 1st Choroko.
- Sampling includes 72 households (18 farms per kebele) and 216 measurement sites (3 zones per household × 72 households).
- Replication across socioeconomic classes:
  - BREADIPORE: 3 classes; total replicates across the design: 6 per household/zone configuration.
  - Overall replicates per fertility zone: 3; total replicates: 6 per household/zone.
- Data organization includes separate datasets for different kebeles (Asore, Lay Arisho; Konicha, 1st Choroko).

## Experimental design and replication specifics
- Number of households: 72 (across 4 kebeles).
- Number of measurement sites: 216.
- Replicates per fertility zone: 6 (across socioeconomic classes).
- Number of samples: 648 total.
- Soil types sampled: 2 types (per kebele, with total aggregation across sites).
- Kebeles and soil types included in data subsets (BREAD vs IPORE subsets).

## Collection methods and field procedures
- Sampling positions within areas are randomly determined.
- Three fertility zones sampled in each household: home, near, far.
- In each kebele area, 18 farms sampled (4 kebeles total).
- Soil cores collected at two depths: 0–20 cm and 20–50 cm.
- All samples collected from farmers with varying wealth status (poor, medium, rich).
- Sample handling:
  - Randomly positioned soil cores.
  - Samples stored in cool locations/out of sun in cool boxes.
  - Samples transported to Aberdeen for analysis with maintained cooling; arrival communicated to laboratory for proper storage.

## Analytical methods and data collected
- Carbon and Nitrogen
  - Method: CNS elemental analyzer (no ball-milling).
- Soil pH
  - Method: pH meter (Hannah Instruments) in 1:5 soil:CaCl2 solution; temperature recorded.
- Soil mineral nitrogen
  - Analytes: nitrate (NO3–) and ammonium (NH4+).
  - Extraction: 10 g soil with 30 ml 1 M KCl; pre-treatment in triplicate.
  - Nitrate/Nitrite: colorimetric assay on a 96-well plate after standard preparation; absorbance read at 540 nm.
  - Ammonium: indophenol method with prepared standards; color development read at 620 nm.
- Soil moisture
  - Measured at time of sampling and at -10 kPa matric potential (where possible).
  - In some sites (Ethiopia) in-country analysis was not possible; disturbed soil repacked and treated to -10 kPa.
- Soil texture
  - Method: Laser diffraction (Beckman-Coulter LS 13 320).
  - Preparation included organic matter removal, dispersion, and standardization steps with H2O2, sodium hexametaphosphate, and suspension analysis.
- Aggregate stability
  - Method: Wet sieving with NaOH treatment to determine stable vs unstable aggregates.
- Data files generated per site
  - Metadata and primary measurement data files (e.g., BREAD-Master_data.csv, BREAD-Mineral_N_data.csv, BREAD-Soil_C_N_and_pH.csv, BREAD-Soil_moisture.csv, BREAD-Particle_size_analysis.csv, BREAD_Aggregate_stability.csv) plus corresponding IPORE equivalents.

## Data management, provenance, and potential governance considerations
- Data files are organized by site sets and kebeles, with clear metadata linking sample IDs to field locations and measurement types.
- Primary data collection and lab analyses were centralized (samples sent to Aberdeen for analysis); documentation should capture chain-of-custody, transport conditions, and timing.
- Metadata.csv provides essential context for samples, identifiers, and study design.
- Data provenance notes include method-specific details (e.g., whether ball-milling changed CNS results; specific reagent volumes and standards for mineral N analyses).
- Key governance considerations for data stewards:
  - Ensure consistent units and naming across all datasets.
  - Maintain traceability from field collection to lab results to final data files.
  - Provide data dictionaries and variable definitions for all CSV files.
  - Identify any data limitations or missing values due to field constraints (e.g., in-country analysis gaps).
  - Consider future updates or expansions (e.g., additional kebeles or soil types) and document embargo/status if applicable.

## Data files and metadata (structure overview)
- Metadata.csv – dataset metadata and sample identifiers.
- BREAD-Master_data.csv – sample identifiers for Asore and Lay Arisho.
- BREAD-Mineral_N_data.csv – soil mineral nitrogen measurements for Asore and Lay Arisho.
- BREAD-Soil_C_N_and_pH.csv – soil carbon, nitrogen, and pH for Asore and Lay Arisho.
- BREAD-Soil_moisture.csv – soil moisture measurements for Asore and Lay Arisho.
- BREAD-Particle_size_analysis.csv – particle size analysis for Asore and Lay Arisho.
- BREAD_Aggregate_stability.csv – aggregate stability measurements for Asore and Lay Arisho.
- IPORE-Master_data.csv – sample identifiers for Konicha and 1st Choroko.
- IPORE-Mineral_N_data.csv – soil mineral N measurements for Konicha and 1st Choroko.
- IPORE-Soil_C_N_and_pH.csv – soil C, N and pH for Konicha and 1st Choroko.
- IPORE-Soil_moisture.csv – soil moisture measurements for Konicha and 1st Choroko.