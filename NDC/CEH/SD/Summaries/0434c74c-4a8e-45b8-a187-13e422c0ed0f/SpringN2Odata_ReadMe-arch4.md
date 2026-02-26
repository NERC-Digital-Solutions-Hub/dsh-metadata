# ReadMe file for SpringN2OData.csv

- This ReadMe describes the SpringN2OData.csv dataset, which records N2O emissions under different urine treatments (control, artificial urine, real urine) applied to an orthic podzol in semi-improved upland grassland at Henfaes Research Station, North Wales, in spring 2016.
- The data were collected from a randomized block experimental design with both high-frequency automated measurements and later manual monthly measurements.

## Dataset scope and experimental design

- Treatments: Control (no urine), ArtUrine (artificial urine), Urine (real urine).
- Site: Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Soil/vegetation: Orthic podzol in semi-improved upland grassland.
- Design: Randomised block experimental design.
- Timeframe: Spring 2016.
- Measurements include both high-frequency flux data ( automated system ) and monthly flux measurements from smaller chambers.

## Instruments, data collection, and calibration

- Automated system (QUT) with an SRI 8610 GC:
  - Eight flux measurements per chamber per day.
  - Each 1-hour chamber closure period; four gas samples analysed per 1-hour closure.
  - Calibration standard analysed after every fourth gas sample.
- Chamber details for automated measurements:
  - Basal area: 0.25 m²
  - Chamber dimensions: 50 cm × 50 cm × 15 cm (L × W × H)
- Manual measurements:
  - Smaller chambers: 40 cm × 20 cm × 20 cm (L × W × H)
  - Gas analysis: Perkin Elmer 580 GC with Turbo Matrix 110 autosampler
  - Calibration: four gas standards spanning measured concentration ranges (BOC gases)
- Data type:
  - Represent flux data verified for quality (not raw gas concentrations)
  - Fluxes below detection limit in manual data replaced with zero

## Data structure and headers

- Timestamp format: dd/mm/yy hh:mm
- Flux columns: B to M represent N2O fluxes (micrograms N2O-N m⁻² h⁻¹)
- Column headers encode treatment and chamber/plot identifiers:
  - Treatments include Control, ArtUrine, and Urine
- Data include both high-frequency flux measurements and later monthly measurements; structure differentiates the two phases

## Data quality, provenance, and processing

- Quality assurance:
  - Inspection of raw data files and GC chromatograms for anomalies; removals performed if necessary (e.g., gas peak interference)
- Data handling:
  - Fluxes below detection limit set to zero in manual data
- Data provenance:
  - Clear instrumentation and calibration procedures documented
  - Acknowledgement required for data reuse or reproduction

## Metadata, discoverability, and governance considerations

- Metadata captured in the header (treatment, chamber/plot identifiers) and timestamp
- Data are described as quality-assessed flux data (not raw concentration data), with processing steps noted
- Clear lineage from field sampling to processed flux values, aiding reproducibility and validation
- Attribution requirement (authors acknowledged if reused) supports data governance and reuse accountability

## Context and usage considerations for data leaders

- Demonstrates end-to-end data lifecycle: from field measurements and instrumentation through QA, processing choices (zeroing undetectable fluxes), to structured data ready for analysis.
- Highlights importance of metadata clarity and standardized headers for cross-study discoverability and integration.
- Illustrates potential challenges when merging high-frequency and lower-frequency datasets (temporal alignment, methodology differences).
- Provides a concrete example of how to document data provenance, calibration, and quality checks to support reliable data-driven decisions across networks.