# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) Core Native Woodland fragments across Scotland April 2013

## Purpose and updates
- Updated risk analysis for Phytophthora infection in core native woodland fragments across Scotland (April 2013), incorporating new infection sites in larch woodlands and garden/trade premises.
- Introduces a climate suitability model to estimate climatically driven, pathogen-specific risk (days suitable for transmission).
- Presents new, pathogen-specific risk maps for P. ramorum (Pr) and P. kernoviae (Pk), showing regional variation driven by climate and host presence.

## Key findings
- Overall risk concentrated in the south and west of Scotland, aligning with current infection locations and larch presence.
- P. kernoviae risk is more extensive than P. ramorum in some areas, including the northeast, due to host and climate suitability.
- Scotland is predicted to be more climatically suitable for Pr than for Pk; typical suitable days per year: Pr 50–200 days (median ~117), Pk < 30 days (median ~17.6).
- Climate suitability and host availability drive risk: regions with favorable Rhododendron ponticum habitat and Vaccinium myrtillus presence, plus larch proximity, show higher risk.
- Risk maps reflect relative, not absolute, risk between species; some high-risk areas lie distant from known infections, highlighting surveillance priorities.

## Risk factors and data inputs
- Core Native Woodland fragments analyzed: 79,269.
- Proximity-related factors: distance to premises, infected premises, larch proximity (within 5 km and within 500 m; infection proximity within 100 m).
- Host-related factors:
  - Rhododendron ponticum habitat suitability (models using 11 datasets; Maxent, training AUC ~0.838).
  - Vaccinium myrtillus abundance (DOMIN scale; 335 NVC surveys; 1 km resolution; presence/absence and then abundance modeled).
- Climatic suitability: pathogen-specific thresholds for Pr and Pk (days suitable per year provided as model inputs).
- Additional factors: proximity to watercourses and roads (as risk modifiers).
- Data sources: garden/trade premises and infection data from FC Scotland and SASA; infection datasets updated through early 2013.

## Methodology and risk scoring
- Final risk score framework combines multiple risk factors with weighted contributions (Table 1; pathogen-specific). Maximum scores: Pr up to 17; Pk up to 16.
- Climate scoring is pathogen-specific to capture different climatic sensitivities.
- Scoring details include:
  - Premises proximity (0–3 points) based on distance to premises and infection status.
  - Larch proximity/infection (0–4 points) based on distance and infection status.
  - Rhododendron ponticum habitat suitability (0–3 points).
  - Vaccinium myrtillus habitat suitability (0–2 points).
  - Climatic suitability (Pr: 0–3; Pk: 0–2, based on days suitable).
  - Watercourses and roads (0–1 point each).
- Output risk indicators:
  - adj_risk_p (Pr) and adj_risk_1 (Pk): risk scores adjusted for maximum possible score given available risk factors.
  - Uncertainty measures (Uncert_pr, Uncert_pk) reflect data gaps.
- Output data formats:
  - FHN_2013.csv: tabular risk scores.
  - FHN_2013.shp: ArcGIS shapefile with full calculations and original fields; both linkable by fragment ID.

## Host and climate modeling details (appendix highlights)
- Rhododendron ponticum modeling:
  - Maxent models using 11 datasets; 1691 points, 8455 polygons.
  - Predicted suitable habitat aligns with broadleaf woodland, low elevation, moderate soil moisture.
- Vaccinium myrtillus abundance:
  - Modeled from 335 NVC surveys; DOMIN class intervals treated as interval-censored data.
  - Two-phase GLMM (presence/absence via binomial model; abundance via logit-normal model) within a Bayesian framework to handle latent true percent cover and random site/quadrat effects.
- Missing data handling:
  - Some fragments missing climate data (west coast), or VM habitat suitability (east/south). Final risk scores are adjusted by the maximum possible score given available data.
  - Missing-type indicator identifies which risk factors are missing for each fragment.

## Outputs and interpretation for data-driven action
- Maps show risk scores across Scotland:
  - Green = low risk; yellow to red = medium to high risk for each pathogen.
  - Figures illustrate distribution relative to current premises and larch infections.
- Surveillance and management implications:
  - Direct attention to high-risk regions, including those distant from known infections, to improve early detection.
  - Use of pathogen-specific risk maps enables prioritization of monitoring, resource allocation, and potential intervention planning.
- Data accessibility and format implications:
  - Shapefile provides comprehensive calculation details for reproducibility and review; CSV offers a lighter, tabular alternative for rapid assessment.
  - Fields such as adj_risk_p and adj_risk_1 are recommended risk indicators; uncertainty fields help gauge data confidence.

## Limitations and considerations
- Relative risk: risk scores are comparative across regions and species, not absolute cross-species equivalents.
- Risk depends on current knowledge of host distributions, infection locations, and climate suitability; updates to data can shift risk patterns.
- Some regions have data gaps that introduce uncertainty, necessitating cautious interpretation and ongoing data collection.