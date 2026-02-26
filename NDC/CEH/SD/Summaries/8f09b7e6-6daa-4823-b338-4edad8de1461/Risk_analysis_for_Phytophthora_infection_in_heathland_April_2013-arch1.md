# The risk analysis for Phytophthora infection in heathlands fragments across Scotland

- Purpose and scope
  - Update risk analysis to include new infection sites in larch woodlands and garden/trade premises; use a climate suitability model to estimate climatically driven infection risk for two Phytophthora species (P. ramorum and P. kernoviae).
  - Produce risk maps showing how climate and host suitability create differing geographic risk patterns between species; highlight regions with high predicted risk even where no current infections exist.

- Data sources and risk factors
  - Heathland fragments: CEH Landcover Map 2007, BH_10 (heather and dwarf shrub, burnt heather, gorse, dry heath) and BH_11 (heather grass) across Scotland; 112,977 BH_10 polygons and 182,544 BH_11 polygons.
  - Infection data: current outbreaks in premises (gardens and trade premises) and larch infections up to 2013, with proximity analyses using a 1.5 km buffer.
  - Host plant abundance: Vaccinium myrtillus, V. vitis-idaea, Arctostaphylos uva-ursi modeled at 1 km resolution using DOMIN cover classes; host data derived from SNH NVC surveys (994 sites with varying presence/cover).
  - Climate and other risk factors: climatic suitability for each pathogen; proximity to infected/uninfected premises; proximity to larch; proximity to roads and rivers; additional habitat and topographical factors.

- Modelling host plant distributions (Appendix B)
  - Data and approach
    - Presence/absence phase: overdispersed binomial GLMM with site and quadrat random effects to handle zero-inflation and overdispersion.
    - Abundance phase: for sites with presence, a logit-normal model for percent cover with site and quadrat random effects; interval censoring to reflect DOMIN class uncertainty.
    - Bayesian framework used to estimate latent variables and account for uncertainty.
  - Predictors used
    - Climate (temperature, precipitation, seasonality), soil properties (water content, pH, carbon), topography (elevation, aspect), grazing pressure (sheep and red deer density), habitat (conifer and broadleaf cover, bracken patches).
  - Validation
    - Training AUCs > 0.90; test AUCs ~0.77–0.85 (good discrimination; typical threshold ~0.80+ for strong models).
  - Key findings
    - Vaccinium myrtillus: abundance driven by temperature, precipitation, soil properties, elevation, herbivore density, bracken, and woodland cover; predicted more in eastern Scotland, with some west coast underprediction due to data gaps.
    - Vaccinium vitis-idaea and Arctostaphylos uva-ursi: similar climate/soil drivers; distributions predicted with regional variation; some west underprediction noted.

- Risk scoring framework
  - Species-specific maximum risk scores: Pr (P. ramorum) up to 14; Pk (P. kernoviae) up to 13.
  - Weighted risk factors (per Table 1 design)
    - Premises proximity within 1.5 km: uninfected (0), uninfected near infected premises (1), infected within 1.5 km (2).
    - Larch proximity (within 5 km) and larch infections (within 5 km; within 500 m for higher scores up to 3).
    - Host species abundance: presence/absence and DOMIN class-based scoring for V. myrtillus, V. vitis-idaea, A. uva-ursi.
    - Climatic suitability: pathogen-specific thresholds (Pr: 100–150 days, 150–200 days, >200 days; Pk: <100, 100–150, 150–200, >200 days; higher days yield higher scores).
    - Water courses and roads: proximity adds risk.
  - Data gaps and uncertainty
    - Missing climate or host data flagged (missing_type); final risk scores adjusted to reflect data availability; uncertainty metrics (Uncert_pr, Uncert_pk) quantify data gaps and influence on risk estimates.
  - Outputs
    - Output formats capture risk factors and scores per heathland fragment:
      - BH_10.xlsx and BH_11.xlsx: risk factors and scores with fields such as PARCEL_ID, roads, rivers, DOMIN for each host species, Climsuit_p, Climsuit_1, prem_score, larch_sc_3, Vm_score, Vv_score, AS_score, clim_sco_3, clim_sco_4, road_score, river_sco_3, Avail_pr, Avail_pk, Risk_sco_3, Risk_sco_4, Adj_risk_p, Uncert_pr, Adj_risk_3, Uncert_pk, missing_type.
      - BH_10.shp and BH_11.shp: ArcGIS shapefiles with full calculation details and original CEH fields; JOIN via PARCEL_ID; recommended risk measures are Adj_risk_p (Pr) and Adj_risk_3 (Pk).
  - Output interpretation
    - adj_risk_p and adj_risk_3 provide adjusted risk scores taking into account the maximum possible scores given available data.
    - Avail_pr and Avail_pk indicate the maximum achievable score given current data for each pathogen.
    - Uncert_pr and Uncert_pk quantify uncertainty due to missing data.

- Geographic results and interpretation
  - Phytophthora ramorum (Pr)
    - High climate and host suitability in southern and western Scotland; risk is concentrated in these regions with current infection sites reinforcing risk patterns.
    - Notable risk in south-central Scotland even where current outbreaks are absent.
    - North Scotland shows fewer high-risk areas, with some isolated pockets.
  - Phytophthora kernoviae (Pk)
    - Greater risk in central Highlands and north Highlands due to climate and host suitability.
    - Additional high-risk areas exist but are less extensive than Pr in the south; overall, different regional emphasis compared with Pr.
  - Overall message
    - Climate suitability and host plant distributions create distinct, species-specific risk landscapes; premises and larch infection data strongly shape the southern/western patterns for both species, while central-northern Scotland shows notable Pk risk due to climate/host factors.

- Data quality, limitations, and usage notes
  - Climate data gaps and host habitat data gaps introduce uncertainty; missing_type flags indicate which factors are missing.
  - The risk maps provide relative (not directly comparable) risk by species due to species-specific climate scoring.
  - Some western regions may be underrepresented in host abundance data, potentially underestimating risk there.

- Appendices (highlights)
  - Appendix A: detailed scoring rules for premises proximity, larch proximity and infection, host abundance categories (Vaccinium myrtillus, V. vitis-idaea, Arctostaphylos uva-ursi), and climate thresholds; example scoring per factor.
  - Appendix B: modelling approach for heathland host plants (GLMMs in a Bayesian framework) including handling of overdispersion, interval-censored DOMIN data, latent variables, and the two-phase presence-absence then abundance modelling structure.