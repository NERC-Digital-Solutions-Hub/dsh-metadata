# High-resolution hydraulic parameter maps for surface soils in tropical South America

## Overview
- Six sets of files offering high-resolution parameter maps for surface soils in tropical South America.
- Designed to support soil hydraulic modeling in land surface models by providing key soil hydraulic parameters derived from pedotransfer functions (PTFs) using soil profile data.

## Data content and formats
- Parameter maps for all soil quantities available as raster GeoTIFF and NetCDF formats at 15 arc-sec resolution (about 450 m at the equator).
- NetCDF files follow Climate and Forecast (CF) conventions to ensure interoperability.
- Data package includes three PTF families:
  - Cosby et al. (CosbyB, Cosbyλ, Cosbypsiem, CosbypsiePa, Cosbythsat, Cosbyksat)
  - Hodnett & Tomasella (HT) parameter set (HTalphaperm, HTaphaperPa, HTn, HTthres, HTthsat)
  - Tomasella & Hodnett (TH) parameter set (THB, THλ, THpsiem, THpsiePa, THthres, THthsat)

## Variables and parameterizations
- Core variables (Cosby-based and general ocean/soil parameters):
  - λ (dimensionless)
  - B (= 1/λ)
  - Air-entry (bubbling) pressure ψe (Pa or m pressure head)
  - Saturated soil water content θsat (cm³/cm³)
  - Saturated soil hydraulic conductivity ksat (mm/s)
- Additional tropical PTF parameters (HT/TH families):
  - n (dimensionless)
  - α (1/m or 1/Pa)
  - θsat and θres (residual water content)

## Data structure and access
- Data are provided in a zip archive containing:
  - geotiff.Cosby*, netcdf.Cosby* files (Cosby parameterization)
  - geotiff.HT*, netcdf.HT* files (HT parameterization)
  - geotiff.TH*, netcdf.TH* files (TH parameterization)
- Each file group includes the corresponding parameter fields (e.g., CosbyB, Cosbyλ, Cosbypsiem, CosbypsiePa, Cosbythsat, Cosbyksat; and analogous fields for HT and TH).
- References for the standard parameters and methods:
  - Marshall et al. (1996)
  - Marthews et al. (2014)
  - Hodnett & Tomasella (2002)
  - Tomasella & Hodnett (1998)
  - Cosby et al. (1984)

## Significance for data management and practice
- Enables high-resolution, interoperable data products suitable for integration into land surface models and interdisciplinary analyses.
- CF-compliant NetCDF and GeoTIFF formats support discoverability, reuse, and cross-platform compatibility.
- Documented parameterizations (Cosby, HT, TH) provide methodological transparency and options for sensitivity analyses and model comparisons.

## Implications and considerations for Data Leaders
- Data governance: ensure comprehensive metadata and clear documentation of each parameterization, variable definitions, and file naming conventions to support discoverability and reuse.
- Data quality and standards: align with established PTF references and maintain consistency across Cosby, HT, and TH datasets; monitor for metadata clarity on units and parameter roles.
- User needs and co-ownership: enable policy and research teams to access parameter maps that integrate with their soil and hydrological analyses; foster collaboration across networks using standardized CF-compliant NetCDF files.
- Data interoperability: CF-compliant NetCDF enhances cross-system interoperability; maintain versioning and changelogs to track updates or corrections.
- Access and coordination: coordinate with partners to manage data distribution, licensing, and potential expansions (additional regions or resolutions) while minimizing duplication of effort.