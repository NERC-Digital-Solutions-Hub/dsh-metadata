# Real-time bioaerosol emission data from a range of environmental sources, UK, 2016-2018

- A dataset from a Natural Environment Research Council project evaluating a novel UV-LIF based bioaerosol sensor (Spectral Intensity Bioaerosol Sensor, SIBS) to quantify and characterise bioaerosol emissions and dispersion from industrial and agricultural sources.
- Primary goal: assess the capabilities of SIBS to measure size, number, shape, and resolved fluorescence across 16 wavelength bands for real-time single particles, to support understanding of bioaerosol emissions and their spatio-temporal distribution.
- Study scope includes both controlled chamber experiments and field measurements across diverse UK environments.

## Overview of the sensor and measurements

- Instrument: Spectral Intensity Bioaerosol Sensor (SIBS) with UV excitation (285 nm and 370 nm) and 16 emission channels (298–735 nm) for single particles in real-time.
- Outputs:
  - Particle size, concentration, and shape
  - Resolved fluorescence emission spectra per particle
  - Fluorescence data across 16 channels for two excitation wavelengths
- Data processing: offline toolkit with 60-second averaging, predefined particle size bins, and total/excited/fluorescent particle concentrations. Fluorescence thresholds established using Forced Trigger mode (mean + 3 standard deviations per channel) prior to sampling.
- Data products include time-series of total, excited, and fluorescent particle concentrations, as well as site-specific mean fluorescence spectra.

## Chamber-based studies (controlled environment)

- Location: Environmental chamber at PHE Porton with HEPA-filtered air and high air-change rate (up to 250 ACH).
- Timeframe and sources:
  - 2016: Compost only
  - 2018: Compost and chicken litter
- Study design: Parallel testing of SIBS alongside other methods to elucidate physico-chemical and biological characteristics of bioaerosols in controlled conditions.
- Publications: open-access articles detailing the chamber study design and data (DOI references provided in the dataset).
- Associated data files (examples):
  - ChamberStudiesEmissionintensity2016.csv
  - ChamberStudiesParticleconcentrations2016.csv
  - ChamberStudiesParticlesize2016.csv
  - ChamberStudies2018EmissionSpectraChickenLitter.csv
  - ChamberStudies2018EmissionSpectraCompost.csv

## Field measurements (real-world deployments)

- 2016 scoping studies to evaluate SIBS utility across multiple site types:
  - Green waste composting, dairy farms, sewage treatment works, urban background, and agricultural farms
  - Sites included downwind measurements and, where possible, source measurements within plumes or exhaust vents
  - Data collected at approximately 1–1.5 m height with daytime measurements; continuous real-time measurements using SIBS
  - Data files for 2016 scoping studies include particle concentrations and emission intensity across multiple sites
  - Data sources documented in associated open-access publication
- 2017–2018 follow-up campaigns:
  - Green waste composting (2017) and associated source measurements (2017)
  - Agricultural farm (2017)
  - Chicken farm and chicken farm source (2018)
  - 2018 measurements included both downwind plume and source conditions (e.g., broiler shed exhaust)
- Data outputs per site include:
  - FieldMeasurementsCompostingDay1/2/3 (2016 and 2017)
  - FieldMeasurementsCompostingSource2017
  - FieldMeasurementsAgriculturalDay1/2/3 (2017)
  - FieldMeasurementsChickenFarmDay1/2/3 (2018)
  - FieldMeasurementsChickenfarmSource2018
  - Emission spectra data across sites (FieldMeasurementsEmissionSpectra.csv)
- Measurements at each site included:
  - 60-second averaged time-series of particle concentrations
  - Downwind and source measurements where possible
  - Site activity logs during sampling (where available)

## Emission spectra and data organization

- Emission spectra for Green Waste Composting, Chicken Farm, Agricultural Farm, chicken farm source, and green waste composting source are provided in:
  - FieldMeasurementsEmissionSpectra.csv
- Data processing details:
  - Offline analysis with averaging interval of 60 seconds
  - Defined particle size bins to produce total and size-segregated concentrations
  - Fluorescence thresholding using Forced Trigger to distinguish fluorescent particles
  - Fluorescent particle concentration corrected for excitation and emission measurements (formulas described in the methodology)
  - Fluorescence spectra calculated by site, using mean fluorescence across wavelengths and two excitation wavelengths

## Data handling and accessibility

- Data are organized into clearly named CSV files corresponding to site type, year, and measurement context (e.g., chamber vs field).
- Data outputs include time-series of concentrations, downwind vs source spectra, and site-specific mean fluorescence spectra, enabling cross-site comparisons and temporal trend analyses.
- The project emphasizes data quality assurance through calibration steps (Forced Trigger thresholding) and standardized processing to support reproducibility and comparability across sites and campaigns.

## Relevance for environmental monitoring and analysis

- Provides a standardized, time-resolved dataset to inform environmental health assessments and biogeochemical studies of bioaerosols.
- Enables analysts to:
  - Track temporal changes in bioaerosol emissions linked to specific activities (e.g., compost turning, exhaust from poultry facilities)
  - Compare bioaerosol characteristics across diverse environments (industrial vs agricultural vs urban)
  - Integrate bioaerosol emission data with other environmental datasets to assess exposure and policy performance over time
- Highlights the value of UV-LIF-based measurements for quantifying and characterising bioaerosols alongside particle size distributions.

## Key considerations for analysts

- Data are provided as CSVs with site- and campaign-specific naming conventions, suitable for ingestion into standard analytics workflows.
- Some measurements may have gaps or changes in methodology between chamber and field campaigns; account for differences in height, sampling context, and activity logs when performing comparative analyses.
- The Forced Trigger approach defines fluorescence thresholds, which affect the categorisation of particles into total, excited, and fluorescent subsets; ensure consistent application if combining datasets across campaigns.
- The data support multi-site, multi-year monitoring to evaluate environmental health indicators and policy-relevant trends related to bioaerosol emissions.