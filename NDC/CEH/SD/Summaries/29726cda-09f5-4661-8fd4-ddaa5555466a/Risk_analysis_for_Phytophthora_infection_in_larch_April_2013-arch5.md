# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) in Larch across Scotland April 2013

## Summary
- Updated risk analysis incorporating new infection sites in larch woodlands, gardens, and trade premises, using a climate suitability model to estimate climatically-driven transmission risk for P. ramorum (Pr) and P. kernoviae (Pk) specific to each pathogen.
- New pathogen-specific risk maps reflect differences in climate suitability and host presence; climate strongly shapes relative risk patterns alongside infected larch premises.
- Scotland is predicted to be more climatically suitable for Pr than for Pk; typical suitable days per year are lower for Pk (median ~17.6; mean ~17.5) and higher for Pr (median ~117.2; mean ~118.4).
- High Pr risk areas: primarily in the south-west and parts of central Scotland (e.g., Dumfries & Galloway, eastern Strathclyde, Argyll & Bute, Ayrshire). Pk risk shares the south-west pattern but shows relatively higher suitability in central/east regions.
- Two pathogen-specific risk maps are produced due to different climate thresholds; risk scores combine multiple factors to yield fragment-level scores (Pr max 17, Pk max 16).
- Outputs are provided in two formats (CSV and GIS shapefiles) for the larch datasets: Larch_SC_March2012 (SC) and Larch_Combined (LC). Outputs include adj_risk_p and adj_risk_2 to reflect data completeness and maximum achievable scores.
- Datasets involved: 16,090 larch fragments in SC and 10,363 fragments on private land (LC); infection premises data (up to 2013); hosts Rhododendron ponticum and Vaccinium myrtillus used to model reservoir/habitat suitability and abundance.
- Climate, host, and landscape factors integrated: host habitat suitability (R. ponticum), Vaccinium myrtillus abundance, climate-based suitability, proximity to infected premises, proximity of larch infections, roads and rivers, and host/landscape context (deer and sheep presence, soil, elevation).
- Data gaps and uncertainty are acknowledged; missing data are mapped, and uncertainty increases with data gaps. Outputs include uncertainty indicators and data-resolution caveats; some Scotland-wide maps are restricted due to data access limits.

## Data sources and risk factors
- Larch fragments:
  - SC: National Forest Estate sub-compartments (Larch_SC_March2012)
  - LC: Private land larch fragments (Larch_Combined)
- Infection data: Locations of larch infections and premises updated through 2011–May 2013 (Forestry Commission Scotland; SASA; FC Scotland data sharing).
- Host species models:
  - Rhododendron ponticum: Maxent habitat suitability model (11 datasets; 1691 points, 8455 polygons) using landscape, soil, climate predictors.
  - Vaccinium myrtillus: abundance model across woodlands using NVC surveys (335 sites; DOMIN scale 0–10), analyzed with a two-phase Bayesian GLMM approach (presence/absence, then abundance) to handle interval-censored DOMIN data and overdispersion.
- Environmental covariates (1 km resolution) used to predict V. myrtillus percent cover:
  - Climate: annual mean temp, annual precipitation, seasonality metrics (BioClim)
  - Soil: water content, carbon content, pH
  - Topography: elevation, aspect
  - Grazing: red deer density, sheep numbers
  - Habitat: percent broadleaf, percent conifer woodland, bracken patches
- Proximity metrics:
  - Within 1.5 km to garden/trade premises; proximity to infected premises; proximity to larch infections (±5 km, 500 m, 5000 m)
- Data restrictions:
  - Scotland-wide maps of some risk factors not provided due to data access restrictions.

## Modelling approach
- Two-stage modelling for host presence and abundance:
  - Rhododendron ponticum: habitat suitability predicted using Maxent (presence/absence across 1 km cells).
  - Vaccinium myrtillus: presence/absence modeled with a binomial GLMM; given presence, abundance modeled with a logit-normal GLMM; both phases Bayesian to handle interval-censored data.
- Climate suitability modelling:
  - Species/strain-specific thresholds define “days suitable” for infection; used as a climatic risk component (Pr vs Pk).
- Risk factor weighting (Table 1):
  - Premises proximity (within 1.5 km, 250 m, 100 m; presence/absence of infected premises)
  - Larch infections in proximity (within 5 km vs within 0–5 km)
  - R. ponticum habitat suitability
  - V. myrtillus habitat suitability/abundance
  - Climatic suitability (Pr and Pk thresholds)
  - Watercourses and roads within fragments
- Final risk scores:
  - Pr (P. ramorum): maximum 17
  - Pk (P. kernoviae): maximum 16
  - Climate scoring is pathogen-specific to reflect differing climate suitability.

## Outputs and data formats
- Output data formats provided for both larch datasets:
  - CSV: LC_RISK.csv (LC) and SC_RISK.csv (SC) containing risk scores and related fields
  - Shapefiles: LC_RISK.shp and SC_RISK.shp with full calculations and original FC fields
- Key fields (examples):
  - OBJECTID, prem_score, larch_score, Rp_score, Vm_score, clim_score, clim_sco_2, road_score, river_score
  - Adj_risk_p (Pr-adjusted risk), Adj_risk_2 (Pk-adjusted risk)
  - Risk_score (sum for Pr), Risk_sco_2 (sum for Pk)
  - missing_type indicators for data gaps
- Linking fields:
  - OBJECTID (SC) or SUBCOMPTID (SC); and corresponding identifiers to join outputs with original fragment data
- Output interpretation:
  - Risk maps display fragment-level risk with color gradations (grey = low risk; green to red = medium-high risk)
  - Species-specific maps emphasize regional differences due to climate suitability

## Geographic risk patterns
- P. ramorum (Pr):
  - Predominant high-risk zone in the south-west and parts of eastern Strathclyde; elevated risk linked to proximity to infections and higher climate/host suitability in these areas.
  - North-east regions generally lower risk.
- P. kernoviae (Pk):
  - Similar south-westward pattern but relatively higher risk in central Scotland and the east due to climate suitability.
  - Central/east regions show comparatively higher Pr vs Pk climate suitability differences.

## Data quality, gaps, and uncertainty
- Data gaps exist in some fragments for Vaccinium myrtillus and climate layers; adverse data gaps increase uncertainty in risk scores.
- Two data formats and explicit uncertainty indicators (Uncert_pr, Uncert_pk) accompany risk scores to reflect missing information and data quality.
- Some nationwide climate maps are restricted due to data-access constraints; risk mapping is therefore partial at national scale.

## Implications for data governance and stewardship
- Provenance and data management:
  - Data from FC Scotland, SASA, and Forestry Commission; versioned larch fragment datasets; premises and outbreak data integrated up to 2013.
  - Clear documentation of methods (GLMM, Maxent, and climate thresholds) and data processing steps.
- Metadata and accessibility:
  - Outputs delivered in CSV and Shapefile formats with explicit field definitions; fields designed to facilitate reproducibility and GIS integration.
  - Data constraints include data-access restrictions, especially for some pre-climate factors and national-scale maps.
- Maintenance and updates:
  - Model updated to incorporate new infection sites; approach supports future updates as new premises and infection data become available.
  - Recommend systematic updates of host habitat data (R. ponticum and V. myrtillus) and climate layers to maintain current risk assessments.
- Operational use:
  - Data stewards can use the provided risk scores to prioritize surveillance and monitoring in higher-risk fragments.
  - The separation of Pr and Pk risk scores supports pathogen-specific management decisions and communications.

## How to use the outputs
- Identify high-risk fragments by examining adj_risk_p (Pr) and adj_risk_2 (Pk) values and the overall risk_score fields.
- Use the 1 km-resolution raster-based input fields (e.g., host habitat suitability, climatic suitability) to contextualize management actions at the fragment level.
- Leverage the provided GIS shapefiles for spatial analyses in ArcGIS/QGIS and link to the original fragment attributes using OBJECTID or SUBCOMPTID.
- Consider data gaps and uncertainty indicators when interpreting risk, prioritizing fragments with high risk scores and low data uncertainty for immediate surveillance.