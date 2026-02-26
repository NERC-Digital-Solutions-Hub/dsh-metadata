# Vietnam flood maps (1 in 20 year return period) for present day and future SSP/RCP scenarios (2070-2100)

- Purpose and scope
  - Provides fluvial flood inundation depth maps for present day (1 in 20 year return period) and three future SSP/RCP scenarios for 2070-2100.
  - Future changes derived from CMIP6 projections; present-day map used as baseline.
  - Focus is on riverine (fluvial) flooding; excludes pluvial and coastal flooding and does not include explicit flood defences.

- Data sources and model lineage
  - Generated with an updated global flood model (Fathom 2.0) building on Sampson et al. (2015).
  - Improvements include updated channel conveyance capacity (Neal et al., 2021) and higher-quality elevation data (MERIT DEM; Yamazaki et al., 2017).
  - Future return periods calibrated to Hirabayashi et al. (2021) CMIP6 projections.

- Data content and units
  - Flood maps depict flood inundation depth in metres.
  - Return period for all maps is 1 in 20 years (present and future).
  - File set includes present-day and three future scenario maps.

- Data structure and files
  - 4 GeoTiff files plus one readme:
    - VNM_1in20.tif (present-day map)
    - VNM_ssp5rcp85_20.tif (SSP5/RCP8.5)
    - VNM_ssp2rcp45_20.tif (SSP2/RCP4.5)
    - VNM_ssp1rcp26_20.tif (SSP1/RCP2.6)
  - VNM denotes Vietnam (ISO3 code).
  - 0 in a map typically represents 0 m of flood depth; recommended to treat 0 as NoData or adjust color scales accordingly.
  - A readme document accompanies the GeoTiffs.

- Experimental design and processing
  - Future return-period maps from Hirabayashi et al. (2021) are rescaled to the nearest available return period in the Fathom 2.0 suite (5, 10, 20, 50, 75, 100, 200, 250, 500, 1000) and then mosaicked across Vietnam.

- Analytical methods and validation
  - Present-day map performance can be compared to observations (remote sensing, photographs, articles, wrack marks).
  - Skill metrics proposed: critical success index, hit rate, false alarm ratio, bias.
  - Cited methodological context from multiple publications (e.g., Bernhofen et al. 2022; Hawker et al. 2020; Hirabayashi et al. 2021; Mitchell et al. 2022; Neal et al. 2021; Rentschler et al. 2022; Yamazaki et al. 2017; Sampson et al. 2015).

- Guidance for use in GIS and visualization
  - Best viewed in GIS software (e.g., QGIS, ArcMap).
  - Set 0 as NoData or use a color scale that starts above 0 to highlight flooded areas (e.g., start at 0.1 m).
  - Suitable for spatial and statistical analyses in R or Python.

- Quality control and provenance
  - The underlying model (Fathom 2.0) is employed in peer-reviewed studies, supporting traceability and reproducibility.
  - Documentation references model updates, data sources, and validation practices.

- Data governance and stewardship considerations
  - Clear metadata and consistent file naming (country code, scenario, return period) to support discoverability and interoperability.
  - Versioning and provenance should be maintained across present and future scenarios; updates should reference the CMIP6-based basis and model version (Fathom 2.0 with MERIT DEM and channel capacity updates).
  - Understand and document scope limitations (only riverine flooding, no defences, no other flood types) to prevent misapplication.
  - Ensure data are stored in accessible portals, with guidance for end-users on appropriate usage, limitations, and recommended GIS workflows.
  - Documentation should capture methodology, assumptions, and references to enable reuse and reproducibility.