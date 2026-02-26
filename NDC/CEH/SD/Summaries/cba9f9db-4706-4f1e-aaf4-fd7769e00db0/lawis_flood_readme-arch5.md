# Gridded flood frequency estimates for Kerala, India

## Overview
- A set of six gridded datasets providing estimates of peak river flow with return periods of 2, 5, 10, 25, 50 and 100 years across the Kerala river network.
- Based on annual maxima extracted from Central Water Commission daily river flow products for 23 stations in Kerala, 2000–2020.
- Generated to support engineers, policymakers, and hydrology/engineering students with easily accessible flood frequency estimates; produced under the LAWIS project funded by UKRI/NERC National Capability.
- Data sharing and discovery facilitated via an Open Government Licence with a formal citation requirement.

## Data content and methodology
- Data format and structure:
  - Six ESRI ASCII grid files, each corresponding to a return period (2, 5, 10, 25, 50, 100 years).
  - Grids represent peak daily river flow magnitudes in cubic metres per second (m3 s-1).
  - Grid header example: NCOLS 593, NROWS 1076, XLLCORNER 74.8958, YLLCORNER 8.3125, CELLSIZE 0.0041667, NODATA_value -9999.
  - Projection: WGS 84, 15-arc-second resolution; extent 74.90–77.37 E, 8.31–12.80 N.
  - Data modeled for the river network, based on HydroRIVERS, and converted to a grid aligned with HydroSHEDS.
- Data collection and generation:
  - Annual maxima from 23 stations used after quality screening (years with fewer than 30 missing days excluded; stations with at least 5 annual maxima retained).
  - Flood frequency estimation approach:
    - QMED (median of annual maxima) estimated via linear regression with LASSO using catchment descriptors from HydroSHEDS, GAEZ, and IMD rainfall products.
    - QMED extended to 318 sites using the catchment-descriptor equation plus a top-kriging residual to maintain spatial consistency.
    - For non-annual-maxima return periods, regional growth curves derived from the GEV distribution (selected via Hosking-Wallis test) and scaled to true T-year values using site-specific QMED and lmomRFA-based methods.
- Provenance and tools:
  - Uses pre-existing CRAN packages, which supports perceived quality and reproducibility.
  - Ground-truthing and data alignment draw on CWC data, HydroRIVERS, and HydroSHEDS-derived inputs.
  - Documentation and methods place the work within the LAWIS and broader UKRI-NERC National Capability program.

## Access, licensing and citation
- Licensing: Open Government Licence; dataset downloadable from the provided DOI.
- Citation requirements: Grifi n, A.; Vesuviano, G.; Cole, S. (2022). Gridded flood frequency estimates for Kerala, India. NERC Environmental Information Data Centre. (Dataset). DOI provided.
- Usage notes: Users must adhere to the licence terms and cite the dataset as specified.

## Data governance, ownership and maintenance
- Authors and affiliations: Adam Griffin, Gianni Vesuviano, Steven Cole (UKCEH).
- Funders and program: LAWIS project funded by UKRI/NERC National Capability.
- Data management considerations:
  - Clear metadata and structure are provided (grid dimensions, coordinates, resolution, and nodata value).
  - Data are explicitly limited to the Kerala river network, with gridded outputs intended for practical use by engineers and policymakers.
  - Updates and future maintenance are not specified; current dataset covers 2000–2020 and may require renewal for new data beyond that period.

## Limitations and scope
- Spatial scope restricted to the river network; other hydrological contexts not included.
- Temporal scope limited to annual maxima data from 2000–2020; future updates would be needed to cover additional years.
- File format is ESRI ASCII grids, which are widely supported but may require conversion for some workflows.

## Usage guidance and caveats
- Appropriate for planning, policy development, and educational purposes related to flood frequency in Kerala.
- Ensure proper citation and acknowledgment of sources; comply with the Open Government Licence terms.
- Be mindful of the data’s coverage limitations (river network only) and the temporal window when applying to current planning scenarios.