Data resource description for C_SIDE_saltmarsh_radioisotopes_ concentrations.csv

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC
- Data resource: Radioisotope concentrations in UK saltmarsh soils (2018–2021)
- Samples: 1,358 down-core samples from 19 saltmarshes across the UK
- Radionuclides: 210Pb, 214Pb, 137Cs, 241Am (including total 210Pb and unsupported 210Pb_ex)
- Purpose: Enable environmental health monitoring, sedimentation/radiochemical histories, and cross-site comparisons

## What the data contain
- Core and location details:
  - Core_ID, Location (saltmarsh name), Lat_dec_deg, Long_dec_deg
  - Sampling_Date, Depth (Sample_Depth_cm; Mid_Depth_cm)
- Sample characteristics:
  - Mass_g (sample mass), number of samples per core (approximately 25)
- Observed concentrations (Bq kg^-1) and uncertainties:
  - Cs-137_Bq_kg, Cs-137_2-sigma
  - Pb-210_Bq_kg, Pb-210_2-sigma
  - Pb-214_Bq_kg, Pb-214_2-sigma
  - Pb-210ex_Bq_kg (excess Pb-210), Pb-210ex_2-sigma
  - Am-241_Bq_kg, Am-241_2-sigma
- Data format:
  - File: CSV
  - Includes decay corrections to sampling date and mass-based attenuation corrections

## Sample collection and measurement methods
- Sample preparation:
  - Freeze-dried and lightly milled; sealed in gas-tight containers
  - Sub-sample masses range ~0.2–40 g; packed to ≤30 g for calibration
  - Incubation: ≥21 days prior to counting
- Measurement:
  - Instrument: Ortec GEM-FX8530-S N-type HPGe planar detector (ultra-low background)
  - Target isotopes detected via gamma emissions at 46.5, 59.5, 295.3/352.0, and 661.6 keV
  - Counting duration: ~86,000 s (~24 hours) per sample
  - Timeframe: Data collected over 3+ years (Nov 2019–Feb 2023)

## Calibration and QA
- Calibration:
  - Using low-background soil spiked with certified radioactive standard across representative masses (3.2, 9.9, 16.6, 30.4 g)
  - Calibration relationships developed with GammaVision software
  - Verified by inter-laboratory tests using IAEA materials
- QA and proficiency:
  - QA based on moss soil materials with radionuclides (210Pb, 208Tl, 137Cs, 40K) spanning the energy spectrum
  - Equipment calibrated according to University of Plymouth practices
  - Inter-laboratory comparison via IAEA proficiency testing (IAEA-CU2009-03)

## Data processing and formats
- Data processing:
  - All activity concentrations decay-corrected to sampling date
  - Attenuation corrections for sample mass applied
  - Calibration curves derived per target radionuclide
- Data documentation:
  - Data resource description provides full metadata and field definitions for the CSV
  - Example columns described include Core_ID, Location, Sample_Depth_cm, Mid_Depth_cm, Lat_dec_deg, Long_dec_deg, Sampling_Date, Mass_g, Cs-137_Bq_kg, Cs-137_2-sigma, Pb-210_Bq_kg, Pb-210_2-sigma, Pb-214_Bq_kg, Pb-214_2-sigma, Pb-210ex_Bq_kg, Pb-210ex_2-sigma, Am-241_Bq_kg, Am-241_2-sigma

## Data accessibility and governance
- Data format and metadata are explicitly described to facilitate reuse in monitoring frameworks
- Underlying measurements are accompanied by uncertainties (2-sigma) and QA information
- The resource emphasizes robust data provenance, calibration standards, and traceability to ensure comparability across sites for environmental monitoring and policy evaluation

## Relevance for Monitoring Frameworks
- Provides a long-running, site-structured dataset suitable for:
  - Chronologies of sedimentation rates and mantle processes in saltmarshes
  - Historical contamination assessment via cesium-137 and lead-210 decay signatures
  - Cross-site comparisons to identify spatial trends and regional differences
- Rich metadata enables data integration with other environmental indicators and dashboards
- High-quality QA and calibration details support data trustworthiness and governance expectations for monitoring outputs

## Considerations and limitations
- Spatial coverage: 19 saltmarshes; may limit broad national extrapolation
- Temporal span: samples from 2018–2021 with counting data spanning 2019–2023; not a continuous time series
- Variable sample masses and depths require careful standardization for comparative analyses
- Data sharing and accessibility policies are described through the resource, but users should verify any access constraints in the original data repository if applicable