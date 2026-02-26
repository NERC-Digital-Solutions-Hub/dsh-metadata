# Biofilm data of plastic degrading bacteria on PCL beads in laboratory conditions

## Overview
- Purpose: determine if artificially modulating intracellular levels of cyclic-di-GMP by overexpressing plasmid-encoded diguanylate cycle genes ( wspR and dgcC ) in a plastic-degrading E. coli strain leads to increased biofilm on plastic beads.
- Dataset scope: information on the number of bacterial colonies recovered from PCL beads after 24 hours of incubation under controlled conditions.

## Dataset structure and format
- Primary data: colony-forming units (CFUs) recovered from PCL beads for different bacterial strains and replicates.
- File format: listed as .csv; file name provided as Biofilm_on_PCL_beads.xlsx (inconsistency between format and name requires clarification).
- Metadata fields implied: Strain (Description and Units), Replicate (Description and Units), CFU (Counts).

## Metadata and variables
- Strain, Description = Name of each strain and plasmid context (or empty vector if not encoded).
- Strain, Units = Text.
- Replicate, Description = Biological replicate identifier for each strain.
- Replicate, Units = Colony Forming Units (CFUs).

## Collection, processing, and measurement methods
- Culture and induction: Overnight cultures inoculated into fresh cultures to OD600 0.1; induction at OD600 0.6 with 1 mM IPTG.
- Inoculation: 150 μL of induced culture added to a well of a 96-well plate containing a sterile PCL bead; performed in triplicate.
- Incubation: 24 hours at 37°C.
- Biofilm recovery: Beads removed, washed 3 times in PBS, then sonicated for 10 minutes to detach biofilm.
- Plating and counting: Serial dilutions prepared from PBS suspension; spotted in triplicate on LB agar with appropriate antibiotics; incubated 16 hours at 37°C to count CFUs.
- Replication and controls: Three biological replicates; controls with empty vectors (EV) included.

## Instrumentation and calibration
- Instruments: Fisher Scientific Cell Density Meter (OD600), Sci-Quip S-Series Incubator (Incu-80S), Camlab Transsonic T460 bath (sonicator).
- Calibration and QA: OD meter blanked with uninoculated media; incubator temperature alarms; all equipment with valid portable appliance certificates.

## Data governance, provenance, and sharing
- Key governance needs:
  - Clear metadata mapping for all variables (strain/plasmid context, replicate IDs, units, experimental conditions).
  - Consistent file formats and naming conventions; resolve CSV vs XLSX discrepancy.
  - Documentation of versioning, licensing, and access restrictions (not specified in the dataset).
  - Explicit description of data provenance, including lot IDs, plate layouts, and any data transformations.

## Limitations and notes
- Outcome is based on CFU counts from plate assays, subject to plating and washing variability.
- Experimental conditions are specific (24 h at 37°C, particular beads and plasmids); cross-study comparability may require harmonized metadata and methods.

## References
- Howard SA, McCarthy RR. Modulating biofilm can potentiate activity of novel plastic-degrading enzymes. NPJ Biofilms Microbiomes. 2023 Oct 3;9(1):72. doi: 10.1038/s41522-023-00440-1. PMID: 37788986; PMCID: PMC10547765.