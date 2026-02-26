# Functionalisation data, materials, and method statements of a carbon electrode biosensor for detection of antimicrobial resistance

## Overview and context

- Part of NERC Water Quality (Newton) program focusing on antimicrobial resistance (AMR) sensing platforms for point-of-care use.
- Goal: develop low-cost, electrochemical biosensors to detect AMR genes and quantify DNA targets via changes in electrochemical impedance.
- This document provides handover notes, fabrication details, functionalisation procedures, and results from Heriot-Watt University (HWU) experiments using carbon screen-printed electrodes (SPCE) on LTCC substrates.

## Sensor platform and detection principle

- Platform: electrochemical SPCE sensors on low-temperature co-fired ceramic (LTCC) substrates designed for nucleic acid detection.
- Target: AMR gene OXA-1 as a positive control; complementary (CT) and non-complementary (NCT) DNA targets used for validation.
- Biorecognition elements:
  - Peptide Nucleic Acid (PNA) probes immobilised on the carbon working electrode.
  - ssDNA targets used for hybridisation tests.
- Detection method: Electrochemical Impedance Spectroscopy (EIS) to measure changes in Charge Transfer Resistance (R_CT) as a function of target binding.
- Key observation: R_CT increases with incubation time and with higher CT concentrations; NCT shows minimal R_CT change, enabling discrimination.
- Data interpretation: Nyquist plots and equivalent circuit modeling are used to extract R_CT values (R_p.p. in Nova software).

## Sensor fabrication and functionalisation workflow

- Sensor type: LTCC-based SPCE with working electrode (WE), counter electrode (CE), and reference electrode (RE).
- Main fabrication steps (Appendix 1 summary):
  - Laser-cut LTCC layers and screen-printed silver electrodes.
  - Stacked LTCC layers, vacuum sealing, isostatic pressing, and sintering.
  - Screen-printed carbon and dielectric layers; dicing into sensors.
- PNA functionalisation (Section 1.4 and Appendix 3):
  - Pre-treatment: chronoamperometric cleaning in saturated Na2CO3.
  - In-situ diazonium formation to generate 4-carboxyphenyl film on SPCE (electrodeposition of diazonium-derived layer).
  - Activation: 60 min incubation in EDC/NHS in MES buffer to activate carboxyl groups.
  - PNA immobilisation: incubation with amino-modified PNA probe (10 μM) for surface attachment.
  - Blocking: 30 min incubation with 1% ethanolamine in PBS to block non-specific sites.
- Target and measurement (Section 2.3–2.4):
  - 52 min incubation with target DNA in EIS buffer (1 mM KCl + 2 mM ferri/ferrocyanide).
  - EIS measurements to determine R_CT before and after target incubation.
  - Data analysis via Nyquist plots and a simplified Randles circuit to extract R_CT.

## Data formats, outputs, and key results

- Data/file naming convention (Section 2.1):
  - Files labeled A_B_C_D_E_.jpeg representing Date (ddmmyy), Experiment, Target Type (CT/NCT), DNA concentration (μM), Incubation time (s).
  - Example: 160721_EX02_CT_20_30 corresponds to 16/07/2021, Experiment EX02, CT target at 20 μM, 30 s incubation.
- Output metrics:
  - Primary metric: Charge Transfer Resistance (R_CT, in MΩ) from EIS data.
  - Observed trend: R_CT increases with longer incubation times and higher CT concentrations (Figure 6 and related data).
  - CT vs NCT comparison: CT yields larger R_CT increases than NCT at corresponding conditions (Figure 7).
  - R_CT vs CT concentration: Significant positive correlation (Pearson 0.810, p < 0.001) between CT concentration and R_CT (Table 1 and Figure 9–10).
- Limit of detection (LOD):
  - LOD observed at 500 nM OXA-1 gene CT in HW SPCE with OXA-1 CT target (Figure 11).
- Time and concentration dependence:
  - R_CT rises over incubation (0, 30, 52 minutes) with CT targets; CT concentration effects evident across tested ranges (Figures 6, 9, 10, 11).

## Data management, quality, and accessibility

- Data organization and terminology:
  - Appendix 9 provides a catalog of R_CT values across multiple experiments, CT/NCT concentrations, and incubation times.
  - Consistent use of CT/NCT labels and concentration-time points to enable cross-comparison.
- Data handling practices:
  - Reference to stored datasets, with explicit instructions for naming, uploading, and portal storage (aligned with analysts’ aim to ensure datasets are accessible and reusable).

## Results in depth (highlights)

- R_CT vs incubation time:
  - Longer incubation results in higher R_CT for CT targets, indicating stronger hybridisation signal.
- Complementary vs non-complementary discrimination:
  - CT produces notable R_CT increases; NCT yields comparatively small changes, enabling specificity.
- Correlation and detection limits:
  - Strong positive correlation between CT concentration and R_CT (0.810); LOD established around 500 nM CT for detectable signal over background.

## Future work and development directions (as listed)

- Complete assembly of a readout multiplexing system.
- Assess readout system stability and accuracy.
- Design a microfluidic multiplexer for multiple sensors reading.
- Develop a multi-working-electrode (multi-WE) sensor approach to reduce readout system size.

## Relevance to environmental monitoring perspective

- Provides a standardized, data-rich workflow for environmental AMR surveillance by enabling:
  - Clear documentation of fabrication, functionalisation, and measurement protocols.
  - Quantitative, comparable data (R_CT) across time and targets.
  - Clear data formats and storage practices to facilitate reuse and scrutiny of environmental AMR sensor performance.
- Aligns with Analysts Monitoring the Environment emphasis on data quality, standardisation, and accessibility to support long-term environmental health assessment and policy evaluation.