# Biofilm data of plastic degrading bacteria on PCL beads in laboratory conditions.

## Overview
- Dataset documenting the number of bacterial colonies recovered from plastics beads incubated in a 96-well plate for 24 hours at 37°C.
- Objective: assess whether artificially modulating intracellular levels of the second messenger cyclic-di-GMP by overexpressing plasmid-encoded diguanylate cyclases (WspR and DgcC) in a plastic-degrading E. coli strain increases biofilm formation on plastic beads.

## Data content
- File format: .csv (with file naming Biofilm_on_PCL_beads.xlsx referenced in the text).
- Recorded values: colony counts (CFUs) recovered from selective LB agar plates after biofilm removal.
- Metadata fields:
  - Strain: name and plasmid description (what was encoded or if plasmid is empty).
  - Strain units: Text.
  - Replicate: description of biological replicate for each strain.
  - Replicate units: CFUs.

## Methods and sampling
- Inoculation and culture:
  - Overnight cultures used to inoculate new cultures to starting OD600 = 0.1; raised to OD600 = 0.6.
  - Induced with 1 mM IPTG.
  - After mixing, 150 μL of induced culture added to a well containing a sterile PCL bead, in triplicate.
- Incubation:
  - 24 hours at 37°C.
- Biofilm recovery:
  - Beads removed, washed 3 times in PBS, then sonicated for 10 minutes to detach biofilm.
  - Serial dilutions prepared from PBS suspension, spotted in triplicate on LB agar with appropriate antibiotics.
  - Plates incubated 16 hours at 37°C; CFUs counted.

## Experimental design
- Three biological replicates per condition.
- Controls included bacteria with empty vectors (EV) that do not encode biofilm-inducing genes.

## Instrumentation and calibration
- Instruments:
  - Fisher Scientific Cell Density Meter 40-80-3000-45-D1-FR-E for OD measurements.
  - Sci-Quip S-Series Incubator Incu-80S.
  - Camlab Transsonic T460 bath for sonication.
- Calibration and quality checks:
  - OD600 meter blanked with uninoculated media.
  - Incubator temperature set to 37°C with alarms on deviation.
  - All equipment with valid portable appliance testing certificates.

## Quality control and context
- Negative controls: EV plasmids to establish baseline biofilm levels.
- Replication: three biological replicates to ensure robustness.
- Data context: aims to link plasmid-encoded diguanylate cyclases with enhanced biofilm formation on PCL beads.

## References
- Howard SA, McCarthy RR. Modulating biofilm can potentiate activity of novel plastic-degrading enzymes. NPJ Biofilms Microbiomes. 2023 Oct 3;9(1):72. doi: 10.1038/s41522-023-00440-1. PMID: 37788986; PMCID: PMC10547765.