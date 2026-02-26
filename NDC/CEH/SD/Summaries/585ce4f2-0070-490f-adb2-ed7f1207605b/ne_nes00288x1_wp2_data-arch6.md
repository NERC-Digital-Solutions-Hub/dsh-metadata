# Inundation results simulated by HiPIMS model for the pluvial flooding and fluvial flooding in Can Tho city Vietnam

## Overview
- Dataset describes inundation results simulated by the HiPIMS model for pluvial and fluvial flooding in Can Tho city, Vietnam.
- Pluvial flooding results are driven by design rainfall with return periods of 2, 5, 10, 20, 50, and 100 years.
- Fluvial flooding results are driven by the river water level boundary in 2011.
- Each TIFF file provides the maximum inundation water depth (in meters) for the corresponding scenario.

## Collection/Generation Methods
- Inundation data generated using the HiPIMS hydrodynamic model.
- HiPIMS has been previously used for flood risk assessment in multiple projects (Zhao & Liang 2022; Xia et al. 2019; Xing et al. 2019).
- Data are organized as TIFF files representing the maximum depth during each flood event.
- Scenario categorization:
  - Pluvial: 2years.tif, 5years.tif, 10years.tif, 20years.tif, 50years.tif, 100years.tif
  - Fluvial: 2011inundationMap.tif

## Quality Control
- Development and generation follow well-established procedures.
- Model validated through prior applications in flood risk assessment, indicating reliability for the presented scenarios.

## Data Structure and Content
- File format: TIFF (.tif) with cell-averaged maximum inundation depth (meters).
- Pluvial inundation results:
  - 2years.tif
  - 5years.tif
  - 10years.tif
  - 20years.tif
  - 50years.tif
  - 100years.tif
- Fluvial inundation result:
  - 2011inundationMap.tif
- Each file includes information about the resolution of the base data and the depth values per cell.

## Usage and Applications for Data Support
- Enables comparison of flood depths under multiple rainfall return periods and the 2011 river flood scenario.
- Can be used to create self-serve data products (e.g., dashboards, GIS maps, reports) for flood risk visualization and planning.
- Useful for integrating with other datasets (topography, land use, drainage networks) for broader flood risk analyses and decision support.

## Access and Metadata
- Data are provided as georeferenced TIFFs with depth in meters.
- Filenames encode the scenario (years or 2011) to aid quick identification and filtering.
- Base data resolution is included within each file’s metadata.

## References
- Xia, X., Liang, Q., Ming, X., 2019. A full-scale fluvial flood modelling framework based on a high-performance integrated hydrodynamic modelling system (HiPIMS). Advances in Water Resources 132, 103392.
- Xing, Y., Liang, Q., Wang, G., Ming, X., Xia, X., 2019. City-scale hydrodynamic modelling of urban flash floods: the issues of scale and resolution. Nat Hazards 96, 473-496.
- Zhao, J., & Liang, Q. (2022). Novel variable reconstruction and friction source term discretisation schemes for hydrodynamic modelling of overland flow and surface water flooding. Advances in Water Resources, 104187.