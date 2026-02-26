# Soil mid-infrared spectroscopy data from arable and grassland in Countryside Survey, Great Britain 2007 Version: 2: 13-01-2021

## Overview
- Diffuse reflectance mid-infrared (DRIFT) spectroscopy data for archived soils from 427 plots across 151 1km squares in Great Britain (Countryside Survey 2007).
- Data published as two CSV files: MIR_raw_data.csv and MIR_wavenumbers.csv.

## Data files and structure
- MIR_raw_data.csv
  - SQUARE_ID: 1km square sampling site code (text)
  - PLOT_ID: Plot identifier (text)
  - SINGLE_SCAN: Indicates if the sample is represented by a single spectrum (Y or text)
  - R1 to R1868: Absorbance values at successive wavenumbers (cm-1) (numbers)
- MIR_wavenumbers.csv
  - REFLECTANCE_ID: Link between absorbance columns and wavenumbers (text)
  - WAVENUMBER: Specific wavenumber (cm-1) (number)

## Sampling strategy and coverage
- Sampling design aligned with Countryside Survey: stratified by Land Classes; 1km squares selected within classes.
- 591 sample squares surveyed in 2007; 427 plots yielded usable MIR spectral data across GB (England, Scotland, Wales).
- Soil sampling: top 0–15 cm, ~15 g subsamples, air-dried, 2 mm sieved, homogenised.

## Laboratory protocol
- Instrument: Bio-Rad FTX3000MX FTIR with diffuse reflectance attachment.
- Procedure: ~150 mg soil ground for 45 s, no KBr; spectra recorded 4000–400 cm-1, 2 cm-1 resolution, 100 scans per acquisition; two spectra per sample (rotated 180 degrees).

## Data quality control
- Field and laboratory QA: sampling manual, trained personnel; spectra visually inspected before averaging.
- Outlier suppression: six spectra discarded; final sample represented by a single spectrum (flagged in SINGLE_SCAN).
- Quality assurance: UKCEH ISO 9001:2015 certified; formal QA policy and procedures.

## Context and interpretation
- MIR spectroscopy provides a combined signature of mineralogical and organic soil components.
- DRIFT/MIR data used to develop calibrations predicting soil properties (e.g., organic matter content, carbon), with recognition of the broader MIR/NIR spectral monitoring context.

## References and provenance
- Countryside Survey framework and GB soil sampling (Carey et al. 2008; Emmett et al. 2008/2010).
- Method and analytical context (Morton et al. 2011; Nocita et al. 2015).
- Technical details on DRIFT and related studies (Vane 2003; Tonks et al. 2016).

## Practical considerations for analysts
- Scale and granularity: GB-wide baseline with 427 plots; local-level inferences may be limited by sample density.
- Data usage: map R1–R1868 to WAVENUMBER via MIR_wavenumbers.csv; respect SINGLE_SCAN flag when interpreting representativeness.
- Data lineage: dataset is part of the UK Countryside Survey; acknowledge data owners and consult associated literature for method details.

## Acknowledgements and licensing
- Data owned by UK Centre for Ecology & Hydrology; Countryside Survey ©. All rights reserved. Acknowledgement required in publications and presentations.