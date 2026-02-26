# Working Title Biofilm data of plastic degrading bacteria on PCL beads in laboratory conditions.

## Overview
- Dataset documenting the number of bacterial colonies (CFUs) recovered from plastic beads (PCL) after 24 hours of incubation at 37°C in a 96-well plate.
- Purpose: assess whether increasing intracellular levels of the second messenger cyclic-di-GMP via overexpression of diguanylate cyclases (wspR and dgcC) in a plastic-degrading E. coli strain enhances biofilm formation on plastic beads.

## Data Content and Format
- File format: CSV (with an associated file naming convention Biofilm_on_PCL_beads.xlsx).
- Recorded values: CFUs of colonies recovered on selective LB agar plates from each culture.
- Key data fields:
  - Strain, Description: name of each strain and plasmid content (or empty).
  - Strain, Units: Text.
  - Replicate, Description: bacteria recovered from each biological replicate per strain.
  - Replicate, Units: CFUs.
- Experimental setup:
  - Bacteria induced with 1 mM IPTG at OD600 of 0.6; 150 μL added to a sterile PCL bead in triplicate per condition.
  - After 24 hours, beads washed, sonicated to detach biofilm, serial dilutions prepared, and plated on LB with appropriate antibiotics.
  - Incubation: 16 hours at 37°C before CFU counting.

## Metadata and Provenance
- Instruments and equipment used:
  - Fisher Scientific Cell Density Meter 40-80-3000-45-D1-FR-E
  - Sci-Quip S-Series Incubator Incu-80S
  - Camlab Transsonic T460 bath (35 kHz)
- Calibration and controls:
  - OD600 measurements blanked with uninoculated media.
  - Temperature controlled at 37°C with alarms; no deviation events reported.
  - All equipment had valid portable appliance testing certificates.
- Experimental design details:
  - Overnight cultures used to inoculate new culture with starting OD600 0.1; induction at OD600 0.6.
  - Triplicate wells per condition; 24-hour incubation before processing.

## Methods and Quality Assurance
- Experimental design included three biological replicates.
- Quality controls consisted of strains with empty vectors lacking biofilm-inducing genes.
- Processing workflow ensures removal of unattached bacteria (washing) and detached biofilms (sonication) prior to CFU enumeration.
- Documentation of strains/plasmids and replication ensures traceability and reproducibility.

## Data Access, Use and Governance
- Primary data format: CSV; filename hints at a related Excel file (Biofilm_on_PCL_beads.xlsx) for reference.
- Data are linked to a published reference:
  - Howard SA, McCarthy RR. Modulating biofilm can potentiate activity of novel plastic-degrading enzymes. NPJ Biofilms Microbiomes. 2023;9(1):72. doi: 10.1038/s41522-023-00440-1.
- Metadata captures organism constructs, replication, experimental conditions (IPTG induction, OD600, temperature, duration), and processing steps to support discoverability and reuse.

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle: experimental design, data capture, processing (detachment, dilution, plating), and metadata provisioning.
- Supports data stewardship practices: clear description of strains/plasmids, units, replicates, and processing steps; enables traceability and reproducibility.
- Highlights data governance considerations:
  - Importance of consistent metadata (strain descriptions, replicate identifiers, units).
  - Need for standardized data formats and naming conventions to improve discoverability and interoperability.
- Illustrates potential data quality challenges and controls (biological replicates, proper controls, calibration steps) relevant to planning and scaling data programs.