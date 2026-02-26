# Biofilm data of plastic degrading bacteria on PCL beads in laboratory conditions.

## Overview
- Dataset describes the number of bacterial colonies recovered from plastic beads (PCL) incubated in a 96-well plate for 24 hours at 37°C.
- Purpose: test whether overexpressing plasmid-encoded diguanylate cyclases (wspR and dgcC) to modulate intracellular Cyclic-di-GMP increases biofilm on plastic beads using a plastic-degrading E. coli strain.
- Data format: CSV; related file named Biofilm_on_PCL_beads.xlsx.

## Data content and structure
- Primary measurements: Colony Forming Units (CFUs) recovered from beads for each bacterial strain and replicate.
- Key fields:
  - Strain, Description: name and plasmid content (or empty plasmid).
  - Replicate, Description: biological replicate details.
  - Replicate, Units: CFUs.
- Notes on file naming and conventions:
  - Data file format: .csv
  - Related Excel file: Biofilm_on_PCL_beads.xlsx
  - Columns capture strain, description, replicate details, and CFU counts.

## Methods and experimental design
- Inoculation and growth:
  - Overnight cultures used to start new cultures at OD600 0.1.
  - Induction with 1 mM IPTG at OD600 ~0.6.
  - 150 µL induced culture added to a single sterile PCL bead in each well, in triplicate.
- Biofilm recovery and CFU measurement:
  - After 24 hours, beads removed, washed three times in PBS.
  - Beads sonicated for 10 minutes to detach biofilm.
  - PBS suspension serially diluted and plated in triplicate on LB agar with appropriate antibiotics.
  - Incubation: 16 hours at 37°C; colonies counted to determine CFUs per bead.
- Experimental design: 24-hour incubation with bacteria engineered for higher biofilm formation; triplicate measurements per condition.

## Data collection and quality control
- Fieldwork/lab instrumentation:
  - Fisher Scientific Cell Density Meter 40-80-3000-45-D1-FR-E
  - Sci-Quip S-Series Incubator Incu-80S
  - Camlab Transsonic T460 bath
- Calibration and measurement practices:
  - OD600 measurements or similar blanking performed with uninoculated media.
  - Incubator temperature set to 37°C with alarms for deviations; no temperature alarm events reported.
  - All equipment with valid portable appliance test certificates.
- Quality controls:
  - Negative/controls: bacteria with empty vectors (EV) lacking biofilm-inducing genes.
  - Biological replication: three replicates per condition.

## Data interpretation and potential uses
- Allows comparison of biofilm-associated CFU counts across different strains and plasmid constructs.
- Facilitates analysis of the effect of engineered biofilm regulators (wspR, dgcC) on biofilm formation on plastic beads.
- Can be integrated with additional datasets (e.g., gene expression, plasmid constructs) to explore genotype–phenotype relationships in biofilm formation.
- Suitable for creating dashboards or reports that enable end-users to explore strain performance and replicate variability.

## Data provenance and documentation
- Experimental references: Howard SA, McCarthy RR. Modulating biofilm can potentiate activity of novel plastic-degrading enzymes. NPJ Biofilms Microbiomes. 2023;9(1):72. DOI: 10.1038/s41522-023-00440-1.
- Detailed methodological description supports reproducibility and data reuse, including culture conditions, induction, washing, sonication, dilution, plating, incubation, and CFU calculation.