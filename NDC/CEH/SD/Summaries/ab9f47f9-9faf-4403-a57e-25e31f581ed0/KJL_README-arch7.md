# This file contains supporting information for datasets:

## Overview
- Documents supporting information for multiple datasets: KJL_data_lab, KJL_corrections_lab, KJL_data_field, KJL_species_field, KJL_TGdevelopment_MODIS, KJL_TGWa_development_MODIS, KJL_restoration_MODIS, KJL_data_MODIS.
- Raw flux and spectral measurement data reside at The James Hutton Institute.
- Datasets cover laboratory experiments on Sphagnum moss, field measurements, and MODIS-based remote sensing products.

## Spatial scope and sites
- Lab work: Forsinard Flows RSPB reserve lab setup at Talaheel, Catanach, Raphan (provided WGS84 coordinates).
- Field work: Three Forsinard sites—Lonielist (L), Talaheel (T), Cross Lochs (CL)—with eight plots per site along two perpendicular transects; collar-based observations and microform differences.
- Field coordinates are provided in WGS84 for field locations L1–L8, T1–T8, CL1–CL8.
- Field data include collar-level measurements with two microforms per collar and associated plot-level environmental data.

## Laboratory setup and experimental design
- Sphagnum samples (S. capillifolium and S. papillosum) collected at 6 cm depth, 10 cm diameter.
- Growth cabinet conditions: 12-hour day/night; day 20,000 lx; 15°C day; 5°C night; 70% RH (day) with unregulated humidity at night.
- Experimental treatments: five rainfall regimes across four replicates per species, over 12 weeks; a control group (A) maintained at 20 ml water three times per week.
- Post-treatment rewetting: samples flooded to top within 2 cm, kept at high humidity for one month, followed by measurements after drainage.

## Measurements and data collection
- Gas flux measurements: LICOR-8100 gas analyser with a custom chamber; 90-second measurements; GPP calculated as difference between light and dark fluxes.
- Carbon and moisture: samples weighed; dry weights measured at 70°C for moisture content.
- Spectral reflectance: Ger3700 spectrometer; measurements from three angles; Spectralon reference panel used; nadir viewing.
- Calculated spectral indices and bands: fWBI, NDWI, NDVI, EVI, PRI, SIPI, CIm, with defined blue, red, NIR, SWIR bands and wavelengths.
- Corrections for background light: PAR sensor added; GPP corrections using regression-based adjustments (GPP = GPPm − GPPr + constant); time-based corrections for measurement number.
- Data fields (lab): detailed columns for sample ID, species, group, day, date, moisture, fluxes (flux_light, flux_dark), PAR, GPP_raw, GPP, respiration (R), NDVI, EVI, PRI, SIPI, NDWI, fWBI, Cim, etc.

## Field measurements and data
- Field data collection at Lonielist, Talaheel, and Cross Lochs during 2017 growing season (Mar–Sep).
- CO2 flux: LICOR-8100 with clear Perspex chambers; 5-minute measurements with a 20-second stabilization.
- Spectral measurements: handheld spectroradiometer (SVC HR-1024); three measurements per collar, rotated to minimize shadows; Spectralon reference panel used.
- PAR, soil moisture (ThetaKit), soil temperature (5 cm and 15 cm), and surface temperature recorded.
- Data fields (field): site, collar ID, microfeature (hummock vs hollow), date, DoY, month, time, time correction, PAR, GPP, GPP2 (PAR-corrected GPP), NDVI, EVI, PRI, SIPI, Clm (CIm), fWBI, NDWI; dipwell water table depth only at Lonielist.
- Species composition per collar provided in KJL_species_field (percent cover by species; abbreviations for common peatland species and other flora/fauna).

## Remote sensing data and processing (MODIS)
- Datasets referenced: KJL_TGdevelopment_MODIS, KJL_TGWa_development_MODIS, KJL_restoration_MODIS, KJL_data_MODIS.
- Cloud/snow/cloud-affected pixels filtered using product-specific quality metrics:
  - MOD17A2H: remove clouds; gap-fill year-round (Wang et al. 2012 method).
  - MOD13Q1: remove snow/ice or cloud-affected values via pixel reliability.
  - MOD11A2: remove periods with no data due to cloud or other issues.
  - MOD09A1: remove cloud-affected pixels using surface reflectance state data.
- Gap-filling: applied for each year using Wang et al. (2012) three-dimensional approach.
- NDWI calculation: NDWI = (NIR − SWIR) / (NIR + SWIR) using MODIS bands (500 m resolution in MOD09A1).
- Processed and gap-filled data are stored in respective KJL_ directories:
  - KJL_TGdevelopment_MODIS: processed data used to develop the TG model (Lonielist/Talaheel; includes MOD17, daily estimates, LST, NDVI, scaled LST/NDVI, TG results).
  - KJL_TGWa_development_MODIS: data for TGWa model (Glencar; includes MOD17, daily estimates, LST, NDVI, TG results, NDWI, season indicators).
  - KJL_restoration_MODIS: restoration site data (six sites A–F and controls Ac–Fc; years since felling; TG and TGWa outputs by year and JAS/OND NDWI).
  - KJL_data_MODIS: 2017 MODIS-derived processor outputs for Forsinard (Lonielist, Talaheel, Cross Lochs): DoY, NDVI, LST, TG (TG model calibrated to EC data).
- Output products support GIS-ready mapping and modeling of GPP, LST, and vegetation indices across sites and years.

## Data quality, provenance, and references
- Emphasizes data provenance: multiple datasets with explicit storage locations and field/experimental details.
- Indicates lack of eddy covariance data ownership restrictions for MODIS-related outputs.
- Reference for gap-filling methodology: Wang, G. et al. 2012 (three-dimensional gap filling for large geophysical datasets).
- MODIS-based processing includes explicit quality-control and structured metadata to enable spatial analyses and reproducibility.

## Metadata and data structure notes
- Structured in modular datasets with consistent fields across lab, field, and MODIS data.
- Site codes and field coordinates provided for reproducibility and GIS integration.
- Spectral indices and environmental measurements accompany flux data to enable spatial and temporal analysis of peatland carbon dynamics.