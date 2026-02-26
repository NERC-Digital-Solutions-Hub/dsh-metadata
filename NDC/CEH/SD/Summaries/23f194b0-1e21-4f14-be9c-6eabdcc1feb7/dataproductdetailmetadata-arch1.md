# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

## Overview
- Open data product combining macroinvertebrate taxonomic abundance for 1,519 monitoring sites across English rivers (1965–2018) with 41 water quality determinands, river flow, and air temperature derived values.
- Includes static site descriptors (e.g., wastewater dilution factor, habitat quality, upstream land cover, altitude, slope, channel metrics).
- Developed under the ChemPop project to enable environmental data and modelling analyses; harmonised from diverse EA and UKCEH datasets with quality checks and documentation.

## Context and Rationale
- Macroinvertebrates as indicators: rapid responses to chemical and other environmental stressors due to short lifespans.
- Long-term monitoring (1960s–present) provides a robust resource for studying chemical pollution impacts on freshwater biota beyond lab settings.
- Data assembled to investigate links between chemical exposure, habitat, climate, land cover, and macroinvertebrate communities.

## Data Sources and Integration
- Macroinvertebrate time series: Freshwater river macroinvertebrate surveys (FRMS) from Environment Agency Biosys (EA).
- Water quality: 41 determinands from EA Water Quality Data Archive (and pre-2000 licensed EA data).
- River flow: Mean gauged daily flow from NRFA (NRFA/EA data).
- Air temperature: CHESS-met daily meteorological data (Great Britain; 1961–2017).
- Wastewater exposure: EDF (effluent dilution factor) derived from LF2000-WQX model (LF2000 extension for water quality).
- Habitat and landscape context: River Habitat Survey (RHS) indices; Land Cover Map 2015 (LCM2015); Integrated Hydrological Digital Terrain Model (IHDTM) for catchment delineation.
- River network and spatial framework: UKCEH digital river network (1:50,000), with network-based matching and flow direction grids.

## Methodology and Data Processing

### 3.1 Data Integration Approach
- Three-step workflow:
  - Spatial matching: pair macroinvertebrate sampling sites with nearest water quality, river flow, and RHS survey sites along the river network.
  - Spatial integration: extract modelled/analysed variables (EDF, land cover, air temperature) at macroinvertebrate-site locations.
  - Temporal matching: align time-series environmental data to the macroinvertebrate sampling dates using a 6-month look-back window.

### 3.1.1 Data Sources and Linkages
- BIO time series: 1,519 sites across EA regions.
- Water quality: 41 determinands; data from 2000 onward (plus pre-2000 licensed EA dataset).
- River flow: daily mean flows from NRFA; matching based on proximity along river network.
- EDF: model-derived percent wastewater per site from LF2000-WQX; notes on WWTW coverage and potential headwater limitations.
- Air temperature: CHESS-met time series matched to site locations; final CHESS-met series ends 2017.
- Habitat: RHS indices (HMS, HMS_Class, RHS_RSB_SubScore, HQA, HQA_ADJ) matched to macroinvertebrate sites within 5 km along river.
- Land cover: upstream catchment percentages and areas for woodland, arable, seminatural, urban derived from LCM2015; catchments delineated via IHDTM flow accumulation.

### 3.1.2 Data Matching and Processing Details
- Spatial matching based on river-network proximity; macroinvertebrate sites linked to nearest WQ, RF, and RHS sites.
- Temporal aggregation:
  - Water quality, river flow, and air temperature: aggregated over the 6 months preceding each macroinvertebrate sampling date.
- Data handling and QA:
  - FRMS data cleaned to address duplicates, incorrect site IDs, taxonomic name changes (mapped to Davies & Edwards 2011 standard; added family/order columns).
  - Land cover treated as static due to resource constraints and methodological consistency concerns.
  - Land cover and EDF data ensured for all sites; some EDF mismatches noted due to truncated vs full river networks.

### 3.3 Effluent Dilution Factor (EDF)
- EDF linked macroinvertebrate sites to a modeled wastewater exposure proxy using LF2000-WQX.
- EDF values provided as mean, standard deviation, and 90th/95th percentiles; stipulations about headwater WWTW inclusion and 0 values indicating <5% contribution.

### 3.4 Water Quality Chemistry Determinants
- 41 determinands extracted for water quality sites matched to macroinvertebrate sites.
- Six-month period statistics calculated per macroinvertebrate sampling date:
  - Minimum, maximum, median, mean, standard deviation (sample SD).
  - Counts of total samples, samples below LoQ, samples above upper quantification limit.
- Handling of LoQ:
  - Three configurations for values below LoQ (LoQ, 0, LoQ/2) applied to compute statistics.
- Data processing: Python-based workflow; regional processing using Linux and ArcGIS for site matching.

### 3.5 River Flow
- River flow statistics calculated for both the entire period of interest (POI; 20/05/1974–29/03/2019) and the 6-month preceding each macroinvertebrate date.
- Statistics include mean, median, SD, coefficient of variation, Q5/mean, Q95/mean, plus detailed exceedance metrics (number of days exceeding thresholds, number of exceedances, average patch length) for multiple quantiles (5th, 25th, 75th, 95th).
- Nearest gauging station matching along the river network with manual verification.

### 3.6 Air Temperature
- CHESS-met daily mean air temperature at macroinvertebrate site locations (converted to °C).
- 6-month statistics computed (mean, median, min, max, SD).
- CHESS-met ends in 2017, limiting post-2017 site temperature pairing.

### 3.7 Habitat Quality Indices
- RHS metrics linked to macroinvertebrate sites:
  - Habitat Modification Score (HMS) and Class (HMS_Class)
  - Resectioned Bank/Bed Sub-Score (RSB_SubScore)
  - Habitat Quality Assessment Score (HQA) and Adjusted (HQA_ADJ)
- RHS data is cross-sectional (single survey per site), with some sites having multiple RHS surveys.

### 3.8 Land Cover
- Upstream catchment land cover: woodland, arable, seminatural, urban (percent and area in km2) derived from LCM2015.
- Processing: rasterized 50 m cells aligned to IHDTM flow grid; accumulated upstream proportions computed; 21 original classes aggregated to four broad categories.
- Validation: distance to IHDTM cell < 1 km; cumulative land cover sums within 99.96–100.04%.

### 4. Data Files and Accessibility

- 4.1 Site descriptors
  - CP_<REGION>_MInv_siteVariables.csv for each EA region (1519 records total).
  - Columns include BIO_SITE_ID, altitude, slope, distance from source, discharge, width, depth, substrate cover (%), EDF mean/quantiles, and related metrics.

- 4.2 Data product time-series files
  - 4.2.1 Macroinvertebrate taxon abundance
    - CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv
  - 4.2.2 Water quality determinand statistics
    - CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv (41 determinands across regions)
  - 4.2.3 River flow statistics
    - CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv
  - 4.2.4 Air temperature statistics
    - CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv

- 4.3 Site locations
  - CP_<REGION>_MInv_siteMatchedLocation.csv linking macroinvertebrate sites to matched water quality, river flow, RHS sites with coordinates and identifiers.

- 4.4 Additional RHS data
  - SiteswithmultipleRHSsurveys.csv for sites with more than one RHS survey.

- 4.5 Data notes
  - NA handling guidance and data type considerations for reading CSVs (e.g., use NA recognition in Python).

## Data Quality, Limitations, and Considerations
- Gaps and missing data:
  - Inevitable gaps (noData) in many variables due to non-overlapping records across datasets and temporal scope.
  - Some water quality matches excluded due to EA licensing restrictions; a few matched WQ sites lacked actual data due to extraction failures.
- Data standardisation and historical variation:
  - Early macroinvertebrate data often semi-quantitative or recorded at family level; full quantification began post-2002 with taxon naming changes addressed via taxonomic reference mapping.
  - Land cover harmonisation across time is limited; land cover treated as static due to resource demands.
- Temporal coverage constraints:
  - CHESS-met ends in 2017, limiting post-2017 air temperature matching.
- EDF caveats:
  - EDF values reflect modelled network-wide wastewater contributions; 0 values may not be true zeros in headwater streams due to excluded small WWTWs.
- Data processing decisions:
  - Land cover and some modelled variables are site descriptors rather than time-variant measurements; spatial matching prioritises nearest-neighbor philosophy along river networks.

## Usage and Citation Guidance
- Data are provided to support correlation analyses, model development, and hypothesis testing linking macroinvertebrate communities with water quality, flow, temperature, and habitat variables.
- Users should consult the methodological overview (Sections 3.x) and appendices for data processing choices, LoQ handling, and QA steps.
- Proper citations: ChemPop project outputs and underlying datasets (EA Biosys, Water Quality Archive, NRFA, CHESS-met, LF2000-WQX, RHS, LCM2015, IHDTM, River Network).

## Notes on Appendices and Visualizations
- Appendix 1 lists the 41 water quality determinands and their naming/units.
- Appendix 4 provides heatmaps illustrating temporal data completeness and coverage for each covariate by EA region (useful for assessing data gaps prior to analyses).

## Author Contributions and Acknowledgements
- Developed data analysis protocols, data management, validation, and documentation; acknowledged EA, UKCEH, NRFA data providers and project funders (NERC/NE).