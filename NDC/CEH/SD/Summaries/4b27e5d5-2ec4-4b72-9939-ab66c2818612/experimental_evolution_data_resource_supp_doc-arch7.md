# Experimental_Evolution_Design.csv

- Overview of the experimental evolution microcosm study to understand bacterial adaptation to drought, using two taxa across drought and control treatments in a factorial randomized block design.
- Four drought cycles plus a final drought treatment with rewetting to assess resistance and resilience; all microcosms receive artificial root exudate.

## Experimental design and data structure

- Factorial, randomised block design:
  - 12 isolates of each of two bacterial taxa (inoculated into microcosms).
  - Two treatments: drought and control (continuously high moisture).
  - Four experimental blocks; one replicate per isolate-treatment per block; a fifth replicate allocated to a block at random.
  - Microcosm spatial position within blocks randomized (grid layout).
- Data are distributed across multiple CSV datasets linked by metadata (e.g., jarID).

## Data collection and monitoring (structure and scope)

- Soil moisture and mass monitoring:
  - Four timepoints for mass measurements (SWC calculations/soil moisture).
  - Additional moisture measurements for a subset of microcosms.
- Bacterial population monitoring (qPCR):
  - 11 timepoints (launch, end of each drought, post-wetting through four drought cycles; final drought and rewet).
  - 12 microcosms randomly selected per taxon-treatment combination for qPCR (total 48 microcosms; 3 technical replicates per sample).
  - Target loci: Bacillus (23S) and Pseudomonas (16S); primers designed for specificity with Locked Nucleic Acids.
- Post-evolution analyses:
  - Soil samples after the fourth drought cycle for genome resequencing and respiration physiology assessment (see Experimental_Evolution_Microresp.csv).

## Metadata and variables (key fields)

- Metadata Table 1 (design and lab setup):
  - jarID (microcosm identifier), batch, inoculation (bacteria genus), isolate, replicate, treatment, block, row, column, jar_mass, soil_mass, microcosm_dry_mass, target_mass_0.4, date, evo_strain_ID, comment.
- Metadata Table 2 (SWC observations):
  - jarID, date, phase (calibration, launch, end drought, etc.), total_mass, mass_loss, SWC (soil water content as mass proportion), comment.
- Metadata Table 3 (qPCR-related data, end-of-drought rewet phase):
  - jarID, date, SWC_cat (high/low), SWC (mean proportion), food (nutrient environment), dilution, extraction_soil_mass, Cp1/Cp2/Cp3 (qPCR crossing points), mean_cp, mean_cp_adjusted_for_soil_mass, Order.
- Metadata Table 4 (MicroResp):
  - sort, plate, jarID, substrate (H2O, Cellulose, Glucose, RE), analytical_rep, T0, T6, Ai_t0, Ai_t6, %CO2, efflux, mean_efflux, se_efflux.

## Instrumentation and analytical methods

- Mass and physical measurements:
  - 2-decimal pan balance for masses; soil and microcosm mass determinations.
- qPCR workflow (qPCR/qRT-qPCR):
  - PowerLyser homogeniser for RNA extraction; Luna Universal One-Step RT-qPCR kit; Roche LightCycler 480.
  - Target loci: Bacillus (23S), Pseudomonas (16S); three technical replicates per sample.
  - Calibration: threshold (Cp) values set in log-linear range; mean Cp adjusted for soil mass.
- MicroResp respiration measurements:
  - Substrates: glucose, cellulose, artificial root exudate (ARE) mix, plus water control.
  - Pre-incubation to 50% SWC, then incubation with detection plate; absorbance read at 570 nm; CO2 efflux calculated from calibration.
  - Three technical replicates per substrate per microcosm; blanks included.

## Data quality control

- Randomisation and blocking implemented to maintain valid experimental design.
- qPCR and RNA/DNA extractions performed in dedicated clean lab space; three technical replicates; blanks used to identify leaks.
- MicroResp measurements include blank corrections and baseline normalization; calibration of CO2 detection.

## GIS-relevant data considerations and potential visualizations

- Spatial layout enable GIS mapping of microcosms:
  - Use jarID with block, row, column as spatial attributes to create point or gridded representations of microcosm locations.
  - Attribute layers can include treatment (drought vs control), taxon, block, and replicate information.
- Integrating time-series data:
  - SWC measurements (four phases) can be mapped as time-series soil moisture layers.
  - qPCR relative abundance (log-transformed) and MicroResp efflux rates can be joined by jarID for multi-criteria spatial analysis.
- Data fusion and standardization:
  - Align datasets by jarID/date to produce composite GIS layers showing moisture, microbial abundance, and respiration across space and time.
  - Address varying resolutions (per-timepoint data) with clear metadata and consistent units.
- Visualization ideas:
  - Spatial heatmaps of soil moisture and substrate-specific respiration across blocks.
  - Temporal maps showing shifts in taxa abundance and respiration through drought cycles.
  - Integrated dashboards combining moisture, qPCR signals, and respiration for policy or stakeholder communication.

## Summary of purpose and scope

- Provides a comprehensive, multi-modal dataset to study how two bacterial taxa adapt to drought under a controlled, spatially structured experimental design.
- Facilitates data-driven GIS-based exploration of spatial and temporal patterns in moisture, microbial abundance, and soil respiration across microcosms.
- Emphasizes robust metadata, standardized measurements, and rigorous quality control to support cross-dataset integration and visualization.