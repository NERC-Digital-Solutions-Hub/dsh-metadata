# April 2013

## Overview
- Update to the risk analysis of Phytophthora infection in heathland fragments across Scotland, incorporating new infection sites in larch woodlands and in garden/trade premises.
- Introduction of a climate suitability model to estimate climatically driven infection risk, with pathogen-specific risk maps for P. ramorum (Pr) and P. kernoviae (Pk).
- Finding: climate and host suitability strongly influence national-scale risk; high climate suitability for Pr in several regions and varying patterns for Pk; some areas with high predicted risk despite no known infections.

## Data sources and holdings
- Heathland fragments: two GIS datasets (BH_10_Scotland and BH_11_Scotland) derived from the CEH Land Cover Map 2007, comprising 112,977 BH_10 and 182,544 BH_11 polygons.
- Premises and host infection data: current infection data up to May 2013 from SASA, FC Scotland, St Andrews University; updated to include new premises and larch infections.
- Proximity factors: distances to premises (1.5 km buffer) and larch outbreaks (within 5 km, plus more detailed proximity metrics).
- Host plant distribution data: abundance estimates for Vaccinium myrtillus, V. vitis-idaea, and Arctostaphylos uva-ursi derived from NVC heathland surveys (994 records; DOMIN cover classes 0–10).
- Environmental predictors: climate (Bioclim variables), soil (Macaulay Soil Map), topography (SRTM), grazing pressure (deer and sheep densities), habitat composition (LCM2000).
- Data handling notes: Scotland-wide layers may have data access restrictions for some risk factors; missing data indicators (missing_type) used to flag climate or host data gaps.

## Modelling approach

### Heathland risk framework
- Two pathogen-specific risk scores (Pr and Pk) calculated by weighting factors:
  - Premises proximity and infection status (infected, uninfected, none nearby)
  - Proximity to larch woodlands and larch infections
  - Host plant abundance for V. myrtillus, V. vitis-idaea, A. uva-ursi (DOMIN-based categories)
  - Climatic suitability for each pathogen
  - Proximity to water courses and roads
- Factor weights chosen in agreement with SASA and SNH; maximum risk scores differ by pathogen (Pr up to 14, Pk up to 13).
- Climate scoring tailored separately for Pr and Pk due to Scotland’s differential suitability, enabling comparative spatial patterns even if absolute scores differ between species.
- Model outputs include risk factors and two main risk scores:
  - Risk_sco_3 (Pr) and Risk_sco_4 (Pk)
  - Adj_risk_p (adjusted Pr risk) and Adj_risk_3 (adjusted Pk risk) to reflect factor availability and data gaps.

### Host species distribution modelling
- Objective: predict abundance (percent cover) of heathland host species across BH_10 and BH_11.
- Modelling approach:
  - Phase 1: presence/absence modeled with an overdispersed binomial GLMM, incorporating site (g_i) and quadrat (h_ij) random effects to handle between-site variability and quadrat-level overdispersion.
  - Phase 2: conditional on presence, abundance modeled with a logit-normal GLMM to handle interval-censored DOMIN-class data (latent true percent cover).
  - Bayesian framework used to incorporate censoring and random effects.
- Data and validation:
  - 994 NVC surveys; presence/absence and DOMIN-class-derived abundance.
  - Training/testing: 70% of data used for training; 30% for testing.
  - Model performance: training AUC > 0.90; test AUCs around 0.77–0.85 (indicating good predictive capability, with some regional underprediction in the far west due to data gaps).
- Important drivers identified:
  - Vaccinium myrtillus: influenced by temperature, precipitation, soil pH and water content, elevation, grazing, and conifer/broadleaf woodland cover; most abundant in eastern Scotland.
  - Vaccinium vitis-idaea: influenced by temperature, precipitation, soil water, elevation, grazing, and bracken presence; less common, with higher predicted abundance in central/northern Scotland.
  - Arctostaphylos uva-ursi: influenced by temperature, precipitation, soil characteristics, elevation/aspect, grazing, and woodland cover; predicted to be less widespread, with greatest abundance in northern-central Scotland.
- Uncertainty handling: missing climate and hostData flagged; final fragment risk scores adjusted to reflect available data; missing_type field indicates which factors were missing.

## Outputs and data formats

- Data products
  - BH_10.xlsx and BH_11.xlsx: tabular risk factor data and scores per heathland fragment.
  - BH_10.shp and BH_11.shp: GIS shapefiles with full calculation details and original CEH Landcover fields.
- Linking key: PARCEL_ID used to join excel and shapefile data.
- Field descriptions (highlights)
  - PARCEL_ID: fragment identifier
  - Climsuit_p (Pk) and Climsuit_1 (Pr): climate suitability days
  - prem_score, larch_sc_3, Vm_score, Vv_score, AS_score: risk-factor scores for respective indicators
  - clim_sco_3 (Pr) and clim_sco_4 (Pk): climate-related scores
  - adj_risk_p (Pr) and adj_risk_3 (Pk): adjusted risk scores used for interpretation
  - Risk_sco_3 and Risk_sco_4: aggregate risk scores prior to adjustment
  - missing_type: indicator of missing data (climate, host, both)
- Additional notes
  - Appendix A/B provide detailed methods for risk factor extraction and habitat modelling
  - Appendix includes data processing steps (e.g., use of SummaryStatisticsDeluxe_BP.py) and GIS workflows

## Results and interpretation

- Spatial patterns
  - For both pathogens, higher risk concentrated in the south and west where current infection sites exist (premises and larch infections).
  - Pk shows significant risk in central and northern Scotland due to climate and host suitability.
  - Pr exhibits notable risk in the south-central region despite fewer observed infections there.
- Visual outputs
  - Maps (Figures 7–14) illustrate Pr and Pk risk distributions across Scotland, overlaid with current infection points (premises and larch).
  - Uncertainty maps (Figures 5–6) indicate fragments with missing climate or host data, guiding interpretation and potential data collection needs.

## Data governance, quality, and stewardship implications

- Data provenance and update cycles
  - Updated risk assessment incorporating new infection sites up to 2013; plans implied for ongoing updates as new outbreak and environmental data become available.
- Data interoperability and standards
  - Use of consistent fragment identifiers (PARCEL_ID) to link datasets; two formats (Excel and GIS shapefiles) to accommodate tabular analyses and spatial queries.
  - Clear documentation of fields and modelling steps (Tables/Apendices) to support reproducibility.
- Data completeness and uncertainty
  - Systematic tagging of missing data and explicit adjustment of risk scores to account for data gaps; emphasis on uncertainty measures (uncert_prk/uncert_pk).
- Access and sharing considerations
  - Acknowledgement of data access restrictions for certain risk-factor layers; outputs are designed for use with linked identifiers and documented risk components.
- Governance recommendations for Data Stewards
  - Maintain provenance: archive source datasets (infection data, host data, environmental predictors) with timestamps.
  - Version and track updates: document revisions to infection sites, proxy layers, and modelling parameters.
  - Metadata standards: provide thorough field-level metadata (data type, units, data quality, missing data flags).
  - Data quality assurance: keep validation metrics (AUC values) and model assumptions transparent; monitor data gaps and update host/climate layers accordingly.
  - Reproducibility: preserve modelling code and GIS workflows (Appendices, Python scripts) to enable re-running analyses with new data.