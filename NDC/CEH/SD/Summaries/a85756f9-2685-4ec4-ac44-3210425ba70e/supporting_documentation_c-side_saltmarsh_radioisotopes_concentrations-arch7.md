# C_SIDE_saltmarsh_radioisotopes_concentrations.csv

## Overview
- Data from the Carbon Storage in Intertidal Environments (C-SIDE) project, funded by NERC (NE/R010846/1).
- Radioisotope concentrations in UK saltmarsh soils: 1358 down-core samples from 19 saltmarshes, collected 2018–2021; analyzed via gamma spectrometry for Cs-137, Pb-210, Pb-214, and Am-241.
- Counting period extended across 2019–2023; samples counted for ~86,000 seconds (~24 hours) each, with typical ~25 samples per core.

## Spatial and site information
- Observations located across the United Kingdom saltmarsh coastline; sites chosen to represent diverse saltmarsh habitats.
- Locations provided as decimal degrees (WGS84) with Lat_dec_deg and Long_dec_deg.
- Location field lists saltmarsh name for each observation.

## Data content and structure
- File format: CSV (C_SIDE_saltmarsh_radioisotopes_concentrations.csv).
- Core and sample metadata:
  - Core_ID (text)
  - Location (saltmarsh name)
  - Sample_Depth_cm (depth interval of sub-sample)
  - Mid_Depth_cm (mid-point depth of the interval)
  - Lat_dec_deg, Long_dec_deg (spatial coordinates, WGS84)
  - Sampling_Date (date of sample collection)
  - Mass_g (mass of sample)
- Radionuclide concentrations (per sample) with uncertainties:
  - Cs-137_Bq_kg; Cs-137_2-sigma
  - Pb-210_Bq_kg; Pb-210_2-sigma
  - Pb-214_Bq_kg; Pb-214_2-sigma
  - Pb-210ex_Bq_kg; Pb-210ex_2-sigma
  - Am-241_Bq_kg; Am-241_2-sigma

## Methods and QA
- Sample preparation: freeze-dried, milled, sealed in gas-tight containers; typical sub-sample masses range from 0.2 g to ~30 g.
- Measurement: Ortec planar detector system (GEM-FX8530-S) and HPGe gamma spectrometry optimized for low background, targeting 210Pb, 214Pb, 137Cs, 241Am via characteristic gamma emissions.
- Calibration: instrument calibrated with low-background soil spiked with certified radioactive standard across multiple masses (3.2 g, 9.9 g, 16.6 g, 30.4 g); calibration built in EG&G GammaVision software; validated via inter-laboratory comparison (IAEA moss soil QA, materials IAEA-CU2009-03).
- Corrections: decay corrections applied to sampling date; attenuation corrections based on calibration data across sample masses.
- Data quality: laboratory equipment calibrated per standard practices; QA includes moss soil reference checks.

## Data structure notes
- All data are stored in a single CSV with explicit 2-sigma uncertainty fields for each radionuclide concentration.
- Depth and coordinate data enable construction of depth-resolved, geolocated radionuclide maps within GIS workflows.

## GIS relevance and applications
- Directly support map-based visualization of radionuclide distributions across UK saltmarshes and through depth profiles.
- Enables spatial comparisons among sites, integration with saltmarsh extent layers, chronology, and environmental covariates.
- Suitable for creating interactive maps showing core depth slices, sampling dates, and concentration gradients.

## Access, provenance, and lineage
- Project and data provenance tied to C-SIDE under NERC funding; dataset includes detailed methodological notes and QA procedures.
- Data resource description accompanies the CSV, outlining header fields and their formats for accurate ingestion into GIS and data analysis workflows.