# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) Core Native Woodland fragments across Scotland April 2013

## Overview
- Updated from August 2012 to include new infection sites in larch woodlands and garden/trade premises (data from FC Scotland and SASA).
- Introduces a climate suitability model that estimates the number of suitable days per year for pathogen transmission, specific to P. ramorum (Pr) and P. kernoviae (Pk).
- Produces pathogen-specific risk maps; risk is regionally concentrated in the south and west of Scotland, with notable high-risk areas for Pk in the northeast due to hosts and climate suitability.

## Key findings
- Climate and host presence drive national-scale Phytophthora risk; climate is generally more suitable for Pr than for Pk in Scotland.
- Pr risk is high in southern/western woodlands and also in some northern areas; Pk risk is high in the south/west and in the northeast, with extensive risk in areas distant from current infections.
- Risk maps provide relative, species-specific spatial variation rather than absolute cross-species comparability.

## Data and study scope
- Core Native Woodland fragments analyzed: 79,269 fragments across Scotland.
- Data sources for risk factors include: current infections and premises (gardens/trade), larch presence/infections, host distributions, and landscape features.
- Key risk layers considered (but not all layers distributed nationwide due to data access restrictions): host habitat suitability for Rhododendron ponticum; Vaccinium myrtillus abundance; climatic suitability for Pr and Pk; proximity to premises and infected premises; proximity to larch and larch infections; presence of watercourses and roads.

## Methods summary
- Risk factors and weights:
  - Proximity to premises and infected premises (scored 0–3 based on distance and infection status).
  - Larch presence/infection proximity (scored 0–4 with increasing risk near infected larch).
  - Rhododendron ponticum habitat suitability (0–3 based on suitability/abundance).
  - Vaccinium myrtillus habitat suitability (0–2 based on abundance class DOMIN 1–10).
  - Climatic suitability (species-specific): Pr (0–3) and Pk (0–2) based on thresholds of suitable days.
  - Watercourses and roads within the fragment (each scored 0 or 1).
- Risk scores are calculated separately for Pr and Pk; maximum possible scores are 17 (Pr) and 16 (Pk) with site-specific adjustments for missing data.
- Host modelling:
  - Rhododendron ponticum: Maxent modeling using 11 datasets to predict suitable habitat (training AUC ~0.838; external validation ~0.838).
  - Vaccinium myrtillus: abundance modeled with a two-stage Bayesian GLMM (presence/absence, then abundance) to handle data interval censoring (DOMIN classes) and random effects at site and quadrat levels.
- Climate and other covariates: area-weighted covariates used to derive per-woodland estimates; zonal statistics employed to compute mean climate suitability for each woodland polygon.

## Outputs and data formats
- Risk scores delivered in two formats:
  - FHN_2013.csv: Excel/CSV with fragment-level risk scores and supporting fields.
  - FHN_2013.shp: ArcGIS shapefile with full calculation details and original FC fields; large and may be less convenient to manipulate.
- Key output fields (examples):
  - adj_risk_p (Pr risk score adjusted for available maximum), adj_risk_1 (Pk adjustment).
  - risk_sco_1 (sum of risk scores for Pr), risk_sco_2 (sum for Pk).
  - av ail_pr / avail_pk (maximum possible scores given available data).
  - Missing data indicators (missing_type) and uncertainty measures (Uncert_pr, Uncert_pk).
- Fields align via a unique fragment ID; two formats can be linked through this ID.

## Handling missing data
- Some fragments lack climate data or Vaccinium myrtillus habitat suitability data.
- Missing data are mapped (Figures 4 and 5 in the report); the final risk score for fragments with missing factors is adjusted to reflect the maximum possible score given available data.
- missing_type field indicates which risk factors are missing (clim, host, both, none).

## Spatial results and interpretation
- Maps show low-risk fragments (green) to high-risk fragments (yellow/red) across Scotland.
- Pr risk tends to follow climate suitability and host presence; Pk risk extends beyond current infections in several regions due to host suitability and habitat presence combined with climate.
- Figures illustrate:
  - Overall Pr and Pk risk distribution across Scotland (Figs 6–13).
  - Locations of current premises and larch infections (for context).
- Appendix highlights the V. myrtillus modeling approach and the two-stage GLMM method used to estimate abundance.

## Appendix: detailed methods (V. myrtillus and risk scoring)
- V. myrtillus modelling:
  - Addressed overdispersion, uneven quadrat counts, and interval-censored DOMIN data.
  - Joint presence/absence model (binomial GLMM) and abundance model (logit-normal GLMM) via a Bayesian framework.
  - Covariates include climate (Bioclim), soil (pH, carbon, water content), elevation, vegetation, and grazing pressure (deer, sheep).
- Risk framework details (Table-style descriptions):
  - Proximity to premises and infected premises, larch proximity, Rhododendron ponticum habitat suitability, Vaccinium myrtillus abundance, climatic suitability by species, presence of watercourses, and roads each have defined scoring rules and methodologies.
  - Specific GIS/ArcGIS steps described for calculating proximity and zonal statistics.

## Practical considerations for Data Stewards
- Data provenance and governance:
  - Data integrated from FC Scotland and SASA (infection premises, larch data) with explicit collaboration partners.
  - Some risk-factor layers are restricted; not all Scotland-wide risk layers are publicly distributed due to data access restrictions.
- Data formats and metadata:
  - Outputs include both a simple risk-score CSV and a detailed shapefile with calculation traceability.
  - Field names and scoring logic are documented to support reproducibility and auditing.
- Data quality and updates:
  - Risk scores are species-specific and relative; updating requires re-running models with new infection data and host/climate layers.
  - Missing data handling is explicit, with uncertainty metrics to inform interpretation.
- Interoperability and maintenance:
  - Relationship between CSV and shapefile via ID supports integration into other systems.
  - Clear separation of risk factors by species facilitates targeted governance and reporting.