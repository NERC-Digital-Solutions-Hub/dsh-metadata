# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## Overview
- GIS-based, map-focused dataset linking fish site information with habitat, land use, altitude and water quality covariates across English rivers.
- Combines site-level fish data with spatially derived covariates (land cover, altitude, baseflow, wastewater dilution) for analyses of abundance, habitat suitability, and environmental context.
- Data collection dates span approximate range 2019/04/03–2022/07/26; dataset covers historical records from 1975–2017.

## Data content and structure
- File structure:
  - Regional site and data tables split into regional files (Anglian, Midlands, North East, North West, Thames, Southern and South West).
  - Species table is a single, central file.
  - CP_Fish_SiteVariables_region.csv provides site-level information including location and covariates.
- Core relationships:
  - Fish_SiteID in site tables matches Fish_SiteID in DataTable files, Hydrology files, and chemical determinand files.
- File updates:
  - Updated dataset version in 2021: 20211116_HIFI_JuvenileFish_England_SiteTable.
  - Updates in 2022 split site covariates (HQA/HMS/land use/BFI) from data table into regional files; updated 2022-05-31 and 2022-08-12.

## Spatial and temporal scope
- Geographic focus: England (England rivers).
- Site and data alignment:
  - RHS (River Habitat Survey) habitat quality/ modification scores linked to closest fish site within 5 km along the river.
  - Land use and altitude covariates derived for upstream catchments of each fish site.
- Temporal coverage:
  - Fish site covariates and auxiliary data updated for years around 1994–2022; data product synthesizes long-term covariates with site data.

## Data sources and processing (methodology)
- Habitat data:
  - HQA (Habitat Quality Assessment) and HMS/HQS (Habitat Modification/Score) from RHS; matched to fish sites via ArcGIS IRN extension.
  - HQA data from 1994 differs from later years; recalibrated protocols applied for year-to-year comparability.
- Land use (upstream catchment):
  - 21 land cover categories from CEH Land Cover Map 2015 (LCM2015) at 25 m resolution.
  - Upstream catchment percentages/areas computed by GRASS GIS (r.accumulate) and DataLabs Python scripts; collapsed into four macro-categories: Woodland, Arable, Semnatural, Urban.
  - Upstream land use extracted for each fish site.
- Altitude:
  - CEH IHDTM 50 m elevation data; two values computed per site (cell-centre value and bilinear-interpolated average); centre value used in dataset.
- Baseflow and water quality covariates:
  - BFI (Base Flow Index) from CEH National Flow Archive.
  - EDF (Effluent Dilution Factor) derived from LF2000-WQX model; site-era wastewater percentage estimated via closest river reach matching; non-significant stretches result in blank EDF values.
- Data processing tools:
  - ArcGIS 10.7+ or ArcGIS Pro for land use and altitude extraction.
  - GRASS GIS for land-use accumulation rasters.
  - DataLabs for catchment-area calculations.
  - Python 3 for land use and EDF-related processing.
- Data calibration and QA:
  - Distances from fish points to RHS points checked; acceptable if <1 km.
  - Sum of macro-category percentages consistently ~100%.
  - EDF data left blank for mismatched river stretches; nodata handling noted.
  - Nodata cells treated as 0 m elevation only in estuarine/low data zones.

## Variables and data fields
- Core covariates (per Fish_SiteVariables_region.csv):
  - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing
  - HQA_Score, HMS_Score (habitat quality metrics)
  - Fish_Altitude
  - LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per
  - LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area
  - BFI
  - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95
  - ED_SITE_ID (effluent dilution site identifiers)
- Data structure:
  - Site and data tables are regional; Species table is central and single.
  - 18 variables in CP_Fish_SiteVariables_region.csv (region-dependent).

## Access, licenses, and related data
- Licensing:
  - NFPD data and RHS are open.
  - Crown copyright and database rights (EMOU206.2); usage for lawful purposes.
- Public data links:
  - NFPD fish data: data.gov.uk dataset link
  - Land cover map: CEH catalogue link
  - Altitude (IHDTM): CEH data portal
  - EDF/lowFlows resources cited in references
- Data and related datasets:
  - Ancillary datasets include site-level data, land use, altitude, and hydrological/EDF components.

## Software and interpretation notes
- GIS/software requirements:
  - ArcGIS 10.7+ or ArcGIS Pro for land use and altitude interpretation.
  - GRASS GIS for land-use accumulation processing.
  - DataLabs for catchment-based calculations.
  - Python 3 for land-use and EDF processing.
- Data interpretability:
  - Cohesive linkage between site-level fish data and spatial covariates enables spatial analyses of abundance vs. habitat and water quality factors.

## Usage guidance for GIS specialists
- integrate regional site tables with the central species table to build comprehensive maps of fish sites and covariates.
- exploit the 4 macro land-use categories to simplify landscape context around each site.
- use EDF_Mean/SD/Q90/Q95 to chart wastewater influence across reaches; note blank values where model fits are inapplicable.
- ensure ArcGIS/GRASS/DataLabs workflows align with the provided processing steps for reproducibility.
- consult the version history to identify updates that split covariates into regional files and removed redundant fields from the data table.