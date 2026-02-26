# Inundation results simulated by HiPIMS model for pluvial and fluvial flooding in Can Tho city Vietnam

## Overview
- Describes inundation results simulated by the HiPIMS model for pluvial flooding and fluvial flooding in Can Tho city, Vietnam.
- Pluvial flooding results are driven by design rainfall corresponding to 2-, 5-, 10-, 20-, 50-, and 100-year return periods.
- Fluvial flooding results are driven by river water level boundary from 2011.
- The dataset has been used to support flood risk assessment in multiple projects.

## Collection and generation methods
- Data generated using the HiPIMS (high-performance integrated hydrodynamic modelling system) for inundation mapping.
- The HiPIMS model has been previously applied in flood risk assessment in various projects (citations provided).

## Quality control
- Data development and generation follow established procedures.
- HiPIMS-based inundation results have been used in prior work to support flood risk assessments (references: Zhao & Liang 2022; Xia et al. 2019; Xing et al. 2019).

## Data structure and content
- Data are provided as TIFF (.tif) files containing the maximum inundation water depth (in meters) during a specific flood event.
- Pluvial flooding files (driven by rainfall)
  - 2years.tif
  - 5years.tif
  - 10years.tif
  - 20years.tif
  - 50years.tif
  - 100years.tif
- Fluvial flooding file
  - 2011inundationMap.tif (inundation depth for 2011 flood)
- Each file includes information about the resolution of the base data and the cell-averaged maximum inundation depth (meters).

## Usage and considerations
- The dataset documents the maximum inundation depth per cell for each scenario, enabling assessment and comparison of flood risk across return periods and flood drivers.
- Data are suitable for integration into flood risk analyses, planning, and related decision-making tasks, with emphasis on understanding how different rainfall intensities or historical river levels influence inundation.

## References
- Xia, X.; Liang, Q.; Ming, X. (2019). A full-scale fluvial flood modelling framework based on a high-performance integrated hydrodynamic modelling system (HiPIMS). Advances in Water Resources, 132, 103392.
- Xing, Y.; Liang, Q.; Wang, G.; Ming, X.; Xia, X. (2019). City-scale hydrodynamic modelling of urban flash floods: the issues of scale and resolution. Nat Hazards, 96, 473-496.
- Zhao, J.; Liang, Q. (2022). Novel variable reconstruction and friction source term discretisation schemes for hydrodynamic modelling of overland flow and surface water flooding. Advances in Water Resources, 104187.