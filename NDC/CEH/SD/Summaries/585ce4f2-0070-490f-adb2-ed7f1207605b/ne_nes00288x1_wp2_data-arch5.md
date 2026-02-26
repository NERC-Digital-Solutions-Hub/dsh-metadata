# Supporting information

- Overview
  - The dataset describes inundation results simulated by the HiPIMS model for pluvial flooding and fluvial flooding in Can Tho City, Vietnam.
  - Pluvial flooding results are driven by design rainfall for 2-, 5-, 10-, 20-, 50-, and 100-year return periods; fluvial flooding results are driven by the river water level boundary in 2011.

- Data generation and drivers
  - Pluvial flooding: inundation maps produced using design rainfall corresponding to each listed return period.
  - Fluvial flooding: inundation map produced using the 2011 river water level boundary.

- Data structure and content
  - Data are provided as TIFF files (maximum inundation water depth in meters) for each flood scenario.
  - Pluvial results:
    - 2years.tif (2-year return period)
    - 5years.tif (5-year return period)
    - 10years.tif (10-year return period)
    - 20years.tif (20-year return period)
    - 50years.tif (50-year return period)
    - 100years.tif (100-year return period)
  - Fluvial result:
    - 2011inundationMap.tif (2011 flood event)
  - Files contain information on the resolution of the base data and cell-averaged maximum inundation depth (meters).

- Quality control and provenance
  - HiPIMS model has established procedures and has been used in prior flood risk assessment projects.
  - Data generation and quality assurance are documented in related publications, indicating methodological rigor.

- Authors and references
  - Jiaheng Zhao, Qiuhua Liang
  - References:
    - Xia, X., Liang, Q., Ming, X., 2019. A full-scale fluvial flood modelling framework based on HiPIMS. Advances in Water Resources.
    - Xing, Y., et al., 2019. City-scale hydrodynamic modelling of urban flash floods. Nature Hazards.
    - Zhao, J., & Liang, Q., 2022. Novel variable reconstruction and friction source term discretisation for hydrodynamic modelling. Advances in Water Resources.

- Governance considerations for Data Stewards
  - Relevance: Suitable for flood risk assessment and urban planning; supports scenario analysis for Can Tho.
  - Metadata needs: document drivers (design rainfall returns, 2011 river level), date of data generation, spatial resolution, coordinate reference system, and data licensing.
  - Data quality and lineage: clearly capture model version (HiPIMS), calibration/validation references, and prior usage in projects.
  - Access and sharing: verify any usage restrictions or licensing; ensure clear attribution in any reuse.
  - Update strategy: define whether and when new design rainfall scenarios or updated river levels should be incorporated to keep datasets current.