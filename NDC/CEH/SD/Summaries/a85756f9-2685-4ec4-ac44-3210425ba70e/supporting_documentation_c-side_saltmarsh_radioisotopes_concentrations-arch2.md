# Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Project funded by NERC (NE/R010846/1) focusing on carbon storage in UK intertidal saltmarshes.
- Data resource comprises radioisotope concentrations to inform sedimentation rates and carbon burial assessments across saltmarsh habitats.

## Dataset scope
- Radioisotope concentrations in soil samples from UK saltmarshes.
- 1358 down-core samples from 19 saltmarshes across the UK (sampling 2018–2021).
- Geographic coverage: UK saltmarsh sites with coordinates provided (WGS84).
- Variables observed: Sample Mass (g), Cs-137, Pb-210, Pb-214, Pb-210-excess, and Am-241 concentrations.

## Sampling and observational methods
- Sample preparation: freeze-dried, lightly milled, sealed in gas-tight containers; mass range 0.2–40 g (typical up to 30 g to fit calibration); samples incubated ≥21 days prior to counting.
- Analysis: activity concentrations measured with an Ortec planar detector and HPGe gamma spectrometry optimized for low background, targeting specific gamma emissions for each radionuclide.
- Key radionuclide calculations: total Pb-210 measured; Pb-210ex (unsupported) derived by subtracting Ra-226 activity (via 214 Pb gamma emissions).
- Counting duration: minimum ~86,000 seconds (~24 hours) per sample, over 3+ years (Nov 2019–Feb 2023).
- Throughput: on average ~25 samples analysed per core.
- Corrections: decay-corrected to core sampling date; attenuation corrections for increasing sample mass; calibration adjustments per calibration soils.

## Calibration and quality assurance
- Calibration: using low-background soil spiked with certified mixed radioactive standard across representative masses (3.2, 9.9, 16.6, 30.4 g) and matched geometry; calibration relationships derived in GammaVision; cross-validated via inter-laboratory tests with IAEA materials (including moss soil reference).
- QA: Moss soil-based QA using radionuclides 210Pb, 208Tl, 137Cs, 40K across energy spectrum (46 keV to 1460 keV).
- Data quality checks: laboratory equipment calibrated per University of Plymouth practices.
- Statistical treatment: not applicable/NA in the dataset documentation.

## Data formats and documentation
- Primary data format: CSV (C_SIDE_saltmarsh_radioisotopes_concentrations.csv).
- Data resource description includes:
  - Core_ID, Location (saltmarsh name), Sample_Depth_cm, Mid_Depth_cm, Lat_dec_deg, Long_dec_deg, Sampling_Date, Mass_g.
  - Concentrations and uncertainties: Cs-137_Bq_kg, Cs-137_2-sigma, Pb-210_Bq_kg, Pb-210_2-sigma, Pb-214_Bq_kg, Pb-214_2-sigma, Pb-210ex_Bq_kg, Pb-210ex_2-sigma, Am-241_Bq_kg, Am-241_2-sigma.
- Additional data descriptions and headers provided to facilitate data interpretation and reuse.

## Relevance to environmental monitoring
- Demonstrates standardized data collection, processing, and QA for environmental radioisotope datasets.
- Supports long-term monitoring and comparison of sedimentation and carbon storage dynamics across UK saltmarshes.
- Data structure and documentation are aligned with common monitoring portal practices to enable data sharing and accessibility.

## Data access and reuse considerations
- Data are prepared with decay corrections and mass-attenuation adjustments, enabling integration with other environmental datasets.
- Rich metadata and a structured data dictionary facilitate reuse in analyses of sedimentation rates, carbon burial, and inter-site comparisons.
- The dataset exemplifies efforts to increase dataset value by enabling broader data sharing and cross-dataset analyses in environmental monitoring contexts.