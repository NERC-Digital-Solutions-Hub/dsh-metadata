# Experimental_Evolution_Design.csv

## Overview
- Describes an experimental evolution microcosm study to understand drought adaptation in two bacterial taxa using sterilised natural rendzina soil and artificial root exudate.
- Factorial, randomized block design with two taxa, two treatments (drought vs. control), and four blocks; five replicates per isolate-treatment combination allocated with randomization.
- Multi-dataset synthesis: linking soil moisture, microbial population data (qPCR), and microbial respiration physiology for post-evolution analysis.

## Experimental design and governance
- 12 isolates per taxon exposed to each treatment; replicate allocation to blocks with randomization to ensure valid design.
- Monitoring plan includes:
  - Soil moisture: four timepoints, plus subset of microcosms with additional measurements.
  - Microbial populations: qPCR at 11 timepoints to estimate relative abundances of inoculated taxa; three technical qPCR replicates per sample.
  - Post-evolution sampling: soil samples after the fourth drought for genome resequencing and respiration physiology assessment.
- Data management focus:
  - Clear identifiers (jarID, block, replicate, date, etc.) to enable linking across datasets.
  - Documentation of sampling phases and experimental conditions to support reproducibility and reuse.

## Data collection and measurements

### Experimental_Evolution_SWC.csv
- Contains observations of microcosm masses, mass losses, and soil water content (SWC) across four dates/phases.
- Measurements use a 2-decimal pan balance; SWC calculated as the ratio of water mass to total soil + water mass.
- Metadata includes jarID, date, phase (calibration, launch, end drought, etc.), mass measurements (total_mass, mass_loss), SWC, and a comment field.

### Experimental_Evolution_qPCR.csv
- qPCR data describing relative abundance of inoculated populations at 11 timepoints (launch, drought endpoints, post-drought rewetting, etc.).
- Sampling: 12 microcosms per taxon × moisture treatment, one timepoint per microcosm (3 technical replicates per sample; total 48 microcosms).
- RNA extraction and qPCR protocol details:
  - Target loci: 23S for Bacillus and 16S for Pseudomonas.
  - Primers designed for specificity; Locked Nucleic Acids used.
  - RT-qPCR with specific cycling parameters; crossing points (Cp) recorded for three technical replicates and averaged.
- Quality control:
  - Nucleic acid extractions and qPCR performed in a dedicated molecular biology facility to minimize contamination.
- Instrumentation:
  - PowerLyser for lysis; LightCycler 480 for qPCR.
- Data processing:
  - Thresholds set in the log-linear region per target; Cp values used to estimate relative abundances.
  - Adjustments for soil mass used in RNA extraction to compute mean_cp_adjusted_for_soil_mass.
- Metadata includes jarID, date, SWC category, SWC value, substrate/food context, dilution factor, extraction soil mass, Cp1-3, mean_cp, and ordering.

### Experimental_Evolution_Microresp.csv
- Measures the effect of substrate additions on soil CO2 efflux (soil respiration) using the MicroResp method.
- Sampling performed 15/01/2020 after four drought cycles; soils equilibrated to 50% SWC, pre-incubated, then incubated with substrates (glucose, cellulose, artificial root exudate; water control).
- Incubation and measurement:
  - Soils placed in 1.2 ml 96-well plates with 0.35 g soil per well; readings at baseline (T0) and after 6 hours (T6) of incubation.
  - Absorbance measured at 570 nm; three analytical replicates per soil-substrate combination.
  - Data corrected with blanks; plate and sample alignment maintained via plate and jar identifiers.
- Data processing:
  - Ai_t0 and Ai_t6 used to compute normalized absorbance (Ai_t6 adjusted for baseline).
  - %CO2 derived from a calibration curve; efflux calculated as micrograms CO2 per gram soil per hour.
  - Mean efflux and standard error across three technical replicates reported.
- Metadata includes sort order, plate ID, jarID, substrate (H2O, Cellulose, Glucose, RE), analytical_replicate, T0, T6, Ai_t0, Ai_t6, %CO2, efflux, mean_efflux, se_efflux.

## Metadata and data structure
- Metadata Tables summarize variables and units for each dataset:
  - Table 1 (Experimental_Evolution_Design.csv): jarID, batch, inoculation, isolate, replicate, treatment, block, row, column, jar_mass, soil_mass, microcosm_dry_mass, target_mass_0.4, date, evo_strain_ID, comment.
  - Table 2 (Experimental_Evolution_SWC.csv): jarID, date, phase, total_mass, mass_loss, SWC, comment.
  - Table 3 (Experimental_Evolution_qPCR.csv): jarID, date, SWC_cat, SWC, food, dilution, extraction_soil_mass, Cp1, Cp2, Cp3, mean_cp, mean_cp_adjusted_for_soil_mass, Order.
  - Table 4 (Experimental_Evolution_Microresp.csv): sort, plate, jarID, substrate, analytical_rep, T0, T6, Ai_t0, Ai_t6, %CO2, efflux, mean_efflux, se_efflux.

## Quality control, calibration, and instrumentation
- Quality control:
  - Randomization used in design to ensure valid experimental structure.
  - qPCR performed with three technical replicates; dedicated lab space to minimize contamination.
  - MicroResp calibration conducted to relate absorbance to CO2 and substrate responses; use of blanks for correction.
- Instrumentation:
  - Mass measurements: two-decimal pan balance.
  - qPCR: PowerLyser 24 homogenizer; LightCycler 480 instrument.
  - MicroResp: microplate reader (FLUOstar Omega) for 570 nm absorbance.

## Data governance considerations for Data Stewards
- Data are distributed across multiple CSV files with interconnected identifiers (e.g., jarID, date, block, replicate) facilitating cross-dataset linkage.
- Rich metadata and explicit units enable interoperability, reproducibility, and discoverability.
- Clear documentation of experimental phases (calibration, launch, drought cycles, rewetting) and data processing steps (e.g., SWC calculation, Cp thresholding, soil-mass corrections) supports reuse and auditability.
- Potential for data integration with external portals or catalogs; ensure consistent naming, versioning, and licensing to support discovery and timely sharing.

## Challenges and considerations for data stewardship
- Incomplete or evolving user needs across diverse data types (design, SWC, qPCR, Microresp) may require flexible metadata schemas and versioning.
- Coordinating data from many systems and formats, including large time-series qPCR and respiration datasets.
- Handling legacy or outdated databases; ensuring interoperability and standardization across datasets.
- Maintaining up-to-date updates and embargoes to balance data sharing with ongoing analyses.

## Practical implications for reuse
- The dataset collection provides a comprehensive, linked view of drought adaptation experiments in soil microbial communities, suitable for meta-analyses of microbial responses to water stress, community composition shifts, and respiration dynamics.
- Clear identifiers and thorough metadata enable researchers to reproduce the experimental design, compare across taxa and treatments, and integrate with external genomic or metabolic datasets.