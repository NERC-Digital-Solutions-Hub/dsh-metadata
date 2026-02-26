# Fish abundance, habitat, water quality, flow and climate in English rivers 1975-2017 dataset

## Overview and purpose
- Time series dataset covering 1975–2017 for 1180 fish survey sites across English rivers.
- Combines fish abundance data with covariates on habitat, water quality, hydrology and climate.
- Open data product developed under the NERC ChemPop project to investigate whether chemical releases affect wildlife populations and how chemical effects compare to other drivers.
- Sources include Environment Agency’s National Fish Population Database (NFPD) and the University of Hull (UoH) population data, with additional habitat, water quality and environmental covariates.

## Data sources and components
- Primary fish data: EA National Fish Population Database (NFPD) for adult fish counts; juvenile data removed; densities computed to standardize sampling effort.
- Habitat data: River Habitat Survey (RHS) and HABSCORE habitat assessments (Atlantic salmon and brown trout) to estimate habitat quality and modification.
- Water quality: 41 determinands from the UK Water Quality Archive (WQ determinands) and LowFlows2000-WQX effluent dilution factor (EDF) modeled coverage.
- Hydrology and climate covariates: River flow statistics from NRFA; water temperature modeled from gauging stations and CHESS-Met meteorology; Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI).
- Land use and altitude: Land Cover Map 2015 processed into macro-categories upstream of each fish site; altitude derived from Integrated Hydrological Digital Terrain Model (IHDTM).

## Data integration and workflow
- Three main steps:
  - Spatially match surveyed locations along the river network; match RHS/HABSCORE data to nearest fish site within 5 km along the river.
  - Spatial/temporal integration of model-generated variables (e.g., EDF, land cover) with fish site locations.
  - Temporal alignment of covariates with fish survey dates (ecologically meaningful timeframes).
- Proximity-based matching governs pairing of fish sites with water quality, flow and habitat variables.
- Land cover data processed through rasterization, flow-direction alignment, and accumulation to upstream catchment scales.
- Water temperature modeled using GAMMs across seven BFI (baseflow index) ranges; best-performing GAMM (Model 1: month, time, and air temperature) selected per BFI interval.
- River flow statistics derived from NRFA gauging stations matched to fish sites via river-network distance; multiple temporal windows (3, 6, 12 months) calculated, including distributional and threshold metrics.

## Data completeness and data quality
- Covariates show varying completeness; some are 100% complete (e.g., altitude, land use, BFI, GSI, NAOI for corresponding records).
- Other covariates have missing matches due to temporal overlap, proximity, or data availability.
- 33 fish sites lack water quality data due to licensing restrictions (excluded from water quality data tables).
- Quality checks include distance thresholds (within 1 km acceptable) and sum-of-percentages near 100% for land cover categories upstream of each site.

## Data structure and files
- Five data file types created:
  - Species table: CP_Fish_SpeciesTable.csv (Fish_SpeciesCode, Latin_Name, EA_SpeciesCode, Common_Name)
  - Site variables by region: CP_Fish_SiteVariables_region.csv (location, habitat scores, altitude, land-use metrics, BFI, EDF statistics, etc.)
  - Data tables by region: CP_Fish_DataTable_region.csv (survey-level densities, locations, date, species codes, habitat scores, climate covariates)
  - Hydrology statistics by region: CP_Fish_HydrologyStats_Region.csv (flow metrics and various RF-related statistics)
  - Water-quality determinand statistics by region: Region_FISHWIMSStats_DET.csv (detailed determinand metrics and metadata)
- Determinands: 41 WQ determinands (A1) with LOQ handling and various summary statistics (min, max, median, mean, std; counts and LOQ considerations).
- Data sources and data provenance documented, including licensing restrictions and data ownership.

## Key variables and measurements
- Fish data: densities per 100 m^2 for each species, with species codes linking to the Fish_SpeciesTable.
- Habitat metrics: RHS (HMS, HQA, adjusted 1994 data) and HABSCORE-derived HQS for salmon and trout of various sizes.
- Land use: four macro-categories upstream of each site (Woodlands, Arable, Seminatural, Urban) with percentages and areas (km^2).
- Climate and hydrology: GSI, NAOI; Degree Days (cumulative days ≥12°C) for the prior year; EDF_Mean, EDF_Q90, EDF_Q95, EDF_SD; river flow statistics (mean, median, SD, CV, various quantiles), flow thresholds, exceedance metrics, patch lengths, and related durations.
- Water temperature: modeled time series per site across BFI ranges, converted to degree days for prior-year calculations.
- Water quality determinands: 41 chemicals with stats computed over antecedent periods (12 months prior to survey date) under multiple LOQ handling schemes.
- Altitude: two calculations derived from IHDTM (cell center value and bilinear-average of adjacent cells).
- Spatial matching metadata: nearest NRFA station or WQ determinand site used for linkage, with distance-based suitability checks.

## Data exclusions and caveats
- Some sites lack water quality data due to licensing restrictions (Appendix Table A2).
- Smaller wastewater treatment works may be omitted from EDF estimates; EDF values represent significant contributors to catchment DWF and assume a conservative emission scenario.
- LOQ handling options for water quality data provide multiple configurations due to measurement limits; users should select among LOQ configurations as needed.
- Data are regionally partitioned into seven regions (Anglian, Midlands, North East, North West, Thames, Southern, South West) for site-specific outputs.

## Data usage and accessibility
- Designed as an analysis-ready, open data product to support environmental data analyses and modelling.
- Data provenance and acknowledgments documented; licensing restrictions noted for certain water quality data.
- Files and metadata provide linkage between fish sites, survey dates, species, habitat, water quality, hydrology, and climate covariates to enable reproducible analyses.

## Acknowledgments and references
- Contributors spanning multiple institutions; funded under the NERC ChemPop project.
- References detail methodological foundations for habitat, fish recruitment, temperature modeling, flow analyses, and data integration approaches used in assembling the dataset.