# Risk analysis for Phytophthora infection in heathlands fragments across Scotland

## Overview
- Updated risk analysis incorporating new infection sites in larch woodlands and garden/trade premises.
- Introduces a climate suitability model to estimate climatically driven infection risk, with pathogen-specific risk maps for P. ramorum (Pr) and P. kernoviae (Pk).
- Reveals geographic differences in climate suitability and host presence, with high predicted risk in areas not currently known to be infected.

## Data and sources
- Heathland fragments derived from CEH Land Cover Map 2007, comprising BH_10 (112,977 polygons) and BH_11 (182,544 polygons) for Scotland.
- Infection data from SasA/FC Scotland, updated up to May 2013 for premises and larch infections.
- Host plant data for Vaccinium myrtillus, V. vitis-idaea, Arctostaphylos uva-ursi obtained from SNH NVC surveys; host abundance mapped on the DOMIN scale (1–10).
- Climate, soil, topography, grazing (red deer density, sheep numbers) and habitat cover (conifer/broadleaf woodland, bracken) factors used to model host abundance and risk.

## Risk factors and scoring
- Two major risk score frameworks: Pr (Pr) and Pk (Pk), with maximum scores of 14 and 13 respectively.
- Weighting of risk factors established in consultation with SASA and SNH; factors include:
  - Proximity to premises (infected or uninfected) within 1.5 km
  - Proximity to larch and presence/infection status of larch within defined buffers
  - Abundance of heathland host species (VM, VV, AU) using DOMIN-derived classes
  - Climatic suitability for each pathogen (days suitable per year)
  - Proximity to water courses and roads
- Data on host abundance derived from GLMM-based modelling (logit-normal) with presence/absence phase followed by abundance phase; models are Bayesian to handle interval-censored DOMIN data and random effects (site and quadrats).

## Modelling approach
- Presence/absence modelling: binomial GLMM with site and individual random effects, using predictors including climate, soil, elevation, deer and sheep density, and habitat characteristics.
- Abundance modelling (given presence): logit-normal GLMM for DOMIN class-derived proportions, with site and quadrat random effects to capture residual variation.
- Habitat suitability inputs: 1 km resolution incorporating climate, soil, topography, grazing, and habitat covariates.
- Model validation: training AUCs > 0.90 and test AUCs around 0.77–0.85 depending on species, indicating strong but species-specific predictive performance.
- Climate suitability thresholds differ by species, reflecting Scotland’s higher suitability for Pr relative to Pk.

## Outputs and data formats
- Outputs provided as two data formats:
  - Excel: BH_10.xlsx and BH_11.xlsx containing risk factors, scores, and derived metrics
  - ArcGIS shapefiles: BH_10.shp and BH_11.shp with full calculation details and original CEH-LCM fields
- Key fields include PARCEL_ID, proximity metrics, DOMIN-derived host scores, climate scores (Climsuit_1, Climsuit_p), and risk scores (risk_sco_3 for Pr, risk_sco_4 for Pk), plus Adjusted risk and data-uncertainty indicators (Adj_risk_p, Adj_risk_pk, Uncert_pr, Uncert_pk).
- Handling missing data: a missing_type field flags whether climate data, host data, or both are missing; final risk scores are adjusted for the maximum possible score given available data, with uncertainty quantified.

## Results: risk patterns and interpretation
- For both pathogens, highest risk concentrated in the south and west of Scotland near known infections in premises and larch woodlands.
- Pk shows additional significant risk in central and northern regions due to climate and host suitability; Pr risk is notable in south-central areas.
- Maps illustrate areas of low, medium, and high risk, with explicit accounting for data gaps.

## Data gaps, uncertainty, and governance
- Missing climate data (blue areas) common along the west coast; missing host data (red areas) more prevalent in eastern/southern regions.
- Uncertainty fields (Uncert_pr, Uncert_pk) accompany risk scores to reflect data gaps; fragments with missing data have adjusted risk estimates.
- Data sharing across agencies is essential but can be a barrier; outputs are provided in open formats to facilitate transparency and reproducibility.
- The framework emphasizes the need for metadata, standardised data sharing, and governance to sustain timely, quality-assured monitoring data.

## Implications for monitoring frameworks
- Demonstrates a practical, policy-relevant approach to monitoring environmental health risks by integrating pathogen, climate, host, and infrastructure data.
- Provides pathogen- and species-specific risk measures that can guide targeted surveillance, early-warning efforts, and resource allocation.
- Highlights the importance of:
  - Data integration across organisations and open data sharing
  - Metadata standardisation and data provenance
  - Transparent scoring systems with uncertainty quantification
  - Regular updates to incorporate new infection sites and climate data
- Useful for informing future monitoring decisions, data governance, and risk communication to stakeholders.