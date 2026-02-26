# Physical and chemical properties of wildfire ash collected from different ecosystems and burn severities across the globe, 2003-2021

## Overview
- A global dataset characterizing wildfire ash chemical and physical properties.
- Two data files: ash_chemical_properties.csv (chemical characteristics) and ash_physical_properties.csv (physical characteristics).
- Produced by Swansea University, UK; intended for GIS-based map visualisations and spatial analysis.

## Spatial and Temporal Coverage
- Temporal scope: ash samples collected 2003–2021; laboratory analyses conducted 2003–2022.
- Geographic scope: multiple ecosystems worldwide; sampling sites identified by country and site name.
- Specific sampling sites and coordinates:
  - Madre del Agua, Tenerife, Spain (UTM 28N 28R 343340 3119657)
  - Thompson reservoir, Victoria, Australia (UTM 55H 441956 5822296)
  - Higher Swineshaw reservoir, Manchester, UK (UTM 30U 566670 5927917)
  - Mesa Fire, Idaho, USA (UTM 11T 551172 4950864)
- Data provenance: chemical analyses conducted at Swansea University (UK).

## Data Structure and Variables
- Chemical characteristics (ash_chemical_properties.csv):
  - Variables include: country, site name, year, burn severity, sample name; δ13C; total concentrations of C, CO3, N; mass fractions of P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, Cr, Co, Br, Sr; dissolved concentrations (DOC, NH4+, NO3−, Cl−, SO4−, F−, P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, B); Hg, As, Cd (both total and dissolved where applicable); pH; electrical conductivity (EC); UV transmittance (%T); and other detailed leachate-derived metrics.
  - Replication: 2–20 replicates per site and treatment.
  - Observations: 296 chemical samples.
- Physical characteristics (ash_physical_properties.csv):
  - Variables include: country, site name, year, burn severity, sample name; water retention at 33 kPa (WR_33kPa) and 1500 kPa (WR_1500kPa); particle density (g cm−3); water drop penetration time (WDPT) categories (WDPT_1 to WDPT_10 with defined time ranges).
  - Replication: 4 replicates per site and treatment.
  - Observations: 36 physical samples.
- Treatments: ash produced at extreme, high, moderate, and low burn severities.
- Data completeness: chemical characteristics—some parameters not analysed for certain samples; physical characteristics—complete dataset.

## Analytical Methods and Protocols
- Chemical analyses (summary):
  - pH and EC measured from leachates; instruments include pH meter (Crison micro pH 2000) and conductivity meter (Crison GLP 31).
  - Major and trace elements measured via leachate or acid digestion; techniques include Ion Chromatography (Cl−, NO3−, SO4−), Atomic Absorption Spectrometry (As, Ca, Br, Mg, Al, Cd, Co, Cr, Cu, Fe, Mn, Ni, Pb, Sr, Zn, Na), Atomic Emission (Na), and Hg via EPA 7473.
  - Carbon content (%C, %N) via elemental analyzer (LECO TruSpec CHN).
  - Carbonates (CO32−) determined with Bernard Calcimeter following ISO 10693:1995.
  - UV index measured with spectrophotometry (254 nm).
  - DOC determined using colorimetric method after digestion.
  - P and PO4 determined with ascorbic acid method; calibration with mixed reagents.
- Physical analyses (summary):
  - Bulk density measured on oven-dried samples.
  - Water retention capacity at field capacity (33 kPa) and wilting point (1500 kPa) via pressure plate method.
  - Particle density determined with pycnometer.
  - WDPT used to assess water repellency (classification into time-based drops).
- Sample preparation and digestion:
  - Total analysis digestion per EPA 3051: approx. 0.25 g ash with nitric and hydrochloric acids, microwaved, diluted to 50 mL.
  - Leachate experiments follow a standardized protocol with 4 g sample in 100 mL water, shaking, standing, filtering, and sub-sampling for subsequent analyses.

## Data Quality, Completeness, and Provenance
- Completeness:
  - Chemical dataset: some parameters not analysed for certain ash samples.
  - Physical dataset: complete dataset.
- Observations counts: 296 chemical samples; 36 physical samples.
- Provenance: laboratory analyses performed at Swansea University; methods documented for reproducibility and cross-study comparison.

## GIS and Applications
- Suitable for map-based visualization of chemical and physical properties by location, burn severity, and year.
- Enables spatial analysis of ash characteristics across ecosystems and burn conditions.
- Can be integrated with site metadata (country, site name, sampling year) and geospatial coordinates (UTM) for GIS workflows and policy/research communication.