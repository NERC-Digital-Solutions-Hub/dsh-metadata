# Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017

## Overview
- Dataset documenting fish abundance, habitat, water quality, flow, and climate variables for English rivers, covering 1975-2017, with data collection around 2019-04-03 to 2022-07-26.
- Authors include Ainsworth, Nunn, Bachiller-Jareno, Rizzo, Scarlett, Antoniou, and colleagues; funded by NERC Chempop.
- Purpose aligned with environmental health monitoring to support policy scrutiny, evaluation, and future decision-making.
- Licensing: NFPD data and RHS are open; Crown copyright; links to licenses and related data sources provided.
- Citation: DOI and dataset title provided for Environmental Information Data Centre (EIDC).

## Data and access
- Files: CP_Fish_SiteVariables_region.csv contains site-level covariates; data are organized as regional files (Anglian, Midlands, North East, North West, Thames, Southern, South West).
- Data relationships: Fish_SiteID matches across SiteVariables, DataTable, Hydrology, and chemical determinand files.
- Related datasets used in construction: Land Cover Map 2015 (LCM2015), CEH IHDTM altitude data, EDF/LF2000-WQX model outputs, Base Flow Index (BFI).
- Access and reuse: Data linked to public portals (data.gov.uk, CEH Atlas) and NERC EIDC citation; underlying data intended to be openly shared where possible.

## Data structure and content
- Primary file: CP_Fish_SiteVariables_region.csv with 18 variables (region-dependent); site-level covariates include:
  - Fish_SiteID, Fish_Name, Fish_River, Fish_Catchment, Fish_Easting, Fish_Northing
  - HQA_Score, HMS_Score (habitat quality indicators)
  - Fish_Altitude (meters above sea level)
  - LC_Woodland_Per, LC_Arable_Per, LC_Seminatural_Per, LC_Urban_Per (land use percentages upstream)
  - LC_Woodland_Area, LC_Arable_Area, LC_Seminatural_Area, LC_Urban_Area (land use areas upstream)
  - BFI (Base Flow Index)
  - EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95 (effluent dilution factors)
  - ED_SITE_ID (effluent dilution factor site identifiers)
- Relationship: Fish_SiteID in CP_Fish_SiteVariables_region.csv links to DataTable and other related files.
- Versioning: Noted update 20211116_HIFI_JuvenileFish_England_SiteTable; reasons include restructuring of data tables and removal of some covariates from the main data table into regional files; updates occurred 2022-05-31 and 2022-08-12.

## Methods and data provenance
- Data sources and covariates:
  - HQA and HMS: RHS-derived habitat quality and modification scores joined to fish sites via nearest RHS site within 5 km; 1994 RHS data differ from later years; cross-year comparability protocols developed.
  - Land use: Upstream catchment land cover derived from CEH LCM2015; 21 categories collapsed into four macro-categories (Woodland, Arable, Semi-natural, Urban); upstream proportions/areas calculated using GRASS GIS and DataLab extraction.
  - Altitude: Elevation extracted from CEH IHDTM 50 m grid; two approaches computed, with preference for cell-centre value.
  - BFI: Base Flow Index sourced from CEH/National Flow Archive.
  - EDF: Wastewater influence estimated with LowFlows2000-WQX model; percentage wastewater assigned to each fish site via nearest river network reach; outputs include mean, SD, Q90, Q95.
- Data processing:
  - RHS-derived scores (HQA/HMS/HQ_S) used as-is for most sites; some sites could not be matched to RHS data.
  - Land use calculations performed with 21 categories aggregated to four macro-categories; upstream catchment metrics computed per site.
  - EDF values computed by linking sites to LF2000-WQX network and assigning model outputs; discrepancies flagged and left as no data.
  - Elevation data handled with NoData treated as estuarine or below sea level with 0 m elevation.
- Quality assurance:
  - Site matching: RHS site within 5 km; distance checks ensuring acceptable matches (<1 km for points used).
  - Land use sums: macro-category percentages sum to ~100% (99.96–100.04%), indicating precise aggregation.
  - EDF handling: missing EDF values flagged when river network mismatch occurred.
  - Documentation of data provenance and cross-checks by Nunn, A. (14/07/2022).

## Instrumentation, software and standards
- Software/tools required:
  - ArcGIS (10.6.1 to 10.7 or later) for elevation and land-use extraction.
  - GRASS GIS (r.accumulate) for land-use accumulation rasters.
  - DataLab for extracting land-use area/percentages.
  - Python 3 for land-use and EDF data processing.
  - LF2000-WQX model outputs require interpretation of EDF statistics.
- Standards and calibration:
  - Specific calibration details are not broadly documented; emphasis is on reproducible GIS and modeling workflows.
- Data governance and openness:
  - Underlying datasets intended for public sharing; data governance considerations noted, including how to handle sensitive or restricted data.

## Data quality, limitations, and caveats
- Coverage and gaps:
  - Some RHS sites could not be matched to fish sites; 1994 HQA data differ from later years, necessitating new comparators for temporal analyses.
  - EDF data may be blank where river network matching or model application was not feasible.
- Data granularity and transformation:
  - Land use is derived from 2015 land cover data and aggregated to four macro-categories; potential discrepancies with site-specific catchments.
  Potential interpretation considerations for policymakers:
  - Cross-year comparability requires applying the described harmonization protocols.
  - Regional file structure means careful joining by Fish_SiteID when aggregating across regions.

## Data usage, licenses and citation
- Licensing: NFPD data and RHS are open; Crown copyright and database rights.
- References and sources cited within the dataset metadata (e.g., Dawon 2002; Gustard et al. 1992; Young et al. 2003; Williams et al. 2009) relevant to methods (RHS, LF2000-WQX, IHDTM, LCM2015).
- Citation: Ainsworth et al. (2024) Fish abundance, habitat, water quality, flow and climate data from English rivers,1975-2017. NERC EDS Environmental Information Data Centre. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## Supporting information and references
- Links to ancillary data: NFPD fish data, CEH land cover map, IHDTM elevation, LF2000-WQX model outputs.
- Key methodological references provided for replication and understanding of RHS matching, low-flow/water-quality modeling, and land-cover derivation.