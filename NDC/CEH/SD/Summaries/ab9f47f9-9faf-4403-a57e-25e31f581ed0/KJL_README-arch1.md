# Supporting information for datasets: KJL_data_lab, KJL_corrections_lab, KJL_data_field, KJL_species_field, KJL_TGdevelopment_MODIS, KJL_TGWa_development_MODIS, KJL_restoration_MODIS, KJL_data_MODIS

## Overview
- This document provides detailed supporting information for multiple datasets related to lab experiments on Sphagnum moss, field measurements in Forsinard Flows, and MODIS-based modelling products.
- Raw flux and spectral data are held by The James Hutton Institute.
- The work includes experimental design, measurement protocols, data corrections, and data storage schemas to enable replication and reuse.

## Laboratory experiment setup (Sphagnum moss)
- Species studied: Sphagnum capillifolium and Sphagnum papillosum.
- Sites for sampling: Talaheel, Catanach, and Raphan in Forsinard Flows RSPB reserve with precise WGS84 coordinates provided.
- Sample geometry: 6 cm deep, 10 cm diameter cores placed in 1 L jars.
- Growth conditions: 12-hour light/dark cycle; day 20,000 lx light, 15°C, 70% RH; night dark at 5°C.
- Pre-experiment conditioning: samples saturated with water for a week; watering every 2 days during conditioning.
- Experimental design: four replicates per species exposed to five rainfall regimes across 12 weeks (80 days).
- Treatments:
  - Group A (control): 120 ml per fortnight, 6 events; upkeep to steady-state water content.
  - Group B: 120 ml per fortnight, 3 events.
  - Group C: 60 ml per fortnight, 3 events.
  - Group D: 60 ml per fortnight, 6 events.
  - Group E: total drought (0 ml; frequency not applicable).
- Post-treatment rewetting: after 12 weeks, samples flooded to ~2 cm below top; remained inundated for one month, then drained; carbon flux measurements repeated three times over a week.

## Measurements and instruments (lab)
- Carbon fluxes: measured with LICOR-8100 gas analyzer; 90-second chamber measurements; light and dark fluxes used to compute Gross Primary Productivity (GPP = light minus dark fluxes).
- Sample monitoring: periodic weighing; final drying at 70°C for 72 hours to compute moisture content.
- Spectral measurements: Ger3700 spectrometer; three angles per sample; Spectralon reference panel; nadir viewing.
- Spectral indices and bands used:
  - Blue (450–515 nm), Red (630–680 nm), NIR (NDVI range), SWIR (NDVI/EVI ranges).
  - fWBI, NDWI, NDVI, EVI, PRI, SIPI, CIm, and other indices with defined wavelength equations.
- Corrections for background light:
  - PAR sensor added 4 weeks into experiment; corrections applied to remove background light effects on GPP.
  - Regression-based corrections using nine samples to relate PAR and measured GPP (GPPr = 0.0204 × PAR; GPP = GPPm − GPPr + 1.4).
  - Time-based correction using measurement number (GPPr = 0.0054 × measurement_no; GPP = GPPm − GPPr + 0.2).
  - Constant offset adjustments (1.4 and 0.2) added to align midpoints across data.
- Data storage (lab):
  - KJL_data_lab: contains per-sample IDs, species, group, day, date, water content, fluxes, GPP (raw and corrected), respiration (R), NDVI, NDWI, fWBI, EVI, PRI, SIPI, Cim, and related changes and ratios.
  - KJL_correction_lab: contains measurement-level corrections (time_corr, PAR_corr) and corrected GPP values.

## Field study (Forsinard sites: Lonielist, Talaheel, Cross Lochs)
- Setup: eight plots per site along two perpendicular transects within eddy covariance footprints.
- Site specifics:
  - Lonielist: main transect 80 m, secondary 60 m; plots 20 m apart; dipwells for water table height with collars.
  - Talaheel: transects 100 m and 75 m; plots 25 m apart.
  - Cross Lochs: transects 120 m and 90 m; plots 30 m apart.
- Collar and species surveying: species composition measured in June 2017; data stored in KJL_species_field as percentage cover per collar.
- Measurements per month (Mar–Sep 2017): CO2 fluxes, spectral reflectance, and environmental conditions.
- Field instrumentation:
  - CO2 flux: LICOR-8100 with clear Perspex chambers; five-minute measurements with airflow via small fans; light and dark measurements consecutively.
  - Spectral measurements: handheld SVC HR-1024 spectroradiometer; three measurements per collar from different angles; Spectralon reference panel; PAR measured with a sensor inside the collar; leaf/peat reflectance indices calculated from handheld spectra.
  - Environmental measures: soil moisture (ThetaKit), soil temperature at 5 cm and 15 cm, surface temperature inside the chamber; collar-level PAR and flux measurements by LICOR.
- Field data storage:
  - KJL_data_field: extensive fields including Site, Collar, microform, date, DoY, time, time corrections, PAR, fluxes (light/dark), GPP, NDVI, EVI, PRI, SIPI, fWBI, NDWI, Cim, and other spectral indexes; geographic coordinates for field locations.
  - Site codes: L = Lonielist, T = Talaheel, CL = Cross Lochs.
- Location coordinates: WGS84 coordinates provided for all collar and field locations (dense table of points).

## Satellite MODIS datasets and modelling (KJL_TGdevelopment_MODIS, KJL_TGWa_development_MODIS, KJL_restoration_MODIS, KJL_data_MODIS)
- Data processing and quality control:
  - Cloud filtering applied to MODIS products; data quality flags used to exclude heavily cloud-affected pixels.
  - For MOD17A2H (GPP): remove pixels with significant cloud impact.
  - For MOD13Q1 (NDVI): remove snow/ice/cloud-affected values using pixel reliability index.
  - For MOD11A2: remove periods without data due to cloud or other issues.
  - For MOD09A1: remove pixels with cloud impact on surface reflectance.
- Gap filling: executed year-wide using methods described by Wang et al. (2012) to fill gaps in time series.
- NDWI calculation (MODIS-based): NDWI = (NIR - SWIR) / (NIR + SWIR) using MODIS band data.
- Datasets and storage:
  - KJL_TGdevelopment_MODIS: processed and gap-filled data used to develop the TG model; fields include Site (Lonielist, Talaheel), Date (8-day period), MOD17 (GPP), MOD17day (daily GPP), TG model results, LST, NDVI, scaled LST/NDVI.
  - KJL_TGWa_development_MODIS: includes GLencar site; DoY, year, daily MOD17, LST, NDVI, scaled LST/NDVI, TG results, NDWI, Season.
  - KJL_restoration_MODIS: six restoration sites labeled A–F and six controls Ac–Fc; Years_since_felling, Year, TG model outputs (TGa, TGWa) and NDWI measures for JAS and OND.
  - KJL_data_MODIS: 2017 MODIS data for Lonielist, Talaheel, Cross Lochs; DoY, NDVI, LST, TG (TG model results calibrated to EC data).
- Modelling references:
  - TG and TGWa models integrate NDVI and LST data to estimate gross primary productivity across sites and years.
  - Wang et al. (2012) cited as the basis for the gap-filling approach.

## Practical considerations and notes for analysts
- Data accessibility challenges highlighted:
  - Some datasets require navigation of multiple sources and access controls; metadata and portals are used to make datasets discoverable.
  - The field and lab data include extensive metadata to ensure traceability of samples, methodologies, and corrections.
- Data quality and preprocessing:
  - Background light corrections and PAR-based adjustments are essential for accurate GPP estimation in lab measurements.
  - Timing and measurement number used as proxies for PAR in the initial weeks reflect pragmatic calibration steps.
- Data scope:
  - The document provides both raw measurement details and structured data schemas, enabling replication and secondary analyses.
  - Raw lab data are stored separately from processed results, with explicit correction procedures and model outputs described.

## Summary of data organization
- Lab data and corrections: KJL_data_lab, KJL_corrections_lab
- Field data and species information: KJL_data_field, KJL_species_field
- MODIS processing and model outputs: KJL_TGdevelopment_MODIS, KJL_TGWa_development_MODIS, KJL_restoration_MODIS, KJL_data_MODIS
- Raw data sources: Flux and spectral measurements held at The James Hutton Institute
- Documentation preserves site coordinates, plot layouts, collar setups, sampling dates, and a detailed variable glossary to support reproducibility and cross-dataset analyses.