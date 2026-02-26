# A high-resolution global dataset of topographic index

## Overview
- Global high-resolution dataset of topographic index for use in large-scale hydrological modelling.
- The dataset’s single variable (topographic index) is designed as a topographic ancillary for TOPMODEL routing within the JULES land surface model.

## Data format and standards
- Format: NetCDF (one GIS data layer) in an archive; CF (Climate and Forecast) conventions.
- Archive/file naming: ga2_Global_15s_netcdf.zip containing ga2.nc.
- Size: 11.0 Gb.
- Resolution: 15 arc-seconds (global).
- Geographic scope: global extent.

## Dataset content
- The only variable is the topographic index itself.
- Calculated from the GA2 program using the standard algorithm with minor modifications for a global DEM.
- Directly comparable to the USGS HYDRO1k compound topographic index at 30-second resolution.

## Spatial information
- Corner coordinates:
  - Upper Left: (-180.0000000, 86.1000000)
  - Lower Left: (-180.0000000, -56.3541678)
  - Upper Right: (180.0000029, 86.1000000)
  - Lower Right: (180.0000029, -56.3541678)
- Center: (0.0000014, 14.8729161)

## Use and scope
- Intended as a topographic ancillary file for the TOPMODEL routing option within the JULES land surface model.

## Access and provenance
- Core file: ga2.nc within the ga2_Global_15s_netcdf.zip archive.
- Variable: topographic index (single variable in the file).

## Governance and stewardship considerations
- Metadata gaps to address: variable units, data provenance, processing steps, version, and licensing.
- Ensure complete metadata for discovery, reuse, and interoperability; document lineage and any modifications to the standard algorithm.
- Plan for handling and storing a large dataset (11 GB); ensure catalogue indexing and cross-referencing with HYDRO1k equivalence.