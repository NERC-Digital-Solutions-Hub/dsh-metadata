# Procedure for Real-time PCR assay

## Objective
- Assess the presence of bla CTX-M-1 and bla NDM-1 in environmental and human fecal samples using quantitative PCR (qPCR).

## Data Generated and Outputs
- qPCR results: presence/absence of bla CTX-M-1 and bla NDM-1 per sample.
- Quantitative data: copy numbers derived from a standard curve using plasmid DNA containing conserved sequences of both targets.
- Supporting details: amplicon sizes (CTX-M-1 ~159 bp; NDM-1 ~152 bp), Ct values for each reaction, and plasmid concentration points used to construct the standard curve.
- Documentation elements: primer and probe sequences, and probe labels (FAM with BHQ) for both targets.

## Experimental Design and Protocol Details (Data Elements to Capture)
- Equipment: CFX96 Touch Real-Time PCR Detection System (Bio-Rad); PCR hood with UV; vortex mixer; rotor; 2–8°C and -20°C storage.
- Reagents and assay design:
  - TaqMan-based amplification and detection for both targets (in-house designed).
  - In-house primers:
    - bla CTX-M-1 F: 5-ACGTGGCGATGAATAAGCTG-3
    - bla CTX-M-1 R: 5-CCCGAGGTGAAGTGGTATCA-3
    - bla NDM-1 F: 5-CAA CAC AGC CTG ACT TTC GC-3
    - bla NDM-1 R: 5-CAG CCA CCA AAA GCG ATG TC-3
  - In-house probes:
    - bla CTX-M-1 Probe: 5-FAM-ACGTTAAACACCGCCATTCC-3BHQ
    - bla NDM-1 Probe: 5-FAM-TGGCCCGCTCAAGGTATTTT-3BHQ
- Primer/probe optimization:
  - Tested primer concentrations: 200, 300, 500, 900 nM
  - Probe concentrations: 100, 200, 300 nM
  - Final optimized concentrations: primers 500 nM, probe 200 nM
- Master mix and reaction setup:
  - 20.0 µL reaction volume
  - 10.0 µL of SsoAdvanced Supermix (2x) (Bio-Rad)
  - 0.2 µL of each primer (500 nM)
  - 0.2 µL of probe (200 nM)
  - 7.4 µL nuclease-free water
  - 2.0 µL DNA sample
- qPCR conditions:
  - Initial denaturation: 3.0 min at 95°C
  - 35 cycles: 15 s at 95°C, 25 s at 57°C
- Standard curve and quantification:
  - Use plasmid DNA with conserved sequences of both bla CTX-M-1 and bla NDM-1 as positive control and for calibration.
  - Prepare varying plasmid DNA concentrations to generate standard curve (Ct vs. log DNA quantity).
  - Quantification derived from the standard curve per Naas et al. 2011 protocol.

## Data Quality, Provenance and Reproducibility
- Positive control and standard curve generation are integral to interpretation.
- Protocol includes explicit reagent concentrations, instrument, and cycling parameters to enable reproducibility.
- In-house primer/probe designs and associated sequences are documented for traceability.
- Reference methodology for quantification provided (Naas et al., 2011).

## Interpretation and Data Management Considerations for Data Stewards
- Data to be stored with clear linkage:
  - Sample identifiers, run dates, operator, instrument settings.
  - Primer/probe sequences, amplicon sizes, and probe labels.
  - Master mix composition and reaction volumes.
  - Ct values for each target per sample, and calculated copy numbers from the standard curve.
- Documentation and metadata:
  - Versioning of the protocol; any changes to primer/probe sequences or concentrations.
  - Lot numbers and sources for reagents (if available) to support QA.
  - Description of how positive determinations are made (thresholds, controls) and the method used for quantification (standard curve approach).
- Data sharing and publication:
  - Ensure that plasmid standard sequences and assay details are shared in a manner consistent with institutional policies and any biosafety considerations.
  - Cite the Naas et al. (2011) method when reporting quantification results.

## Reference
- Naas T, Ergani A, Carrèr A, Nordmann P. Real-time PCR for detection of NDM-1 carbapenemase genes from spiked stool samples. Antimicrob Agents Chemother. 2011 Sep; 55(9):4038-43.