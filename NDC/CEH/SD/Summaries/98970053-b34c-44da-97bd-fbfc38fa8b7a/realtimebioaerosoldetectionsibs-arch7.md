# Real-time bioaerosol emission data from a range of environmental sources, UK, 2016-2018

## Overview
- Project funded by the Natural Environment Research Council to detect and characterize inflammatory agents in bioaerosols emitted from biowaste and intensive agriculture.
- Uses a novel ultraviolet light-induced fluorescence (UV-LIF) sensor unit (Spectral Intensity Bioaerosol Sensor, SIBS) to measure size, number, shape, and resolved fluorescence across 16 wavelength bands (298–735 nm) for two excitation wavelengths (285 nm and 370 nm) in real-time.
- Aims to quantify bioaerosol emissions and dispersion and to characterize airborne biological materials alongside size distribution and intrinsic biofluorophores signatures.
- Measurements conducted in controlled chamber settings and real-world environments (composting facilities, dairy farms, chicken farms, sewage treatment plants, urban/agricultural sites).
- Data products include emission intensity, particle concentrations, particle size distributions, and fluorescence spectra (across multiple sites and years).

## Data and methods at a glance
- Instrumentation: SIBS records particle size, shape, and fluorescence across 16 channels with two excitation wavelengths; real-time data processing to generate time-series on concentrations and spectra.
- Data processing approach:
  - Offline data analysis with 60-second averaging intervals.
  - Establishes fluorescence thresholds using Forced Trigger (FT) mode (mean + 3×SD per channel) prior to sampling.
  - Distinguishes total particles, excited particles, and fluorescent particles; fluorescent concentration corrected using total, excited, and fluorescent counts.
  - Fluorescence spectra computed site-by-site by comparing site measurements to FT values and averaging across emission bands.
- Sampling protocol: daytime measurements at 1–1.5 m height; both downwind measurements at sources and direct source measurements under vents or within plumes where possible.
- Outputs include negative and positive controls for background fluorescence and site-specific spectra across two excitation wavelengths.

## Chamber studies (controlled environment)
- Purpose: elucidate physico-chemical and biological characteristics of bioaerosols under controlled conditions, using compost and chicken litter as sources.
- Locations: environmental chamber at PHE Porton; high air-change rates to rapidly remove test aerosols.
- Studies:
  - 2016: compost-focused chamber study.
  - 2018: both compost and chicken litter aerosolisation studies.
- Associated data files:
  - ChamberStudiesEmissionintensityAnalysis2016.csv
  - ChamberStudiesParticleconcentrations2016.csv
  - ChamberStudiesParticlesize2016.csv
  - ChamberStudies2018EmissionSpectraChickenLitter.csv
  - ChamberStudies2018EmissionSpectraCompost.csv
- Related methods and study designs described in open-access articles.

## Field measurements (real-world environments)
- 2016 scoping studies across multiple environments to evaluate SIBS utility in quantifying emissions and recording high-resolution emission spectra.
  - Sites: Green Waste Composting, Dairy Farm, Sewage Works, Urban Background, Agricultural Farm.
  - Data files:
    - ScopingstudiesParticleConcAgricultural2016.csv
    - ScopingstudiesParticleConcComposting2016.csv
    - ScopingstudiesParticleConcDairyfarm2016.csv
    - ScopingstudiesParticleConcSewageworks2016.csv
    - ScopingstudiesParticleConcUrbanbackground2016.csv
    - ScopingstudiesEmissionintensity2016.csv
    - ScopingstudiesParticlesizeanalysis2016.csv
- 2016–2017 field campaigns at:
  - Green Waste Composting (2016, 2017) and Composting Source (2017)
  - Agricultural Farm (2017)
  - Urban/Background sites summarized in scoping datasets
- 2018 field campaigns at:
  - Green Waste Composting and Chicken Farm (2018)
  - Chicken Farm Source (2018)
- Data files by site/year:
  - Green Waste Composting (2016): FieldmeasurementsCompostingDay12016.csv; FieldmeasurementsCompostingDay22016.csv; FieldmeasurementsCompostingDay32016.csv
  - Green Waste Composting and Composting Source (2017): FieldmeasurementsCompostingDay12017.csv; FieldmeasurementsCompostingDay22017.csv; FieldmeasurementsCompostingDay32017.csv; FieldMeasurementsCompostingSource2017.csv
  - Agricultural Farm (2017): FieldMeasurementsAgriculturalDay12017.csv; FieldMeasurementsAgriculturalDay22017.csv; FieldMeasurementsAgriculturalDay32017.csv
  - Chicken Farm and Chicken Farm Source (2018): FieldMeasurementsChickenFarmDay12018.csv; FieldMeasurementsChickenFarmDay22018.csv; FieldMeasurementsChickenFarmDay32018.csv; FieldMeasurementsChickenfarmSource2018.csv
  - Emission spectra data: FieldMeasurementsEmissionSpectra.csv
- Outputs include continuous real-time particle concentration time series, site-specific emission spectra, and aggregated mean fluorescence spectra across sites and years.

## Spatial and temporal scope
- Geography: United Kingdom.
- Timeframe: 2016–2018, with both chamber-based experiments and multiple field campaigns.
- Spatial resolution: site-level measurements and plume interactions in real-world environments; data suitable for mapping emissions by site and for temporal analyses aligned with site activities.

## GIS relevance and potential uses
- Map-based visualization of bioaerosol emissions by site, source type (composting, farms, sewage, urban), and year.
- Temporal mapping and time-series analysis of particle concentrations and fluorescence spectra to identify emission patterns and dispersion.
- Integration with ancillary spatial data (land use, meteorology, habitat) to model dispersion or exposure.
- Creation of GIS-ready layers:
  - Total, excited, and fluorescent particle concentrations (time-series by site).
  - Emission spectra profiles per site and year.
  - Site activity indicators and logs to contextualize emissions.

## Data quality, standards, and caveats
- Multi-source data with both chamber and field measurements; calibration and background correction rely on FT-based fluorescence thresholds.
- Data processing involves averaging and spectral calculations that require careful handling when merging across years/sites.
- Real-world data may have gaps or uneven sampling due to site access, environmental conditions, or instrument operation.
- Method references to open-access articles provide methodological context for reproducibility and comparison.

## References and sources
- Open-access articles detailing the chamber study designs and methodology (e.g., URLs provided in the dataset descriptions for further methodological background).