# This file contains supporting information for datasets: KJL_data_lab KJL_corrections_lab KJL_data_field KJL_species_field KJL_TGdevelopment_MODIS KJL_TGWa_development_MODIS KJL_restoration_MODIS KJL_data_MODIS

## Overview
- Describes supporting information and metadata for multiple datasets related to lab and field measurements, as well as MODIS-based processing outputs.
- Raw flux and spectral data are held by The James Hutton Institute.
- Datasets cover laboratory experiments, field measurements, and satellite-derived vegetation and climate proxies, with associated processing, corrections, and model outputs.
- Includes data storage schemas, site and sample identifiers, and QC/processing steps to enable reuse and integration with other environmental monitoring data.

## Experimental setup

- Laboratory experiments
  - Sphagnum species: S. capillifolium and S. papillosum collected from Forsinard Flows RSPB reserve (sites Talaheel, Catanach, Raphan) with precise coordinates.
  - Growth conditions: 12-hour day/night cycle in a controlled growth cabinet; day 20,000 lx; 15°C day, 70% RH; night dark at 5°C.
  - Experimental design: four replicates per species across five rainfall regimes (A–E) for 12 weeks; Group A is control (20 ml water, three times per week).
  - Treatments: two rainfall amounts, two frequencies; drought group E (no rainfall). After 3 weeks, humidity lowered to 55%.
  - Post-treatment: samples flooded to simulate rewetting; carbon flux measurements repeated after inundation.

- Field experiments
  - Sites within Forsinard: Lonielist, Talaheel, Cross Lochs; eight plots per site along two transects per site.
  - Setup: collars placed on higher and lower microforms; Lonielist included dipwells for water table height.
  - Measurements: CO2 fluxes, spectral reflectance, and environmental conditions once a month during 2017 growing season (Mar–Sep).
  - Species survey and collar-specific data collected; coordinates provided for field locations.

## Measurements and data collected

- Laboratory measurements
  - Carbon flux: LICOR-8100 with a custom chamber; GPP calculated from light/dark flux difference.
  - Biomass and moisture: sample weighing and drying to determine moisture content.
  - Spectral data: Ger3700 spectrometer; multi-angle reflectance; reference panel measurements.
  - Spectral indices: NDVI, EVI, NDWI, fWBI, PRI, SIPI, CIm, and related pigment indices with defined wavelength ranges.
  - Data fields stored in KJL_data_lab include sample metadata, fluxes, PAR, GPP (raw and corrected), respiration, NDVI, NDWI, and various indices.

- Field measurements
  - CO2 flux: LICOR-8100 with clear Perspex chambers; light and dark measurements, 5-minute runs.
  - Spectral data: handheld spectroradiometer; multiple measurements per collar with reference panel.
  - PAR, soil moisture (ThetaKit), soil temperature (5 cm and 15 cm), surface temperature.
  - Derived metrics: GPP (clear-dark), GPP corrected for PAR, NDVI, EVI, PRI, SIPI, fWBI, NDWI, Clm, TG model outputs, and site/ collar metadata.
  - Field data stored in KJL_data_field with site, collar, microform, dates, times, and measurement series.
  - Species composition per collar provided in KJL_species_field.

## Corrections and data processing

- Background light correction
  - PAR sensor added four weeks after start to correct for variable ambient light; regression used to estimate PAR-driven GPP (GPPr).
  - Two correction equations applied:
    - GPP = GPPm - GPPr + 1.4 (PAR-based correction)
    - GPP = GPPm - GPPr + 0.2 (time-based adjustment)
  - Regression based on sample subset to estimate GPPr; overall slope used to adjust GPPm.
- Timing proxy used for early weeks when PAR data unavailable.
- Lab corrections stored in KJL_corrections_lab with fields for measurement corrections, including time_corr and PAR_corr.

## Datasets and data storage

- Lab data
  - KJL_data_lab: contains unique sample IDs, species, group, day/date, water content, fluxes (flux_light/flux_dark), PAR, GPP_raw and GPP (corrected), respiration, NDVI, NDWI, and spectral indices.
  - KJL_corrections_lab: stores correction parameters and application details.

- Field data
  - KJL_data_field: stores site, collar, microfeature, date, DOY/Month, PAR, flux values, start/end temperatures, soil moisture/temperature, NDVI/EVI/PRI/SIPI indices, and model outputs (TG, TGWa).
  - KJL_species_field: provides collar-level species presence/absence and relative cover.

- Spatial and site metadata
  - Field coordinates are provided in WGS84 for all sites and collars (Lonielist, Talaheel, Cross Lochs and sub-sites).
  - Site codes: L (Lonielist), T (Talaheel), CL (Cross Lochs).

## MODIS data and processing

- Datasets and storage
  - KJL_TGdevelopment_MODIS: processed, gap-filled data used to develop the TG model (site, date, MOD17 GPP, daily TG, LST, NDVI, scaled LST/NDVI).
  - KJL_TGWa_development_MODIS: processed data for TGWa model (Glencar site in this dataset; DoY, year, MOD17, dayM, LST, NDVI, TG, NDWI, Season).
  - KJL_restoration_MODIS: processed data for six restoration sites and six controls; includes TG and TGWa results, seasonal NDWI.
  - KJL_data_MODIS: 2017 MODIS data for Forsinard sites with DoY, NDVI, LST, TG.
- Data processing steps
  - Cloud filtering to retain usable pixels; MODIS quality data used to discard problematic pixels (clouds, snow/ice).
  - Gap-filling applied per Wang et al. 2012 methodology.
  - NDWI calculated from MODIS band 2 (NIR) and band 6 (SWIR) for each valid pixel.
- Notes
  - Eddy covariance data are not included in these MODIS-derived datasets and remain with original data owners.

## Data accessibility and ownership

- Raw flux and spectral measurements are held by The James Hutton Institute.
- MODIS-derived products and model outputs are produced for research use and stored in the specified KJL_* datasets.
- Data quality and provenance are documented (measurement conditions, corrections, coordinates, and table schemas) to enable integration with other environmental monitoring datasets.
- References: Wang et al. (2012) for large geophysical data gap-filling methodology.

## Relevance for environmental monitoring

- Provides standardized, QAed datasets across lab and field measurements plus satellite-derived proxies, enabling temporal and spatial comparisons.
- Facilitates cross-linking of ground-based flux measurements with spectral indices and MODIS-derived GPP/LST/NDVI for ecosystem health and response to moisture/rainfall regimes.
- Supports data integration and transparency by detailing storage schemas, corrections, and data provenance, aligning with common monitoring workflows and data portals.