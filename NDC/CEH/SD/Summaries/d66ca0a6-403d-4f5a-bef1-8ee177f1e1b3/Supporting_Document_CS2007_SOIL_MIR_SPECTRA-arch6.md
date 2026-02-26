# Soil mid-infrared spectroscopy data from arable and grassland in Countryside Survey, Great Britain 2007 Version: 2: 13-01-2021

## Overview
- Diffuse reflectance mid-infrared spectroscopy data for archive soils from 427 soils sampled across 151 1km squares in Great Britain (as surveyed in 2007).
- Primary data files: MIR_raw_data.csv (absorbance spectra) and MIR_wavenumbers.csv (mapping of absorbance columns to wavenumbers).
- Context: supports spectral analysis and development of data products to predict soil properties; linked to the Countryside Survey sampling framework.

## Data files and structure
- MIR_raw_data.csv
  - Columns: SQUARE_ID (1km square code), PLOT_ID (within-square plot), SINGLE_SCAN (Y indicates a single spectrum), R1 … R1868 (absorbance values at successive wavenumbers).
  - R1–R1868 represent absorbance at 1868 measured wavenumbers (cm^-1).
- MIR_wavenumbers.csv
  - Columns: REFLECTANCE_ID (links to the R1–R1868 columns), WAVENUMBER (cm^-1).
- SINGLE_SCAN flag
  - Y indicates the sample is represented by a single spectrum; otherwise two spectra were collected and variability inspected during QC.
- Data characteristics
  - Wavenumber range: 4000 to 400 cm^-1
  - Resolution: 2 cm^-1
  - Acquisition: 100 internal scans per spectrum; two spectra per sample (one re-measured after rotating the sample cup 180°)
  - Processed spectrum used for analysis after QC; six spectra discarded if scanning errors detected.

## Sampling design and sample selection
- Countryside Survey 2007 sampling design: GB stratified by Land Classes; randomly selected 1km squares to ensure national representativeness.
- 591 sample squares surveyed in 2007 (England 289, Wales 107, Scotland 195).
- Soil sampling for MIR analysis selected based on filters:
  - Broad Habitat: Arable, Improved Grass or Neutral Grass
  - Plots sampled in both 1998 and 2007
  - Aggregate Vegetation Classification: Crops and Weeds, Tall Grass and Herb, Fertile Grassland or Infertile Grassland
  - Sufficient archived soil mass
- Result: 427 plots distributed across Great Britain (from archived Countryside Survey 2007 soil samples).

## Sample preparation and laboratory protocol
- Soil collection: top 0–15 cm; 15 g subsamples used for MIR analysis
- Preparation: air-dried, 2 mm sieved; homogenised and loaded into sample holders
- Spectroscopy: diffuse reflectance infrared spectroscopy (DRIFT) using Bio-Rad FTIR with diffuse reflectance accessory
- Sample processing: dried and finely ground (~150 mg per analysis) for 45 seconds; spectra recorded as absorbance without KBr; two spectra per sample recorded (one after 180° rotation)

## Quality control and assurance
- Field and laboratory QC: field sampling manual; trained surveyors; documented protocols from logging to analysis
- Spectral QC: two spectra per sample visually inspected; eight spectra compared; six spectra discarded if errors detected; a single representative spectrum used (indicated by SINGLE_SCAN)
- UK Centre for Ecology & Hydrology (UKCEH) Quality Management System (ISO 9001:2015) in place; QA Policy and procedures to ensure high research quality
- Outputs and data usage should acknowledge Countryside Survey data and UKCEH copyright

## Usage, metadata, and data products
- Purpose: enable “self-serve” data exploration and development of data products (dashboards, pivot tables, charts) for end users to derive soil insights
- Key mappings and considerations:
  - R1–R1868 values tie to wavelengths via MIR_wavenumbers.csv
  - SINGLE_SCAN indicates data representativeness (single spectrum vs. averaged QC spectrum)
  - Data can be linked to the Countryside Survey soil context and broader CS datasets for enhanced analyses
- Typical applications: calibrations and predictions of soil properties (e.g., organic matter content, carbon concentration) using MIR spectra

## References and acknowledgments
- Countryside Survey resources and methodologies referenced (various Carey et al., Emmett et al., Morton et al.)
- Acknowledgement: Countryside Survey data owned by UKCEH; data usage should include proper acknowledgement and copyright notice
- Funded by NERC Soil Security Programme; project details and related literature cited in the document

## Access and licensing notes
- Use requires acknowledgement per CS data policy; data are owned by UKCEH and are subject to copyright and rights restrictions as applicable