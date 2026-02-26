# Gridded flood frequency estimates for Kerala, India

- Purpose and audience
  - Six gridded datasets (ESRI ASCII) showing peak river flow with return periods of 2, 5, 10, 25, 50 and 100 years across Kerala’s river network.
  - Intended for engineers, policy makers, hydrology/engineering students, and GIS-based decision support.

- Data contents
  - Six files, each representing one return period.
  - Grid resolution: 15 arc-seconds on the WGS84 projection.
  - Extent: 74.90–77.37°E, 8.31–12.80°N.
  - File header (applies to all six):
    - NCOLS 593, NROWS 1076
    - XLLCORNER 74.8958, YLLCORNER 8.3125
    - CELLSIZE 0.0041667
    - NODATA_value -9999

- Data generation and methodology
  - Based on Central Water Commission (CWC) daily river flow products (2000–2020) from 23 stations.
  - Annual maxima extracted with quality control: exclude years with ≥30 missing days; keep stations with ≥5 annual maxima.
  - QMED (median of annual maxima) estimated via linear regression with LASSO using catchment descriptors from HydroSHEDS, FAO Harmonised World Soil Database, and IMD rainfall grids.
  - QMED extended to 318 sites; residuals added via top-kriging (rtop) for spatial consistency.
  - Regional growth curves for higher return periods derived using GEV distribution (Hosking-Wallis test to select model).
  - Site-specific QMED used to scale to true T-year estimates (lmomRFA).
  - Validation facilitated by use of established CRAN packages, supporting reproducibility.

- Data sources and alignment
  - Data tied to the HydroRIVERS river network shapefile, regridded to match the 15-arc-second HydroSHEDS grid.
  - Data aligned to an existing GIS framework to enable integration with other spatial datasets.

- Quality control
  - Pre-screening by CWC; years with insufficient data excluded.
  - Use of validated CRAN packages to ensure robust, repeatable outputs.

- Licensing and access
  - Open Government Licence; dataset downloadable from the provided DOI.
  - Users must cite Griffin, Vesuviano, and Cole (2022) in the NERC Environmental Information Data Centre.

- Context and funding
  - Delivered as part of the LAWIS project under UKRI National Capability.
  - Builds on prior work (e.g., SUNRISE in Maharashtra) to provide accessible flood-frequency estimates for engineers, policymakers, and students.

- Authors and funding
  - Authors: Adam Griffin, Gianni Vesuviano, Steven Cole (UKCEH).
  - Funders: LAWIS project, UKRI/NERC National Capability.