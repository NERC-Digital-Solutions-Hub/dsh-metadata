# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017.

## Overview
- Comprehensive dataset on fish abundance, habitat, water quality, hydrology, and climate for English rivers, spanning 1975–2017.
- Data collection and compilation occurred approximately 2019/04/03–2022/07/26; geographic focus is England.
- Funded by NERC Chempop (NE/S000100/2); authors include Ainsworth, Nunn, Bachiller-Jareno, Rizzo, Scarlett, Antoniou, and colleagues.
- Dataset published with formal citation and DOI via NERC EDS Environmental Information Data Centre.

## Access, licensing & publication
- Licensing: NFPD data and RHS are open; Crown copyright and database rights under government licence v3.0; additional data (Altitude, Land use, EDF) licensed by UKCEH.
- Publicly accessible locations: NFPD fish data (data.gov.uk), Land Cover Map 2015 (CEH), CEH IHDTM elevation data; cited publications provide context for EDF and related tools.
- Data citation: Ainsworth et al. 2024, Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e.

## Data structure & relationships
- File organization: Site and data tables are split by region (Anglian, Midlands, North East, North West, Thames, Southern, South West); a single Species table maps Fish_SpeciesCode to species.
- Core file: CP_Fish_SiteVariables_region.csv contains site-level covariates.
- Data relationship: Fish_SiteID links CP_Fish_SiteVariables_region.csv to DataTable files, Hydrology, and chemical determinand data.
- Versioning: A related file (20211116_HIFI_JuvenileFish_England_SiteTable) was updated; covariates (HQA, HMS, land use, BFI) were removed from the data table and split into regional site files. Updates occurred 2022-05-31 and 2022-08-12.

## Methodology & derived data
- Data sources and covariates:
  - HQA/HMS (RHS habitat scores) linked to the nearest fish site via ArcGIS IRN extension (within 5 km); RHS data from RHS survey results; HQA data from 1994 differs from later years, necessitating new comparability protocols.
  - Land use upstream of each fish site derived from CEH Land Cover Map 2015 (25 m); 21 land cover categories reclassified into four macro-categories (Woodland, Arable, Semi-natural, Urban) with both percentage and area upstream calculated.
  - Altitude (m above sea level) from CEH IHDTM 50 m, using center cell value and bilinear interpolation for surrounding values.
  - Base Flow Index (BFI) from CEH National Flow Archive, representing upstream flow characteristics.
  - Effluent Dilution Factor (EDF): modeled from LF2000-WQX to estimate percentage wastewater influence; site-level values include mean, SD, Q90, Q95.
- Processing steps:
  - RHS data for HQA/HMS are used as-is where matched; some sites may not have a suitable RHS match.
  - Land use calculations performed with ArcGIS GRASS r.accumulate; DataLabs used to extract upstream land use metrics.
  - EDF and altitude calculations rely on Python scripts and GIS tools; alignment to the 1:50,000 river network ensured via spatial matching.
- Standards & interpretation:
  - Software requirements: ArcGIS 10.7+ or ArcGIS Pro; GRASS GIS; DataLabs; Python 3.
  - Data interpretation requires GIS and Python-based workflows as described.
- Quality assurance:
  - Data checked by A. Nunn (14/07/2022).
  - Land use sums tested to be within 99.96–100.04% of total.
  - EDF data flagged as blank if river network matching failed; NoData cells handled as estuarine/sea-level elevation (0 m) where applicable.

## Data values, formats & instrumentation
- File: CP_Fish_SiteVariables_region.csv (regional variations; 18 variables per region).
- Variable examples:
  - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing
  - HQA_Score, HMS_Score
  - Fish_Altitude
  - LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per
  - LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area
  - BFI
  - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95
  - EDF_SITE_ID
- Missing data code: -9999.
- Interpretive note: Land cover/altitude data require ArcGIS (10.7+) or ArcGIS Pro; Land Use 2015 maps accessed via DataLabs; EDF requires Python 3 and the 1:50,000 river network.

## Data governance & stewardship considerations
- Provenance and transparency: Detailed methodological notes describe how each covariate was derived and linked to fish sites, including cross-dataset references.
- Licensing & reuse: Open data licenses for primary datasets; explicit citations and DOIs provided to facilitate reuse.
- Version control: Documented file updates and version changes; regional file splitting and covariate reallocation indicate careful version management.
- Metadata completeness: Comprehensive metadata covering collection dates, geographic scope, data sources, processing steps, QA, and software/tools required.
- Data discoverability: Data linked to public data portals (data.gov.uk, CEH catalogues) and DOI-based citation to support discoverability and reuse.
- Potential challenges to address for ongoing stewardship:
  - Incomplete or delayed data from RHS sources affecting timeliness.
  - Interoperability across regionally split files and multiple derived covariates.
  - Ensuring alignment of future updates with existing site identifiers and regional schemas.

## References & related resources
- Key methodological and data sources cited, including RHS River Habitat Survey details, CEH Land Cover Map 2015, IHDTM elevation, LowFlows2000-WQX model, and related publications.