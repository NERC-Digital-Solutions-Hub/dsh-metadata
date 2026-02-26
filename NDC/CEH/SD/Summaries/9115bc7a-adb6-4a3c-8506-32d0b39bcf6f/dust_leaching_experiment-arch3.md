# Dust leaching

## Overview of the data
- Dataset contains the elemental composition of filtered water samples from an experiment testing dust addition effects on leaching in different water types.
- Location/time: KISS research station, Kangerlussuaq, West Greenland; lake SS903 water; April 2017 to 63 days.
- Sampling and analysis: samples filtered (GF/F) and analyzed by ICP-MS and ion chromatography at British Geological Survey laboratories.
- Researchers: Suzanne McGowan and Amanda Burson conducted the experiment; Michael Watts conducted the analyses.
- Aim: determine which elements leach out of dust in different water types.

## Experimental design / sampling regime / collection / generation methods
- Factorial design with two factors: dust (with dust (+) or no dust (-)) and water type (four treatments: D, A, N, B).
- Four replicates per treatment (fully factorial).
- Dust treatments: + (dust added) or - (no dust).
- Water types: D = deionised water autoclaved to remove microbes; A = abiotic lake water filtered and autoclaved; N = nanobiotic lake water filtered; B = biotic lake water filtered to remove zooplankton.
- Incubation: 10°C with a 16:8 light:dark cycle, ~40 μmol photons m⁻² s⁻¹ PAR.
- Sampling points: 0 days (initial), 1 day, 7 days, and 63 days (labelled as 40 in the dataset).
- At the end, the entire sample was filtered and analyzed; samples stored in a refrigerator.

## Analytical methods
- ICP-MS: Agilent 8900 ICP-QQQ-MS with He collision mode (5.5 ml/min) for most elements; O2 (30%) with MS/MS for P, S, As, Se to measure oxide product ions.
- Ion Chromatography: Dionex ICS5000 for anions (using KOH eluents, guard/analytical columns, suppressed conductivity detection).
- Units and data structure are described in the dataset.

## Nature and units of recorded values
- Values are reported in the accompanying spreadsheet and table (specific units per element are listed there).

## Quality control
- Detection limits indicated in the spreadsheet; values below detection limit marked as <n.
- QC check standards analyzed at the start and end of each run and after no more than every 20 samples.
- Laboratories are ISO/IEC 17025 accredited.

## Details of data structure
- Dataset comprises 129 rows (128 samples plus a header) and 71 columns.
- Key schema:
  - Code: description and units; technique (ICP-MS or IC).
  - Water_type: D, A, N, or B.
  - Dust: + or -.
  - Replicate: 1-4.
  - Time: sampling end point (0, 1, 7, 40).
  - Elemental measurements: Ca, Mg, Na, K, Cl, SO4, NO3, Br, NO2, HPO4, F, Total P, Total S, Si, SiO2, and a wide range of trace elements (e.g., Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, V, Cr, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, La, Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Tm, Yb, Lu, Hf, Ta, W, Tl, Pb, Th, U).
- Each row specifies the measurement context (dust, water type, replicate, time) and corresponding concentration values by method.

## Relevance to monitoring frameworks (Authors of Monitoring Frameworks perspective)
- Illustrates a designed data collection workflow for environmental health monitoring, including:
  - Clear experimental design to isolate factors affecting leaching (dust presence and water type).
  - Robust analytical methods with detailed QC and ISO 17025 accreditation, supporting trustworthy data for policy scrutiny.
  - Comprehensive metadata that links samples to treatments, replicates, and time points, aiding reproducibility and data governance.
  - explicit data structure and documentation of measurement techniques, enabling data sharing and integration into dashboards or monitoring reports.
- Highlights typical monitoring framework challenges:
  - Metadata completeness and standardization across datasets (addressed via labeled columns and method details).
  - Data accessibility and openness (dataset notes QC and accreditation, but data sharing would depend on repository policies).
  - Data transformation needs (large panel of elements and units; requires careful harmonization for policy use).
  - Ensuring up-to-date, quality-assured data through governance processes (QC, detection limits, and accreditation are in place).