# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) in Larch across Scotland April 2013

- Updated analysis incorporating new infection sites in larch woodlands and garden/trade premises; uses a climate suitability model to derive pathogen-specific, climatically driven risk.
- Presents separate risk maps for P. ramorum (Pr) and P. kernoviae (Pk) that reflect differences in climate suitability and host interactions.

## Purpose and scope

- Quantifies risk of Phytophthora infection across Scotland using a climate-driven framework augmented by host presence/abundance and proximity to infected premises and larch infections.
- Emphasizes climate and host suitability as key drivers, alongside location of infections and infected premises.

## Data sources and risk factors

- Larch geographic datasets:
  - Larch_SC_March2012 (SC) and Larch_Combined (LC), covering woodland and private land fragments.
- Risk factors (fragment-level):
  - Proximity to infected premises within 1.5 km and within 100–250 m/0–5 km categories.
  - Larch infection presence within 5 km or within 500 m (high-weight factor).
  - Rhododendron ponticum habitat suitability (RP) modeled with Maxent.
  - Vaccinium myrtillus (VM) abundance estimated from DOMIN scale; abundance modeled via a Bayesian GLMM (presence/absence and then abundance).
  - Climatic suitability for growth/sporulation, species-specific thresholds (Pr and Pk).
  - Landscape features: proximity to roads and rivers.
  - Data exclusions: Scotland-wide maps not provided for all factors due to data access restrictions.
- Host data modeling:
  - V. myrtillus: presence-absence and abundance modeled separately (logit-normal GLMM with interval-censored DOMIN data; covariates include climate, soil, topography, grazing, and woodland fragmentation).
  - R. ponticum: Maxent habitat suitability model using 11 datasets; validated with training/test AUC ~0.838.

## Climate suitability modelling and risk scoring

- Climate suitability is pathogen-specific:
  - P. ramorum: typical 50–200+ suitable days/year; mean/median around 118 days; higher suitability in southwest and parts of central Scotland.
  - P. kernoviae: typically far fewer suitable days; median ~17.6 days; higher relative suitability in central/east Scotland than Pr.
- Weighting and scoring (Table 1):
  - Premises proximity to non-infected within 1.5 km: 0 or 1; infected within 100 m: 3.
  - Larch infection within 5 km: 0 or 2 or 4.
  - R. ponticum habitat suitability: 0 (unsuitable) or 3 (suitable).
  - Vaccinium myrtillus abundance: 0 (absent/low) or 1 (low) or 2 (high).
  - Climatic suitability: species-specific,
    - Pr: <100 days (0), 100–150 (1), 150–200 (2), >200 (3).
    - Pk: <17.5 days (0) or >17.5 (2).
  - Watercourses within fragment: 0 or 1.
  - Roads within fragment: 0 or 1.
- Scoring outcomes:
  - Maximum possible score: Pr = 17, Pk = 16 (climate scores differ by species; maps are relative, not strictly comparable between species).
  - Adjacency and data gaps are tracked to adjust risk (Adj_risk_p and Adj_risk_2).
- Outputs and accessibility:
  - Two Excel files: LC_RISK.csv and SC_RISK.csv (risk scores per fragment).
  - Two ArcGIS shapefiles: LC_RISK.shp and SC_RISK.shp (full calculation details; linked via OBJECTID or SUBCOMPTID).
  - Fields include risk_score, adj_risk_p, adj_risk_2, uncertainty measures, and indicators of missing data.

## Key findings and risk patterns

- Pr risk: high in the south-west and parts of eastern Strathclyde, Dumfries and Galloway, and Ayrshire/central belt; influenced by current infections, larch presence, climate suitability, and RP/VM factors.
- Pk risk: similar southwest concentration but relatively higher risk in central and eastern Scotland due to climate suitability patterns; overall climate suitability for Pk is lower than for Pr.
- Data layers with missing values map to higher uncertainty in risk scores; maps depict grey fragments as low risk and green-to-red fragments as medium-to-high risk, with species-specific patterns.

## Outputs and interpretation guidance

- Output datasets provide:
  - Risk_score: overall risk per fragment.
  - Adj_risk_p and Adj_risk_2: risk adjusted for available data and maximum possible score.
  - Uncert_pr and Uncert_pk: data completeness uncertainty measures.
  - Missing_type indicator: which risk factors are missing for a fragment.
- Practical use:
  - Identify regionally high-risk areas for targeted monitoring and management.
  - Compare relative risk between Pr and Pk across Scotland, acknowledging climate and host differences.

## Data gaps and uncertainties

- Some Scotland-wide risk-factor maps not provided due to data access restrictions.
- Missing data in VM habitat, climate suitability, and other covariates lead to uncertainty in risk scoring for certain fragments.
- The climate component is species-specific to avoid misinterpreting Pk risk using Pr-like climate thresholds.

## Appendices: methodological details

- Host species modelling details:
  - V. myrtillus: two-phase Bayesian GLMM approach; presence/absence model (binomial) with site and quadrat random effects; abundance model (logit-normal) for sites with presence; interval-censored DOMIN data incorporated.
  - Covariates for V. myrtillus include climate (temperature, precipitation), soil properties (pH, carbon, water content), elevation, bracken presence, grazing pressure (deer and sheep), and woodland fragmentation metrics.
- Risk scoring framework (Table-style descriptions):
  - Proximity to premises, larch infections, RP habitat suitability, VM abundance, climatic suitability, hydrology (rivers), and roads are combined into an overall risk score with specified scoring rules.
  - Data processing workflows include ArcGIS proximity analyses and Python scripts for summary statistics on rivers and roads.
- Figures and maps referenced (e.g., risk distributions by species, regional maps) demonstrate spatial patterns of climate and host suitability driving risk.

## Summary takeaway for data-led inquiry

- The analysis provides a pathogen-specific, climate-informed risk framework for Phytophthora infection in Scottish larch, integrating host distribution data, proximity to infections, and landscape factors.
- It yields actionable, region-specific risk scores and maps for Pr and Pk, highlighting geographic differences in climate suitability that shape infection risk.
- The approach prioritizes data quality, acknowledges uncertainties due to missing layers, and offers downloadable results in both tabular and GIS formats for practical decision-making.