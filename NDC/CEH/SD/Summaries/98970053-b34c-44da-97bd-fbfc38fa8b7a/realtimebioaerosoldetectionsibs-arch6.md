# Real-time bioaerosol emission data from a range of environmental sources, UK, 2016-2018

## Overview and aims
- A data release from the NE/N M01163/1 project evaluating a ultraviolet light-induced fluorescence (UV-LIF) bioaerosol sensor unit (SIBS) for real-time measurement of bioaerosols.
- SIBS measures particle size, number, shape, and resolved fluorescence across 16 wavelength bands (298–735 nm) for two excitation wavelengths (285 nm and 370 nm).
- Main purpose: assess capabilities of SIBS to quantify bioaerosol emissions and characterize spatio-temporal distribution alongside particle size distributions.
- Data collection included controlled chamber studies and real-world field measurements (composting, dairy and chicken farms, sewage treatment, urban/agricultural sites).

## Data collection and study types

### Chamber-based studies
- Conducted at PHE Porton with HEPA-filtered air (up to 250 air changes per hour) to test methods and emissions from compost and chicken litter sources.
- 2016 study focused on compost; 2018 study included compost and chicken litter.
- Data outputs include chamber-specific emission intensity, particle concentrations, and particle size data.
- Related open-access articles provide detailed methodology (DOIs: 10.3390/Atmos9100379 and 10.1016/j.scitotenv.2018.08.120).

Associated data files:
- ChamberStudiesEmissionintensity2016.csv
- ChamberStudiesParticleconcentrations2016.csv
- ChamberStudiesParticlesize2016.csv
- ChamberStudies2018EmissionSpectraChickenLitter.csv
- ChamberStudies2018EmissionSpectraCompost.csv

### Field measurements (real-world environments)
- 2016 scoping studies at green waste composting, dairy farms, sewage treatment plants, urban background, and agricultural sites to evaluate SIBS utility for quantifying emissions and spectra.
- Following years included longitudinal measurements at composting sites (2016–2017), agricultural farms (2017), and chicken farms (2018), with downwind and source measurements as applicable.
- Detailed methodologies and site contexts documented in open-access articles (DOI: 10.1016/j.scitotenv.2018.08.120 and related).

Associated data files (scoping 2016):
- ScopingstudiesParticleConcAgricultural2016.csv
- ScopingstudiesParticleConcComposting2016.csv
- ScopingstudiesParticleConcDairyfarm2016.csv
- ScopingstudiesParticleConcSewageworks2016.csv
- ScopingstudiesParticleConcUrbanbackground2016.csv
- ScopingstudiesEmissionintensity2016.csv
- ScopingstudiesParticlesizeanalysis2016.csv

Field measurements and spectra (2016–2018):
- Green Waste CompostingDay12016.csv
- Green Waste CompostingDay22016.csv
- Green Waste CompostingDay32016.csv
- FieldmeasurementsCompostingDay12017.csv
- FieldmeasurementsCompostingDay22017.csv
- FieldmeasurementsCompostingDay32017.csv
- FieldMeasurementsCompostingSource2017.csv
- FieldMeasurementsAgriculturalDay12017.csv
- FieldMeasurementsAgriculturalDay22017.csv
- FieldMeasurementsAgriculturalDay32017.csv
- FieldMeasurementsChickenFarmDay12018.csv
- FieldMeasurementsChickenFarmDay22018.csv
- FieldMeasurementsChickenFarmDay32018.csv
- FieldMeasurementsChickenfarmSource2018.csv
- FieldMeasurementsEmissionSpectra.csv (emission spectra across sites)

## Instrument, data processing, and quality control

- SIBS specifications: 16 fluorescence channels across 298–735 nm; two excitation wavelengths (285 nm, 370 nm). Real-time single-particle measurements with size, shape, and fluorescence data.
- Data processing:
  - Offline processing with a toolkit; 60-second averaging interval to create total and size-segregated particle concentration time series.
  - Background fluorescence threshold established via Forced Trigger (FT) mode (minimum 5 minutes prior to sampling): pump off, xenon lamps every 150 ms.
  - Fluorescent particle concentration corrected as Fluorescent = F/E × T, where T = total concentration, E = excited concentration, F = fluorescent concentration derived from FT threshold.
  - Fluorescence spectra calculated per site by correcting particle emission against FT thresholds; particles with no channel signal exceeding thresholds are excluded; mean spectra computed for both excitation wavelengths.
- Outputs include:
  - Time-series data of total and size-segregated particle concentrations.
  - Fluorescence-based particle counts and spectra per site.
  - Emission spectra datasets for composting, chicken farming, agricultural farming, and site sources.

## Data products and potential uses

- Real-time and post-processed data suitable for:
  - Cross-site comparisons of bioaerosol emissions and spectral signatures.
  - Time-resolved dashboards showing emission intensity, particle concentrations, and size distributions.
  - Spectral mapping to identify bioaerosol signatures across different environments (composting, farming, sewage, urban backgrounds).
  - Data-driven evaluation of emission controls and industrial process impacts on bioaerosol generation.
- Outputs enable self-service analysis and visualization for end users who need to explore bioaerosol emissions across diverse environmental sources.

## Access, references, and notes

- Open-access methodology articles detailing chamber study design and field sampling:
  - Atmosphere (2019) article detailing chamber methods: https://doi.org/10.3390/atmos9100379
  - Science of the Total Environment (2018) article detailing scoping studies: https://doi.org/10.1016/j.scitotenv.2018.08.120
- Data files are organized by study type and site, with emission spectra consolidated in FieldMeasurementsEmissionSpectra.csv.
- The dataset supports integration of real-time and post-processed bioaerosol data for broader analyses of bioaerosol emissions from industrial and agricultural sources.