# Soil mid-infrared spectroscopy data from arable and grassland in Countryside Survey, Great Britain 2007 Version: 2: 13-01-2021

## Overview
- Diffuse reflectance mid-infrared (MIR) spectroscopy data from archive soils collected across Great Britain in 2007 as part of Countryside Survey.
- 427 soils sampled across 151 1km squares; aims to support soil property monitoring and development of spectral calibrations for soil attributes.
- Data organized into two CSV files: MIR_raw_data.csv (absorbance spectra) and MIR_wavenumbers.csv (mapping of columns to wavenumbers).

## Data Files and Structure
- MIR_raw_data.csv
  - Contains diffuse reflectance MIR spectra for archive soils.
  - Key columns: SQUARE_ID (1km square code), PLOT_ID (plot within square), SINGLE_SCAN (Y if represented by a single spectrum), R1…R1868 (absorbance values at successive wavenumbers).
- MIR_wavenumbers.csv
  - Links absorbance columns to actual wavenumbers.
  - Columns: REFLECTANCE_ID, WAVENUMBER (cm^-1).
  
## Sampling Context and Design
- Sampling locations tied to the Countryside Survey framework with a statistical, stratified design for national representativeness.
- Great Britain stratified into Land Classes; 591 sample squares were surveyed in 2007 (England, Wales, Scotland distribution provided).
- Soil samples selected for MIR analysis using sequential filters:
  - Land Cover classes: Arable, Improved Grass, or Neutral Grass.
  - Plots previously sampled in both 1998 and 2007.
  - Aggregate Vegetation Classification (AVC) categories: Crops and Weeds, Tall Grass and Herb, Fertile Grassland, or Infertile Grassland.
  - Sufficient soil mass available in archived material.
- Final set: 427 plots across Great Britain (GB-wide distribution shown in accompanying figures).

## Laboratory Protocol
- Instrumentation: Bio-Rad FTX3000MX series FTIR with diffuse reflectance attachment for DRIFT measurements.
- Sample preparation: ~150 mg dried soil ground for 45 seconds; no KBr added; 15 g subsamples prepared for analysis.
- Spectral data: DRIFT spectra from 4000 to 400 cm^-1 at 2 cm^-1 resolution; 100 internal scans per acquisition; two spectra per sample (one with the cup rotated 180 degrees).

## Data Quality Control and Assurance
- Field protocols: Field sampling manual and training provided; processing procedures documented for lab logging, measurements, and archiving.
- Spectral quality: Two scans per sample were inspected prior to averaging; six spectra discarded to avoid scanning errors; a single spectrum used to represent the sample; the SINGLE_SCAN flag records these cases.
- Quality management: UKCEH operates an ISO 9001:2015 certified Quality Management System with documented QA policies and procedures.

## Data Provenance and Usage
- Background: MIR spectroscopy as a robust, efficient tool for soil property monitoring; spectroscopy provides multivariate signals correlated with soil attributes (e.g., organic matter content, C concentration) across mineralogical and organic components.
- References and documentation accompanying Countryside Survey data provide context for sampling, methodology, and prior analyses.

## Access, Acknowledgement, and Licensing
- Countryside Survey data are owned by the UK Centre for Ecology & Hydrology (UKCEH); all uses must acknowledge the Countryside Survey.
- Acknowledgement text to be used: “Countryside Survey data owned by UK Centre for Ecology & Hydrology” with copyright noted as Countryside Survey © UKCEH.
- Data are disseminated with standard references and links to related Countryside Survey materials and reports.