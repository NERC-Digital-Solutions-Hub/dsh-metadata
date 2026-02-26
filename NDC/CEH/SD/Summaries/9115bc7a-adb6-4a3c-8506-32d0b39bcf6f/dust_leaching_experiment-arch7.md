# Dust leaching

## Overview
- Dataset: elemental composition of filtered water samples from a dust leaching experiment.
- Location and samples: conducted at the KISS research station, Kangerlussuaq, West Greenland; water from lake SS903 (coordinates provided) was used.
- Objective: determine which elements leach out of dust in different water types.
- Timeline: experiment started April 2017 and ran for 63 days; samples stored refrigerated after collection.
- Responsible teams: Suzanne McGowan and Amanda Burson (experiments); Michael Watts (analyses).

## Experimental design and sampling
- Factors and design: fully factorial with two factors and four replicates.
  - Dust: with dust (+) vs. no dust (-).
  - Water type: D (deionised autoclaved), A (abiotic lake water filtered and autoclaved), N (nanobiotic lake water filtered), B (biotic lake water filtered to remove zooplankton).
- Replicates: 4 per treatment combination.
- Incubation conditions: 10°C with a 16:8 light:dark cycle; photon irradiance ≈ 40 μmol photons m⁻² s⁻¹ PAR.
- Sampling times: 0, 1, 7, and 63 days (the dataset labels the final time point as 40).
- Post-incubation processing: entire sample filtered through GF/F filter; filtered water analysed; samples stored refrigerated.

## Analytical methods and quality control
- Analytical techniques:
  - ICP-MS (Agilent 8900) with collision cell in He mode for most elements; for P, S, As, Se, O₂ is used with MS/MS to measure oxide product ions.
  - Ion Chromatography (Dionex ICS5000) for anions, using KOH mobile phase and suppressed conductivity detection.
- Quality control:
  - Detection limits are provided in the spreadsheet; values below detection limit shown as <n.
  - QC standards run at the start and end of each run and after no more than every 20 samples.
  - Laboratories are ISO 17025 accredited.

## Data structure and contents
- Dataset size: 129 rows (128 samples + header) and 71 columns.
- Core variables:
  - Metadata: Code, Water_type (D, A, N, B), Dust (+, -), Replicate (1–4), Time (sampling end point).
  - Measurements: multiple elements/ions with concentrations and units (e.g., Ca_mg/L, Mg_mg/L, Na_mg/L, K_mg/L, Cl-_mg/L, NO3-_mg/L, NO2-_mg/L, SO4^2-_mg/L, F-_mg/L, Total P_mg/L, Total S_mg/L, Si_mg/L, SiO2_mg/L, and many trace metals/resources such as Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, V, Cr, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, La, Ce, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Tm, Yb, Lu, Hf, Ta, W, Tl, Pb, Th, U).
  - Methods per measurement: ICP-MS or IC (as indicated in the column descriptions).
- Notes on structure:
  - Column scheme includes codes for treatment, water type, dust presence, replicate, and time point followed by a long list of element concentration measurements with corresponding units and analytical method.

## GIS and spatial considerations
- Spatial context: single study site (Kangerlussuaq region) with sampling from lake SS903; practical for GIS mapping when integrating with site-based or regional datasets.
- Potential GIS use:
  - Create map-based data products by linking each sample (Code) to its spatial origin (lake SS903) and overlaying temporal changes, dust treatments, and water-type categories.
  - Build composite layers showing concentration gradients across time points and treatment combinations.
  - Combine with environmental layers (e.g., groundwater, dust deposition zones) to explore spatial patterns of leached elements.

## Usage notes and caveats
- Data complexity: large number of elements with multiple measurement methods; careful handling required to map each variable to its method and unit.
- Detection limits: some values are below detection limits and are annotated accordingly.
- Provenance: analyses performed at British Geological Survey laboratories; data collection tied to a specific field site and experimental design as described.

## Provenance and references
- Experiment authors: Suzanne McGowan and Amanda Burson (experimental setup); Michael Watts (analytical work).
- Methods and data context: ICP-MS and IC analyses; ISO 17025 quality framework.