The risk analysis for Phytophthora infection in heathlands fragments across Scotland

## Overview
- Updated risk analysis to include new infection sites: larch woodlands and garden/trade premises.
- Introduces climate suitability model to estimate climatically driven infection risk, species-specific for P. ramorum (Pr) and P. kernoviae (Pk).
- Presents risk maps showing how climate and host suitability shape national-scale infection risk, with notable geographic variation between species.

## Data sources and risk factors
- Heathland fragments: two GIS datasets from CEH Landcover Map 2007
  - BH_10_Scotland: heather and dwarf shrub, burnt heather, gorse, dry heath
  - BH_11_Scotland: heathland with grass
- Risk factors for each fragment (within 1.5 km of premises or infected sites):
  - Proximity to premises (uninfected, uninfected near, infected)
  - Proximity to larch woodlands and larch infections
  - Host abundance of heathland plants (Vaccinium myrtillus, V. vitis-idaea, Arctostaphylos uva-ursi) using DOMIN class-based abundance
  - Climatic suitability for Pr and Pk
  - Proximity to roads and rivers
  - Data constraints: Scotland-wide maps not provided for all risk factors due to access; appendix outlines data extraction methods
- Host plant data: abundance predicted from a range of climatic, soil, topography, grazing, and habitat covariates
  - Variables include climate (Bioclim), soil properties, elevation, deer and sheep density, habitat cover

## Modeling approach for host species distribution
- Objective: estimate abundance (percent cover) and presence/absence of host species on heathland
- Data issues addressed: overdispersion, unequal site sampling, interval-censored DOMIN categories
- Two-phase Bayesian GLMM approach (logit transforms):
  - Phase 1: presence/absence modeled with an overdispersed binomial GLMM
  - Phase 2: conditional on presence, abundance modeled with a logit-normal model
  - Site-level random effect and quadrat-level random effect to capture unobserved variation
- Model validation:
  - Training AUCs > 0.90; test AUCs ~0.77–0.85 across species
  - Important predictors:
    - Vaccinium myrtillus: temperature, precipitation, soil pH, soil moisture, sheep and deer density, elevation, bracken, coniferous and broadleaf woodland
    - Vaccinium vitis-idaea: temperature, precipitation, soil moisture, elevation, sheep density, bracken
    - Arctostaphylos uva-ursi: temperature, precipitation, soil moisture, soil carbon and pH, elevation, aspect, grazing, and woodland cover
- Data gaps documented and visualized; missing climate data more common on the west coast, host data missing mainly in eastern/southern areas

## Climate suitability and risk factor weighting
- Two species-specific risk scores with different maximums:
  - Pr: maximum risk score 14
  - Pk: maximum risk score 13
- Climate scoring differs by species due to Scotland’s overall lower suitability for Pk
  - Pk typically has fewer than 30 days/year suitable (median ~17.6)
  - Pr ranges 50–200 days/year suitable (median ~117.2)
- Risk factors combined with weightings (Table 1) to compute:
  - Premises proximity
  - Larch proximity and infections
  - Host species abundance (VM, VV, AS scores)
  - Climate suitability (Pr and Pk specific)
  - Water courses and roads
- Outputs include a measure of data completeness and uncertainty (Uncert_pr, Uncert_pk)

## Outputs and data products
- Data formats provided for end-user exploration:
  - BH_10.xlsx and BH_11.xlsx: risk factors and scores per heathland fragment
  - BH_10.shp and BH_11.shp: full calculation details and original fields from CEH Landcover Map 2007
- Linkable via PARCEL_ID
- Key fields:
  - PARCEL_ID: unique fragment
  - DOMIN19, DOMIN21, DOMIN66: predicted DOMIN abundance for A. uva-ursi, V. vitis-idaea, V. myrtillus
  - Climsuit_p: suitable days for Pk
  - Climsuit_1: suitable days for Pr
  - prem_score, larch_sc_3: proximity scores
  - Vm_score, Vv_score, AS_score: host abundance scores
  - clim_sco_3 (Pr), clim_sco_4 (Pk): climate scores
  - road_score, river_sco_3: proximity to roads and rivers
  - Risk_sco_3 (Pr), Risk_sco_4 (Pk): total risk scores
  - Adj_risk_p, Adj_risk_pk: risk scores adjusted for available data
  - Uncert_pr, Uncert_pk: uncertainty due to data gaps
  - missing_type: indicates missing data factors (clim, host, or both)

## Results: spatial patterns and interpretation
- Pr vs Pk risk patterns differ due to climate and host suitability:
  - Pr risk concentrates in the south and west, aligning with known infections, but also shows central regions with notable risk
  - Pk risk higher in central and northern highlands due to climate and host suitability
  - Northern Scotland shows limited Pr risk except in isolated pockets; Pk shows broader potential in highland areas
- Outputs emphasize relative risk per species across Scotland, not cross-species absolute comparability
- Outputs include maps (Figures 7–14) illustrating risk scores and current infection sites (premises and larch)

## Data quality, uncertainty, and caveats
- Missing data impacts:
  - Climate data gaps: west coast fragments (blue in maps)
  - Host data gaps: eastern and southern fragments (red in maps)
- Final risk scores adjusted for data availability; uncertainty increases as data availability decreases
- Model caveat: climate suitability differs by species; direct comparability of Pr and Pk risk scores is relative, not absolute

## Practical use for data support
- Provides self-serve risk maps and downloadable data to support decision-making and policy planning
- Facilitates integration with other data sources (premises, host distribution, climate)
- Enables targeted monitoring and management by highlighting high-risk heathland fragments and regions
- Appendices (e.g., Appendix A) document scoring rules and methodologies for reproducibility and auditability