# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) in Larch across Scotland April 2013

## Overview
- Updated risk analysis for Phytophthora infection in larch across Scotland, adding new infection sites in both woodlands and garden/trade premises.
- Introduces a climate suitability model that estimates climatically suitable days per year, specific to P. ramorum or P. kernoviae.
- Produces pathogen-specific risk maps; emphasises climate and host suitability as key drivers, in addition to presence/location of infected larch and premises.
- Scotland is predicted to be more climatically suitable for P. ramorum than for P. kernoviae, yielding differing regional risk patterns between species.

## Data sources and risk factors
- Larch datasets: SC (Larch_SC_March2012) and LC (Larch_Combined), comprising thousands of larch fragments.
- Infection data: locations of larch infections (up to April 2013) and outbreak sites on premises (gardens/trade premises).
- Host and reservoir data:
  - Rhododendron ponticum habitat suitability (Maxent models; 11 datasets; 1691 points, 8455 polygons).
  - Vaccinium myrtillus abundance estimated from NVC woodland surveys (335 surveys; DOMIN class intervals).
- Additional predictors:
  - Climate, soil (pH, water content, carbon), topography (elevation, aspect), grazing pressure (deer and sheep density), habitat fragmentation, roads, and rivers.

## Methods and risk scoring
- Climate suitability models are pathogen- and strain-specific, producing a climate-based component of risk for each pathogen.
- Weighting of risk factors (Table 1) combines multiple layers into a composite risk score:
  - Maximum risk scores: Pr (P. ramorum) up to 17; Pk (P. kernoviae) up to 16.
- Proximity factors:
  - Premises within 1.5 km (0, 1, 2, or 3 points depending on proximity to infected premises).
  - Larch infections within 5 km or 500 m (0, 2, or 4 points).
- Host and climate factors:
  - R. ponticum habitat suitability (RP): presence vs absence (0 or 3 points).
  - Vaccinium myrtillus abundance (VM): presence/absence and DOMIN abundance class (0–2 points).
  - Climatic suitability: pathogen-specific thresholds (Pr: 0–3 points; Pk: 0–2 points).
  - Additional factors: presence of watercourses and roads within fragments (0 or 1 point each).
- Outputs include two data streams (one for each larch dataset) with risk scores specific to Pr and Pk.

## Outputs and data formats
- Data products provided in two formats per dataset:
  - Excel/CSV: LC_RISK.csv and SC_RISK.csv (risk scores only).
  - GIS shapefiles: LC_RISK.shp and SC_RISK.shp (full calculations and original fields; linked via OBJECTID or SUBCOMPTID).
- Key output fields (examples):
  - adj_risk_p (adjusted Pr risk score) and adj_risk_2 (adjusted Pk risk score).
  - Risk_score (sum of risk factor scores for Pr) and Risk_sco_2 (for Pk).
  - Covariate-derived fields: AveRhodoHS, DOMIN22, Climsuit_pr, Climsuit_pk, prem_score, Larch_scor, Rp_score, Vm_score, clim_score, clim_sco_2, road_score, river_score.
  - Uncertainty indicators: Uncert_pr, Uncert_pk, missing_type.
- Outputs are designed for GIS integration and cross-referencing via unique fragment identifiers.

## Results: risk patterns and interpretation
- Pr (P. ramorum) risk:
  - High-risk areas concentrated in the south-west, including Dumfries and Galloway and parts of eastern Strathclyde, with notable Argyll regions.
  - Risk influenced by current larch infections, infected premises, and favorable climate/host suitability.
- Pk (P. kernoviae) risk:
  - Similar south-west emphasis but relatively higher predicted risk in central and eastern Scotland due to climate suitability.
  - Overall climate suitability for Pk is lower than for Pr, leading to different regional emphasis.
- Visual risk maps (Figures 6–11) illustrate pathogen-specific patterns and show how known infections and premises relate to predicted risk.

## Handling missing data and uncertainty
- Maps and outputs indicate missing data and data gaps (e.g., VM habitat data gaps, climate data gaps) and their impact on risk scores.
- Uncertainty measures (Uncert_pr, Uncert_pk) quantify data gaps within the risk calculations.
- Some Scotland-wide layers are not provided due to data-access restrictions; outputs include formats that accommodate data gaps and enable adjustments.

## Appendices and methodological details
- Appendix: detailed methodology for host species models:
  - Vaccinium myrtillus: presence/absence modeled with a binomial GLMM; given presence, abundance modeled with a logit-normal GLMM; Bayesian framework handles interval-censored DOMIN data.
  - Rhododendron ponticum: Maxent habitat suitability models using landscape, soil, and climate predictors; model validation reported (AUC ~0.838).
- Appendix tables describe risk factor scoring and data processing steps, including how proximity and climate metrics are derived in ArcGIS and Python workflows.

## Practical implications and usage
- The risk maps and scores provide a decision-support basis for monitoring, surveillance, and management of Phytophthora risk in Scottish larch forests.
- Outputs enable targeted interventions by prioritizing areas with higher adjusted pathogen risk and by considering species-specific climate suitability.
- Data products are designed for integration into GIS workflows, supporting stakeholders in policy, forestry management, and biosecurity planning.