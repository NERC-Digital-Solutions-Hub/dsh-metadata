# Experimental design/Sampling regime: Within each household, three fertility zones are sampled:

## Overview of the sampling framework
- Three fertility zones per household: Home (near the house, higher management and inputs), Near (between home and far), Far (far from the house, more extensive production).
- Sampling targets multiple spatial strata, including socioeconomic classes and kebeles, with randomization within areas.
- Scale of sampling includes multiple households, kebeles, soil types, and measurement sites, culminating in a sizable dataset (up to 72 households and 216 measurement sites at the largest scale, 648 samples across all sites).

## Experimental design details
- Within-household sampling: three fertility zones per household.
- Socioeconomic stratification and kebele coverage: households categorized by wealth status and located across two kebeles (Konicha and 1st Choroko).
- Soil and site stratification: two soil types considered; sampling across fertility zones and depths.
- Replication: three replicates per fertility zone to capture within-zone variability.

## Measurements and depths
- Depths sampled in each zone: 0–5 cm, 5–10 cm, and 10–15 cm.
- Measured variables include volumetric soil water content, soil temperature, and pore water conductivity (EC).

## Collection methods
- Random positioning: sampling locations within each fertility zone selected randomly.
- Field arrangement: measurements taken in three fertility zones per household, across two kebeles.
- Replicates: three replicates per zone to account for spatial variability.
- Data capture: all measurements recorded with a W.E.T soil sensor; data uploaded in real time to a Tablet using an ODK file with defined input variables.
- Equipment handling: two experienced soil scientists conducted fieldwork; calibration and field procedures documented.

## Calibration and sensor setup
- W.E.T soil water content calibration:
  - Two-point calibration using damp and dry soil cores.
  - Determine sensor parameters (b0, b1) and soil type (Custom 1) for field use.
  - Enter calibrated parameters into the W.E.T sensor to enable field measurements without further calibration.
- W.E.T pore water conductivity calibration:
  - Determine EC parameters (ECp, and related soil parameters) using a standardized procedure with soil and water suspensions.
  - Configure the sensor to use Custom 1 parameters for pore water EC calculations.
- Field usage:
  - In the field, select Custom 1 soil type from the Soil type menu prior to measurements.
  - Electrical conductivity reported directly by the sensor based on the calibrated parameters.

## Quality control and data management
- Randomized replicates: three field samples per area to address spatial variability.
- Sensor checks: periodic calibration verification in saline solution; documented accuracy specs (5% for water content, 1.5°C for temperature, 10 mS/m for EC).
- Data capture and storage: data immediately uploaded to a tablet with an ODK file to minimize data loss and mislabeling.
- Labeling and sample handling: soil samples labeled and stored; minimal loss due to label issues (<5%).
- Laboratory analysis: conducted at the University of Aberdeen following standard operating procedures; regular calibration of sensors and cross-checks of analyses (pH, nutrients) for quality control.
- Data quality assessment: all data checked for statistical distribution; distributions were reported as highly normal.

## Data files and structure
- IPORE-Soil EC.csv
  - Columns include: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, and monthly pore water conductivity values (January–July).
- IPORE-Soil water.csv
  - Columns include: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, and monthly volumetric water content values (January–July).
- IPORE-Soil temperature.csv
  - Columns include: S. no., HH no., Kebele, HH ID, Fertility Zone, Top depth, Bottom depth, Replicates, and monthly soil temperature values (January–July).

## Data provenance and accessibility
- Measurements integrate depth-specific, zone-specific, and household-level metadata to enable temporal and spatial analyses of soil moisture, temperature, and pore water conductivity.
- Data are organized for easy comparison across households, zones, and time, supporting environmental health monitoring and policy evaluation over time.