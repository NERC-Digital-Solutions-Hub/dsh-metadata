# Soil mid-infrared spectroscopy data from arable and grassland in Countryside Survey, Great Britain 2007 Version: 2: 13-01-2021

## Overview
- Dataset documenting soil mid-infrared (MIR) diffuse reflectance spectroscopy from arable and grassland plots surveyed in Great Britain in 2007.
- Aims to enable GIS-based analysis and mapping of soil properties through MIR spectra.
- Coverage: 427 archived soil samples from 151 one-kilometre squares across GB; survey part of Countryside Survey 2007.

## Data files and structure
- MIR_raw_data.csv
  - Columns: SQUARE_ID (1 km square code), PLOT_ID (within-square plot), SINGLE_SCAN (Y if only a single spectrum is used), R1…R1868 (absorbance values at successive wavenumbers).
- MIR_wavenumbers.csv
  - Columns: REFLECTANCE_ID (links to R1–R1868), WAVENUMBER (cm^-1).
- Key details
  - Wavenumber range: 4000 to 400 cm^-1; resolution: 2 cm^-1; 100 internal scans per acquisition.
  - Each sample normally has two spectra (before rotating the cup 180 degrees); some samples are represented by a SINGLE_SCAN.

## Sampling and geography
- Sampling design derived from Countryside Survey methodology to support national statistics.
- GB stratified by Land Classes; 1 km squares randomly selected within classes.
- 591 sample squares surveyed in 2007 (289 England, 107 Wales, 195 Scotland).
- Soil samples processed from archived 2007 Countryside Survey materials; 15 g subsamples used for analysis.
- Selection filters for MIR analysis:
  - Land Cover Map class: Arable, Improved Grass, or Neutral Grass.
  - Plots previously sampled in 1998 and 2007.
  - Aggregate Vegetation Classification categories: Crops and Weeds, Tall Grass and Herb, Fertile Grassland, or Infertile Grassland.
  - Sufficient soil mass available in archive material.
- Result: MIR data from 427 plots across GB (Figure provided in original documentation).

## Laboratory protocol
- Instrument: Bio-Rad FTIR (FTX3000MX) with diffuse reflectance accessory.
- Sample preparation: ~150 mg dried soil, ground for 45 seconds; no KBr added.
- Measurement: DRIFT spectra recorded as absorbance from 4000 to 400 cm^-1 with 2 cm^-1 resolution; two scans per sample (rotate cup 180° for a second spectrum).

## Data quality and quality assurance
- Field and lab QC: trained field staff; sampling manual; processing protocols for cores, logging, chemistry, and archiving.
- Spectral QA: visual inspection of the two scans; six spectra discarded prior to averaging; a single spectrum used for those samples (flagged in SINGLE_SCAN).
- Quality Assurance: UK Centre for Ecology & Hydrology maintains ISO 9001:2015 certified Quality Management System.

## How this data can be used in GIS
- Link MIR spectral data (R1–R1868) to spatial identifiers (SQUARE_ID, PLOT_ID) for map-based visualization of spectral signatures across Great Britain.
- Facilitate development of calibrated models to predict soil properties (e.g., organic matter, carbon) over space.
- Combine with other spatial datasets (land cover, AVC, soil classes) to explore spatial patterns and environmental gradients.
- Note: Data are from 2007 with a documentation version updated in 2021; consider temporal context when integrating with newer datasets.

## Acknowledgements and references
- Funded by the NERC Soil Security Programme.
- Data ownership: Countryside Survey, UK Centre for Ecology & Hydrology (UKCEH).
- Acknowledgement and copyright notice required for all data uses.
- Key references and links to Countryside Survey and related methodological documents are provided in the full documentation.