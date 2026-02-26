# C_SIDE_saltmarsh_radioisotopes_concentrations.csv

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE). Funding: NERC (NE/R010846/1).
- Dataset: Radioisotope concentrations in soil samples from UK saltmarshes, collected 2018–2021.
- Scope: 1358 down-core samples from 19 saltmarshes across the UK; UK geographic extent with coordinates provided (WGS84).

## Data content and structure
- Observed radionuclides: 210Pb, 214Pb, 137Cs, 241Am (activity concentrations in Bq/kg).
- Associated measurements: Sample Mass (g); depth information (Sample_Depth_cm, Mid_Depth_cm); location coordinates (Lat_dec_deg, Long_dec_deg); Sampling_Date.
- Data table fields include: Core_ID, Location, Sample_Depth_cm, Mid_Depth_cm, Lat_dec_deg, Long_dec_deg, Sampling_Date, Mass_g, Cs-137_Bq_kg, Cs-137_2-sigma, Pb-210_Bq_kg, Pb-210_2-sigma, Pb-214_Bq_kg, Pb-214_2-sigma, Pb-210ex_Bq_kg, Pb-210ex_2-sigma, Am-241_Bq_kg, Am-241_2-sigma.
- Data formats: .csv files; description headers define field descriptions and formats.

## Sampling, preprocessing, and measurement details
- Sample preparation: Freeze-dried, lightly milled; sealed in polystyrene gas-tight containers; typical pack masses up to 30 g.
- Sample range: Individual packed sample masses 0.2 g to ~40 g, with larger masses deeper in cores.
- Incubation: Samples incubated for ≥21 days prior to counting.
- Counting: Gamma spectrometry with Ortec planar detector system (GEM-FX8530-S N-type); ultra-low background for 210Pb detection; counting time ~86,000 seconds (~24 hours) per sample, across 3+ years (Nov 2019–Feb 2023); average ~25 samples per core.
- Calibration and standards: Instrument calibrated with low-background soil spiked with certified mixed radioactive standard (Eckert & Ziegler, 3.2 g, 9.9 g, 16.6 g, 30.4 g); calibration via EG&G GammaVision; inter-laboratory comparison with IAEA moss soil materials for QA.
- Target radionuclides for QA: 210Pb, 214Pb, 137Cs, 40K (via gamma lines) to ensure energy coverage.

## Data processing and quality control
- Corrections: Activity concentrations decay-corrected to the sampling date; corrected for signal attenuation with increasing sample mass (based on calibration soils).
- QA practices: Laboratory equipment calibrated per University of Plymouth practices; QA against moss soil certification; cross-checks via IAEA materials.
- Statistical treatment: Not provided within the dataset (NA for statistical processing).

## Metadata and documentation
- Data resource description structure included: Description and Cell Format headers clarifying each field’s meaning and units.
- Coordinate system: Latitude and longitude in decimal degrees (WGS84).
- Temporal coverage: Sampling 2018–2021; counting/analysis conducted 2019–2023.

## Governance, usability, and considerations for data leaders
- Provenance and traceability: Clear project backing, calibration standards, and QA provenance support trust and reproducibility.
- Discoverability and format: CSV format with explicit header definitions and field mappings; site-level and core-level identifiers enable cross-dataset linking.
- Data quality and gaps: Robust QA and calibration details included; however, no statistical summaries are provided (NA), so users may need to compute their own summaries if integrating with broader data ecosystems.
- Reuse potential: Suitable for reconstructing sedimentation histories and carbon storage studies in UK saltmarshes; cross-site comparisons facilitated by consistent methodology and decays corrections.

## Practical use cases for Data Leaders
- Align this dataset with broader coastal carbon storage or sedimentation studies by leveraging its traceable QA, calibration, and decay-corrected radionuclide concentrations.
- Integrate with other datasets through consistent metadata (Core_ID, Location, Depth, Date, and radionuclide measurements) to support governance and reporting.
- Assess data gaps and reliability for planning data collection, standardization, or community-of-practice efforts in radiometric soil analyses.