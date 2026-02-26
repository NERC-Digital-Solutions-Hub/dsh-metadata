# Soil mid-infrared spectroscopy data from arable and grassland in Countryside Survey, Great Britain 2007 Version: 2: 13-01-2021

## Overview
- Diffuse reflectance mid-infrared (MIR) spectroscopy data for archive soils from 427 soils across 151 1km squares in Great Britain (surveyed in 2007).
- Data primarily stored in two CSV files:
  - MIR_raw_data.csv: contains absorbance values for R1 to R1868, plus metadata (SQUARE_ID, PLOT_ID, SINGLE_SCAN).
  - MIR_wavenumbers.csv: maps REFLECTANCE_ID to specific WAVENUMBER (cm-1).
- Purpose: enable spectral analyses to predict soil properties (e.g., organic matter content, carbon), supporting environmental monitoring and policy assessment through standardized, scalable outputs.

## Sampling design and coverage
- Grounded in Countryside Survey design: GB stratified by Land Classes; 1km squares randomly selected within classes to ensure national representativeness.
- 2007 sampling: 591 sample squares (289 England, 107 Wales, 195 Scotland); soil selections resulted in 427 plots with MIR data.
- Soil sampling: top 0–15 cm, 15 g subsamples extracted from archived soil samples, air-dried and sieved to 2 mm; archival storage at UKCEH Soil Archive, Lancaster.
- Sampling rationale: aims to provide robust GB-scale statistics across environments while enabling linkage to broader Countryside Survey data.

## Laboratory protocol and data capture
- Instrumentation: Diffuse reflectance infrared Fourier transform spectroscopy (DRIFT) using FTIR with diffuse reflectance attachment.
- Measurement: wavenumber range 4000–400 cm-1, 2 cm-1 resolution, 100 scans per acquisition; two spectra obtained per sample (sample cup rotated 180° for a second measurement).
- Sample preparation: dried soil (~150 mg) ground for 45 seconds; no KBr added; spectra recorded as absorbance values.
- Data representation: MIR_raw_data.csv includes two spectra per sample when applicable; the SINGLE_SCAN column indicates if only one spectrum is used for that sample.

## Quality control and assurance
- Field protocols: trained surveyors and a field sampling manual to ensure consistency.
- Spectral QC: prior to averaging, spectra reviewed to avoid scan errors; six spectra discarded; a single spectrum used for those samples (flagged in SINGLE_SCAN).
- Quality assurance: UKCEH maintains an ISO 9001:2015 certified Quality Management System with documented QA policies and procedures.

## Data structure and interpretation
- MIR_raw_data.csv: 
  - SQUARE_ID, PLOT_ID, SINGLE_SCAN (text indicators), R1–R1868 (absorbance values).
- MIR_wavenumbers.csv:
  - REFLECTANCE_ID (links to MIR_raw_data columns), WAVENUMBER (cm-1).
- The combination of absorbance values with corresponding wavenumbers enables calibration models to predict soil properties and assess soil health indicators.

## Applications for environmental monitoring
- Provides a standardized, auditable dataset to monitor soil properties across GB over time when integrated with other environmental data.
- Facilitates comparisons of soil health and carbon-related metrics across regions and habitat types.
- Supports data-driven assessments of policy outcomes related to soil management, land use, and environmental resilience.

## Access, reuse, and acknowledgement
- Data usage requires acknowledgement of Countryside Survey data and UK Centre for Ecology & Hydrology.
- Funded by the NERC Soil Security Programme; CS data usage and copyright restrictions apply.
- Links and references available in the accompanying documentation for context and methodology.