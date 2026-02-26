# Risk analysis for Phytophthora infection in heathlands fragments across Scotland

- The study updates risk assessment for Phytophthora infection in Scottish heathland fragments, incorporating new infection sites (larch woodlands and garden/trade premises) and a climate suitability model that yields pathogen-specific risk estimates.
- Two pathogens are considered: Phytophthora ramorum (Pr) and Phytophthora kernoviae (Pk); risk maps are produced separately for each species.

## Aim and scope

- Demonstrate climate- and host-driven infection risk in heathland fragments using standardized, comparable outputs.
- Highlight geographic variation in climate suitability and host presence that shapes risk patterns for each pathogen.

## Data and inputs

- Heathland fragments from CEH Land Cover Map 2007:
  - BH_10: Heather and dwarf shrub, burnt heather, gorse, dry heath
  - BH_11: Heather grass
- Risk factors include:
  - Host plant abundance: Vaccinium myrtillus, V. vitis-idaea, Arctostaphylos uva-ursi (derived from NVC surveys; DOMIN cover classes 0–10)
  - Climate suitability for growth and sporulation (pathogen-specific)
  - Proximity to larch woodlands
  - Proximity to inspected garden/trade premises and infected premises
  - Proximity to roads and rivers
- Geographic scope: Scotland (UK-wide layers clipped to Scotland)

## Modelling approach

- Host abundance modelling (three species):
  - GLMM-based two-phase approach within a Bayesian framework:
    - Phase 1: presence/absence using an overdispersed binomial GLMM (with site and quadrat random effects)
    - Phase 2: conditional abundance (percent cover) for sites with presence, using a logit-normal model
  - Latent variables account for interval-censored DOMIN class data
  - Models validated with training/test splits; AUCs: training >0.90; test ~0.80–0.85
- Climate suitability modelling:
  - Species- and region-specific climate scores (days/year suitable for infection)
  - Uses area-weighted climate outputs; incorporates host presence and proximity factors
- Risk scoring framework:
  - Two pathogen-specific risk scores per fragment: Pr (0–14) and Pk (0–13)
  - Weighting applied to factors (premises proximity, larch proximity/infection, host species abundance, climate suitability, water/roads presence)
  - Data gaps handled by adjusting maximum possible scores; climate and host data missingness tracked
- Output formats and linking:
  - Data provided in two formats:
    - BH_10.xlsx and BH_11.xlsx (risk factors and scores)
    - BH_10.shp and BH_11.shp (full calculations and original fields from CEH LCM2007)
  - PARCEL_ID serves as the key to link formats
  - Key output fields: adj_risk_p (Pr) and adj_risk_3 (Pk)

## Key results and interpretation

- Climate suitability differences:
  - Scotland is markedly more climatically suitable for Pr than for Pk.
  - Pk: typically fewer than 30 days/year suitable (median ~17.6; mean ~17.5)
  - Pr: between ~50 and ~200 days/year suitable (median ~117.2; mean ~118.4)
- Geographic risk patterns:
  - For both pathogens, current known infections (premises) and larch infections drive higher risk in the south and west.
  - Pk shows additional high-risk areas in central and northern Scotland due to climate and host suitability.
  - Pr presents notable risk in the south-central region despite fewer known infections, due to host/climate compatibility.
- Risk scoring visualization:
  - Maps categorize fragments from low (green) to high risk (yellow/red) for each pathogen.
  - Figures illustrate risk across regions and alongside infection sites.

## Outputs and data accessibility

- Outputs provided to support monitoring and policy scrutiny:
  - Fragment-level risk scores and underlying factors (BH_10 and BH_11)
  - Spatial representations (ArcGIS shapefiles) with full calculation details
- Key fields for decision use:
  - adj_risk_p (Pr) and adj_risk_3 (Pk) as primary risk indicators
  - Fields documenting risk factor presence/absence and data uncertainty
- Handling of missing data:
  - Clear mapping of fragments with climate data gaps (blue) and host data gaps (red)
  - Uncertainty quantified; final risk scores adjusted by available data

## Practical implications for analysts

- Standardized, species-specific risk outputs enable consistent monitoring of environmental health and policy effectiveness over time.
- Data products are designed for integration into portals and maps, supporting transparent scrutiny of environmental risk.
- The two-stage host modelling and Bayesian framework provide robust estimates under data sparsity and interval-censored observations, improving confidence in risk assessments.

## Appendices and methodological notes

- Appendix A details scoring rules for each risk factor (premises, larch proximity/infection, host abundance, climatic suitability, roads, rivers).
- Appendix B outlines modelling choices for host species abundance, including covariates used (climate, soil, topography, grazing, habitat), and modelling rationale for using a two-stage GLMM with latent variables.