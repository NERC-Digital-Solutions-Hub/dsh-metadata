# Procedure for Real-time PCR assay NERC project NE/N019555/1

- Objective
  - Assess the presence of bla CTX-M-1 and bla NDM-1 in environmental and human fecal samples using quantitative PCR (qPCR).

- Equipment
  - CFX96 Touch Real-Time PCR Detection System (Bio-Rad)
  - PCR hood with UV light
  - Vortex mixer
  - Rotor
  - Refrigerator (2-8°C)
  - Refrigerator (-20°C)

- Reagents
  - Amplification and detection of bla CTX-M-1 (159 bp) and bla NDM-1 (152 bp) amplicons using TaqMan technology (Bio-Rad)
  - In-house designed primers:
    - bla CTX-M-1 F: 5-ACGTGGCGATGAATAAGCTG-3
    - bla CTX-M-1 R: 5-CCCGAGGTGAAGTGGTATCA-3
    - bla NDM-1 F: 5-C AAC CAC AGC CTG ACT TTC GC-3
    - bla NDM-1 R: 5-CAG CCA CCA AAA GCG ATG TC-3
  - In-house designed probes:
    - bla CTX-M-1 Probe: 5-FAM-ACGTTAAACACCGCCATTCC-3-BHQ
    - bla NDM-1 Probe: 5-FAM-TGGCCCGCTCAAGGTATTTT-3-BHQ
  - Probes labeled with 6-carboxyfluorescein (FAM) at 5' and Black Hole Quencher (BHQ) at 3'

- Methods
  - Primer/probe optimization
    - Evaluate primer concentrations (200, 300, 500, 900 nM) and probe concentrations (100, 200, 300 nM) to optimize sensitivity.
    - Final optimization yields best detection limits with primer 500 nM and probe 200 nM for both targets.
  - Master mix and qPCR setup
    - 20.0 µL master mix containing:
      - 10.0 µL of SsoAdvanced Supermix (2x) (Bio-Rad)
      - 0.2 µL of each primer (500 nM)
      - 0.2 µL of probe (200 nM)
      - 7.4 µL nuclease-free water
      - 2.0 µL of DNA sample
  - qPCR cycling conditions
    - Initial denaturation: 3.0 min at 95°C
    - 35 cycles: 15 sec at 95°C, 25 sec at 57°C

- Data interpretation (standard curve)
  - Positive control
    - A plasmid containing conserved sequences of both bla CTX-M-1 and bla NDM-1 is used as a positive control.
  - Standard curve
    - Prepare a series of plasmid DNA concentrations to generate a standard curve by plotting threshold cycle (Ct) values (Y-axis) against log DNA quantity (X-axis).
  - Quantification
    - Determine the quantities of bla CTX-M-1 and bla NDM-1 from the standard curve following the methodology described in Naas et al., 2011.

- Reference
  - Naas T, Ergani A, Carrer A, Nordmann P. Real-time PCR for detection of NDM-1 carbapenemase genes from spiked stool samples. Antimicrob Agents Chemother. 2011 Sep;55(9):4038-43.