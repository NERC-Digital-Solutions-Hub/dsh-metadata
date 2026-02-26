# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) in Larch across Scotland April 2013

- Overall purpose
  - Update risk analysis for Phytophthora infection in Scottish larch, incorporating new infection sites and a climate suitability model to estimate climatically driven transmission risk for P. ramorum (Pr) and P. kernoviae (Pk).
  - Produce pathogen-specific risk maps and provide outputs suitable for monitoring and policy scrutiny.

- Key findings
  - Climate and host suitability strongly shape national risk patterns, with notable geographic differences between the two pathogens.
  - Scotland is predicted to be more climatically suitable for Pr than for Pk; average suitable days per year are higher for Pr (50–200 days; median ~117) than for Pk (generally <30 days; median ~17.6).
  - High Pr risk areas: predominantly in the south-west and parts of central Scotland (e.g., Dumfries and Galloway, eastern Strathclyde, Argyll, and Perthshire/ north Highlands).
  - High Pk risk areas: similar south-west pattern but relatively higher risk in central/east Scotland due to climate suitability differences, with northeast-to-central regions showing relatively greater Pk risk than Pr.

- Data sources and risk factors
  - Larch datasets: 16090 fragments on National Forest Estate (SC) and 10363 fragments on private land (LC).
  - Infection data: current larch infections and premises infection data provided by Forestry Commission Scotland (FC) and SASA; updated to include 2011–2013 outbreaks.
  - Proximity factors: distance to known infected premises (within 1.5 km, 250 m, 100 m) and proximity to infected larch within 5 km or 500 m.
  - Host-related factors:
    - Rhododendron ponticum habitat suitability (R. ponticum as a foliar reservoir) modeled with Maxent using 11 datasets.
    - Vaccinium myrtillus (V. myrtillus) abundance modeled across woodland fragments using a two-phase Bayesian GLMM (presence/absence and, if present, abundance via a logit-normal model) to handle data structure and interval censoring (DOMIN scale).
  - Climatic and environmental covariates: climate (temperature and precipitation metrics, BioClim variables), soil (water content, carbon, pH), elevation, aspect, grazing pressure (deer and sheep), habitat fragmentation (breadth of woodland types and fragmentation).

- Methods and modelling approach
  - Climate suitability modelling
    - Species- and strain-specific climate scoring to derive the number of suitable days per year for Pr and Pk.
    - Climate-based scores are combined with host and proximity factors to compute overall risk scores.
  - Host species modelling
    - Rhododendron ponticum: Maxent model with 11 predictor datasets; performance with training AUC ~0.838 and test AUC ~0.838.
    - Vaccinium myrtillus: presence/absence model (binomial GLMM) and abundance model (logit-normal GLMM) fitted within a Bayesian framework to handle interval-censored DOMIN data and site/quadrat random effects.
  - Weighting and risk scoring
    - Final risk factor weighting agreed with FC; total maximum risk scores: Pr up to 17, Pk up to 16.
    - Distinct climate scores for Pr and Pk to reflect species-specific climate suitability; enables clearer interpretation of spatial variation by pathogen.
  - Outputs and data formats
    - Risk scores produced for each larch fragment (Pr and Pk).
    - Data outputs provided in two formats:
      - Excel CSVs: LC_RISK.csv (Larch_Combined) and SC_RISK.csv (Larch_SC_March2012).
      - ArcGIS shapefiles: LC_RISK.shp and SC_RISK.shp, including all original FC fields plus risk calculations.
    - Key fields for use: adj_risk_p (Pr risk adjusted to maximum possible score given data), adj_risk_2 (Pk risk adjustment), and uncertainty indicators (Uncert_pr, uncert_pk), plus descriptive risk components (prem_score, larch_score, Rp_score, Vm_score, clim_score, clim_sco_2, road_score, river_score).

- Results: risk maps and interpretation
  - Pathogen-specific risk maps show:
    - Pr: high-risk zones concentrated in the south-west and parts of central Scotland; northeast areas generally lower risk.
    - Pk: similar south-west pattern but higher relative risk in central/east regions due to climate suitability.
  - Combined maps illustrate how proximity to infected premises and existing larch infections interact with climate and host habitat suitability to shape national risk.
  - Figures (summarised): separate maps for Pr and Pk risk scores across Scotland, with notable high-risk clusters corresponding to known infection sites and climatically suitable areas; uncertainty maps highlight data gaps, especially for V. myrtillus habitat and regional climate data.

- Handling data gaps and uncertainty
  - Acknowledges missing data for some larch fragments, especially for V. myrtillus habitat suitability and climate suitability layers.
  - Uncertainty is quantified in output (uncertainty metrics for Pr and Pk risk scores) and addressed through data completeness indicators and adjustments to scores where data are missing.

- Practical implications for monitoring and policy
  - The framework provides spatially explicit, pathogen-specific risk assessments to support environmental monitoring and policy evaluation over time.
  - Outputs are designed for integration into standard monitoring portals and datasets, enabling tracking of environmental condition and management effectiveness across Scotland.
  - The approach highlights the relative importance of climate suitability and host presence as drivers of infection risk, guiding targeted surveillance and management in high-risk areas.