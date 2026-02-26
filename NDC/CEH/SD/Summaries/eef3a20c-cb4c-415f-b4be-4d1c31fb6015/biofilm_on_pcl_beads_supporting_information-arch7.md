# Biofilm data of plastic degrading bacteria on PCL beads in laboratory conditions.

## Summary
- Dataset on the number of bacterial colonies recovered from plastic beads (PCL) incubated in a 96-well plate for 24 hours at 37°C.
- Purpose: test whether artificially modulating intracellular cyclic-di-GMP levels by overexpressing plasmid-encoded diguanylate cyclases (WspR and DgcC) in a plastic-degrading E. coli strain increases biofilm formation on beads.
- File format: .csv; file naming noted as Biofilm_on_PCL_beads.xlsx (discrepancy between format and name).
- Recorded values: Colony Forming Units (CFUs) per culture/replicate; Strain and Description identify constructed plasmids or empty vector controls; Replicate captures biological replicates.

## Dataset content and structure
- Primary variables:
  - Strain: name and plasmid description or empty vector (text).
  - Description: details of what is encoded in each plasmid.
  - Replicate: biological replicate identifier (text or numeric).
  - Units: Colony Forming Units (CFUs) (text for descriptive fields; numeric CFU counts in data rows).
- Measurement context: CFUs recovered from each culture after biofilm removal from PCL beads and serial dilutions.

## Collection and processing
- Inoculation and culture:
  - Overnight cultures used to inoculate new cultures starting at OD600 of 0.1; induced at OD600 of 0.6 with 1 mM IPTG.
  - Induced culture (150 μL) added to wells containing a sterile PCL bead (in triplicate).
  - Incubation: 24 hours at 37°C.
- Biofilm recovery and plating:
  - Beads removed, washed 3× in PBS, then sonicated for 10 minutes to detach biofilms.
  - PBS suspension serially diluted and spotted in triplicate on LB agar with appropriate antibiotics.
  - Incubation: 16 hours at 37°C; colonies counted to determine CFUs on beads.
- Experimental design: three biological replicates per condition with triplicate plating.

## Materials and instrumentation
- Fisher Scientific Cell Density Meter 40-80-3000-45-D1-FR-E
- Sci-Quip S-Series Incu-80S incubator
- Camlab Transsonic T460 bath (sonication)
- Sterile PBS, LB agar with antibiotics, sterile PCL beads

## Calibration and quality control
- OD600 measurements blanked with uninoculated media prior to readings.
- Incubator temperature strictly controlled at 37°C; no temperature alarm events.
- All equipment with valid Portable Appliance Testing (PAT) certificates.
- Controls: bacteria with empty vectors (EV) lacking biofilm-inducing genes.
- Three biological replicates conducted.

## Experimental design and sampling regime
- Comparison across strains with different plasmid constructs (including empty vector).
- Triplicate plating for each biological replicate to assess CFU counts.

## References
- Howard SA, McCarthy RR. Modulating biofilm can potentiate activity of novel plastic-degrading enzymes. NPJ Biofilms Microbiomes. 2023 Oct 3;9(1):72. doi: 10.1038/s41522-023-00440-1. PMID: 37788986; PMCID: PMC10547765.

## GIS-relevant notes (data-use considerations)
- Spatial aspect: none inherent; data are lab-based CFU counts. If integrating into GIS workflows, consider adding:
  - Metadata for laboratory location, experiment date, and batch identifiers.
  - Standardized field schemas for Strain, Plasmid, Replicate, and CFU counts to enable cross-dataset joins.
  - Data quality flags and provenance to support reproducibility and traceability.
- Potential GIS use: map-based visualization of experiment conditions or strain performance across replicates if linked with additional contextual data (e.g., bead type, incubation conditions).