# Experimental_Evolution_Design.csv

- Study goal: Establish an experimental evolution microcosm to understand evolutionary adaptation to drought in two bacterial taxa using sterilised natural rendzina soil, with artificial root exudate as a nutrient source.
- Taxa and isolates: Two bacterial taxa with 12 isolates per taxon; inoculated into microcosms.
- Treatments: Two moisture treatments — drought and control (continuously high soil moisture).
- Experimental design: Factorial, randomised block design.
  - 4 experimental blocks.
  - One replicate of each isolate-treatment combination per block; a fifth replicate assigned to a random block.
  - Microcosm spatial position within blocks randomized.
- Data collection timeline:
  - Soil moisture measurements (mass) at four timepoints; additional measurements on a subset of microcosms.
  - Bacterial population relative abundance measured by qPCR at 11 timepoints (launch, end of each drought, post-evolution drought and rewetting).
  - Post-evolution soil samples for genome resequencing and assessment of respiration physiology.
- Data scope: Data describe experimental setup, measurements, and resulting microbial and soil properties across the drought experiment.

- Quality control and randomisation:
  - Randomisation used to support valid experimental design.
  - Dedicated QC steps for molecular measurements and soil measurements.

- Instrumentation and methods (high level):
  - Masses measured with a 2-decimal pan balance.
  - qPCR performed with specified primers, RNA extractions, and one-step RT-qPCR, including multiple technical replicates and contamination controls.
  - Post-evolution respiration assessed via MicroResp™ method with substrate amendments.

- Related datasets:
  - Experimental_Evolution_SWC.csv: Time-resolved soil mass, mass loss, and soil water content (SWC) measurements prior to and during drought phases.
  - Experimental_Evolution_qPCR.csv: qPCR-derived relative abundances for inoculated taxa across timepoints; includes RNA extraction and qPCR workflow details; includes targeted loci (23S for Bacillus, 16S for Pseudomonas) and mean Cp values with soil-mass adjustments.
  - Experimental_Evolution_Microresp.csv: Soil CO2 efflux measured via MicroResp™ after substrate additions (H2O, Cellulose, Glucose, and artificial root exudate); includes baseline and post-incubation reads, 3 technical replicates, and calibration.

- Metadata and data structure (summary by file section):
  - Metadata Table 1 (Design/Variables): jarID, batch, inoculation, isolate, replicate, treatment, block, row, column, jar_mass, soil_mass, microcosm_dry_mass, target_mass_0.4, date, evo_strain_ID, comment.
  - Metadata Table 2 (SWC data): jarID, date, phase, total_mass, mass_loss, SWC, comment; SWC calculated as mass of water divided by total soil-water mass.
  - Metadata Table 3 (qPCR data): jarID, date, SWC_cat, Cp1/Cp2/Cp3, mean_cp, mean_cp_adjusted_for_soil_mass, extraction_soil_mass, order, and related fields; describes PCR targets and data processing steps.
  - Metadata Table 4 (Microresp data): sortplate, plate, jarID, substrate, analytical_rep, T0, T6, Ai_t0, Ai_t6, %CO2, efflux, mean_efflux, se_efflux; includes calibration and substrate treatments.