# Soil mid-infrared spectroscopy data from arable and grassland in Countryside Survey, Great Britain 2007 Version: 2: 13-01-2021

## Overview
- Dataset documenting diffuse reflectance mid-infrared (DRIFT) spectroscopy data from archived soils collected during the Countryside Survey 2007.
- Focus: 427 soils from 151 one-kilometre squares across Great Britain (England, Scotland, Wales).
- Data products:
  - MIR_raw_data.csv: absorbance spectra for each soil sample, with 1868 spectral channels (R1–R1868) and associated location metadata.
  - MIR_wavenumbers.csv: mapping of each spectral channel (R1–R1868) to actual wavenumbers (cm^-1).
- Purpose: support spectral analyses as a proxy for soil properties and facilitate data discovery, reuse, and integration with other Countryside Survey datasets.
- Version and access: Version 2, dated 13-01-2021; Countryside Survey data owned by UKCEH; data use requires acknowledgement.

## Data content and structure
- MIR_raw_data.csv
  - SQUARE_ID: 1 km square sampling site code (text).
  - PLOT_ID: Plot identifier within each square (text).
  - SINGLE_SCAN: Indicates if the sample is represented by a single spectrum (Y text).
  - R1 … R1868: Absorbance values at successive wavenumbers (numbers).
- MIR_wavenumbers.csv
  - REFLECTANCE_ID: Link between absorbance columns and wavenumbers (text).
  - WAVENUMBER: Specific wavenumber in cm^-1 (number).
- Data representation notes
  - Spectra recorded from 4000 to 400 cm^-1 at 2 cm^-1 resolution; 100 scans per acquisition.
  - Two spectra per sample (one rotated 180 degrees); after QA, six spectra were discarded and a single spectrum used for the sample (flagged in SINGLE_SCAN where applicable).
  - Absorbance values extracted without KBr addition.

## Sampling design and provenance
- Sampling framework
  - Based on Countryside Survey’s stratified design using Land Classes derived from environmental gradients.
  - 591 sample squares surveyed in 2007; distribution: 289 England, 107 Wales, 195 Scotland.
- Sample selection criteria for MIR analysis
  - Current Broad Habitat (land cover): Arable, Improved Grass, or Neutral Grass.
  - Plots sampled in both 1998 and 2007.
  - Aggregate Vegetation Classification (AVC) categories: Crops and Weeds, Tall Grass and Herb, Fertile Grassland, or Infertile Grassland.
  - Adequate soil mass available in archived material.
- Soil sampling and storage
  - Soils from archived Countryside Survey 2007 samples stored at UKCEH Soil Archive, Lancaster.
  - Sample handling: air-dried, 2 mm sieved; 15 g subsamples extracted; homogenised prior to analysis.
- Geographic coverage
  - 427 plots distributed across Great Britain; sampling design ensures national representativeness and regional breakdowns.

## Laboratory protocol and quality control
- Instrument and procedure
  - Instrument: Bio-Rad FTX3000MX series FTIR with diffuse reflectance accessory.
  - Sample preparation: ~150 mg dried soil, ground for 45 seconds; no KBr addition.
  - Measurement: DRIFT spectra from 4000 to 400 cm^-1, 2 cm^-1 resolution, 100 internal scans; second spectrum obtained after rotating sample cup 180°.
- Quality control
  - Field and lab QA: staff trained with a field sampling manual; processing protocols for logging, processing, and archiving soil cores.
  - Spectral QA: spectra visually inspected prior to averaging; six spectra discarded per sample due to scanning errors; a single representative spectrum used (SINGLE_SCAN flag).
- Quality assurance and standards
  - UKCEH maintains a Quality Management System across four sites; ISO 9001:2015 certified; QA policy and procedures in place.
  - Data and methods documentation linked to established Countryside Survey technical reports and manuals.

## Data governance, rights, and usage
- Ownership and rights
  - Countryside Survey data owned by UK Centre for Ecology & Hydrology; copyright applies; all rights reserved.
- Acknowledgement and use
  - Any use of Countryside Survey data must include provided acknowledgements:
    - “Countryside Survey data owned by UK Centre for Ecology & Hydrology.”
    - “Countryside Survey © Database Right/Copyright UK Centre for Ecology & Hydrology. All rights reserved.”
- Accessibility
  - Data references and background materials available via Countryside Survey website; detailed references provided in the accompanying documentation.

## Implications for data stewardship
- Metadata completeness
  - Clear linkage between absorbance channels and wavenumbers via MIR_wavenumbers.csv; explicit SINGLE_SCAN flag enhances data quality assessment.
- Provenance and reproducibility
  - Detailed sampling design, site selection criteria, laboratory protocol, and QA processes support reproducibility and traceability.
- Interoperability and standards
  - Data organized in CSV with explicit column definitions; alignment with Countryside Survey standards facilitates integration with other CS datasets.
- Limitations and considerations
  - Spectral data are absorbance values; interpretation relies on multivariate calibration for soil properties.
  - Some spectra were discarded due to quality issues; SINGLE_SCAN provides context for samples with only one representative spectrum.
  - The dataset is historical (2007 sampling); users should consider potential changes in soil properties and metadata standards over time.

## References and acknowledgements
- Core Countryside Survey references and technical reports cited (Emmett et al., Morton et al., Carey et al., etc.).
- Acknowledgement guidance for data usage and links to Countryside Survey resources.