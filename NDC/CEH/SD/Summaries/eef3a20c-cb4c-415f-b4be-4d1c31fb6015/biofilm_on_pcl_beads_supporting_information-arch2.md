# Biofilm data of plastic degrading bacteria on PCL beads in laboratory conditions.

## Purpose and scope
- Dataset records the number of bacterial colonies recovered from plastic beads (PCL) after a 24-hour incubation at 37°C.
- Objective: determine whether artificially modulating intracellular levels of the second messenger cyclic-di-GMP by overexpressing plasmid-encoded diguanylate cyclases (WspR and DgcC) in a plastic-degrading E. coli strain increases biofilm formation on plastic beads.

## Data format and contents
- File format: .csv
- File naming: Biofilm_on_PCL_beads.xlsx (note: CSV format stated; naming suggests Excel)
- Recorded values: number of colonies (CFUs) recovered from selective media plates.
- Metadata columns: Strain (name and plasmid description or empty vector), Replicate (biological replicate), CFU count (Colony Forming Units).

## Experimental design and methods
- Biological setup: Overnight cultures inoculated into fresh media to OD600 = 0.1; induction at OD600 = 0.6 with 1 mM IPTG.
- Procedure: 150 μL of induced culture added to a sterile PCL bead in triplicate.
- Incubation: 24 hours at 37°C.
- Post-processing: beads removed, washed 3× in PBS, sonicated for 10 minutes to detach biofilm.
- CFU determination: serial dilutions of the PBS suspension plated in triplicate on LB agar with appropriate antibiotics; incubated 16 hours at 37°C; CFUs counted.

## Quality control and replicates
- Controls: bacteria with empty vectors (EV) lacking biofilm-inducing genes.
- Replication: three biological replicates per condition.
- Calibration and validation steps noted for accuracy (see instrumentation and calibration sections).

## Instruments and calibration
- Instruments used: 
  - Fisher Scientific Cell Density Meter 40-80-3000-45-D1-FR-E (OD600 measurement)
  - Sci-Quip S-Series Incu-bator Incu-80S
  - Camlab Transsonic T460 bath for sonication
- Calibration notes: 
  - OD600 meter blanked with uninoculated media.
  - Incubator temperature control with alarms; no temperature alarm events reported.
  - All equipment had valid portable appliance testing certificates.

## Data stewardship and accessibility
- Data generated and stored with standardized procedures; outputs formatted for clear interpretation and potential upload to relevant data portals.

## Context and references
- Related research: Howard SA, McCarthy RR. Modulating biofilm can potentiate activity of novel plastic-degrading enzymes. NPJ Biofilms Microbiomes. 2023 Oct 3;9(1):72. doi: 10.1038/s41522-023-00440-1. PMID: 37788986; PMCID: PMC10547765.