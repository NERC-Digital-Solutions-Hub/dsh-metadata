# Fish abundance, habitat, water quality, flow and climate in English rivers 1975-2017

- A time-series dataset detailing species-specific fish abundances and a suite of environmental covariates across 1180 English river sites from 1975 to 2017.
- Built from two major sources: Environment Agency’s National Fish Population Database (NFPD) and University of Hull (UoH) fish population data; developed as part of the NERC ChemPop project to examine whether chemical releases affect wildlife populations in rivers.
- Open data product intended for broad environmental data and modelling analyses; aims to help disentangle chemical impacts from other drivers of fish population dynamics.

## Scope and purpose

- Covers adult fish abundances (juvenile data removed) and associated covariates to relate demographic changes to predicted chemical exposure.
- Focuses on addressing whether chemical releases affect wildlife populations and how such effects compare to other factors.
- Uses fish data to infer ecological responses, with fish biomass/density expressed per area (100 m^-2) to standardize across surveys.

## Data sources and compilation

- Primary fish data:
  - Environment Agency’s National Fish Population Database (NFPD) for open-access adult fish counts.
  - University of Hull (UoH) fish population data for supplementary information.
- Covariates and ancillary data:
  - Habitat: River Habitat Survey (RHS) and HABSCORE (for Atlantic salmon and brown trout) to assess habitat quality.
  - Water quality: 41 chemical determinands from the UK Environment Agency Water Quality Archive (and UKCEH data repositories).
  - Hydrology and climate: river flow (NRFA), water temperature (modelled; CHESS-Met driving data; Base Flow Index), Land Cover Map 2015, Gulf Stream Index (GSI), North Atlantic Oscillation Index (NAOI).
  - Effluent dilution: Effluent Dilution Factor (EDF) via LF2000-WQX model to estimate wastewater influence across reaches.
  - Geography: altitude (IHDTM-based elevations).

## Data integration and processing

- Integration approach:
  - Spatially matched survey locations along the river network; matched hydrology, RHS, RHS-derived variables, RHS/HABSCORE where applicable.
  - Spatial/temporal alignment so covariates correspond to ecologically meaningful timeframes for each fish survey.
  - Proximity-based matching: key covariates linked to the nearest fish site; model-generated data (EDF, land cover) linked via fish-site coordinates along the river network.
- Matching and matching quality:
  - RHS sites linked to nearest fish site within 5 km along the river network.
  - WQ determinand sites matched to fish sites with criteria ensuring upstream/downstream relationships relative to sewage outfalls, overlap of timeframes, and geographic proximity.
  - Gauging stations for river flow matched via river-network distance; multiple flow metrics calculated for 3-, 6-, and 12-month windows prior to each survey.
- Data completeness:
  - Visual figures indicate varying completeness by covariate and region; some covariates have full coverage in certain years/regions, others exhibit gaps (noData).
  - Some covariates (altitude, land use, BFI, GSI, NAOI) show high completeness; others show gaps due to temporal or spatial misalignment or data unavailability.
- Data processing specifics:
  - Fish densities derived from raw counts using standardization to account for sampling area and survey type (semi-quantitative vs. first catch from quantitative surveys); qualitative surveys excluded.
  - Water temperature time series generated using GAMMs stratified by BFI (0.3–0.99 increments) to predict site-specific temperatures from air temperature and other factors; cumulative degree-days (≥12°C) computed for prior year prior to each survey.
  - Water quality metrics calculated for 12 months preceding each survey; LOQ handling options applied (LoQ treated as LOQ, 0, or LOQ/2) and a maximum threshold used for some determinands; multiple summary statistics (min, max, median, mean, SD) plus sample counts and LOQ-related metrics produced.
  -EDF modelling uses a conservative hypothetical distribution of wastewater across significant wastewater treatment works (WWTWs) to estimate percentage wastewater at each reach; EDF outputs include EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95.
- Data outputs and structure:
  - Five data file types produced (per region): species table, site variables (region-specific), data table (survey-level), water quality determinand data tables, and hydrology data tables.
  - Complementary detector and heatmap outputs illustrate data completeness and coverage by year/region and by chemical determinand.

## Covariates and measurements

- Habitat
  - RHS: HMS (habitat modification) and HQA (habitat quality) scores; RHS matching to fish sites limited by available RHS sites within 5 km.
  - HABSCORE: habitat quality scores by species/size classes; linked to survey sites where available.
- Hydrology and climate
  - River flow: daily NRFA flow data; multiple statistics (mean, median, SD, CV, quartiles) and threshold-based metrics for 3-, 6-, and 12-month periods prior to surveys.
  - Water temperature: modeled with GAMMs; degree-days (≥12°C) computed for the year before each survey.
  - Land cover: upstream catchment proportions and areas for woodland, arable, and seminatural/urban macro-categories derived from Land Cover Map 2015; proportion and area upstream from each fish site.
  - Altitude: site elevation from IHDTM (including special handling for estuarine sites with default 0 m).
  - Base Flow Index (BFI): used to differentiate groundwater-influenced regimes; fish sites assigned to BFI ranges to select appropriate temperature modeling.
  - Climatic indices: Gulf Stream Index (GSI) and NAOI (winter NAO) for long-term climate context.
- Water quality and chemistry
  - Water quality determinands: 41 chemicals (e.g., metals, nutrients, organic pollutants) with extensive metadata; linked to fish sites via nearest three WQ determinand sites and selected based on sampling frequency, proximity to effluent sources, and temporal overlap.
  - Data sources include WQ Archive (EA) and UKCEH repositories; data coverage spans 1960–2017 with structured LOQ and threshold handling.
  - WQ statistics: min, max, median, mean, SD for antecedent period (12 months); counts of samples and LOQ-related metrics (below LOQ, above LOQ).
- Spatial and data caveats
  - Some sites have water quality data restricted by licensing; 33 sites excluded from water quality outputs.
  - Data completeness varies by region and year; some covariates have full coverage while others exhibit data gaps and “noData” values.
  - Distances for matching covariates to fish sites are constrained (generally within 1 km for certain checks; other matches rely on nearest-neighbor logic along river networks).

## Data quality, limitations, and caveats

- Standardization challenges:
  - The combination of different data formats and collection goals across sources necessitated careful harmonization; many covariates required transformation, spatial alignment, and temporal matching.
- Data gaps and exclusions:
  - Gaps in covariates due to lack of temporal overlap or nearby covariate data; 33 fish sites lacking water quality data due to licensing restrictions.
- Measurement limitations:
  - Variation between quantitative and semi-quantitative fish surveys required deriving densities with careful calibration; qualitative surveys excluded due to lack of effort data.
  - Water temperature modeling depends on BFI and regional differences; uncertainties inherent in extrapolation for ungauged sites.
- Temporal constraints:
  - Climate indices (GSI and NAOI) are provided as annual means; fine-scale monthly variability is not captured in those indices.
- Usage guidance:
  - EDF outputs are modeled estimates representing wastewater influence; actual concentrations may vary and the EDF is intended as an index across reaches.
  - Users should account for potential residual misalignment between fish survey dates and covariate measurements.

## Data structure and access

- File types and contents (region-specific files):
  - CP_Fish_SpeciesTable.csv: species codes, Latin names, EA codes, common names.
  - CP_Fish_SiteVariables_region.csv: site-level covariates (location, habitat scores, altitude, land cover metrics, BFI, EDF, and EDF-related stats).
  - CP_Fish_DataTable_region.csv: survey-level data including Fish_SurveyDate, species densities, and HAB/SCORE-related habitat data per survey.
  - CP_Fish_HydrologyStats_Region.csv: river flow statistics and various NRFA-derived metrics for each survey site.
  - Region_FISHWIMSStats_DET.csv: determinand-specific data across regions (comprehensive WQ metrics per determinand per site, with multiple potential LOQ configurations).
  - Region_FISHWIMSStats_DET.csv contains numerous fields for each determinand, including WQ metrics over antecedent periods, thresholds, durations, and counts.
- Data provenance and access:
  - Data from NFPD (Environment Agency), RHS, HABSCORE, EDF (LF2000-WQX), NRFA (NRFA API), CHESS-Met, IHDTM, Land Cover Map 2015, Gulf Stream Index, NAOI, and Water Quality Archive (EA/UKCEH).
  - Acknowledgments and citations provide sources and licensing notes; data curation credited to multiple authors and institutions.

## Potential uses for analysts

- Identify correlations between fish densities and chemical exposures while controlling for habitat quality, hydrology, and climate factors.
- Develop predictive models (e.g., GAMMs) to estimate recruitment and adult densities under varying chemical exposure scenarios and environmental contexts.
- Compare regional differences in chemical impacts while accounting for land use, rainfall/runoff patterns, and river network structure.
- Use open, metadata-rich data to reproduce analyses, validate regulator assessments, and inform policy decisions on chemical regulation and aquatic ecosystem health.

## Summary of key takeaways for data-driven analysis

- Rich, multi-faceted dataset linking fish populations to a broad suite of environmental covariates across 1180 sites (1975–2017), enabling exploration of chemical exposure effects vs other drivers.
- Comprehensive data integration workflow, with spatial and temporal alignment along river networks and careful matching criteria for hydrology, water quality, habitat, and climate covariates.
- Transparent handling of data limitations, including incomplete covariate coverage, data licensing exclusions, and methodological choices for converting survey types into densities.
- Data structure supports region-specific analyses and cross-region comparisons, with clearly defined tables for species, sites, surveys, hydrology, and determinands.