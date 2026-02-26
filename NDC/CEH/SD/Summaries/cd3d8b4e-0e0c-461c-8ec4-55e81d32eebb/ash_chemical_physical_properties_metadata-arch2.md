# Physical and chemical properties of wildfire ash collected from different ecosystems and burn severities across the globe, 2003-2021

## Overview
- Global dataset of wildfire ash chemical and physical properties collected from 2003 to 2021.
- Two data files: ash_chemical_properties.csv and ash_physical_properties.csv.
- Chemical analyses coordinated by Swansea University (UK); samples sourced from multiple global sites; laboratory analyses conducted 2003–2022.
- Aim: characterize wildfire ash chemical and physical properties for environmental monitoring and policy assessment.

## Data files and scope
- ash_chemical_properties.csv
  - Chemical characteristics dataset.
  - Key fields: country, sampling site, year, burn severity, material type, sample name, δ13C, total concentrations (C, CO3, N), total and dissolved concentrations of multiple elements (e.g., P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, Cr, Co, Br, Sr), Hg, As, Cd; pH, electric conductivity (EC), UV254; dissolved organic carbon (DOC); Cl−, NO3−, SO42−, F−, P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb; as well as Hg, As, Cd in dissolved form.
  - Observations: 296 wildfire ash chemical samples.
  - Completeness: some chemical parameters not analysed for certain samples.
- ash_physical_properties.csv
  - Physical characteristics dataset.
  - Key fields: country, sampling site, year, burn severity, sample name, water retention at 33 kPa (WR_33kPa), water retention at 1500 kPa (WR_1500kPa), particle density (g cm−3), water drop penetration time (WDPT) classes.
  - Observations: 36 wildfire ash samples.
  - Completeness: complete dataset for physical properties.

## Sampling sites and temporal coverage
- Madre del Agua, Tenerife, Spain
- Thompson Reservoir, Victoria, Australia
- Higher Swineshaw Reservoir, Manchester, United Kingdom
- Mesa Fire, Idaho, USA
- Country field used to identify sampling locations
- Timeframe: ash collection 2003–2021; laboratory analyses 2003–2022

## Measurements and variables
- Chemical characteristics (ash_chemical_properties.csv)
  - Isotopic: δ13C (‰)
  - Total concentrations (mg kg−1 or %): C, CO3, N
  - Major/minor elements: P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, Cr, Co, Br, Sr
  - Trace/heavy elements: Hg, As, Cd (µg kg−1 or mg kg−1 as applicable)
  - pH, electric conductivity (EC; µS cm−1), UV254 (% T)
  - Dissolved concentrations (mg kg−1): organic C (DOC), NH4+, NO3−, Cl−, SO42−, F−, P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, B
  - Dissolved Hg, As, Cd (µg kg−1)
- Physical characteristics (ash_physical_properties.csv)
  - Water retention: WR_33kPa, WR_1500kPa
  - Particle density (g cm−3)
  - Water drop penetration time (WDPT) classes (e.g., WDPT_1 to WDPT_10 with time ranges)

## Analytical methods
- Chemical analyses
  - Digestion for total analysis: EPA 3051 (Microwave digestion)
  - Leachate experiments: standardized leachate protocol based on Southern California wildfire study
  - Carbonates: Bernard Calcimeter (ISO 10693:1995)
  - pH and EC: pH meter (Crison micro pH 2000); conductivity meter (Crison GLP 31)
  - Anions/cations: Cl−, NO3−, SO4−, F− via ion chromatography
  - Dissolved species and elements: UV254, DOC (colorimetric), P and PO4 via colorimetry, multielement determinations via Atomic Absorption Spectrometry (AAS) or Inductively Coupled Plasma methods; Na via AAS or atomic emission
  - Hg: EPA 7473 (thermal decomposition, amalgamation, AAS)
  - Instrumentation: LECO elemental analyzer for %C and %N; various spectrometers and chromatographs for specific analytes
- Physical analyses
  - Bulk density: oven-dried core basis (105°C)
  - Water retention: Richard’s pressure plates method
  - Particle density: pycnometer with deionized water
  - WDPT: standard water repellency test (Doerr scheme)

## Replication, quality, and completeness
- Replication
  - Chemical characteristics: 2 to 20 replicates per site and treatment
  - Physical characteristics: 4 replicates per site and treatment
- Quality notes
  - Completeness: chemical dataset contains some parameters not analysed for certain samples; physical dataset is complete
  - Data provenance: samples originate from defined sampling sites; analyses performed at Swansea University and collaborating laboratories

## Data usage for monitoring and policy
- Provides a standardised, cross-ecosystem set of wildfire ash properties suitable for tracking environmental health indicators over time.
- Facilitates data integration with other environmental datasets and supports assessment of policy performance related to wildfire impacts.
- Clear metadata and replication support enhance reproducibility and transparency for environmental monitoring programs.