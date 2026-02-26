# Radioisotope concentrations of soil samples from UK saltmarshes collected between 2018 and 2021

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE); Funded by NERC (NE/R010846/1)
- Dataset scope: Radioisotope concentrations in 1358 down-core soil samples from 19 saltmarshes across the UK
- Target isotopes: 210Pb, 214Pb, 137Cs, 241Am; includes total 210Pb and the unsupported component 210Pbex
- Timeframe: Samples collected 2018–2021; activity measurements conducted from 2019–2023
- Data format: CSV file(s) with structured metadata and measurements

## Dataset content and structure
- Geographic scope: United Kingdom saltmarsh sites; coordinates provided in decimal degrees (WGS84)
- Observations: Each row corresponds to a sub-sample within a core, with depth information
- Key variables/parameters:
  - Core_ID, Location (saltmarsh name), Sample_Depth_cm, Mid_Depth_cm
  - Lat_dec_deg, Long_dec_deg
  - Sampling_Date
  - Mass_g (mass of each sub-sample)
  - Isotope concentrations: Cs-137_Bq_kg, Pb-210_Bq_kg, Pb-214_Bq_kg, Pb-210ex_Bq_kg, Am-241_Bq_kg
  - Uncertainties: Cs-137_2-sigma, Pb-210_2-sigma, Pb-214_2-sigma, Pb-210ex_2-sigma, Am-241_2-sigma
- Data resource structure: Includes headers and cell formats descriptions for the CSV, with fields such as Description and Cell Format
- Coverage notes: Site selections intended to represent UK saltmarsh diversity; down-core sampling for temporal and depositional analyses

## Methods and quality assurance
- Sample preparation: Freeze-dried, lightly milled; sealed in polystyrene gas-tight containers; typical sub-sample masses 0.2–40 g (max ~30 g for calibration)
- Incubation: Sub-samples incubated for at least 21 days prior to counting
- Counting/measurement: Gamma spectrometry using Ortec planar detector (GEM-FX8530-S N-type) for ultra-low background
  - Target energies: 210Pb (46.5 keV), 214Pb (59.5 keV), 137Cs (661.6 keV), and 241Am (59.5–? energy noted, 295.3 & 352.0 keV for 214Pb and 137Cs; reference lists specific energies for targets)
  - Counting duration: ~86,000 seconds per sub-sample (~24 hours)
  - Instrument calibration and QA rely on a certified mixed radioactive standard (EZN-7603ML) with representative masses (3.2, 9.9, 16.6, 30.4 g)
- Calibration and validation:
  - Calibration performed with moss soil-like material; inter-laboratory comparison with IAEA proficiency materials (IAEA-CU2009-03)
  - Calibration relationships derived using EG&G GammaVision software
  - Attenuation corrections applied based on calibration soils
  - Decay corrections applied to each core’s sampling date
  - 210Pb total and 210Pbex calculated via 226Ra activity (measured through 214Pb gamma emissions)
- Data quality checks:
  - All laboratory equipment calibrated per university practices
  - QA framework includes IAEA moss soil-based QA and cross-checks against known standards

## Data formats and documentation
- Primary data format: CSV (C_SIDE_saltmarsh_radioisotopes_concentrations.csv and related data resource description files)
- Data resource description fields:
  - Core_ID (Text)
  - Location (Saltmarsh name; Text)
  - Sample_Depth_cm (Number)
  - Mid-Depth_cm (Number)
  - Lat_dec_deg (Number)
  - Long_dec_deg (Number)
  - Sampling_Date (Date)
  - Mass_g (Number)
  - Cs-137_Bq_kg (Number); Cs-137_2-sigma (Number)
  - Pb-210_Bq_kg (Number); Pb-210_2-sigma (Number)
  - Pb-214_Bq_kg (Number); Pb-214_2-sigma (Number)
  - Pb-210ex_Bq_kg (Number); Pb-210ex_2-sigma (Number)
  - Am-241_Bq_kg (Number); Am-241_2-sigma (Number)

## Data governance and stewardship considerations
- Metadata completeness: Ensure full capture of sampling dates, depths, locations, and measurement uncertainties; maintain WGS84 coordinates
- Data provenance: Document preparation, counting procedures, calibrations, decay corrections, and QA steps for traceability
- Interoperability: Consistent units (Bq kg^-1, grams, centimeters); clear column naming and units in metadata and CSV headers
- Accessibility and updates: Dataset spans 2019–2023 measurement period; clarify any embargo or access restrictions and plan for future updates or extended measurements
- User alignment: Information provided supports reuse for sediment dating, deposition rate calculations, and environmental radioactivity assessments

## Access, usage notes, and limitations
- Access format: CSV files supplemented by data resource descriptions; suitable for programmatic ingestion and metadata mapping
- Limitations to consider:
  - Variable sub-sample masses and depth intervals across cores
  - Uncertainties provided as 2-sigma values; users should propagate uncertainties in downstream analyses
  - Depth-integrated totals or unsupported isotopes not listed; interpretation requires decay- and attenuation-corrected values as described
  - Site coverage is UK-wide but limited to 19 saltmarshes; representativeness should be considered for regional analyses