# Real-time bioaerosol emission data from a range of environmental sources, UK, 2016-2018

## Overview and purpose
- Part of a Natural Environment Research Council project evaluating a UV light-induced fluorescence sensor (SIBS) to quantify and characterize bioaerosols in real time.
- SIBS measures size, number, shape, and 16 wavelength-band fluorescence across 298–735 nm with two excitation wavelengths (285 nm and 370 nm).
- Aims to understand bioaerosol emissions and dispersion from industrial and agricultural sources, using both chamber-based and real-world environments.
- Data support the assessment of SIBS utility for emissions quantification and spatio-temporal characterization alongside particle size distributions.
- Funding and program context: NE/N01163/1 under Environmental Microbiology and Human Health; open-access methodology references provided.

## Data collection: scope and sites
- Chamber studies (Porton, UK):
  - 2016: compost source tested; high-control chamber conditions (HEPA-filtered air, up to 250 air changes/hour).
  - 2018: emissions studied from compost and chicken litter sources.
  - Detailed chamber study design and data analysis published in open-access articles; similar design used across years.
  - Associated chamber data files:
    - ChamberStudiesEmissionintensityAnalysis2016.csv
    - ChamberStudiesParticleconcentrations2016.csv
    - ChamberStudiesParticlesize2016.csv
    - ChamberStudies2018EmissionSpectraChickenLitter.csv
    - ChamberStudies2018EmissionSpectraCompost.csv

- Field (real-world) measurements:
  - 2016 scoping studies across multiple site types to evaluate SIBS performance:
    - Agricultural, Composting, Dairy farm, Sewage works, Urban background, Emission intensity, and Particle size analyses.
    - Data files:
      - ScopingstudiesParticleConcAgricultural2016.csv
      - ScopingstudiesParticleConcComposting2016.csv
      - ScopingstudiesParticleConcDairyfarm2016.csv
      - ScopingstudiesParticleConcSewageworks2016.csv
      - ScopingstudiesParticleConcUrbanbackground2016.csv
      - ScopingstudiesEmissionintensity2016.csv
      - ScopingstudiesParticlesizeanalysis2016.csv
  - Follow-up measurements by site and year:
    - Green Waste Composting (2016); Green Waste Composting and composting Source (2017)
      - FieldMeasurementsCompostingDay12016.csv
      - FieldMeasurementsCompostingDay22016.csv
      - FieldMeasurementsCompostingDay32016.csv
      - FieldMeasurementsCompostingDay12017.csv
      - FieldMeasurementsCompostingDay22017.csv
      - FieldMeasurementsCompostingDay32017.csv
      - FieldMeasurementsCompostingSource2017.csv
    - Agricultural farm (2017)
      - FieldMeasurementsAgriculturalDay12017.csv
      - FieldMeasurementsAgriculturalDay22017.csv
      - FieldMeasurementsAgriculturalDay32017.csv
    - Chicken Farm and Chicken Farm Source (2018)
      - FieldMeasurementsChickenFarmDay12018.csv
      - FieldMeasurementsChickenFarmDay22018.csv
      - FieldMeasurementsChickenFarmDay32018.csv
      - FieldMeasurementsChickenfarmSource2018.csv
  - Emission spectra data from field measurements:
    - FieldMeasurementsEmissionSpectra.csv

## Instrumentation and data processing
- Spectral Intensity Bioaerosol Sensor (SIBS) capabilities:
  - Real-time single-particle measurements of size, shape, and resolved fluorescence across 16 channels (wavelength bands) with two excitation wavelengths.
  - Fluorescence channels and approximate wavelength bands are detailed (Ch 1–Ch 16 with specific emission ranges).
- Data processing and analysis workflow:
  - All particle data files processed offline with a data analysis toolkit.
  - Data are averaged in 60-second intervals with defined size bins.
  - Background fluorescence quantified using Forced Trigger (FT) mode prior to sampling campaigns (minimum five minutes).
  - Fluorescent particle calculations:
    - Fluorescent concentration = F/E × T, where F = fluorescent particles, E = excited particles, T = total particle concentration.
  - Fluorescence spectra per site derived by subtracting FT background and computing mean fluorescence across wavelength bands for each site and excitation wavelength.
- Reporting and documentation:
  - Emission spectra and time-series data provided for both field and chamber studies.
  - Data attributed to specific sites, dates, and measurement conditions, enabling traceability.

## Data products and file inventory
- Chamber studies (dataset-level focus):
  - ChamberStudiesEmissionintensityAnalysis2016.csv
  - ChamberStudiesParticleconcentrations2016.csv
  - ChamberStudiesParticlesize2016.csv
  - ChamberStudies2018EmissionSpectraChickenLitter.csv
  - ChamberStudies2018EmissionSpectraCompost.csv
- Field measurements (2016 scoping studies):
  - ScopingstudiesParticleConcAgricultural2016.csv
  - ScopingstudiesParticleConcComposting2016.csv
  - ScopingstudiesParticleConcDairyfarm2016.csv
  - ScopingstudiesParticleConcSewageworks2016.csv
  - ScopingstudiesParticleConcUrbanbackground2016.csv
  - ScopingstudiesEmissionintensity2016.csv
  - ScopingstudiesParticlesizeanalysis2016.csv
- Field measurements (Green Waste Composting 2016; 2017):
  - FieldmeasurementsCompostingDay12016.csv
  - FieldmeasurementsCompostingDay22016.csv
  - FieldmeasurementsCompostingDay32016.csv
  - FieldmeasurementsCompostingDay12017.csv
  - FieldmeasurementsCompostingDay22017.csv
  - FieldmeasurementsCompostingDay32017.csv
  - FieldMeasurementsCompostingSource2017.csv
- Field measurements (Agricultural 2017):
  - FieldMeasurementsAgriculturalDay12017.csv
  - FieldMeasurementsAgriculturalDay22017.csv
  - FieldMeasurementsAgriculturalDay32017.csv
- Field measurements (Chicken Farm 2018 and source):
  - FieldMeasurementsChickenFarmDay12018.csv
  - FieldMeasurementsChickenFarmDay22018.csv
  - FieldMeasurementsChickenFarmDay32018.csv
  - FieldMeasurementsChickenfarmSource2018.csv
- Emission spectra data:
  - FieldMeasurementsEmissionSpectra.csv

## Documentation, methods, and provenance
- Methodological references:
  - Open-access article detailing chamber study design and data analysis: Atmosphere (2019) doi:10.3390/atmos9100379
  - Open-access article detailing scanning and measurement approach in field studies: Science of The Total Environment (2018) doi:10.1016/j.scitotenv.2018.08.120
- Sensor and data processing provenance:
  - Detailed description of SIBS measurement channels, wavelength bands, and excitation wavelengths.
  - Documentation of FT-based thresholding, fluorescence correction, and spectral calculations to derive site-level mean spectra.

## Data governance, quality, and reuse considerations
- Data management and standardization:
  - Datasets are organized by study type (chamber vs field) and by site/year; file naming follows consistent conventions to aid discovery and reuse.
  - Metadata implicitly includes site type, date, measurement mode (source vs downwind), and measurement height (1–1.5 m), with logs where possible.
- Data quality and processing notes:
  - Quality assurance via Forced Trigger background characterization prior to campaigns.
  - Real-time measurements complemented by offline processing to produce comparable time-series and spectral data.
  - Background corrections and fluorescent particle concentration calculations are explicitly documented, enabling reproducibility of derived metrics.
- Reuse considerations:
  - Combines raw-like time-series data (concentrations, spectra) with derived spectral metrics; ensure appropriate units and normalization when reusing.
  - Method references provided for replication of processing steps and for understanding potential limitations (e.g., FT gaps during Xenon lamp recharge).
- Limitations and caveats:
  - FT-based thresholds may introduce measurement gaps during lamp recharge periods.
  - Real-world measurements involve diverse sites and conditions; cross-site comparability relies on consistent processing practices described in the documentation and referenced articles.