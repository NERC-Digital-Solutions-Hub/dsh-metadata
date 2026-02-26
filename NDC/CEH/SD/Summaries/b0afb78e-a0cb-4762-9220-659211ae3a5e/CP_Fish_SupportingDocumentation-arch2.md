# Fish abundance, habitat, water quality, flow and climate in English rivers 1975-2017

- Time series dataset covering 1180 fish sites in English rivers from 1975 to 2017.
- Focuses on species-specific fish abundances and a wide set of covariates to explain population trends and environmental health.
- Developed as part of the NERC ChemPop project (open data product) to assess whether chemical releases affect wildlife and how chemical effects compare with other drivers.
- Aims to enable analysis of environmental health and policy performance over time using a consistent, interpretable format.

## Data sources and components

- Environment Agency National Fish Population Database (NFPD) for adult and juvenile fish counts; processed into densities.
- University of Hull (UoH) HABSCORE data; River Habitat Survey (RHS) data; Habitat Quality (HQA) and Habitat Modification Scores (HMS).
- Water quality data from the UK Water Quality Archive (EA) for 41 determinands; supplemented with in-house UKCEH data for earlier years.
- Effluent Dilution Factor (EDF) estimates from LF2000-WQX model to represent wastewater influence on reaches.
- Climate and hydrology covariates:
  - Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI) as climate drivers.
  - Water temperature modeled by GAMMs using gauged stations and CHESS-Met air temperatures, with consideration of Base Flow Index (BFI) to account for groundwater influence.
  - River flow statistics from the National River Flow Archive (NRFA) and NRFA gauging stations.
- Land cover data derived from Land Cover Map 2015 (LCM2015) and the Integrated Hydrological Digital Terrain Model (IHDTM).
- Geographic and altitude data from IHDTM.
- Data integration sources span seven regional areas: Anglian, Midlands, North East, North West, Thames, Southern, South West.

## Data integration and methods

- Spatial and temporal integration:
  - Fish site locations are spatially matched to RHS, WQ determinand sites, river flow gauging stations, and RHS/HABSCORE data using river-network proximity criteria (nearest within 5 km along the river).
  - Model-generated variables (EDF, land cover) linked to fish sites via river-network locations.
  - Temporal matching aligns covariates to ecologically meaningful windows around each fish survey date.
- Adult fish abundance processing:
  - NFPD survey records converted to densities (numbers per 100 m2), excluding juvenile-only sites and qualitative datasets.
  - Handling of uncertain counts (e.g., 1-9, 10-99) via midpoints; “Present” treated as 1; various suffixes handled per established conventions.
- Habitat and habitat quality:
  - RHS and HABSCORE data extracted for fish sites; RHS data matched to nearest fish site; HMS/HQA scores assigned accordingly.
- Water temperature:
  - Seven GAMMs developed across 0.1-BFI ranges to predict site-specific water temperatures based on Air Temperature (CHESS-Met) and time-related covariates; cumulative degree days (≥12°C) computed for the year preceding each survey.
- River flow:
  - NRFA daily flow data linked to nearest survey site along the river network; statistics computed for the full period and thresholds for 3-, 6-, 12-month windows preceding surveys.
- EDF and water quality:
  - EDF estimates derived by linking fish sites to the closest reach on a modelled river network (discarding non-representative sites); EDF outputs include mean, SD, and high-percentile values.
  - Water quality determinands (41 chemicals) matched to fish sites from a subset of determinand sites with sufficient data and appropriate hydrological relationships; multiple matching criteria to ensure representativeness.
  - For each matched determinand/date, statistics calculated for the antecedent 12 months, with LOQ handling (LoQ imputation strategies) and maximum concentration thresholds where applicable.
- Data quality and exclusions:
  - 33 fish sites excluded from water quality data due to licensing restrictions.
  - Quality checks include distance thresholds (<1 km) for matching, and precise aggregation checks for land-cover percentages.

## Key variables and covariates

- Fish data:
  - Species codes, Latin/Common names, EA species codes.
  - Fish site locations, densities (per 100 m2) by survey date.
  - Habitat-related covariates: HQA, HMS, RHS scores; HABSCORE-derived densities for salmon/trout where available.
- Covariates and derived metrics:
  - Land cover macro-categories upstream of each fish site (Woodlands, Arable, Seminatural, Urban) and corresponding areas.
  - Base Flow Index (BFI) for groundwater influence and categorization (used in water temperature modelling).
  - Water temperature: Degree Days (cumulative ≥12°C) prior to survey date.
  - EDF: EDF_Mean, EDF_Q90, EDF_Q95, EDF_SD; site-level EDF with per-reach estimates.
  - Water quality determinands: 41 chemicals with LOQ handling, including min/max/median/mean/SD over antecedent period, counts below/above LOQ, and related metrics.
  - Climate indices: Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI).
  - Altitude/elevation for fish sites.
  - River flow statistics: mean, median, SD, coefficient of variation, quantile-based thresholds (5/25/75/95 percentile) for 3, 6, and 12 months preceding surveys; duration and frequency of exceedance events; patch-level metrics.
  - Hydrology-derived variables: 3M/6M/12M exceedance metrics, patch lengths, and related durations.
- Data structure:
  - Five data file types: species table (CP_Fish_SpeciesTable.csv), site variables by region (CP_Fish_SiteVariables_region.csv), data tables by region (CP_Fish_DataTable_region.csv), water quality determinand data tables (Region_FISHWIMSStats_DET.csv), and hydrology data tables (CP_Fish_HydrologyStats_Region.csv).

## Coverage, completeness, and limitations

- Regional and site coverage:
  - Data compiled across Anglian, Midlands, North East, North West, Thames, Southern, and South West regions; totals include >1180 fish sites and numerous matched covariate points.
- Completeness:
  - Covariates such as altitude, land use, BFI, GSI, and NAOI show complete data for all surveys; other covariates have gaps due to non-overlapping time periods or unsuitable site proximity.
- Data gaps and exclusions:
  - Some covariates could not be matched to certain fish surveys; 33 fish sites lack water quality data due to licensing restrictions and are excluded from WQ components.
- Standardisation challenges:
  - Data originate from multiple sources with varying formats and purposes; the final dataset retains gaps (noData instances) but adds value by integrating diverse sources for broad analyses.
- Modelling assumptions:
  - EDF is based on modeled wastewater distributions and assumes representative coverage of significant wastewater treatment works; smaller works may be omitted.
  - Water temperature modelling uses GAMMs with BFI stratification; predictions depend on model choices and available gauging data.

## Data access and usage

- Open data product intended for broad use in environmental data analyses and modelling.
- Cited sources and datasets include EA/NFPD data, HABSCORE, RHS, WQ Archive, EDF modelling, CHESS-MET, NRFA, GSI, and NAOI, with acknowledgments to funders (NERC) and data providers.
- Documentation and methodological details (including data processing steps, matching criteria, and data tables) provided to support reproducibility and reuse.

## Acknowledgments and references

- Acknowledges contributions from dataset authors, data providers (EA, UKCEH, NRFA, CHESS-MET), and funding support (NERC).
- References include key methodological and data sources used to construct the Chempop dataset and related modelling approaches.