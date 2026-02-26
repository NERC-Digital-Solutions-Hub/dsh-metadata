# Survival of human pathogens bound to microplastics during transfer through the freshwater-marine continuum

## Overview
- A dataset describing mesocosm experiments on the survival of human pathogens (E. coli, Enterococcus faecalis, Pseudomonas aeruginosa) bound to microplastics during transfer through freshwater to marine environments.
- Data are organized into 14 CSV files detailing background and experimental conditions, bacterial counts, and biofilm measurements.

## Data captured
- 14 CSV files:
  - BackgroundWaterCharacteristics_Mesocosm1
  - ExperimentWaterCharacteristics_Mesocosm1
  - InitialBacteriaAdded_Mesocosm1
  - WaterCFU_Mesocosm1
  - PlasticCFU_Mesocosm1
  - GlassCFU_Mesocosm1
  - BackgroundWaterCharacteristics_Mesocosm2
  - InitialBacteriaAdded_Mesocosm2
  - CrystalViolet_Plastic_Mesocosm2
  - CrystalViolet_Glass_Mesocosm2
  - SandDryWeight_Mesocosm2
  - BackgroundCFU_Mesocosm2
  - PlasticCFU_Mesocosm2
  - GlassCFU_Mesocosm2
- File-level notes include data types, dilution factors, measurements (CFU counts, absorbance), and biofilm metrics.

## Sampling location and period
- Location: Mesocosm experiments conducted at the University of Stirling, Scotland.
- Timeframe:
  - Experiment 1: April–June 2022 (field inoculation and sampling around 4–6 June 2022).
  - Experiment 2: April 2022 sampling with downstream simulation through river, estuary, seawater, and beach sand.

## Data collection methods
- Experiment 1: Direct discharge of WWTP effluent containing bacteria into either freshwater or seawater.
  - Sites for effluent collection: Dunblane, Bridge of Allan, Kirkcaldy (Forth Catchment), Scotland.
  - Particles: 100 microplastic beads and 100 glass beads per cage; 30 cages per mesocosm tank.
  - Inoculation: Overnight cultures of E. coli, E. faecalis, P. aeruginosa added to WWTP effluent; initial concentrations quantified by plating.
  - Incubation: 48 h in inoculated effluent, then cages moved to fresh water or seawater (4 replicates).
  - Sampling: At multiple days (1, 2, 3, 4, 5, 6, 7, 9, 12, 17, 22, 27); 100 particles per cage processed for CFU counts on selective media; CFU per 100 ml water estimated.
  - Measurements: pH, electrical conductivity (EC), turbidity, salinity, temperature in tanks; CFU enumeration on MLGA (E. coli), PA (P. aeruginosa), SB (E. faecalis).
- Experiment 2: Downstream transport simulation from effluent to beach environments.
  - Sites for input water: Dunblane, Bridge of Allan, Torryburn, Kirkcaldy (Forth Catchment).
  - Inoculation: WWTP effluent with higher initial bacterial concentrations; subsequent processing included moving cages through river water, estuary water, seawater, and beach sand.
  - Biofilm measurement: Crystal violet staining of 40 particles per cage; absorbance at 550 nm used as proxy for biofilm biomass.
  - Bacterial quantification after incubation: Same vortexing and filtration method as Experiment 1; sand samples processed by suspending 10 g in PBS and filtering for CFU counts.
  - Sand treatment: 40 g sand per dish used for abiotic downstream simulation; incubation at 15 °C.
  - Measurements: CFU counts on plastic and glass surfaces; crystal violet absorbance for biofilm on surfaces.

## Rationale and purpose
- Aimed at understanding the survival and transport of human pathogens bound to microplastics during movement through freshwater to marine environments.
- Supports UKRI NERC grants:
  - Microbial hitchhikers of marine plastics: the survival, persistence & ecology of microbial communities in the Plastisphere (NE/S005196/1)
  - NERC-GCRF SPACES project (NE/V005847/1)

## Data stewardship and completeness
- Responsible for collection and interpretation: Rebecca Metcalf.
- Completeness: Data checked for anomalies and limits; no data were reported as absent.

## Data files and descriptions (summary)
- BackgroundWaterCharacteristics_Mesocosm1: Baseline water characteristics by water type, including pH, EC, turbidity, salinity, and temperature.
- ExperimentWaterCharacteristics_Mesocosm1: In-tank water characteristics over time (pH, EC, turbidity); time (days) and replicate included.
- InitialBacteriaAdded_Mesocosm1: Bacteria species added, replicate, CFU per 10 µL, and dilution factors used for plating.
- WaterCFU_Mesocosm1: Bacteria concentrations in water over time; CFU per 100 mL.
- PlasticCFU_Mesocosm1: Bacterial concentrations on plastic by time, replicate, water type, and multiple dilution factors (DF0, DF10, DF100, DF1000, DF10000) with total CFU accounting for dilution.
- GlassCFU_Mesocosm1: Bacterial concentrations on glass surfaces with similar dilution-structured CFU data as PlasticCFU.
- BackgroundWaterCharacteristics_Mesocosm2: Baseline characteristics for mesocosm 2 with time- and replicate-based structure.
- InitialBacteriaAdded_Mesocosm2: Initial inoculum details for mesocosm 2.
- CrystalViolet_Plastic_Mesocosm2: Biofilm measurements on plastic via crystal violet (absorbance at 550 nm) across time, replicates, and water type.
- CrystalViolet_Glass_Mesocosm2: Biofilm measurements on glass via crystal violet (absorbance at 550 nm).
- SandDryWeight_Mesocosm2: Dry weight metrics for sand used in downstream simulations (before/after drying, difference, and percentage change).
- BackgroundCFU_Mesocosm2: Background CFU data for mesocosm 2 across times, replicates, and dilution factors (DF0, DF10, DF100, DF1000, DF10000, DF100000).
- PlasticCFU_Mesocosm2: CFU on plastic in mesocosm 2, including dilution-factor-based counts and total CFU.
- GlassCFU_Mesocosm2: CFU on glass in mesocosm 2, including dilution-factor-based counts and total CFU.