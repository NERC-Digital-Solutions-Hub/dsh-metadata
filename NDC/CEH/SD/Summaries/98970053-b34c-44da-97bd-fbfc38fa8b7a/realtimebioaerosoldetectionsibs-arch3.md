# Real-time bioaerosol emission data from a range of environmental sources, UK, 2016-2018

## Overview
- Project funded by the Natural Environment Research Council under the Environmental Microbiology and Human Health programme.
- Evaluates a novel ultraviolet light-induced fluorescence (UV-LIF) bioaerosol sensor unit (Spectral Intensity Bioaerosol Sensor, SIBS).
- SIBS measures single-particle size, number, shape, and fluorescence across 16 wavelength bands (298–735 nm) for two excitation wavelengths (285 nm and 370 nm) in real time.
- Primary aim: assess the utility of SIBS for quantifying bioaerosol emissions and characterizing their spatio-temporal dispersion from industrial and agricultural sources.
- Real-time measurements conducted in chamber settings and real-world environments (composting, dairy farms, chicken farms, sewage treatment plants, urban/agricultural sites).

## Methods

### Chamber studies
- Purpose: test SIBS and related methods to elucidate physico-chemical and biological characteristics of bioaerosol emissions under controlled conditions.
- Facility: environmental chamber at Porton with HEPA-filtered air and up to 250 air changes per hour.
- Timelines: 2016 (compost only) and 2018 (compost and chicken litter).
- Data products: chamber emission intensity, particle concentrations, and particle size data.
- Related publications and access: detailed methods reported in open-access articles (DOIs provided in the dataset).
- Data files:
  - ChamberStudiesEmissionintensityAnalysis2016.csv
  - ChamberStudiesParticleconcentrations2016.csv
  - ChamberStudiesParticlesize2016.csv
  - ChamberStudies2018EmissionSpectraChickenLitter.csv
  - ChamberStudies2018EmissionSpectraCompost.csv

### Field measurements
- Scope: real-world environments including composting facilities, dairy farms, sewage works, urban background, and agricultural sites.
- Timeline: scoping studies in 2016; follow-up campaigns at Green Waste Composting (2016–2017) and other sites (2017–2018), including chicken farms (2018) and related source samplings.
- Sampling: continuous real-time SIBS measurements at heights of 1–1.5 m; both downwind and source measurements (e.g., near exhaust vents or within plumes).
- Emission spectra: site-specific fluorescence spectra computed from the measured emissions.
- Data files:
  - Green Waste Composting (2016): FieldmeasurementsCompostingDay12016.csv, FieldmeasurementsCompostingDay22016.csv, FieldmeasurementsCompostingDay32016.csv
  - Green Waste Composting and composting Source (2017): FieldmeasurementsCompostingDay12017.csv, FieldmeasurementsCompostingDay22017.csv, FieldmeasurementsCompostingDay32017.csv, FieldMeasurementsCompostingSource2017.csv
  - Agricultural farm (2017): FieldMeasurementsAgriculturalDay12017.csv, FieldMeasurementsAgriculturalDay22017.csv, FieldMeasurementsAgriculturalDay32017.csv
  - Chicken Farm and related (2018): FieldMeasurementsChickenFarmDay12018.csv, FieldMeasurementsChickenFarmDay22018.csv, FieldMeasurementsChickenFarmDay32018.csv, FieldMeasurementsChickenfarmSource2018.csv
- Emission spectra data: FieldMeasurementsEmissionSpectra.csv

## Instrumentation and data processing
- Instrument: Spectral Intensity Bioaerosol Sensor (SIBS) using UV-LIF.
- Data captured: particle size, concentration (total, excited, fluorescent), and fluorescence spectra across 16 channels for two excitation wavelengths.
- Processing: offline data analysis toolkit with 60-second averaging intervals; defined particle size bins; background fluorescence established via Forced Trigger (FT) mode prior to sampling.
- Fluorescent particle concentration calculation: Fluorescent = (F / E) × T, where F = fluorescent concentration, E = excited concentration, T = total concentration.
- Fluorescence spectra: derived by removing FT background and computing mean spectra across channels; mean spectrum calculated per site.

## Data products and accessibility
- Time-series data: total, excited, and fluorescent particle concentrations for multiple sites and campaigns.
- Emission spectra: site-specific fluorescence spectra and published emission spectra data (e.g., Green Waste Composting, Chicken Farm, Agricultural Farm, and sources).
- Data and analyses are linked to open-access journal articles; primary references provided for methodological details.

## Implications for monitoring frameworks
- Demonstrates an end-to-end workflow for real-time environmental health monitoring: instrument capability, experimental design (chamber and field), data capture, processing, and dissemination.
- Provides structured, multi-site data (time-series, size distributions, and spectra) suitable for evaluating policy-relevant indicators of bioaerosol emissions and exposure.
- Highlights data governance considerations relevant to monitoring frameworks: transparent methods, explicit data processing steps, and publicly referenced data sources.
- Emphasizes the importance of combining controlled experiments with real-world measurements to inform dispersion modeling and decision-making.

## References
- DOI: 10.3390/atmos9100379 (2016 compost chamber study)
- DOI: 10.1016/j.scitotenv.2018.08.120 (field sampling and SIBS methodology)