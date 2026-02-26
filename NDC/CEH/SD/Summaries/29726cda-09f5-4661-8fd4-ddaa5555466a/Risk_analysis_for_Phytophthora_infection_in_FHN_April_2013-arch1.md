# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) Core Native Woodland fragments across Scotland April 2013

## Overview
- Update to the 2012 analysis incorporating new infection sites in larch woodlands and garden/trade premises (provided by FC Scotland and SASA).
- Introduces a climate suitability model that estimates climatically suitable days per year for pathogen transmission, species-specific for P. ramorum (Pr) and P. kernoviae (Pk).
- New risk maps produced for each pathogen; risk concentrated in southern and western Scotland driven by current infections and host/climate factors.
- For P. kernoviae, additional high-risk areas distant from known infections emerge, including the northeast, reflecting host availability and climate suitability.
- Climate and host presence identified as primary drivers of Phytophthora risk at national scale; surveillance should also target regions currently distant from known infections.

## Data and risk factors
- Core Native Woodland dataset: 79,269 fragments analyzed.
- Risk factors used:
  - Habitat suitability for Rhododendron ponticum (RP) – a reservoir host
  - Predicted abundance of Vaccinium myrtillus (VM)
  - Climatic suitability for growth/sporulation (species-specific: Pr and Pk)
  - Proximity to inspected garden/trade premises and to infected premises
  - Proximity to larch and infected larch
  - Fragment-level presence of roads and rivers
- Some Scotland-wide risk-factor layers are not provided in full due to data-access restrictions.

## Modelling approach and data sources
- Premises and infection data:
  - Compiled from 2011–2013 outbreaks, including new sites supplied by SASA and FC Scotland.
  - Spatial data for current infections, garden sites, and larch infections updated to construct the latest risk picture.
- Host modelling:
  - Rhododendron ponticum: MaxEnt modelling using 11 datasets; performance: training AUC ~0.838, test AUC ~0.838.
  - Vaccinium myrtillus: abundance modeled with a two-stage Bayesian GLMM to handle presence/absence and abundance separately, accounting for interval-censored DOMIN class data and random effects.
- Climate modelling:
  - Climate suitability quantified as the average number of climatically suitable days per year for each pathogen.
  - Scores are species-specific due to differing climate suitability; notably, Scotland is more favorable for Pr than for Pk.

## Risk scoring framework
- Final risk scores are computed per core native woodland fragment using a weighted combination of risk factors (Table 1 in the report). Key points:
  - Maximum risk scores: Pr = 17, Pk = 16.
  - Climate scores differ by species to reflect actual climate suitability differences.
  - Factor weights include:
    - Premises proximity (0, 1, 2, 3 depending on distance tiers)
    - Larch proximity (0, 2, 3, 4 depending on proximity and infection status)
    - Rhododendron ponticum habitat suitability (0–3)
    - Vaccinium myrtillus habitat suitability (0–2)
    - Climatic suitability for Pr (0–3)
    - Climatic suitability for Pk (0–2)
    - Water courses within fragment (0 or 1)
    - Roads within fragment (0 or 1)
- Output includes two main risk scores per fragment:
  - adj_risk_p: adjusted risk score for Pr
  - adj_risk_1: adjusted risk score for Pk
- Data gaps are explicitly acknowledged; missing climate or VM data are shown in maps, and risk scores are adjusted by the maximum possible score for available factors.

## Outputs and data formats
- Provided in two formats:
  - FHN_2013.csv: risk scores only
  - FHN_2013.shp: GIS shapefile with full calculation details and original fields
- Both formats can be linked via the fragment ID.
- Key fields to use:
  - adj_risk_p (Pr risk)
  - adj_risk_1 (Pk risk)
  - Avail_pr, Avail_pk (maximum possible scores given available data)
  - Uncert_pr, Uncert_pk (data uncertainty due to missing factors)
  - missing_type (indicates which factors are missing: clim, VM, both, or none)

## Results: spatial patterns and interpretation
- Distribution of risk:
  - Pr risk: high in southern and western Scotland; also notable in some parts of the north-east where host presence and climates favor infection.
  - Pk risk: similarly concentrated in the south/west but also with broader eastern/northeast spread due to climate suitability and host presence, with some areas distant from known infections showing elevated risk.
- Proximity to current premises and larch infections, as well as host availability, drive regional differences in risk.
- Figures (summarized):
  - Figures 6–13 illustrate Pr and Pk risk scores across Scotland, highlighting regional variations and the relation to known infections.

## Missing data and uncertainty
- Some fragments lack climate data or VM habitat suitability data, mapped to show increased uncertainty.
- Missing data handled by adjusting fragment risk scores to reflect available information.
- Data gaps highlighted for planners to assess confidence in risk estimates.

## Appendices: modelling details
- V. myrtillus modelling:
  - Addressed overdispersion and interval-censored DOMIN data via a two-phase GLMM approach within a Bayesian framework.
  - Phase 1: presence/absence modeled with a binomial GLMM, including site and quadrat random effects.
  - Phase 2: abundance modeled for sites with presence, using a logit-normal model with site and quadrat random effects.
  - Covariates included climate, soil, topography, grazing pressure, and habitat fragmentation metrics.
- Rhododendron ponticum modelling:
  - Maxent models using 11 datasets; predicting suitable RP habitat across Scotland.
- Field descriptions:
  - Tables detailing field names and their associated risk scores (e.g., clim_sco_1 for Pr, Clim_sco_2 for Pk, Rp_score, Vm_score, etc.).

## Practical implications for surveillance and management
- Focus surveillance efforts on regions with high adj_risk_p and adj_risk_1, especially in areas with favorable host presence and climate, including regions beyond current infection locations.
- Recognize that Pr generally has higher climatic suitability in Scotland, influencing overall risk patterns.
- Use the provided CSV and shapefile outputs to identify high-risk fragments and prioritize monitoring, biosecurity, and mitigation actions.