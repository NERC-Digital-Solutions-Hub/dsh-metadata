# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) in Larch across Scotland April 2013

- Purpose: update risk analysis for Phytophthora infection in larch across Scotland, incorporating new infection sites and a climate suitability model to produce pathogen-specific risk maps and prioritised surveillance areas.

- Key advancement: use of a climate suitability model that estimates the number of suitable days per year for pathogen transmission, with separate models for P. ramorum (Pr) and P. kernoviae (Pk).

- Outputs: risk maps showing geographic patterns of relative risk for each pathogen species, emphasizing climate and host suitability alongside presence of infected premises and infected larch.

- Data sources and scope:
  - Larch datasets: two GIS-derived fragments datasets from Forestry Commission Scotland
    - Larch_SC_March2012 (SC): 16,090 fragments
    - Larch_Combined (LC): 10,363 fragments
  - Risk factors mapped for each fragment (national-scale risk factors not all shown due to data access restrictions)
    - Habitat suitability for Rhododendron ponticum (R. ponticum) as a reservoir host
    - Abundance of Vaccinium myrtillus (VM) as a secondary host
    - Climatic suitability for growth and sporulation (pathogen- and species-specific thresholds)
    - Proximity to garden or trade premises (within 1.5 km buffer)
    - Proximity to infected larch within 500 m or 5,000 m
    - Presence of roads and rivers within the fragment

- Host species modelling approaches:
  - Rhododendron ponticum:
    - MaxEnt modelling using 11 datasets (1691 points, 8455 polygons)
    - Predictor factors: landscape, soil, climate
    - Output: habitat suitability map with predicted suitable areas (half a dozen regions highlighted as core areas)
    - Model performance: training AUC ≈ 0.838; test AUC ≈ 0.838
  - Vaccinium myrtillus:
    - Data: 335 NVC surveys; 89 non-zero abundance records
    - Abundance measured on DOMIN scale (11 classes)
    - Modelling approach: two-phase Bayesian GLMM
      - Phase 1: presence/absence (overdispersed binomial GLMM)
      - Phase 2: given presence, abundance (logit-normal GLMM)
    - Covariates: climate, soil, topography, grazing, habitat fragmentation
    - Resolution: 1 km
    - Key predictors for presence: annual mean temperature, precipitation, soil pH and carbon content, elevation, bracken presence, deer and sheep grazing, woodland fragmentation
    - Abundance hotspots: west coast (e.g., Argyll and Bute)
  - Climate and other factors for P. ramorum and P. kernoviae:
    - Climate suitability calculated as days with suitable conditions, specific to each pathogen
    - Table 1 factors include: proximity metrics, host habitat suitability, and climatic thresholds

- Risk scoring framework:
  - Overall risk score per larch fragment combines multiple factors (Tables 1 and Appendix)
  - Two separate climate scores:
    - Climatic suitability for P. ramorum (Pr): 0–3 points
    - Climatic suitability for P. kernoviae (Pk): 0–3 points
    - Scotland predicted to be much more climatically suitable for Pr than for Pk
  - Proximity and host factors contribute additively:
    - Premises proximity (0–3)
    - Larch infection proximity (0–4)
    - Rhododendron ponticum habitat suitability (0–3)
    - Vaccinium myrtillus abundance (0–2)
    - Road proximity (0–1)
    - Rivers proximity (0–1)
  - Maximum possible scores:
    - Pr: up to 17
    - Pk: up to 16
  - Outputs and data formats:
    - Risk scores provided in two formats per dataset:
      - LC_RISK.csv and SC_RISK.csv (risk scores only)
      - LC_RISK.shp and SC_RISK.shp (full risk calculation fields)
    - Key fields in outputs include:
      - OBJECTID (fragment ID), prem_score, larch_score, Rp_score, Vm_score, clim_score (Pr), clim_sco_2 (Pk), road_score, river_score
      - Climsuit_pr (Pr climate days), clim_suit (Pk climate days)
      - Risk_score (sum for Pr), Risk_sco_2 (sum for Pk)
      - Adj_risk_p and Adj_risk_2 (risk adjusted by maximum possible score given data availability)
      - Uncert_pr and Uncert_pk (data uncertainty based on missing factors)
      - missing_type (indicates which factors are missing)
  - Usage note: risk maps are species-specific due to differing climate suitability; other risk factors are common to both pathogens

- Spatial results and interpretation:
  - Pr risk:
    - Higher risk in the south-west and western Scotland; notable hotspots in Dumfries and Galloway extending into eastern Strathclyde, north of Arran, and Argyll
  - Pk risk:
    - Overall pattern similar to Pr with high risk in the south-west; comparatively higher risk in central and eastern Scotland due to climate suitability
  - Infected premises and larch distributions contribute to elevated risk in certain zones, but climate and host suitability are key drivers

- Data quality, gaps, and governance:
  - Recognises missing data for several risk factors; results include uncertainty measures
  - Data gaps addressed by adjusting risk scores and providing explicit uncertainty indicators
  - Outputs are designed for integration into monitoring and decision-making processes, supporting prioritisation of surveillance, resource allocation, and risk communication
  - Data formats (CSV and shapefiles) enable incorporation into dashboards and GIS-based monitoring tools
  - Documentation includes methodological details and field descriptions to support auditability and data governance

- Practical implications for monitoring frameworks:
  - The approach offers a structured, data-driven way to monitor Phytophthora infection risk across Scotland by fragment
  - Supports policy decisions on where to intensify surveillance, preventive measures, and response planning
  - Highlights the importance of maintaining metadata, data accessibility, and transparent data sharing to overcome barriers noted in monitoring frameworks (data gaps, silos, and governance)