# A high-resolution global dataset of topographic index

## Overview
- Global high-resolution dataset of the topographic index, produced with the GA2 program at 15 arc-second resolution.
- File intended as a topographic ancillary for the TOPMODEL routing model option within the JULES land surface model.
- One NetCDF data layer included in the archive; variable is the topographic index itself.
- Format adheres to CF conventions; named ga2_Global_15s_netcdf.zip and sized at about 11.0 Gb when uncompressed.
- Directly comparable to the compound topographic index from USGS HYDRO1k at 30 arc-seconds.

## Data details
- File: ga2_Global_15s_netcdf.zip
- Variable: topographic index (single variable in the file)
- Resolution: 15 arc-seconds
- Coverage: global, with corner coordinates spanning from -180 to 180 longitude and approximately -56.3541678 to 86.1 latitude
- Center: (0, 14.8729161)
- The index is calculated using the standard algorithm with minor modifications to align with a global DEM

## Corner coordinates
- Upper Left: (-180.0000000, 86.1000000)
- Lower Left: (-180.0000000, -56.3541678)
- Upper Right: (180.0000029, 86.1000000)
- Lower Right: (180.0000029, -56.3541678)
- Center: (0.0000014, 14.8729161)

## Formats and metadata
- NetCDF data layer; conforms to Climate and Forecast (CF) conventions
- Archive includes a single GIS data layer
- Metadata supports discoverability and reuse, with the dataset designed for integration into hydrological modelling workflows

## Use cases and applications
- Suitable as a topographic ancillary input for TOPMODEL routing in the JULES land surface model
- Useful for large-scale hydrological modelling and for cross-comparison with HYDRO1k topographic index (30 sec)
- Supports model parameterisation and sensitivity analyses where topographic index informs routing and runoff generation

## Practical considerations
- Size: 11.0 Gb when unzipped; requires substantial storage and bandwidth to download
- Polar coverage is limited to ~86.1 degrees latitude, with no data beyond that in the provided extent
- Contains only the topographic index variable, implying limited scope beyond routing/topography applications
- Data access may involve handling large NetCDF files and ensuring CF-compliant reading in analysis environments

## Implications for analysis
- Enables correlation analyses between topographic index and hydrological responses at a global scale
- Facilitates validation of TOPMODEL-based predictions within JULES or cross-model comparisons
- Offers a consistent, high-resolution topographic context for land-surface and hydrology research, with clear comparability to HYDRO1k benchmarks