# Procedure for Real-time PCR assay NERC project NE/N019555/1

## Objective
- Assess the presence of bla CTX-M-1 and bla NDM-1 in environmental and human fecal samples using quantitative PCR (qPCR).

## Equipment
- CFX96 Touch Real-Time PCR Detection System (Bio-Rad)
- PCR hood with UV light
- Vortex mixer
- Rotor
- Refrigerator (2–8°C)
- Refrigerator (-20°C)

## Reagents
- TaqMan-based amplification and detection for bla CTX-M-1 (159 bp) and bla NDM-1 (152 bp)
- In-house designed primers:
  - bla CTX-M-1 F: 5-ACGTGGCGATGAATAAGCTG-3
  - bla CTX-M-1 R: 5-CCCGAGGTGAAGTGGTATCA-3
  - bla NDM-1 F: 5-CAA CAC AGC CTG ACT TTC GC-3
  - bla NDM-1 R: 5-CAG CCA CCA AAA GCG ATG TC-3
- In-house designed probes:
  - bla CTX-M-1 Probe: 5-FAM-ACGTTAAACACCGCCATTCC-3BHQ
  - bla NDM-1 Probe: 5-FAM-TGGCCCGCTCAAGGTATTTT-3BHQ
- Probes labeled with FAM (5') and BHQ (3'); in-house synthesized

## Methods
- Optimization:
  - Evaluate primer concentrations: 200, 300, 500, 900 nM
  - Evaluate probe concentrations: 100, 200, 300 nM
- Final optimization:
  - Best detection limits with primer 500 nM and probe 200 nM
- Master mix (20 µL):
  - 10.0 µL SsoAdvanced Supermix (2x) (Bio-Rad)
  - 0.2 µL each primer (500 nM)
  - 0.2 µL probe (200 nM)
  - 7.4 µL nuclease-free water
  - 2.0 µL DNA samples
- qPCR cycling:
  - 3.0 min at 95°C
  - 35 cycles: 15 sec at 95°C, 25 sec at 57°C

## Interpretation of qPCR results using standard curve
- Positive control: plasmid containing conserved sequence for both bla CTX-M-1 and bla NDM-1
- Standard curve: plot threshold cycle (Ct) versus log of plasmid DNA quantity using varying concentrations
- Quantification: determine bla CTX-M-1 and bla NDM-1 quantities from the standard curve as per Naas et al., 2011

## Reference
- Naas T, Ergani A, Carrër A, Nordmann P. Real-time PCR for detection of NDM-1 carbapenemase genes from spiked stool samples. Antimicrob Agents Chemother. 2011 Sep;55(9):4038-43.

## Relevance to GIS and data visualization
- Potential outputs: sample-specific Ct values and estimated gene copy numbers with associated spatial metadata (location, time, sample type)
- Data integration: require standardized units, naming, and units for copy numbers to enable cross-site mapping
- Quality and provenance: document assay conditions, standard curve parameters, and detection limits to ensure comparability across datasets
- Visualization: map prevalence and abundance of bla CTX-M-1 and bla NDM-1 to support spatial analyses and policy/research communication