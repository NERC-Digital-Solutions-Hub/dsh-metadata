# C_SIDE_saltmarsh_radioisotopes_concentrations.csv

## Overview
- Dataset from the Carbon Storage in Intertidal Environments (C-SIDE) project, funded by NERC.
- Radioisotope concentrations measured in UK saltmarsh soils to support coastal carbon storage studies.
- 1358 down-core soil sub-samples from 19 saltmarsh sites across the UK.
- Sampling period for collection: 2018–2021; counting and analysis conducted 2019–2023.
- Data suitable for age-dating, sedimentation rate assessment, and carbon storage investigations.

## Scope and Provenance
- Geographic coverage: United Kingdom saltmarshes; site locations provided with decimal lat/long (WGS84).
- Sites selected to represent a diverse range of UK saltmarsh habitats for comparability.
- Data resource describes measured radionuclide activities and associated metadata.

## Data Content and Variables
- Core metadata:
  - Core_ID: Core identification
  - Location: Saltmarsh name
  - Sampling_Date: Date of sample collection
- Sub-sample metadata:
  - Sample_Depth_cm: Depth interval of sub-sample (cm)
  - Mid_Depth_cm: Mid-point depth (cm)
  - Lat_dec_deg, Long_dec_deg: Geographic coordinates (decimal degrees, WGS84)
  - Mass_g: Mass of the sub-sample (g)
- Measured radionuclide activities (Bq kg-1) with uncertainties (2-sigma):
  - Cs-137_Bq_kg, Cs-137_2-sigma
  - Pb-210_Bq_kg, Pb-210_2-sigma
  - Pb-214_Bq_kg, Pb-214_2-sigma
  - Pb-210ex_Bq_kg, Pb-210ex_2-sigma
  - Am-241_Bq_kg, Am-241_2-sigma
- Additional notes:
  - All activity concentrations are decay-corrected to the sampling date for their respective cores.
  - Pb-210 measurements include the total Pb-210 and the unsupported/excess Pb-210 (Pb-210ex) derived via the 226Ra activity (measured via 214Pb).

## Methods: Measurement, Calibration and QA
- Sample preparation:
  - Freeze-dried and lightly milled; sealed in polystyrene gas-tight containers.
  - Sample sizes typically 0.2–30 g (max 30 g for calibration compatibility); incubation of at least 21 days before counting.
- Instrumentation:
  - Ortec planar detector system (GEM-FX8530-S N-type detector) with ultra-low background configuration for 210Pb.
  - Gamma energies used: 46.5 keV (210Pb), 59.5 keV (208Tl proxy), 295.3 and 352.0 keV (214Pb), 661.6 keV (137Cs).
- Calibration:
  - Instrument calibrated with low-background soil spiked with certified mixed radioactive standard (Eckert & Ziegler Analytics, masses 3.2, 9.9, 16.6, 30.4 g).
  - Calibration relationships derived using EG&G GammaVision software.
  - Verified by inter-laboratory comparisons with IAEA materials (IAEA-CU2009-03 proficiency test).
- QA and quality control:
  - Moss soil used for QA checks; selected radionuclides based on energy distribution (210Pb, 208Tl, 137Cs, 40K).
  - Laboratory practices and equipment calibration aligned with University of Plymouth standards.
- Counting regime:
  - Each sub-sample counted for a minimum of ~86,000 seconds (~24 hours) over multiple sessions within a 3+ year window.

## Data Structure and File Format
- File format: CSV (comma-separated values).
- Data resource description structure includes:
  - Core_ID, Location, Sample_Depth_cm, Mid_Depth_cm, Lat_dec_deg, Long_dec_deg, Sampling_Date, Mass_g
  - Cs-137_Bq_kg, Cs-137_2-sigma
  - Pb-210_Bq_kg, Pb-210_2-sigma
  - Pb-214_Bq_kg, Pb-214_2-sigma
  - Pb-210ex_Bq_kg, Pb-210ex_2-sigma
  - Am-241_Bq_kg, Am-241_2-sigma
- Data corrections documented:
  - Decay correction to sampling date
  - Attenuation correction for varying sample masses

## Processing, Corrections and Uncertainty
- Decay corrections applied to all activity concentrations.
- Signal attenuation corrections applied based on calibration across sample mass range.
- Uncertainties provided as 2-sigma values for each reported concentration.
- Data quality assurance includes instrument calibration, QA samples, and inter-lab proficiency checks.

## Access, Reuse and Notes
- Data described as CSV with accompanying metadata fields detailing units, formats, and decay corrections.
- Suitable for integration into age-dating workflows, sedimentation-rate analyses, and interpretation of coastal soil radioactivity profiles.
- Users should account for reported uncertainties (2-sigma) and the decay-corrected nature of the concentrations when combining across cores or sites.