# A high-resolution global dataset of topographic index

## Overview
- A high-resolution global dataset of the topographic index intended for large-scale hydrological modelling.
- Single GIS data layer in NetCDF format, conforming to Climate and Forecast (CF) conventions.
- File ga2_Global_15s_netcdf.zip contains an 11.0 GB global layer produced from the GA2 program at 15 arc-second resolution.

## Data content and format
- The only variable in the file is the topographic index itself.
- Calculated using the standard algorithm with minor modifications for compatibility with a global DEM.
- NetCDF format with CF conventions to support interoperability and modelling workflows.

## Geographic scope and coordinates
- Global coverage with specified corner coordinates:
  - Upper Left: (-180.0000000, 86.1000000)
  - Lower Left: (-180.0000000, -56.3541678)
  - Upper Right: (180.0000029, 86.1000000)
  - Lower Right: (180.0000029, -56.3541678)
  - Center: (0.0000014, 14.8729161)

## Intended use and compatibility
- Intended as topographic ancillary data for TOPMODEL routing model option within the JULES land surface model.
- Directly comparable to the USGS HYDRO1k compound topographic index at 30 arc-second resolution, enabling benchmarking and cross-dataset comparability.

## Metadata, standards, and data quality
- Uses CF conventions and a standard topographic index algorithm with minor modifications for global DEM context.
- Only variable is the topographic index, facilitating focused use in hydrological modelling.
- Requires clear metadata to verify suitability for specific applications; potential barrier if metadata are incomplete or not publicly accessible.

## Access, sharing, and governance considerations
- Dataset is large (11.0 GB) and delivered as a ZIP of a NetCDF file, which has implications for storage, transfer, and data governance.
- Public sharing of underlying data is a consideration; ensuring provenance, versioning, and data management standards are in place is important.
- Metadata availability and clarity are critical to assess fit for purpose and to avoid silos or duplication across datasets.

## Relevance for monitoring frameworks (archetype perspective)
- Demonstrates the process of describing a high-value environmental data asset that can support policy monitoring and decision-making in hydrological and land-surface contexts.
- Highlights governance needs: metadata completeness, data standards (CF conventions), data provenance, and data sharing considerations for publicly funded datasets.
- Shows the importance of interoperability and benchmarking (comparability to HYDRO1k) to avoid duplication and enable cross-dataset synthesis in monitoring frameworks.
- Illustrates potential challenges for monitoring authors: large data volumes, access barriers, and ensuring data remain up-to-date and properly governed over time.