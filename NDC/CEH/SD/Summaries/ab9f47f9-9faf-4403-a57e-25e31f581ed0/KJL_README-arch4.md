# This file contains supporting information for datasets: KJL_data_lab KJL_corrections_lab KJL_data_field KJL_species_field KJL_TGdevelopment_MODIS KJL_TGWa_development_MODIS KJL_restoration_MODIS KJL_data_MODIS

## Overview
- Provides supporting information and metadata for multiple datasets related to lab experiments, field measurements, and MODIS-based processing.
- Datasets cover carbon flux measurements, spectral data, corrections, species and site metadata, and processed MODIS-derived model outputs (TG and TGWa).
- Raw flux and spectral data are archived at The James Hutton Institute; some data (eddy covariance) is not included due to ownership.

## Datasets and Components
- KJL_data_lab: Lab-based measurements of Sphagnum spp. including GPP, respiration, PAR, moisture, and spectral indices; includes corrected GPP values and various field-derived indices (NDVI, NDWI, EVI, PRI, SIPI, fWBI, Cim, etc.).
- KJL_corrections_lab: Details on corrections applied to lab GPP data to account for background light and measurement timing; provides regression-based correction equations and constants.
- KJL_data_field: Field measurements from three Forsinard Flows sites, including CO2 fluxes, spectral indices, PAR, soil moisture/temperature, collar-level data, and species percentage cover per collar.
- KJL_species_field: Species presence/absence data per collar (wide range of peatland flora and lichens) and habitat descriptors.
- KJL_TGdevelopment_MODIS: Processed and gap-filled MODIS data used to develop the TG model (site, date, MOD17, LST, NDVI, TG, etc.).
- KJL_TGWa_development_MODIS: Processed and gap-filled MODIS data used to develop the TGWa model (Glencar site, date, DoY, TG, NDWI, season, etc.).
- KJL_restoration_MODIS: Processed MODIS data for restoration sites, including years since felling and TG/TGWa outputs, plus NDWI indices by season (JAS, OND).
- KJL_data_MODIS: 2017 processed MODIS data for Lonielist, Talaheel, and Cross Lochs (NDVI, LST, TG, etc.).
- Data organization: Lab data (KJL_data_lab) and field data (KJL_data_field) with detailed variable schemas; field coordinates are provided in WGS84; site codes include L (Lonielist), T (Talaheel), CL (Cross Lochs).

## Data Collection Methods
- Lab experiments:
  - Sphagnum capillifolium and S. papillosum collected from Forsinard Flows reserve.
  - Growth cabinet conditions with controlled temperature, humidity, and light; edge effects minimized by randomization across shelves and days.
  - Five rainfall regimes plus drought; 12-week duration; 4 replicates per species per treatment.
  - Carbon fluxes measured with LICOR-8100; GPP derived from light/dark flux differences.
  - Spectral reflectance measured with Ger3700 spectrometer; indices calculated from defined wavelength bands.
- Field experiments:
  - Three Forsinard sites with eight plots per site; collars placed on different microforms.
  - Monthly measurements during 2017 growing season: CO2 flux (LICOR-8100), spectral data (handheld spectroradiometer), PAR, soil moisture/temperature, and surface temperature.
  - Species surveys conducted; field coordinates and collar metadata recorded.
  - Data captured include site, collar, microform, date, DoY, flux values, spectral indices, NDVI/EVI, and modeled outputs.

## Data Corrections and Processing
- PAR-based corrections to GPP:
  - PAR sensor added after four weeks; regression-based correction to remove background light effects.
  - Correction equations adjust GPPm (measured) to GPP using PAR-derived and time-based adjustments, with constants to align midpoints (e.g., +1.4 and +0.2 adjustments).
- Data quality and gap-filling:
  - MODIS data filtered to exclude cloud-affected or snow/ice pixels; quality flags used (MOD17A2H, MOD13Q1, MOD11A2, MOD09A1).
  - Gap-filling performed per Wang et al. (2012) methodology to produce usable annual data.
- Data provenance:
  - Clear separation between raw measurements, corrections, and processed/model outputs; detailed file-level metadata and field definitions accompany each dataset.

## Location, Metadata, and Access
- Site coordinates and field locations provided in WGS84 (with explicit coordinates for Forsinard sites and field collars).
- Site codes and naming conventions documented (L, T, CL; L1–L8, T1–T8, CL1–CL8, etc.).
- Species and sample metadata stored in dedicated fields; table schemas describe each variable (e.g., GPP, R, NDVI, NDWI, etc.).
- Access note: Eddy covariance data is not included in this dataset due to ownership constraints; MODIS-derived datasets are processed and stored for modeling purposes.

## Data Governance and Stewardship
- Ownership considerations highlighted for eddy covariance data; other datasets appear to be organized under clearly named repositories with defined storage tables.
- Comprehensive documentation and metadata accompany each dataset to support reuse, replication, and modeling work.
- Data products include both measurements and model outputs (TG, TGWa) intended for integration into broader carbon flux analyses and ecosystem modeling.

## Key Takeaways for Data Leaders
- End-to-end data pipeline is documented from raw lab/field measurements through corrections to processed MODIS products and model outputs.
- Rich metadata and defined variable schemas enhance discoverability, interoperability, and reuse across networks.
- Data governance considerations are explicit, including data ownership restrictions for certain components and the explicit treatment of data quality (cloud filtering, gap filling, and calibration corrections).
- The collection combines controlled experiments, in-situ field data, and satellite-derived modeling, enabling multi-scale carbon flux analyses and vegetation/phenology assessments.