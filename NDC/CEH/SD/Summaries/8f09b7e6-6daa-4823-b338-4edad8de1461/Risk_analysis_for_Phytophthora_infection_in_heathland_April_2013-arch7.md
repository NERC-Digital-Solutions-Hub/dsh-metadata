# The risk analysis for Phytophthora infection in heathlands fragments across Scotland

## Overview
- Updated risk analysis (April 2013) for Phytophthora infection in heathland fragments across Scotland.
- Introduces new infection sites in larch woodlands and garden/trade premises; uses a climate suitability model to estimate transmission risk for P. ramorum and P. kernoviae.
- Presents pathogen-specific risk maps; climate and host suitability drive risk more than current infection locations.
- Highlights geographic differences: Scotland is more climatically suitable for P. ramorum than for P. kernoviae; high-pr suitability for Pr in Argyll & Bute, Ayrshire, Dumfries and Galloway, with distinct patterns for Pk including central/north regions.

## Data sources and layers
- Heathland fragments from CEH Land Cover Map 2007 (BH_10: "heather and dwarf shrub..." and BH_11: "heather grass").
- Scotland-wide layers created from 100 km tiles; clipped to Scotland to form BH_10_Scotland.shp and BH_11_Scotland.shp (112,977 BH_10 polygons; 182,544 BH_11 polygons).
- Risk factors include:
  - Host plant abundance: Vaccinium myrtillus, V. vitis-idaea, Arctostaphylos uva-ursi (predicted percent cover on the DOMIN scale).
  - Climatic suitability for growth and sporulation (species/strain specific thresholds).
  - Proximity to larch and proximity to inspected garden/trade premises within 1.5 km.
  - Presence of roads and rivers within a fragment.
- Additional data: infection premises (garden sites, current infections), larch infections (current up to Apr 2013).
- Data limitations: Scotland-wide maps of all risk-factor layers not provided due to data access restrictions.

## Risk factors and scoring framework
- Risk factors combined into a scoring system with species-specific weightings (Table 1):
  - Premises proximity (within 1.5 km) and infection status (uninfected vs infected) contribute to risk scores.
  - Larch proximity within 5 km and presence/infection status contribute scores.
  - Host species abundance (VM, VV, AU) scores based on DOMIN class predictions (absent, low, high).
  - Climatic suitability for Pr and Pk (days suitable; thresholds).
  - Proximity to water courses and roads contribute to risk.
- Overall risk scores:
  - Pr (P. ramorum) maximum score: 14.
  - Pk (P. kernoviae) maximum score: 13.
- Climate scoring differs by species to reflect geographic differences in suitability; maps indicate relative (not absolute) risk comparisons between species.
- Data gaps are tracked with a missing data framework and adjusted risk scores when data are incomplete.

## Output data products
- Risk scores provided in two formats:
  - BH_10.xlsx and BH_11.xlsx (risk-factor fields and scores).
  - BH_10.shp and BH_11.shp (full calculation details and original CEH Landcover 2007 fields).
- Link between formats via PARCEL_ID (unique fragment identifier).
- Key fields and recommended metrics:
  - adj_risk_p (Pr risk score adjusted for maximum available score).
  - adj_risk_3 (Pk risk score adjusted for maximum available score).
- Field overview (examples):
  - PARCEL_ID, Roads, Rivers, DOMIN19/21/66 (predicted host abundances), Climsuit_p (Pk), Climsuit_1 (Pr), prem_score, larch_sc_3, Vm_score, Vv_score, AS_score, clim_sco_3 (Pr), clim_sco_4 (Pk), road_score, river_sco_3, Avail_pr, Avail_pk, Risk_sco_3, Risk_sco_4, Uncert_pr, Uncert_pk, Adj_risk_p, Adj_risk_3, missing_type.
- Data can be joined with GIS workstreams using PARCEL_ID to map risk across Scotland.

## Modelling host plant distributions (habitat suitability)
- Objective: estimate abundance of host species (VM, VV, AU) across heathland habitats (BH_10 and BH_11) at 1 km resolution.
- Modelling challenges addressed:
  - Overdispersion and unequal quadrat/site sampling.
  - Uncertainty from DOMIN class interval data (latent true percent cover).
- Modelling approach:
  - Two-stage GLMM in a Bayesian framework:
    1) Presence/absence stage: inflated binomial GLMM with site and quadrat random effects to account for between-site variation and within-site quadrat variability.
    2) Abundance stage: given presence, a logit-normal model (log-normal on transformed scale) for percent cover with site and quadrat random effects.
  - Interval-censored latent variable z_ij to reflect DOMIN class bounds.
  - Predictors include climate, soil, topography, grazing (deer and sheep density), and habitat covariates; area-weighted covariates used for predictions.
- Outputs and validation:
  - Training AUCs > 0.90; test AUCs ~0.80 for all three species:
    - Vaccinium myrtillus: train 0.93, test 0.77.
    - Vaccinium vitis-idaea: train 0.95, test 0.85.
    - Arctostaphylos uva-ursi: train 0.96, test 0.77.
- Important predictors:
  - VM: temperature, precipitation, soil pH and water content, elevation, grazing (sheep/deer), bracken presence, conifer/broadleaf woodland cover.
  - VV: temperature, precipitation, soil water content, elevation, sheep density, bracken.
  - AU: temperature, precipitation, soil water content, soil carbon/pH, elevation, aspect, grazing, woodland cover.

## Missing data and uncertainty
- Some heathland fragments lack climate data (west coast) or host-habitat data (east/south).
- Missing data flags (missing_type) indicate which factors are missing (climate, host, both).
- Risk scores are adjusted to reflect the maximum possible score given available data.
- Uncertainty metrics (Uncert_pr, Uncert_pk) quantify data gaps effect on risk scores.

## Results: spatial patterns and interpretation
- Phytophthora ramorum:
  - Higher risk in south-central Scotland; notable concentrations in the south and west near current infection sites.
  - North regions show lower overall climate suitability with pockets of higher risk where hosts/climate align.
- Phytophthora kernoviae:
  - Risk concentrated in central and northern regions due to climate and host suitability.
  - Some southern areas also at risk, but overall climate suitability is lower than for Pr.
- Maps accompany the report (Figures 7–14) showing risk scores across fragments with current infection and larch infection locations overlaid.

## How to use in GIS workflows
- Data products:
  - Use BH_10.shp and BH_11.shp with their corresponding BH_10.xlsx and BH_11.xlsx to map risk.
  - Join via PARCEL_ID; use adj_risk_p for Pr risk and adj_risk_3 for Pk risk as primary risk indicators.
- Overlay opportunities:
  - Compare risk layers with infection outbreak data to identify high-priority management zones.
  - Combine with host species distribution maps (VM, VV, AU) to understand drivers of risk in given areas.
- Resolution and scale:
  - 1 km resolution host habitat models; 100 km tile-derived risk factors; Scotland-wide clip for consistent geographic scope.

## Appendices and methodological notes
- Appendix A: detailed HEATHLAND SCORING FOR RISK FRAMEWORK, including scoring rules for premises proximity, larch proximity/infection, and host species abundance (DOMIN-based) and climate components.
- Appendix B: modelling approach details for host species distributions, data sources, and covariates.

## Context and provenance
- Authors: Beth Purse & Kate Searle (on behalf of CEH under Scottish Government contract CR/2008/55 and extension CRF925_extension).
- Date: April 2013.
- Scope: national-scale risk assessment integrating infection data, host habitat suitability, and climate factors for two Phytophthora pathogens in Scotland.