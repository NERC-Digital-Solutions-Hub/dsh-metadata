# Experimental_Evolution_Design.csv

- Purpose: Describe the experimental design and data collection plan for an experimental evolution microcosm study to understand evolutionary adaptation to drought in two bacterial taxa.
- System: Bacterial isolates inoculated into sterilised natural rendzina soil in microcosms, subjected to four drought cycles or maintained under control (high moisture); all microcosms receive artificial root exudate.
- Post-treatment: A final drought is applied to all microcosms followed by rewetting to assess resistance and resilience; soil moisture monitoring and bacterial population assessments occur throughout.
- Outcome focus: Post-evolution soil samples collected for genome resequencing and assessment of shifts in microbial respiration physiology.

- Experimental design
  - Factorial, randomised block design.
  - 12 isolates per bacterial taxon, exposed to two treatments (drought and control) across four experimental blocks.
  - Fifth replicate of each isolate-treatment is allocated to blocks at random; microcosm placement within blocks randomized.

- Measurements and timing
  - Soil moisture conditions monitored by mass determination at four timepoints per microcosm; additional monitoring on a subset of microcosms at other timepoints.
  - Bacterial population relative abundance measured by qPCR at 11 timepoints (launch, end of each drought cycle, after wetting across four cycles; final drought and post-evolution rewetting phase).
  - Post-evolution sampling after the fourth drought for genome resequencing and assessment of respiration physiology.

- Data structure and metadata
  - Metadata Table 1 outlines key variables: jarID, batch, inoculation, isolate, replicate, treatment, block, row, column, jar_mass, soil_mass, microcosm_dry_mass, target_mass_0.4, date, evo_strain_ID, and comments; includes units where applicable.
  - Randomisation and blocking are explicitly noted to control for spatial effects.

- Instrumentation and methods
  - Mass measurements: 2 decimal place pan balance.
  - Calibration: No explicit calibration methods required for mass measurements.

- Data governance and sharing
  - Metadata and documentation accompany the data (as described in Metadata Table 1) to ensure transparency and reproducibility.
  - Notes imply data sharing and clear data management practices are important considerations for monitoring framework authors.

- References
  - Not applicable within this file beyond internal study description; related methodological references are provided in related datasets (qPCR and MicroResp) descriptions.

- Related files and their purpose (summarised)
  - Experimental_Evolution_SWC.csv: Four mass-date measurements of soil water content, mass, and related variables; SWC calculated as the inferred mass of water divided by total mass of soil and water; includes date, phase, total_mass, mass_loss, SWC, and comments (Metadata Table 2).
  - Experimental_Evolution_qPCR.csv: qPCR data describing relative bacterial abundance across 11 timepoints; includes RNA extraction protocol, primers targeted to Bacillus (23S) and Pseudomonas (16S), technical replicates, and calibration details; provides Cp1-3, mean_cp, and mean_cp_adjusted_for_soil_mass (Metadata Table 3).
  - Experimental_Evolution_Microresp.csv: MicroResp measurements of CO2 efflux after substrate additions (H2O, Cellulose, Glucose, RE root exudate); includes pre-incubation steps, 0 h baseline, 6 h reading, three technical replicates, and derived metrics (mean_efflux, se_efflux); uses a 96-well plate format with 0.35 g soil per well; data linked to plate and substrate (Metadata Table 4).

- Specific methodological details per related datasets
  - SWC dataset (Experimental_Evolution_SWC.csv): Four dates corresponding to different experiment phases; mass and water content calculations; calibration narrative for SWC calculation.
  - qPCR dataset (Experimental_Evolution_qPCR.csv): Dedicated molecular facility for extraction and qPCR; targets are taxa-specific loci with Locked Nucleic Acids for specificity; RNA extracted and treated to remove DNA; qPCR cycling and Ct/ Cp data; plate-based instrument (LightCycler 480); quality control in a room without bacterial cultures.
  - Microresp dataset (Experimental_Evolution_Microresp.csv): MicroResp method following Campbell et al. and Creamer et al.; substrates prepared with defined carbon content; soils conditioned to 50% SWC and pre-incubated; 7 days total pre-incubation; absorbance read at 570 nm; calibration curve used to convert to % CO2 and efflux rates; three technical replicates per condition; blank controls included.

- References (methodological context)
  - Campbell et al. 2003; Creamer et al. 2009; Griffiths et al. 2000; Lopez-Sangil et al. 2017.