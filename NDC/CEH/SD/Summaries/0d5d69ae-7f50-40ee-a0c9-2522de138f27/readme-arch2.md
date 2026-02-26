# Fluvial flood maps of Vietnam for present day and future SSP/RCP scenarios (2070-2100)

- Purpose and scope
  - Provides fluvial flood maps for present day at 1 in 20 year return period and corresponding flood extents for three future SSP/RCP scenarios (2070-2100).
  - Future change in flood return periods estimated from CMIP6 projections and used to extract flood maps from a global flood model.
  - Focuses on riverine (fluvial) flooding; does not include pluvial or coastal flooding or explicit flood defences.

- Data generation and modelling
  - Flood maps generated with an updated global flood model (Fathom 2.0), building on Sampson et al. 2015.
  - Model enhancements include improved channel conveyance capacity (Neal et al., 2021) and an updated elevation dataset (MERIT DEM, Yamazaki et al., 2017).
  - Present-day maps use the 1 in 20 year return period; future maps use the nearest available return period from the Fathom 2.0 suite.

- Future scenarios and experimental design
  - Future maps derived for three scenarios: SSP5-8.5, SSP2-4.5, and SSP1-2.6.
  - Hirabayashi et al. 2021 CMIP6-based return-period maps converted to the nearest available return period in Fathom 2.0 (covering 5, 10, 20, 50, 75, 100, 200, 250, 500, 1000 year return periods) and then mosaicked across Vietnam.

- Data content and structure
  - 4 GeoTiff files and 1 readme:
    - VNM_1in20.tif (present-day 1 in 20 year flood depth)
    - VNM_ssp5rcp85_20.tif (future 1 in 20 year flood depth under SSP5-8.5)
    - VNM_ssp2rcp45_20.tif (future 1 in 20 year flood depth under SSP2-4.5)
    - VNM_ssp1rcp26_20.tif (future 1 in 20 year flood depth under SSP1-2.6)
  - Each file represents flood depth in metres; values of 0 correspond to no flood depth.
  - File sizes range from ~4.6 to ~5.5 MB.

- Data usage and interpretation
  - Present-day results can be compared with flood observations (remote sensing, photographs, articles, wrack marks) and assessed with skill metrics such as critical success index, hit rate, false alarm ratio, and bias.
  - For visualization, recommended to view GeoTiffs in GIS software (QGIS, ArcMap); set 0 as nodata or start color palettes at a small positive value (e.g., 0.1 m) to denote flooding.

- Analytical guidance
  - Spatial and statistical analyses are best conducted in R or Python.
  - The dataset supports monitoring by enabling standardized comparison across time and scenarios and facilitates integration with other relevant data.

- Quality control and provenance
  - The Fathom 2.0 model has been used in multiple publications (e.g., Bernhofen et al. 2022; Hawker et al. 2020; Mitchell et al. 2022; Rentschler et al. 2022).
  - References cited for underlying methods and data sources (Sampson et al. 2015; Yamazaki et al. 2017; Neal et al. 2021; Hirabayashi et al. 2021; etc.).

- References
  - Key supporting publications listed, including general flood hazard modeling and CMIP6-based flood risk work (Sampson et al. 2015; Bernhofen et al. 2022; Hawker et al. 2020; Hirabayashi et al. 2021; Neal et al. 2021; Yamazaki et al. 2017; Rentschler et al. 2022; Mitchell et al. 2022).