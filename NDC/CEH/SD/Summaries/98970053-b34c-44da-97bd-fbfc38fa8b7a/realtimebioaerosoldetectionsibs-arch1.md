# Real-time bioaerosol emission data from a range of environmental sources, UK, 2016-2018

## Overview
- Part of a Natural Environment Research Council project evaluating a ultraviolet light-induced fluorescence (UV-LIF) bioaerosol sensor (SIBS) to quantify bioaerosols, their size, and fluorescence signatures in real time.
- SIBS measures single-particle size, shape, and fluorescence across 16 wavelength bands (298–735 nm) for two excitation wavelengths (285 nm and 370 nm).
- Study design includes chamber experiments and real-world measurements (composting, dairy farms, chicken farms, sewage treatment plants, urban/agricultural sites) to assess emission capability and dispersion.
- Output aims to support quantification and spatio-temporal characterization of bioaerosols alongside size distributions and intrinsic fluorophore signatures.
- Methods and data analysis are described in open-access articles (DOIs provided within the document).

## Chamber-based studies
- Conducted at the environmental chamber at PHE Porton (HEPA-filtered, up to 250 air changes/hour).
- Two campaigns:
  - 2016: compost only
  - 2018: compost and chicken litter
- A consistent study design was used across campaigns; detailed methods and analysis are reported in a linked open-access article.
- Associated data files (emission intensity, particle concentrations, particle sizes) are provided:
  - ChamberStudiesEmissionintensityAnalysis2016.csv
  - ChamberStudiesParticleconcentrations2016.csv
  - ChamberStudiesParticlesize2016.csv
  - ChamberStudies2018EmissionSpectraChickenLitter.csv
  - ChamberStudies2018EmissionSpectraCompost.csv

## Field measurements
- Scoping studies (2016) across multiple environments to evaluate SIBS capability for bioaerosol quantification and emission spectra:
  - Green waste composting
  - Dairy farms
  - Sewage works
  - Urban background
  - Agricultural farm
- Detailed sampling sites, study designs, SIBS usage, and data analysis are described in an open-access article.
- Associated field data files for 2016:
  - ScopingstudiesParticleConcAgricultural2016.csv
  - ScopingstudiesParticleConcComposting2016.csv
  - ScopingstudiesParticleConcDairyfarm2016.csv
  - ScopingstudiesParticleConcSewageworks2016.csv
  - ScopingstudiesParticleConcUrbanbackground2016.csv
  - ScopingstudiesEmissionintensity2016.csv
  - ScopingstudiesParticlesizeanalysis2016.csv
- Follow-up measurements by site and year:
  - Green Waste Composting (2016): FieldmeasurementsCompostingDay12016.csv; FieldmeasurementsCompostingDay22016.csv; FieldmeasurementsCompostingDay32016.csv
  - Green Waste Composting and composting Source (2017): FieldmeasurementsCompostingDay12017.csv; FieldmeasurementsCompostingDay22017.csv; FieldmeasurementsCompostingDay32017.csv; FieldMeasurementsCompostingSource2017.csv
  - Agricultural farm (2017): FieldMeasurementsAgriculturalDay12017.csv; FieldMeasurementsAgriculturalDay22017.csv; FieldMeasurementsAgriculturalDay32017.csv
  - Chicken Farm and Chicken farm Source (2018): FieldMeasurementsChickenFarmDay12018.csv; FieldMeasurementsChickenFarmDay22018.csv; FieldMeasurementsChickenFarmDay32018.csv; FieldMeasurementsChickenfarmSource2018.csv
- Emission spectra data across sites is provided in:
  - FieldMeasurementsEmissionSpectra.csv

## Data processing and measurement details
- SIBS provides continuous real-time measurements with nighttime daytime sampling at 1–1.5 m height; downwind and source sampling where feasible.
- Data processing included offline analysis with 60-second averaging, size-binned concentration time series, and defined fluorescence thresholds.
- Background fluorescence is quantified using Forced Trigger (FT) mode (minimum five minutes prior to sampling). Fluorescent particle concentration is corrected using the relationship:
  Fluorescent particle concentration = F/E × T (where F = fluorescent particles, E = excited particles, T = total particles).
- Fluorescence spectra at sites are calculated by subtracting FT intensities and computing mean spectra for each site, for both excitation wavelengths.
- SIBS fluorescence channels and emission wavelength ranges are explicitly defined (Ch 1–16 with corresponding λem ranges).

## Potential uses for analysts
- Correlate emission intensities, particle concentrations, and sizes with site activity and environmental conditions.
- Compare chamber-derived emission profiles with field measurements to assess real-world applicability.
- Build predictive models of bioaerosol dispersion and exposure across different environments (composting, livestock operations, wastewater, urban areas).
- Leverage spectral data to explore source attribution and temporal changes in bioaerosol fluorescence signatures.
- Utilize the provided datasets and metadata for reproducible analyses and to create discoverable data assets (as metadata and portal uploads imply).