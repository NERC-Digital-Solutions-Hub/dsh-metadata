# Experimental_Evolution_Design.csv

## Overview
- Describes an experimental evolution microcosm study to understand drought adaptation in two bacterial taxa.
- Microcosms use sterilised natural rendzina soil, inoculated with bacterial isolates, and fed artificial root exudate.
- Includes drought and control (high moisture) treatments, followed by a final drought and rewetting to assess resistance and resilience.
- Data collection spans soil moisture, bacterial population abundance, and microbial respiration physiology.

## Experimental Design and Treatments
- Factorial, randomised block design.
- 12 isolates of each of two taxa exposed to two treatments: drought and control.
- Four experimental blocks; one replicate of each isolate-treatment in each block.
- A fifth replicate per isolate-treatment assigned randomly to one of the blocks.
- Microcosm positions within blocks randomized (grid arrangement).
- Drought cycles plus rewetting used to probe adaptive responses.

## Data Collected and Timepoints
- Soil moisture monitoring: four timepoints during the experiment; subset microcosms monitored at additional timepoints.
- Bacterial population relative abundance: measured by qPCR at 11 timepoints (launch, end of each drought, rewetting, through four drought cycles; two additional post-evolution timepoints).
- Post-evolution sampling: soil samples after the fourth drought for genome resequencing and respiration physiology assessment.

## Data Structure and Metadata
- Data structure follows a factorial design with attributes including:
  - jarID: unique microcosm identifier
  - batch: inoculation batch
  - inoculation: genus of inoculated bacteria
  - isolate: unique isolate identifier
  - replicate: replicate number per isolate-treatment
  - treatment: control or drought
  - block: blocking factor
  - row, column: microcosm position within blocks
  - soil and microcosm masses, target masses, dates
  - evo_strain_ID: end-of-evolution strain identity
- Metadata tables outline variable names, units, and descriptions for traceability.

## Quality Control and Instrumentation
- Randomisation used to ensure valid experimental design.
- Mass measurements obtained with a 2-decimal pan balance.
- No calibration or analytical methods required for the design file itself (metadata-focused).

## Datasets Included and Key Content
- Experimental_Evolution_SWC.csv
  - Observations of microcosm masses, mass losses, and soil water content (SWC) across four dates/phases.
  - SWC calculated as water mass divided by total soil and water mass.
  - Metadata includes jarID, date, phase, total_mass, mass_loss, SWC, and comments.
- Experimental_Evolution_qPCR.csv
  - qPCR data estimating relative abundance of inoculated populations at 11 timepoints.
  - Primers target Bacillus 23S and Pseudomonas 16S loci; Locked Nucleic Acids used for specificity.
  - RNA extracted and DNase-treated; RT-qPCR performed with technical triplicates.
  - Quality control: dedicated clean lab space; calibration of threshold crossing values; mean Cp values and adjustments for soil mass and extraction.
- Experimental_Evolution_Microresp.csv
  - MicroResp™ assay measuring soil CO2 efflux in response to substrates (glucose, cellulose, artificial root exudate) and water control.
  - Soils pre-treated to 50% SWC, pre-incubated, then incubated with substrates; absorbance read at 570 nm to estimate CO2 production.
  - Technical replicates (three per substrate), blanks, and calibration with a CO2 standard.
  - Metadata includes plate ID, jarID, substrate, analytical_rep, baseline T0, final T6, Ai_t0, Ai_t6, %CO2, efflux, mean_efflux, se_efflux, and ordering variable.
- References for the MicroResp method, RNA/DNA co-extraction, root exudate system, and qPCR primer design.

## Data Stewardship and Implications for Data Leaders
- Demonstrates end-to-end data lifecycle: experimental design, data collection across multiple modalities, and integration of metadata for reproducibility.
- Highlights importance of:
  - Comprehensive metadata tables to enable data discoverability and re-use.
  - Clear data structure (IDs, replicates, blocks, treatments) to support cross-study comparability.
  - Rigorous quality control and documentation of instrumentation, calibration, and analytical methods.
  - Cross-domain data integration (soil physics, molecular biology, and microbial physiology) for a holistic data product.
- For data leadership: emphasizes planning for data management, data standards, and community access to complex, multi-modal research outputs.