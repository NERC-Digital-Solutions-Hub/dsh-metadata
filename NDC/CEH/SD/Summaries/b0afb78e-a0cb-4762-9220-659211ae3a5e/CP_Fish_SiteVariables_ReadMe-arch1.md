# CP_Fish_SiteVariables_readme.txt

## Overview
- Purpose: NFPD site variable data for fish sites in English rivers from 1975 to 2017.
- Content: Site-level covariate data that do not change over time, including habitat quality indicators (HQS and HMS) and physical site characteristics (altitude, land use, wastewater and Base Flow Index).
- Dataset context: Used to link fish site data with habitat and environmental covariates for analysis and modelling.

## Data structure and files
- Main region file: CP_Fish_SiteVariables_Region.csv containing information about individual NFPD fish sites (names, location, land use and habitat variables).
- Species reference: A single Species table indicating species referred to in Fish_SpeciesCode in data tables.
- Regional organization: Data and file structure are split by region (Anglian, Midlands, North East, North West, Thames, Southern, South West).
- Relationship: Fish_SiteID in the region file matches Fish_SiteID in DataTable files, Hydrology files, and chemical determinand files.
- File versioning: Multiple versions exist; notable update 2021-11-16 with subsequent changes on 2022-05-31 and 2022-08-12.

## Notable updates and version history
- Updated file: 20211116_HIFI_JuvenileFish_England_SiteTable
- Rationale for update: Removed site covariates HMS, HQS land use, and BFI from the data table and split into regional files.
- Update timelines: 2022-05-31 and 2022-08-12.

## Provenance and data sources
- Habitat quality indicators (HQA and HMS): Derived from River Habitat Survey (RHS) data; RHS sites were linked to the nearest fish site within 5 km of the river using ArcGIS tools.
  - RHS data source: https://www.data.gov.uk/dataset/4cb467c9-346e-44ac-85c66cd579111e2c/river-habitat-survey-survey-details-and-summary-results
- Altitude: CEH Integrated Hydrological Digital Terrain Model (IHDTM), 50 m gridded data, elevation (metres above sea level).
- Land use: CEH Land Cover Map 2015 (LCM2015); land cover categories pooled into four macro-categories.
  - LCM2015 source: CEH
- Base Flow Index (BFI): CEH National Flow Archive (upstream catchment baseflow data).
  - Source: nrfa.ceh.ac.uk
- Effluent Dilution Factor (EDF): Modeled from LF2000-WQX (LowFlows2000) to estimate wastewater contribution as a percentage of wastewater discharged by WWTWs.
  - Model details: Williams et al. 2009; regional application across England and Wales.
- Supporting references: Dawson et al. 2002; Gustard et al. 1992; Young et al. 2003; Williams et al. 2009.

## Methodology and data processing
- Data collection and linkage:
  - HQA/HMS: RHS habitat quality and modification scores, matched to the nearest fish site within 5 km; 1994 HQA data differ from later years, prompting new comparability protocols.
  - Land use: Upstream catchment land cover (21 categories) derived from LCM2015 and IHDTM; using GRASS GIS (r.accumulate) to create proportion/area metrics; later aggregated into four macro-categories: Woodlands, Arable, Sem natural, Urban.
  - Altitude: IHDTM elevation extracted for fish sites using ArcGIS; two values computed (cell-centre value and bilinear-interpolated average); the centre value used in the dataset.
  - EDF: LF2000-WQX model applied to model wastewater distributions; sites matched to the closest reach on the 1:50,000 river network; outputs include mean, standard deviation, 90th and 95th percentiles.
- Data processing steps:
  - HQA/HMS: RHS values retained as-is for matched sites; some sites may not be matched.
  - Land use: 21-class raster data processed in ArcGIS; accumulated rasters produced; percentages/areas summed to four macro-categories; consistency checks performed.
  - EDF: Python script linked each fish site to the closest LF2000-WQX reach; outputs stored as EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95.
  - Altitude: Elevation values extracted via IHDTM; NoData treated as 0 m for estuarine or below-sea-level areas.
- Software/tools required:
  - ArcGIS (10.6.1) for altitude extraction; ArcGIS Pro or later recommended for newer workflows.
  - GRASS GIS (r.accumulate) for land-use accumulation.
  - DataLabs for land-use extraction workflows.
  - Python for linking fish sites to LF2000-WQX network and computing EDF statistics.
- Quality assurance:
  - Distance checks between fish sites and nearest RHS points (acceptable if < 1 km).
  - Sum of macro-categorised land-use percentages checked to lie around 100% (99.96–100.04%).
  - EDF discrepancies flagged when a stretch of the river network is omitted; such sites have no data for wastewater metrics.
  - Data integrity checks for NoData handling (e.g., estuarine areas assigned 0 m elevation).

## Data-specific information for CP_Fish_SiteVariables_Region.csv
- Structure: Region-specific file with region-dependent rows/columns.
- Number of rows/columns: Variable by region.
- Number of variables: 18 (as stated in the document; the listed variable descriptions include more fields in practice).
- Key variables (as described in the Variable List):
  - Fish_SiteID: unique fish site identifier (Chempop project reference)
  - Fish_Name: site name
  - Fish_River: river/watercourse
  - Fish_Catchment: catchment/basin
  - Fish_Easting: easting coordinate
  - Fish_Northing: northing coordinate
  - HQA_Score: Habitat Quality Assessment score
  - HMS_Score: Habitat Modification Score
  - Fish_Altitude: site altitude (m above sea level)
  - LC_Woodland_Per: upstream woodland percentage
  - LC_Arable_Per: upstream arable percentage
  - LC_Seminatural_Per: upstream semi-natural percentage
  - LC_Urban_Per: upstream urban percentage
  - LC_Woodland_Area: upstream woodland area (km2)
  - LC_Arable_Area: upstream arable area (km2)
  - LC_Seminatural_Area: upstream semi-natural area (km2)
  - LC_Urban_Area: upstream urban area (km2)
  - BFI: Base Flow Index
  - EDF_Mean: mean effluent dilution factor
  - EDF_SD: standard deviation of EDF
  - EDF_Q90: 90th percentile of EDF
  - EDF_Q95: 95th percentile of EDF
  - ED_SITE_ID: site identifier for EDF data

## Practical use and context
- Intended for researchers and analysts combining site-specific covariates with hydrology, land use and wastewater factors to model fish site conditions and potential responses to environmental actions.
- Data linkages to hydrology, chemistry and habitat information enable multivariate analyses and the development of predictive models at regional scales.

## References
- Dawson, F. H., Hornby, D. D., and Hilton, J. (2002). A method for the automated extraction of environmental variables to help the classification of rivers in Britain. Aquatic Conservation: Marine and Freshwater Ecosystems, 12, 391-403. doi:10.1002/aqc.534
- Gustard, A., Bullock, A., Dixon, J. M. (1992). Low flow estimation in the United Kingdom. Institute of Hydrology.
- LC Map 2015 (UKCEH Land Cover Map 2015). https://catalogue.ceh.ac.uk
- Young, A.R., Grew, R., Holmes, M.G.R. (2003). Low Flows 2000: A national water resources assessment. Water Science and Technology.
- Williams, R.J. et al. (2009). A national risk assessment for intersex in fish arising from steroid oestrogens. Environmental Toxicology and Chemistry.