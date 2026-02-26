# Biofilm data of plastic degrading bacteria on PCL beads in laboratory conditions.

## Purpose and context
- Investigates whether artificially increasing intracellular Cyclic-di-GMP by overexpressing plasmid-encoded diguanylate cyclases (wspR and dgcC) in a plastic-degrading E. coli strain enhances biofilm formation on plastic beads (PCL) in a controlled laboratory setup.

## Data description
- Dataset details:
  - File format: .csv (with a naming convention referencing Biofilm_on_PCL_beads.xlsx)
  - Recorded values: number of bacterial colonies (colony forming units, CFUs) recovered from PCL beads for each culture/strain.
  - Metadata fields include: Strain (name and encoded plasmid or empty vector), Description; Units (Text); Replicate (biological replicate) with CFUs as units.
- Nature of data: CFU counts from cultures exposed to different plasmid constructs/conditions.

## Experimental design and collection methods
- Culture and induction:
  - Overnight cultures inoculated into new cultures to OD600 = 0.1.
  - Induction at OD600 = 0.6 with 1 mM IPTG.
- Inoculation and sampling:
  - 150 μL induced culture added to a 96-well plate containing a sterile PCL bead, in triplicate.
  - Incubation for 24 hours at 37 °C.
  - Beads removed, washed three times in sterile PBS, then sonicated for 10 minutes to detach biofilms.
  - Serial dilutions prepared from PBS suspension and spotted in triplicate on LB agar with appropriate antibiotics.
  - Plates incubated for 16 hours at 37 °C to count CFUs.

## Laboratory instrumentation and fieldwork
- Instruments:
  - Fisher Scientific Cell Density Meter 40-80-3000-45-D1-FR-E
  - Sci-Quip S-Series Incubator Incu-80S
  - Camlab Transsonic T460 bath
- Calibration and quality checks:
  - OD600 measurements blanked with uninoculated media.
  - Incubator temperature monitored with a 37 °C set point; no deviation alarms reported.
  - Equipment accompanied by valid portable appliance testing certificates.

## Quality control and replication
- Controls:
  - Bacteria with empty vectors (EV) served as negative controls for biofilm induction.
- Replication:
  - Three biological replicates per condition.

## Data governance and provenance
- Data origin referenced to a published work:
  - Howard SA, McCarthy RR. Modulating biofilm can potentiate activity of novel plastic-degrading enzymes. NPJ Biofilms Microbiomes. 2023;9(1):72.
- Data availability and sharing implications:
  - Metadata present for some key aspects, but explicit metadata completeness and data sharing permissions are not detailed in the document.

## Implications for monitoring frameworks
- Relevance:
  - Demonstrates a structured approach to linking experimental manipulation (genetic constructs) with measurable environmental-relevant outcomes (biofilm formation on plastic surfaces).
  - Provides a clear data lineage from culture conditions to CFU outcomes, essential for reproducibility and policy-relevant evaluation.
- Considerations for policy-oriented monitoring:
  - Emphasizes the need for complete metadata, standardized data formats, and transparent data governance to enable reuse in environmental health assessments.
  - Highlights potential data-management barriers such as metadata completeness, data sharing requirements, and coordination across labs to avoid silos.

## Limitations
- Lab-based, not environmental-field data; direct extrapolation to real-world plastic degradation requires caution.
- Metadata scope is somewhat limited; additional details (plasmid specifics, antibiotic concentrations, bead characteristics, and exact culture conditions) would strengthen interpretability and reuse.

## References
- Howard SA, McCarthy RR. Modulating biofilm can potentiate activity of novel plastic-degrading enzymes. NPJ Biofilms Microbiomes. 2023 Oct 3;9(1):72.