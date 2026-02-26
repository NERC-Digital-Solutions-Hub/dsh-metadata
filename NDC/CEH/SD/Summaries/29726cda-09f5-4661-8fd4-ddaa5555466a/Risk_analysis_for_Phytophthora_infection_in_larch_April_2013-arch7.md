# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) in Larch across Scotland April 2013

## Overview
- Updated analysis (from August 2012) incorporating new infection sites in larch woodlands, gardens, and trade premises.
- Introduces a climate suitability model to estimate climatically driven infection risk, yielding pathogen-specific risk maps.
- Climate suitability predicts Scotland is more conducive to P. ramorum than P. kernoviae; differing regional risk patterns for the two species.
- Risk maps emphasize climate and host suitability alongside presence of infected larch and premises as risk drivers.

## Data and inputs
- Larch fragment datasets (risk factors derived from FC data):
  - Larch_SC_March2012 (SC): 16,090 fragments
  - Larch_Combined (LC): 10,363 fragments
- Risk factors considered (mapped to fragments):
  - Habitat suitability for Rhododendron ponticum (RP)
  - Abundance of Vaccinium myrtillus (VM)
  - Climatic suitability for pathogen growth and sporulation (Pr and Pk)
  - Proximity to inspected garden/trade premises (within 1.5 km)
  - Proximity to infected larch (within 500 m or 5,000 m)
  - Presence of roads and rivers within fragment
- Access constraints: Scotland-wide maps of some risk factors not provided due to data access restrictions.

## Modelling approach for host species
- Rhododendron ponticum (RP)
  - Maxent habitat suitability modelling using 11 data layers; model performance: training AUC ~0.838, test AUC ~0.838.
  - Continuous broadleaf woodland, low elevation (<400 m), moderate soil moisture (or EVIs) favored RP presence.
  - Predicted suitable RP habitat in Scotland covers about 24% of 1 km grid cells.
- Vaccinium myrtillus (VM)
  - Abundance model using a two-stage Bayesian GLMM approach to handle presence/absence and then abundance (DOMIN scale) with interval-censored data.
  - Predictors include climate (temp, precip), soil properties (pH, carbon, water content), elevation, bracken, deer and sheep grazing, woodland fragmentation.
  - VM presence influenced by temperature, precipitation, soil properties, elevation, bracken, grazing, and fragmentation; hotspots predicted in west Scotland (e.g., Argyll and Bute).
  - VM abundance shows higher predicted DOMIN classes in core native woodlands on the west coast.
- Modelling outputs are produced at 1 km resolution for the VM component and used to derive risk factors.

## Climatic suitability and risk scoring framework
- Climatic thresholds are species-specific:
  - P. ramorum: 50–200+ days suitable (modeled as higher suitability in regions like south-west and central Scotland)
  - P. kernoviae: typically < 17.5 days suitable (relative climate suitability generally lower in Scotland)
- Risk factor weighting (Table 1) determines maximum risk scores:
  - Pr (P. ramorum) maximum score: 17
  - Pk (P. kernoviae) maximum score: 16
- Risk scores are calculated per fragment by summing factor scores; climate is scored separately for the two species.
- Resulting risk maps show relative spatial variation by species; not directly comparable across species due to different climate scoring.

## Risk factors and weighting (highlights)
- Premises proximity (within 1.5 km, 250 m, etc.) with scores 0–3 depending on proximity and infection status.
- Larch infection proximity (within 5 km, 500 m) with scores 0–4.
- RP habitat suitability score (0 for unsuitable, 3 for suitable).
- VM abundance score (0 for absent, 1–2 for low to high abundance).
- Climatic suitability scores for Pr and Pk (range 0–3 for Pr; 0–2 for Pk, depending on thresholds).
- Watercourses and roads within fragment contributing modest scores (0 or 1).
- Outputs include fields for maximum achievable score given available data and data uncertainty measures.

## Outputs and data products
- Data formats provided for practical GIS use:
  - CSV risk score files: LC_RISK.csv (Larch_Combined) and SC_RISK.csv (Larch_SC_March2012)
  - Shapefiles: LC_RISK.shp (Larch_Combined) and SC_RISK.shp (Larch_SC_March2012)
- Key output fields (examples):
  - OBJECTID; ROAD; RIVER; AvRhodoHS (RP habitat suitability); DOMIN22 (VM abundance); Climsuit_p (Pk climate suitability); Climsuit_pr (Pr climate suitability)
  - prem_score; Larch_scor; Rp_score; Vm_score; clim_score; clim_sco_2
  - road_score; river_scor; adj_risk_p (adjusted Pr risk); adj_risk_2 (adjusted Pk risk)
  - Uncert_pr; Uncert_pk; missing_type
- Linking between formats:
  - CSV and Shapefiles linked via OBJECTID (LC) or SUBCOMPTID (SC)
- Output emphasis:
  - Focus on adj_risk_p and adj_risk_2 as practical risk indicators for management and decision-making.

## Results: spatial patterns and interpretation
- P. ramorum risk (Pr)
  - Higher risk in the south-west and parts of central Scotland; influenced by climate suitability and presence of infected premises/ larch infections.
  - Notable high-risk zones include Dumfries and Galloway, eastern Strathclyde, central Scotland up to Argyll.
- P. kernoviae risk (Pk)
  - Similar southwest-dominant pattern but with relatively higher risk in central and eastern Scotland due to climate suitability differences.
  - Overall climate suitability for Pk is lower than for Pr, yet regional patterns differ, with central/east areas showing relatively higher suitability for Pk than for Pr in some locales.
- Maps incorporate known infection data and host/climate suitability; demonstrate geographic heterogeneity in risk between species.

## Uncertainty, data gaps, and GIS considerations
- Data gaps in VM habitat data and climate layers create uncertainty in risk scores; uncertainty metrics are provided (e.g., Uncert_pr, Uncert_pk).
- Missing data types indicated (missing_type) and adjusted risk scores account for data completeness.
- Some layers are not provided Scotland-wide due to access restrictions; results are spatially explicit at fragment scales and require GIS handling for map production and interpretation.

## How to use these data products (GIS-focused)
- Use the SC_RISK.shp and LC_RISK.shp layers to visualize and query risk by fragment, with fields for climate, host presence, and proximity scores.
- Compare Pr and Pk risk surfaces to assess pathogen-specific management priorities.
- Overlay risk surfaces with known larch infection sites and premises data to identify hotspots and surveillance targets.
- Leverage adj_risk_p and adj_risk_2 for prioritizing interventions under species-specific climate scenarios.
- Utilize the VM and RP host models to interpret risk drivers and to refine local surveillance and habitat management.

## Appendices and methodological notes (summary)
- Detailed modelling equations for VM presence and abundance (Bayesian GLMM with interval-censored DOMIN data).
- Maxent modelling approach for RP habitat suitability with model validation metrics.
- Table-based risk scoring framework (Table 1) and field descriptions (Table 3) for output data.
- GIS workflow notes include proximity calculations, zonal statistics for climate suitability, and data integration steps for producing the risk scores.