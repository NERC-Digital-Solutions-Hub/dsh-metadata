# Procedure for Real-time PCR assay

## Objective
- To assess the presence of bla CTX-M-1 and bla NDM-1 in environmental and human fecal samples using quantitative PCR (qPCR) with a TaqMan assay.

## Equipment
- CFX96 Touch™ Real-Time PCR Detection System (Bio-Rad)
- PCR hood with UV light
- Vortex mixer
- Rotor
- Refrigerator (2-8°C)
- Refrigerator (-20°C)

## Reagents

1. Amplification and detection of the bla CTX-M-1 (159 bp) and bla NDM-1 (152 bp) amplicons will be done with TaqMan technology (Bio-Rad).
2. Primer sequences (designed in-house):
   - bla CTX-M-1 F: 5-ACGTGGCGATGAATAAGCTG-3
   - bla CTX-M-1 R: 5-CCCGAGGTGAAGTGGTATCA-3
   - bla NDM-1 F: 5-CAA CAC AGC CTG ACT TTC GC-3
   - bla NDM-1 R: 5-CAG CCA CCA AAA GCG ATG TC-3
3. Probes sequences (designed in-house, labeled with 6-carboxyfluorescein (FAM) at 5' and Black Hole Quencher (BHQ) at 3'):
   - bla CTX-M-1 Probe: 5-FAM-ACGTTAAACACCGCCATTCC-3BHQ
   - bla NDM-1 Probe: 5-FAM-TGGCCCGCTCAAGGTATTTT-3BHQ

## Methods

1. Primer and probe concentrations will be optimized by testing primer concentrations of 200, 300, 500, and 900 nM and probe concentrations of 100, 200, and 300 nM.
2. Final optimization results indicate the best detection limits at: primers 500 nM and probe 200 nM.
3. Master mix (20.0 µL total) will contain:
   - 10.0 µL of SsoAdvanced Supermix (2x) (Bio-Rad)
   - 0.2 µL of each primer (500 nM)
   - 0.2 µL of probe (200 nM)
   - 7.4 µL nuclease-free water
   - 2.0 µL of the respective DNA samples
4. qPCR cycling conditions:
   - 3.0 min at 95°C
   - 35 cycles of: 15 sec at 95°C, 25 sec at 57°C

## Interpretation of qPCR results using standard curve

- A plasmid containing conserved sequences of both bla CTX-M-1 and bla NDM-1 will be considered positive by qPCR.
- A standard curve will be generated from different plasmid DNA concentrations by plotting threshold cycle (CT) values (Y-axis) against the log of DNA quantity (X-axis).
- Quantities of bla CTX-M-1 and bla NDM-1 will be determined from the standard curve as described in Naas et al., 2011.

## Reference
- Naas T, Ergani A, Carrër A, Nordmann P. Real-time PCR for detection of NDM-1 carbapenemase genes from spiked stool samples. Antimicrob Agents Chemother. 2011 Sep; 55(9):4038-43.

## Data management considerations for Data Leaders
- Outputs to capture: CT values and quantified copies of bla CTX-M-1 and bla NDM-1 derived from the standard curve.
- Data provenance: link results to specific primer/probe sets, their concentrations, master mix composition, and exact qPCR cycling parameters.
- Quality controls: include positive plasmid controls and appropriate negative controls to validate results.
- Metadata and discoverability: document primer/probe sequences, amplicon sizes, reaction conditions, and instrument used to ensure reproducibility and future data integration.
- Reproducibility: standardized optimization steps and final conditions to enable cross-lab comparisons and aggregation across studies.