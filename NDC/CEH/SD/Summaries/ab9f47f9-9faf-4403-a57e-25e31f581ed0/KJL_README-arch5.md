# This file contains supporting information for datasets:

- Overview
  - Describes supporting information for multiple datasets related to Forsinard Flows RSPB reserve research, including lab experiments, field measurements, and MODIS-derived products.
  - Raw data files for flux and spectral measurements are held by The James Hutton Institute.
  - Eddy covariance data are not included in this repository due to ownership by dataset creators.

- Data holdings and storage
  - Lab data: KJL_data_lab
  - Lab corrections: KJL_corrections_lab and KJL_correction_lab
  - Field data: KJL_data_field
  - Field species data: KJL_species_field
  - MODIS-derived data: KJL_data_MODIS, KJL_TGdevelopment_MODIS, KJL_TGWa_development_MODIS, KJL_restoration_MODIS
  - Processed MODIS data (TG and TGWa models, gap-filled, quality-filtered): referenced alongside the above
  - Documentation notes include detailed variable dictionaries, site coordinates, and field codes
  - Access note: Ownership and rights for eddy covariance data remain with original data creators

- Lab data (set-up and measurements)
  - Species studied: Sphagnum capillifolium and S. papillosum
  - Experimental set-up: three Forsinard sites; 12-week rainfall manipulation with five treatments including a control and total drought
  - Growth conditions: growth cabinet with controlled light, temperature, and humidity; regular watering to saturation; edge effects mitigated by repositioning
  - Treatments: two rainfall amounts and two frequencies, plus drought; total drought group receives no rainfall
  - Measurements: carbon fluxes (GPP and respiration) via LICOR-8100; light/dark chamber fluxes; spectral reflectance and derived indices (NDVI, NDWI, EVI, PRI, SIPI, fWBI, Cim, etc.)
  - Corrections: background light correction using PAR sensor; regression-based corrections for GPP with PAR and measurement timing; constants added to match dataset midpoints
  - Data fields: extensive lab-wide data table (KJL_data_lab) with identifiers (Species, Group, Day, Date, Water, GPP_raw, GPP, R, NDVI, NDWI, fWBI, etc.) and derived metrics

- Field data (set-up and measurements)
  - Sites and design: three Forsinard sites (Lonielist, Talaheel, Cross Lochs); eight plots per site along two perpendicular transects; collars placed on two microforms per plot; Lonielist includes dipwells for water table
  - Measurements: monthly in 2017 (CO2 fluxes, spectral reflectance, environmental conditions); species composition surveyed in June 2017
  - Field instruments: LICOR-8100 with clear Perspex chambers for CO2 flux; handheld spectroradiometer for NDVI/related indices; PAR sensor; soil moisture probe; soil temperatures at 5 cm and 15 cm; surface temperature in chamber
  - Data fields: KJL_data_field with Site, Collar, microfeature, Date, DoY, Month, PAR, flux_light, flux_dark, GPP, NDVI, EVI, PRI, SIPI, fWBI, NDWI, Cim, and related environmental variables
  - Coordinates and site codes: WGS84 coordinates provided for field locations; site codes L (Lonielist), T (Talaheel), CL (Cross Lochs)

- MODIS data processing and models
  - Data processing and quality control: cloud filtering applied to MODIS products; pixel-level quality data used to determine usable 8-day/16-day periods
  - Specific products and filtering:
    - MOD17A2H (GPP): quality control to remove heavily cloud-affected pixels
    - MOD13Q1 (NDVI): remove snow/ice/cloud-affected values via pixel reliability index
    - MOD11A2 (LST): remove periods with cloud or data gaps
    - MOD09A1 (surface reflectance): remove cloud-affected pixels
  - Gap-filling: year-wide gap-filling following Wang et al. (2012)
  - NDWI calculation: NDWI = (NIR - SWIR) / (NIR + SWIR) using MODIS band data
  - Processed data stores:
    - KJL_TGdevelopment_MODIS: processed and gap-filled data for TG model development (Site, Date, MOD17, day, TG, LST, NDVI, etc.)
    - KJL_TGWa_development_MODIS: TGWa model development (Site, Date, DoY, year, MOD17, dayM, LST, NDVI, TG, NDWI, Season)
    - KJL_restoration_MODIS: processed data for restoration sites (six sites A–F and controls Ac–Fc) with years since felling, TG/ TGWa results
    - KJL_data_MODIS: 2017 data for Forsinard sites with DoY, NDVI, LST, TG, and TG-calibrated values
  - Model outputs: TG and TGWa models calibrated using NDVI, LST, and MODIS-derived indices

- Data governance, provenance, and metadata considerations
  - Data provenance: clear linkage between field measurements, lab experiments, and MODIS-derived products; site/plot/collar identifiers standardized across datasets
  - Metadata and data dictionaries: comprehensive descriptions of variables, units, and measurement methods; explicit column definitions for lab, field, and MODIS datasets
  - Data access and sharing: explicit note that eddy covariance data are not included due to ownership; data are organized in named directories with explicit IDs for traceability
  - Data quality and corrections: documented corrections for background light and PAR-based adjustments; correction datasets stored in KJL_correction_lab and KJL_corrections_lab
  - Data formats and interoperability: consistent naming conventions (KJL_ prefixes), geospatial coordinates, and time-based fields (Date, DoY, Day, Month) to support discovery and reuse

- Relevance to Data Stewards
  - Demonstrates robust data governance practices: structured storage, detailed metadata, correction provenance, and clear data lineage across lab, field, and remote-sensed MODIS data
  - Addresses interoperability challenges by standardizing identifiers, coordinates, and variable definitions; documents data processing steps and quality controls
  - Highlights access restrictions and ownership considerations (eddy covariance data not shared), illustrating alignment with data-sharing policies and licensing
  - Provides a blueprint for managing large, multi-source datasets with varying formats (lab records, field catalogs, and satellite products) and clear pathways for updates and re-use

- Notable references
  - Wang, G. et al. (2012) for the three-dimensional gap-filling method used in large geophysical datasets
  - Specific methodology details for spectral indices, GPP correction, and LD/NDVI-related calculations are documented within the lab and field data sections and accompanying correction files