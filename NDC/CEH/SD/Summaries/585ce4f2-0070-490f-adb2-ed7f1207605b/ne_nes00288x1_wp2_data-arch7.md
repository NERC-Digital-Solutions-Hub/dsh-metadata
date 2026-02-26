# Inundation results simulated by HiPIMS model for pluvial flooding and fluvial flooding in Can Tho city, Vietnam

- Overview
  - Dataset describing inundation results simulated by the HiPIMS model for Can Tho city, Vietnam.
  - Includes pluvial flooding results driven by design rainfall for 2-, 5-, 10-, 20-, 50-, and 100-year return periods.
  - Includes fluvial flooding results driven by river water level boundary in 2011.
  - Intended for flood risk assessment and map-based visualization in GIS workflows.

- Data collection and generation
  - Authors: Jiaheng Zhao, Qiuhua Liang.
  - Method: HiPIMS model; validated and used in multiple flood risk projects.
  - Supporting references provided for the HiPIMS framework and related methods.

- Data structure and file naming
  - Data format: TIFF files containing maximum inundation water depth (meters) for each scenario.
  - Pluvial flooding files:
    - 2years.tif, 5years.tif, 10years.tif, 20years.tif, 50years.tif, 100years.tif
  - Fluvial flooding file:
    - 2011inundationMap.tif
  - Each file includes information about base data resolution and cell-averaged maximum depth.

- Quality control
  - Data developed and generated following established procedures.
  - HiPIMS has been successfully used to support flood risk assessment in prior projects (cited in references).

- Practical usage for GIS
  - Use TIFF layers to visualize maximum inundation depth for specified flood scenarios.
  - Layer selection by return period (pluvial) or by year 2011 (fluvial) for Can Tho city.
  - Helpful for risk communication, planning, and policy discussions; can be combined with other GIS datasets.
  - Be mindful of units (meters) and potential differences in base data resolutions when combining multiple layers.

- Limitations and considerations
  - Data may have varying base resolutions across files; harmonization may be needed for integrated analyses.
  - Scenario-specific results (specific return periods and 2011 river conditions) rather than a single, uniform dataset.

- References
  - Xia, X.; Liang, Q.; Ming, X. (2019). A full-scale fluvial flood modelling framework based on a high-performance integrated hydrodynamic modelling system (HiPIMS). Advances in Water Resources.
  - Xing, Y.; Liang, Q.; Wang, G.; Ming, X.; Xia, X. (2019). City-scale hydrodynamic modelling of urban flash floods: the issues of scale and resolution. Nat Hazards.
  - Zhao, J.; Liang, Q. (2022). Novel variable reconstruction and friction source term discretisation schemes for hydrodynamic modelling of overland flow and surface water flooding. Advances in Water Resources.