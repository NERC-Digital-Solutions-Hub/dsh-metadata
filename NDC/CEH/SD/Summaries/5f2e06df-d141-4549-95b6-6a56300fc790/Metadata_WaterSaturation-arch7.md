# Mathematically modelled daily water saturation profiles for sites on the Namoi River floodplain in south-east Australia, at different distances from the river.

- Overview
  - Dataset of mathematically modelled daily water saturation along vertical soil profiles (0–10 m depth) at six sites near the Namoi River, south-eastern Australia.
  - Based on the HaughFlow model, which predicts water movement in both the vadose and phreatic zones and couples vertical and lateral flow.
  - Outputs are daily time series of soil water saturation for each site, suitable for map-based visualization and GIS analysis.

- Data content and structure
  - Six sites at two locations: Old Mollee (50 m, 140 m, 320 m from river) and Yarral East (40 m, 110 m, 290 m from river).
  - Vertical profiles from soil surface to 10 m depth; depth axis across 0–10 m.
  - Water saturation is a proportion (0 to 1) with 7 decimal places.
  - Outputs: daily values; first column = date, first row = depth levels; 944 grid points across 10 m depth at half-grid intervals.
  - Data files correspond to figures in Evans et al. (2018): Figure6a–6f and Figure7b, with file names like Figure6a_OldMollee50m_WaterSaturation.csv, etc.

- Spatial and temporal details
  - Site coordinates (latitude, longitude in decimal degrees) and elevations (m AHD) provided for each site.
  - Time frames:
    - Old Mollee Figure 6 datasets: 01-Jul-2011 to 30-Jun-2015.
    - Yarral East Figure 6 datasets: 01-Jan-2013 to 30-Jun-2015.
    - Old Mollee Figure 7 dataset: 01-Jan-2004 to 31-Dec-2016 (different climate inputs).

- Model, calibration, and provenance
  - Governing equations: 1D vertical Richards equation (vadose zone) and 1D lateral Boussinesq equation (phreatic zone), two-way coupled.
  - Implementation: Fortran90 with tri-diagonal solver, predictor–corrector time stepping, centered finite differences spatially.
  - Inputs: river stage levels, climate parameters, and soil properties determine lateral/vertical inputs and flow speed.
  - Calibration: against water table data at Yarral East 290 m for 2013; calibrated soil properties include saturated hydraulic conductivity = 5.756 m/day and drainage = 0.01568 m/day.
  - Data linked to Evans, C.M., Dritschel, D.G., and Singer, M.B. (2018) Water Resources Research; part of a PhD project funded by NERC and the National Trust.

- Data formats and access
  - Outputs originally stored as unformatted files, converted to formatted CSVs for ease of use.
  - Depths in metres; water saturation in decimal form (0–1); dates in daily cadence.

- Site metadata
  - Two main locations with three distances each, giving spatial context for spatial analysis and mapping.
  - Lat/long and elevation provided per site to assist GIS integration and georeferencing.

- References
  - Evans, C.M., Dritschel, D.G., and Singer, M.B., 2018. Modelling subsurface hydrology in floodplains, Water Resources Research.