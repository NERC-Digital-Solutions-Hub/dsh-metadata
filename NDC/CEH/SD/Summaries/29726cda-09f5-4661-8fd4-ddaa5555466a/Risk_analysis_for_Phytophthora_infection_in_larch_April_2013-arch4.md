# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) in Larch across Scotland April 2013

- Purpose and update
  - Updated risk analysis (since August 2012) to include new infection sites in larch woodlands and garden/trade premises.
  - Introduces a climate suitability model to estimate climatically-driven risk for each pathogen (Pr = P. ramorum, Pk = P. kernoviae).
  - Produces pathogen-specific risk maps, emphasizing climate and host suitability alongside infection locations.

- Data assets and sources
  - Larch datasets:
    - Larch_SC_March2012 (National Forest Estate sub-compartments)
    - Larch_Combined (private land fragments)
  - Risk factors data layers:
    - Proximity to infected premises (garden/trade premises) within 1.5 km
    - Proximity to infected larch within 500 m and 5,000 m
    - Host habitat: Rhododendron ponticum suitability (R. ponticum) and Vaccinium myrtillus (V. myrtillus) abundance
    - Climatic suitability for growth/sporulation by pathogen (per species)
    - Additional layers: roads and rivers within fragments
  - Infection outbreak data: premises and larch infection sites up to early/mid-2013 from FC Scotland and SASA
  - Output formats: CSV risk scores (LC_RISK.csv, SC_RISK.csv) and ArcGIS shapefiles (LC_RISK.shp, SC_RISK.shp)

- Methodology and modeling approaches
  - Host species models
    - Rhododendron ponticum: Maxent habitat suitability modeling (11 predictor datasets; AUC ~0.838)
    - Vaccinium myrtillus: Bayesian GLMM with a two-phase approach
      - Phase 1: presence/absence with a binomial GLMM
      - Phase 2: abundance (DOMIN classes) via a logit-normal model
      - Addressed data issues: overdispersion, varying quadrat/site samples, interval-censored DOMIN data
  - Predictor factors (1 km resolution)
    - Climate: mean temperature, precipitation, seasonality
    - Soil: water content, carbon content, pH
    - Topography: elevation, aspect
    - Grazing pressure: deer and sheep densities
    - Habitat: percent cover of coniferous/broadleaf woodland, bracken patches
  - Risk scoring and weighting
    - Pathway-specific risk scores (Pr max = 17, Pk max = 16)
    - Climate scoring differs by species due to differing climate suitability
    - Risk factors combined into overall scores with detailed weighting (see field descriptions)
  - Output data fields
    - Fields include: prem_score, larch_score, Rp_score, Vm_score, clim_score (Pr) / clim_sco_2 (Pk), road/river scores, and composite risk scores (Risk_score, Adj_risk_p, Adj_risk_2)
    - Uncertainty indicators: Uncert_pr, Uncert_pk
    - Missing data indicators: missing_type

- Key findings: risk patterns and drivers
  - Climate suitability vs. host presence drives national-scale risk more than infection location alone
  - Pr (P. ramorum) climate suitability is higher across Scotland than Pk
    - Average suitable days: Pr ~50–200 days/year (median 117.2), Pk typically <30 days/year (median 17.6)
  - Geographic risk patterns
    - Pr high-risk zones: south-west and parts of Dumfries and Galloway, eastern Strathclyde, Arran/Argyll, central belt
    - Pk high-risk zones: similar south-west emphasis but relatively higher central/east risk due to climate suitability
  - Host habitat predictions
    - R. ponticum: ~24% of 1 km grid cells predicted suitable; favored by continuous broadleaved woodland, lower elevation, moderate soil moisture
    - V. myrtillus: presence and higher abundance predicted to be more common on the west coast (e.g., Argyll and Bute), influenced by temperature, precipitation, soil pH, carbon/water content, elevation, bracken presence, and grazing
  - Data limitations and uncertainty
    - Missing data in several fragments for Vaccinium suitability and climate data; uncertainty mapped and adjusted scores
    - Spatial uncertainty higher at fragment edges and where covariates are incomplete

- Data products and accessibility for governance
  - Outputs provided as:
    - Risk scores CSV files: LC_RISK.csv (private land), SC_RISK.csv (national forest estate)
    - Risk score ArcGIS shapefiles: LC_RISK.shp, SC_RISK.shp
  - Linking guidance
    - Use OBJECTID (LC) or SUBCOMPTID (SC) to join risk scores with fragments
    - Key scoring fields to interpret risk: adj_risk_p (Pr) and adj_risk_2 (Pk)
  - Documentation of fields and methodology included in appendices for reproducibility

- Implications for data strategy and action
  - Demonstrates integration of multiple data sources (infections, host species distributions, climate, and land cover) to produce species-specific risk maps
  - Highlights importance of data standardization, metadata, and handling of missing/uncertain data for risk modeling
  - Supports targeted surveillance, management, and resource allocation by identifying high-risk regions and drivers
  - Indicates need for ongoing data sharing across partners (FC Scotland, SASA, SC authorities) and transparent uncertainty reporting
  - Provides a replicable framework for updating risk assessments as new infection sites and climate data become available

- Endnotes and appendix highlights (for data teams)
  - Appendix documents detailed modeling structures for V. myrtillus and R. ponticum
  - Describes data processing steps, weighting schemas, and proximity analyses in ArcGIS
  - Notes data access restrictions and the rationale for species-specific climate scoring to preserve meaningful spatial variation in risk