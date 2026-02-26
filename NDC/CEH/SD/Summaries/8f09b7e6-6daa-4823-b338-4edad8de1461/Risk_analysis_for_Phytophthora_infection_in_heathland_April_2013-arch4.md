# Summary

## Objective and scope
- Update risk analysis of Phytophthora infection in heathland fragments across Scotland.
- Incorporate new infection sites in larch woodlands and garden/trade premises; apply a climate suitability model to estimate climatically-driven infection risk for P. ramorum (Pr) and P. kernoviae (Pk).
- Produce species-specific risk maps that emphasize climate and host suitability alongside current infection sites.

## Data landscape and sources
- Heathland fragments: CEH Land Cover Map 2007 used to define two Scotland-wide fragment datasets:
  - BH_10_Scotland: heather and dwarf shrub, burnt heather, gorse, dry heath.
  - BH_11_Scotland: heathland classified as heather grass.
- Fragment counts (Scotland only): 112,977 (BH_10) and 182,544 (BH_11).
- Current infection data: premises infections ( gardens, trade premises, etc.) and larch infections (current up to April 2013) provided by SASA, Forestry Commission Scotland, and SNH.
- Climate and host modelling inputs: host plant distributions (Vaccinium myrtillus, V. vitis-idaea, Arctostaphylos uva-ursi) predicted via habitat suitability models; factors include climate, soil, topography, grazing, and woodland cover.
- Data gaps and uncertainty: missing climate data concentrated along the west coast; missing host abundance data concentrated in eastern/southern fragments. Missing_type field indicates data gaps and risk scores are adjusted accordingly.

## Modelling approach for host plants
- Habitat suitability for three heathland host species modelled using a two-phase GLMM approach within a Bayesian framework to handle interval-censored DOMIN class data:
  - Phase 1: presence/absence modeled with an overdispersed binomial GLMM incorporating site and quadrat random effects.
  - Phase 2: for sites with presence, abundance (percent cover) modeled with a logit-normal GLMM, again including site and quadrat random effects.
- Predictors used across climate, soil, topography, grazing (deer and sheep), and habitat variables; model validation shows:
  - Training AUCs: >0.90 for all three species.
  - Test AUCs: approximately 0.77–0.85, indicating good predictive capability with some regional underprediction in the far west due to data gaps.
- Outputs provide predicted DOMIN class abundances by fragment and species, forming the basis for risk calculations.

## Risk framework and data outputs
- Risk scoring framework (species-specific) combines multiple factors:
  - Premises proximity (within 1.5 km), larch proximity and infections, host species abundance (VM, VV, AU), climatic suitability for each pathogen, proximity to rivers and roads.
  - Maximum risk scores: Pr up to 14, Pk up to 13.
  - Climate scoring differs between species to reflect Scotland’s relative suitability: Pr often higher; Pk limited by climate suitability.
- Output data formats and fields:
  - Excel files: BH_10.xlsx and BH_11.xlsx containing risk factors and scores.
  - ArcGIS shapefiles: BH_10.shp and BH_11.shp with full calculations and original CEH Landcover 2007 fields.
  - Key fields include PARCEL_ID, DOMIN predictions (VM, VV, AU), climate suitability (Climsuit_p for Pk, Climsuit_1 for Pr), proximity scores (prem_score, larch_sc_3), road and river proximity, and risk scores (Risk_sco_3 for Pr, Risk_sco_4 for Pk).
  - Uncertainty and data completeness fields: Avail_pr, Avail_pk, Adj_risk_p, Adj_risk_3, Uncert_pr, Uncert_pk, missing_type.
- Data interpretation:
  - Adj_risk_p and Adj_risk_3 provide adjusted risk scores accounting for the maximum possible score given available data.
  - Missing_type indicates which risk factors are missing (climate, host, or both), guiding interpretation under data gaps.

## Results and geographic patterns
- Risk maps show:
  - For both Pr and Pk, highest risk in the south and west correlating with known infection sites and larch infection proximity.
  - For Pk, additional high-risk areas in central and northern Scotland driven by climate and host suitability.
  - For Pr, notable risk in south-central Scotland despite fewer current outbreaks, driven by host presence and climatic suitability.
- The spatial patterns emphasize the importance of climate suitability and host availability in driving risk beyond current infection locations.

## Data governance, collaboration, and reuse
- Data assembled through collaboration among CEH, SASA, SNH, and Forestry Commission Scotland.
- Data products are designed for reuse in policy planning, surveillance prioritization, and broader data-sharing within the heathland management and plant health communities.
- Documentation includes detailed methodology, data lineage, and field definitions to support transparency and reproducibility.

## Appendix and methodological notes
- Appendix A: detailed scoring framework for proximity to premises, larch proximity and infection, host species abundance (VM, VV, AU), climatic suitability, and proximity to water courses and roads.
- Modelling methodology: detailed GLMM structure, Bayesian estimation, and handling of interval-censored DOMIN data to derive presence/absence and abundance components.
- The document provides guidance on data gaps, uncertainty handling, and how to interpret risk scores in the presence of incomplete data.