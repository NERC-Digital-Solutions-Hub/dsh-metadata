# This file contains supporting information for datasets: KJL_data_lab
KJL_corrections_lab
KJL_data_field
KJL_species_field
KJL_TGdevelopment_MODIS
KJL_TGWa_development_MODIS
KJL_restoration_MODIS
KJL_data_MODIS
Raw data files for flux and spectral measurements are held by The James Hutton Institute.

## Overview
- Documents the datasets and methods underpinning lab and field measurements of carbon flux, spectral indices, and MODIS-derived environmental variables.
- Clarifies data management, corrections, metadata, and data delivery structures to support monitoring and evaluation of environmental health measures.

## Set-up and experimental design
- Lab experiment (Forsinard Flows RSPB reserve):
  - Sphagnum species: S. capillifolium and S. papillosum; collected from Talaheel, Catanach, and Raphan sites.
  - Sample format: 6 cm deep, 10 cm diameter; stored in 1 L jars in a growth cabinet with controlled day/night cycle.
  - Conditions: day 20,000 lx; 15°C; 70% RH; night dark, 5°C.
  - Pre-treatment: moisture equilibration with watering every 2 days for 1 week.
  - Experimental groups: five rainfall regimes (A control, B–D varying amounts and frequencies, E total drought).
  - Duration: 12 weeks (80 days); post-treatment rewetting and one-month saturated conditions prior to carbon flux re-measurement.
- Field experiment (Forsinard sites):
  - Sites: Lonielist, Talaheel, Cross Lochs with two perpendicular transects and two collars per plot (high vs. low microforms).
  - Measurements: CO2 fluxes, spectral reflectance, environmental conditions, monthly throughout 2017 growing season.
  - Additional data: plant species composition per collar, coordinates for field locations, soil moisture/temperature, PAR, and water-table indicators at Lonielist.

## Measurements and data captured
- Lab measurements:
  - Carbon fluxes using LICOR-8100 with a custom chamber; GPP calculated as difference between light and dark fluxes.
  - Gas concentrations recorded during ~90-second flux measurements; respiration (R) and related metrics tracked.
  - Biomass moisture content via dry weight after oven-drying.
  - Spectral reflectance with a Ger3700 spectrometer; indices computed include NDVI, EVI, NDWI, fWBI, PRI, SIPI, Cim, and related pigment indices.
- Data corrections and calibration:
  - Background light correction introduced mid-way using a PAR sensor; corrections applied to GPP measurements.
  - Two correction formulas:
    - PAR-based correction: GPPr = slope × PAR; GPP = GPPm − GPPr + 1.4
    - Time/measurement-based correction: GPPr = slope × measurement_number; GPP = GPPm − GPPr + 0.2
  - Final GPP values reflect corrected GPP (GPP) alongside raw GPP (GPP_raw) and other flux metrics (flux_light, flux_dark, R).
- Data structure and fields (examples):
  - KJL_data_lab: sample IDs, species, group, day/date, water content, fluxes, PAR, GPP_raw, GPP, R, NDVI, NDWI, EVI, PRI, SIPI, fWBI, Cim, etc.
  - KJL_corrections_lab: measurement-level corrections (time_corr, PAR_corr) and resulting GPP values.

## Field data collection and metadata
- Data stored in KJL_data_field; core fields:
  - Site code (L, T, CL), collar ID, microform (high ground/hummock vs low ground/hollow), date, DoY, time, soil moisture (mV), soil temperatures (5 cm and 15 cm), PAR, flux measurements (flux_light_no, flux_light, flux_dark_no, flux_dark), start/end temperatures, NDVI, EVI, PRI, SIPI, fWBI, NDWI, GPP, model outputs, and other spectral indices.
- Field sampling details:
  - Field locations provided with precise WGS84 coordinates for collars and field plots.
  - Species presence and percent cover recorded per collar in KJL_species_field.
  - Additional site descriptors include site names (Lonielist, Talaheel, Cross Lochs) and field coordinates.

## Species and habitat metadata
- KJL_species_field stores collar-specific species composition data using presence/absence or percent cover indicators for a range of species (e.g., Calluna, Eriophorum species, Sphagnum species, mosses, lichens, and other vegetation components).
- Habitat and ground features (e.g., bare peat, deer dung) captured as part of collar-level metadata.

## MODIS data processing and products
- Datasets and processing:
  - KJL_TGdevelopment_MODIS: processed and gap-filled data to develop the TG model (site, date, MOD17 GPP, day GPP, TG model results, LST, NDVI, scaled LST/NDVI).
  - KJL_TGWa_development_MODIS: similar development data for the TGWa model (Glencar site); includes NDWI, season, TG, and model outputs.
  - KJL_restoration_MODIS: data for six/restoration sites and controls, including years since felling, TG/TGWa results, and NDWI indicators by season (JFM, AMJ, JAS, OND).
  - KJL_data_MODIS: 2017 MODIS-derived variables (Site, DoY, NDVI, LST) and TG model results; site-by-date aggregation.
- Quality control and gap filling:
  - Cloud screening applied to MODIS products; pixel-level quality flags used to exclude poor data (snow, ice, or cloud-affected values).
  - Gap filling follows methods described by Wang et al. (2012) for large geophysical datasets.
- NDWI construction:
  - NDWI calculated as (NIR − SWIR) / (NIR + SWIR) from MODIS bands (band 2 and band 6, or equivalent).

## Data ownership and governance
- Note: Eddy covariance data are not included in these datasets because ownership remains with the original data creators.
- Emphasis on data provenance, processing steps, and clear documentation to support transparency, reproducibility, and future monitoring decisions.

## Models and outputs
- TG and TGWa models:
  - TG model outputs calibrated to NDVI and LST data; daily or period-averaged GPP estimates.
  - TGWa model outputs for TGWa with NDWI and seasonal adjustments.
- Model inputs/outputs stored with corresponding metadata (site, date, DoY, NDVI, LST, TG/TGWa, NDWI, etc.) to support trend analysis and monitoring evaluations.

## Data references and provenance
- Wang, G. et al. (2012) referenced for the gap-filling methodology: “A three-dimensional gap filling method for large geophysical datasets: Application to global satellite soil moisture observations.”
- Additional methodological references underpin quality control, index calculations, and MODIS data handling.