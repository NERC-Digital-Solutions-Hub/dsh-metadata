# Real-time bioaerosol emission data from a range of environmental sources, UK, 2016-2018

## Overview
- Part of a Natural Environment Research Council (NE/NERC) project on detection and characterization of inflammatory agents in bioaerosols from biowaste and intensive agriculture.
- Evaluates a novel ultraviolet light-induced fluorescence (UV-LIF) sensor unit (Spectral Intensity Bioaerosol Sensor, SIBS) for real-time measurement of bioaerosols, including size, number, shape, and resolved fluorescence across 16 wavelength bands (298–735 nm) for two excitation wavelengths (285 nm and 370 nm).
- Aims to understand bioaerosol emissions and dispersion from industrial processes; combines chamber studies and real-world field measurements to quantify bioaerosols and characterize spectra.

## Methods and data collection

### Chamber based studies
- Purpose: test SIBS and other methods to elucidate physico-chemical and biological characteristics of bioaerosols under controlled conditions.
- Settings: environmental chamber at Porton with HEPA-filtered air; up to 250 air changes per hour.
- Studies:
  - 2016: compost source only.
  - 2018: compost and chicken litter emissions.
- Associated data files (emission and particle data for chamber studies):
  - ChamberStudiesEmissionintensityAnalysis2016.csv
  - ChamberStudiesParticleconcentrations2016.csv
  - ChamberStudiesParticlesize2016.csv
  - ChamberStudies2018EmissionSpectraChickenLitter.csv
  - ChamberStudies2018EmissionSpectraCompost.csv
- References to methodology and results are available in open-access articles:
  - 2016 study details: https://doi.org/10.3390/atmos9100379
  - Data analysis and sampling design detailed in: https://doi.org/10.1016/j.scitotenv.2018.08.120

### Field measurements
- Scope: real-world environments including green waste composting, dairies, urban background, sewage works, and agricultural farms (scoping in 2016); follow-up campaigns at specific sites in 2016–2018.
- SIBS deployed at 1–1.5 m height with daytime measurements; both downwind and source measurements (e.g., near vents, compost windrows, broiler shed exhaust).
- Field data categories:
  - Green Waste Composting (2016)
  - Green Waste Composting and composting Source (2017)
  - Agricultural farm (2017)
  - Chicken Farm and Chicken farm Source (2018)
  - Emission spectra data across sites (FieldMeasurementsEmissionSpectra.csv)
- Field data files:
  - Green Waste Composting 2016:
    - FieldmeasurementsCompostingDay12016.csv
    - FieldmeasurementsCompostingDay22016.csv
    - FieldmeasurementsCompostingDay32016.csv
  - Green Waste Composting and Composting Source 2017:
    - FieldmeasurementsCompostingDay12017.csv
    - FieldmeasurementsCompostingDay22017.csv
    - FieldmeasurementsCompostingDay32017.csv
    - FieldMeasurementsCompostingSource2017.csv
  - Agricultural farm 2017:
    - FieldMeasurementsAgriculturalDay12017.csv
    - FieldMeasurementsAgriculturalDay22017.csv
    - FieldMeasurementsAgriculturalDay32017.csv
  - Chicken Farm and Source 2018:
    - FieldMeasurementsChickenFarmDay12018.csv
    - FieldMeasurementsChickenFarmDay22018.csv
    - FieldMeasurementsChickenFarmDay32018.csv
    - FieldMeasurementsChickenfarmSource2018.csv
  - Emission spectra:
    - FieldMeasurementsEmissionSpectra.csv

## Instrumentation and data processing

- Instrument: Spectral Intensity Bioaerosol Sensor (SIBS) measuring:
  - Size, shape, and fluorescence across 16 wavelength channels (298.2–734.7 nm) for two excitations (285 nm and 370 nm).
  - Real-time data collection with 60-second averaging.
- Data processing and thresholds:
  - Background fluorescence characterized using Forced Trigger (FT) mode pre-sampling (minimum 5 minutes) to establish fluorescence thresholds per channel.
  - Particles categorized as total, excited, and fluorescent; fluorescence-concentration corrected using: Fluorescent concentration = F/E × T, where F = fluorescent concentration, E = excited concentration, T = total concentration.
  - Fluorescence spectra across sites derived by subtracting FT intensities from particle-by-particle intensities, then computing mean fluorescence intensity across emission bands.
  - Emission spectra reported for Green Waste Composting, Chicken Farm, Agricultural Farm, Chicken Farm Source, and Green Waste Composting Source.
- Data products:
  - Number concentration time series (per site and campaign) derived from offline analysis.
  - Emission spectra data corresponding to measured sites.
- Related reference data and methodology provided in open-access sources:
  - Emission spectra and SIBS methodology detailed in associated articles (DOIs provided above).

## Data structure and accessibility

- All chamber data files are organized by study year and site; field data are grouped by site and year with accompanying emission spectra data.
- The dataset enables:
  - Quantification of bioaerosol emissions and real-time spectral characterization.
  - Comparison of emissions across different environmental sources (composting, farms, sewage, urban background).
  - Temporal analysis with 60-second resolution and site-specific emission spectra for integration with broader air quality assessments.

## Relevance to data strategy and governance

- The dataset exemplifies end-to-end data governance for a specialized sensor system:
  - Clear documentation of data collection settings (sites, heights, timings, and campaigns).
  - Comprehensive data processing workflow (thresholding, categorization, spectral calculations).
  - Availability of raw- and processed-data files with standardized naming conventions.
  - Links to open-access publications to contextualize methods and results.
- Demonstrates how to curate multi-site, multi-year sensor data to support cross-site comparisons, reproducibility, and collaborative research across environmental microbiology and human health disciplines.