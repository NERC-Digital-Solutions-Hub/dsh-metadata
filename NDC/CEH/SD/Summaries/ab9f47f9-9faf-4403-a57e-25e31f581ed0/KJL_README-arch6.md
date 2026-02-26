# This file contains supporting information for datasets:

- Raw data storage
  - Raw data files for flux and spectral measurements are held by The James Hutton Institute.

- Datasets and data products (KJL series)
  - Laboratory data: KJL_data_lab
  - Lab corrections: KJL_corrections_lab and KJL_correction_lab
  - Field data: KJL_data_field
  - Species field: KJL_species_field
  - MODIS-derived datasets:
    - KJL_TGdevelopment_MODIS
    - KJL_TGWa_development_MODIS
    - KJL_restoration_MODIS
    - KJL_data_MODIS

- Experimental set-up and scope
  - Lab experiments
    - Species: Sphagnum capillifolium and S. papillosum
    - Location: Forsinard Flows RSPB reserve (sites Talaheel, Catanach, Raphan)
    - Design: 4 replicates per species exposed to five rainfall regimes (A–E) over 12 weeks; control group A receives steady watering; drought group E receives no water
    - Environment: growth cabinet with 12 h day/night cycle; daytime 20,000 lx, 15°C, 70% RH; nighttime dark, 5°C
    - Procedures: randomised placement to minimise edge effects; post-treatment rewetting and re-measurement
  - Field experiments
    - Sites: Lonielist, Talaheel, Cross Lochs (Forsinard)
    - Setup: two PVC collars per plot (high and low microform) across eight plots per site along two transects
    - Measurements: CO2 fluxes, spectral reflectance, environmental conditions; monthly during 2017 growing season (Mar–Sep)
    - Additional data: species surveys per collar (percentage cover)

- Measurements and instruments
  - Laboratory measurements
    - Gas flux: LICOR-8100 with custom chamber; 90-second measurements; GPP calculated as difference between light and dark fluxes
    - Weighing: samples weighed; dry weights after 72 h at 70°C for moisture content
    - Spectral reflectance: Ger3700 spectrometer; three angles per sample; reference panel with Spectralon
    - Wavelength bands and indices:
      - Blue 450–515 nm; Red 630–680 nm
      - NIR 841–876 nm (NDWI) / 845–885 nm (NDVI & EVI)
      - SWIR 1628–1652 nm
      - Indices: fWBI, NDWI, NDVI, EVI, PRI, SIPI, CIm
    - Corrections for background light
      - PAR sensor added after four weeks; background light corrections applied to GPP
      - Regression-based corrections using a set of sampled mornings for GPP and PAR
      - Time/measuring-number-based corrections to align GPP
    - Metadata fields in KJL_data_lab include: ID, SpeciesGroup, Species, Group, Day, Date, Water, flux_light, flux_dark, PAR, measurement_no, GPP_raw, GPP, R, NDVI, fWBI, EVI, PRI, SIPI, Cim, NDWI, etc.
  - Field measurements
    - Gas flux: LICOR-8100 with clear Perspex chamber; five-minute measurements; light and dark consecutive measurements
    - Spectral measurements: handheld spectroradiometer (SVC HR-1024) with Spectralon reference; three measurements per collar
    - PAR: sensor in peat outside chamber
    - Soil measurements: soil moisture (ThetaKit/dynamax), soil temperature at 5 cm and 15 cm, surface temperature
    - Derived field indices: NDVI, EVI, PRI, SIPI, CIm, fWBI, NDWI
    - Metadata fields in KJL_data_field include: Site, Collar, microfeature, Date, DoY, Month, Time, Time_diff, Time2, soil_moisture, soil_temp_5cm, soil_temp_15cm, flux_light_no, flux_light, start_light, end_light, flux_dark_no, flux_dark, start_dark, end_dark, PAR, GPP, GPP2, NDVI, EVI, PRI, SIPI, CIm, fWBI, NDWI, Duplicates for collar-level measurements
  - Field locations and coding
    - Site codes: L = Lonielist, T = Talaheel, CL = Cross Lochs
    - Field coordinates provided for collar locations (WGS84)

- Species and site metadata
  - KJL_species_field stores collar-level species composition; listed taxa include Calluna vulgaris, Erica tetralix, Eriophorum spp., Molinia, Sphagnum species, Cladonia lichens, mosses, and other ground cover
  - Location data for field sites and collars include precise coordinates (WGS84) and collar IDs

- Data management, processing, and quality control
  - MODIS processing and quality control
    - Cloud filtering to remove extensively cloud-affected pixels; usable data retained
    - Quality indicators used: MOD17A2H (GPP, gap-filled), MOD13Q1 (NDVI/NDWI reliability and snow/cloud removal), MOD11A2 (data availability), MOD09A1 (cloud-affected pixels)
    - Gap-filling performed per Wang et al. 2012 method
  - NDWI calculation from MODIS
    - NDWI = (NIR - SWIR) / (NIR + SWIR) using MOD09A1 band 2 (NIR) and band 6 (SWIR)
  - Data ownership
    - Eddy covariance data not included in the datasets; ownership retained by original data creators
  - Data storage and structure
    - Processed and gap-filled data for TG model and TGWa model are stored in the respective KJL_MODIS datasets
    - 2017 Forsinard MODIS data stored in KJL_data_MODIS with site, DoY, NDVI, LST, TG, etc.

- References and methodology notes
  - Gap-filling methodology reference: Wang, G. et al. (2012)
  - NDWI and related indices defined within the described spectral framework
  - PAR and background-light corrections are detailed in the lab correction files (KJL_corrections_lab, KJL_correction_lab)

- End-user guidance
  - Outputs include self-serve data products (GPP, NDVI, NDWI, EVI, PRI, SIPI, fWBI, Cim) and model outputs (TG, TGWa)
  - Careful attention to data provenance, site and collar metadata, and correction steps when combining lab and field datasets with MODIS-derived products