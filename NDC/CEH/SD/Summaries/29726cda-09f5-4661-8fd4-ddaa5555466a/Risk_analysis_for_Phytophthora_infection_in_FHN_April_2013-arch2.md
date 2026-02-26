# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) Core Native Woodland fragments across Scotland April  2013

## Overview
- Updated risk analysis for Phytophthora infection in core native woodland fragments across Scotland, building on August 2012 version.
- Adds new infection sites in larch woodlands and garden/trade premises (from FC Scotland and SASA).
- Uses a climate suitability model to estimate climatically driven infection risk, producing pathogen-specific risk maps.
- Findings: risk concentrated in the south and west of Scotland, aligned with current infections; P. kernoviae shows notable risk in additional areas distant from known infections, with northeast Scotland showing high risk for P. kernoviae due to hosts and climate suitability.
- Conclusion: climate and host distribution are major drivers of national-scale Phytophthora risk; identifies regions for enhanced surveillance beyond currently infected sites.

## Data and sources
- Core Native Woodland: 79,269 fragments analyzed; data restricted in some risk-factor layers for Scotland-wide maps.
- Infection data: 2011–2013 outbreaks and current infections (garden sites reclassified for clarity; updated to May 2013).
- Hosts and habitat modeling:
  - Rhododendron ponticum habitat suitability: MaxEnt models using 11 datasets (landscape, soil, climate).
  - Vaccinium myrtillus abundance: derived from NVC woodland surveys (335 surveys; DOMIN scale).
- Climate data: climate suitability thresholds for Pr and Pk (based on BIOCLIM-like variables 1950–2000).
- Additional risk factors: proximity to roads and rivers, proximity to infected premises and larch presence, and host habitat data.
- Spatial outputs: GIS datasets and shapefiles; two main output formats (Excel and ArcGIS shapefile) with linked IDs.

## Methods and risk framework
- Risk factors considered (within 1.5 km windows unless noted): premises proximity, larch presence and infection proximity, Rhododendron ponticum habitat suitability, Vaccinium myrtillus habitat/abundance, climate suitability specific to Pr or Pk, watercourses, and roads.
- Proximity scoring (Table 1): increasing risk with closer proximity to premises and infected premises; larch proximity and infection yield higher scores; host habitat suitability contributes to risk (R. ponticum and Vaccinium presence/abundance).
- Climate suitability: separate scoring for Pr and Pk due to different climate thresholds; Pr generally requires many more climatically suitable days than Pk.
- Risk scores: maximum 17 for Pr and 16 for Pk per fragment, with regionally varying climate scores to reflect species-specific suitability.
- Output scoring: two main score fields used for risk interpretation (adj_risk_p for Pr; adj_risk_1 for Pk).
- Data visualization: risk maps show fragments from green (low risk) to yellow/red (medium/high risk).

## Host and habitat modeling details
- Rhododendron ponticum:
  - MaxEnt modelling using 11 datasets; predicted broad-leaved woodland cover, lower elevation, and moderate soil moisture favored presence.
  - Scotland-wide predicted suitable habitat for R. ponticum covers about 24% of 1 km grid cells.
- Vaccinium myrtillus:
  - Addressed presence and abundance separately due to data structure (interval-censored DOMIN classes).
  - Used a two-phase GLMM approach (presence-absence via overdispersed binomial; abundance via logit-normal model) within a Bayesian framework to accommodate latent true percent cover.
  - Key predictors include climate, soil pH/content, elevation, bracken presence, deer density, and woodland fragmentation.

## Results and risk maps
- General pattern: risk for both pathogens is higher in southern and western Scotland; this aligns with current infection distributions and host/climate suitability.
- P. ramorum (Pr):
  - High risk in southern/western woodlands close to infected premises or larch associations, with notable risk even in woodlands distant from known infections where host presence and climate are favorable.
  - North-east also shows risk pockets due to host presence and larch proximity.
- P. kernoviae (Pk):
  - Risk concentrated in south/west as expected, but also higher in north/east regions where climate suitability is favorable for Pr host presence and larch is present.
  - Distinctive pattern: broader potential risk areas for Pk than for Pr, reflecting different climate suitability and host distributions.
- Relative risk interpretation: maps provide species-specific relative risk comparisons across Scotland; not directly comparable between Pr and Pk due to differing climate scoring.

## Data products and field descriptions
- Output formats:
  - FHN_2013.csv: risk scores only, with fields suitable for analysis.
  - FHN_2013.shp: ArcGIS shapefile with full calculation details and original fields from FC; large but comprehensive.
- Key fields for risk interpretation:
  - ID: unique fragment identifier
  - Premises-related fields: prem_score
  - Larch-related field: larch_sc_1
  - Host habitat fields: Rp_score (R. ponticum), Vm_score (Vaccinium myrtillus)
  - Climate fields: clim_sco_1 (Pr), clim_sco_2 (Pk); Climsuit_1 (Pr), Climsuit_p (Pk)
  - Proximity and landscape features: road_score, river_sc_1
  - Risk scores: risk_sco_1 (Pr total), risk_sco_2 (Pk total)
  - Availability and uncertainty: Avail_pr, Avail_pk, adj_risk_p, adj_risk_1, Uncert_pr, Uncert_pk
  - Missing data indicators: missing_type
- Data integration: ID used as a key to link the Excel and shapefile outputs.

## Missing data and uncertainty
- Some fragments lack climate data (west coast) or Vaccinium habitat data (east/south), introducing uncertainty in risk scores.
- Missing data accounted for by adjusting final risk scores to the maximum possible given available factors.
- Figures illustrate uncertainty locations and data gaps.

## Appendices and methodological details
- Appendix on V. myrtillus modeling:
  - Describes the two-phase GLMM (presence/absence; and, if present, abundance) with site and quadrat random effects.
  - Addresses interval censoring of DOMIN class data and latent true percent cover.
  - Bayesian framework used to manage uncertainty in latent variables.
- Appendix tables describe risk scoring logic and field mappings for the two output formats.

## Implications for monitoring and policy
- Surveillance planning:
  - Focus surveillance in NE Scotland for P. kernoviae due to unique northeast risk pattern.
  - Consider high-risk fragments in south/west and near larch woodlands for both pathogens.
  - Use the two-pathogen, region-specific risk maps to prioritize monitoring, early detection, and resource allocation.
- Data integration and accessibility:
  - Outputs provide both a lightweight risk score (CSV) and a full spatial dataset (Shapefile) for detailed analyses and decision-making.
  - Data layers and risk factors are designed to be stored and shared with relevant monitoring portals.
- Monitoring tools and methods:
  - Emphasizes combining networked datasets (host distributions, climate suitability, and proximity to infected sites) to improve the value of monitoring datasets beyond single-use analyses.
  - Encourages broader data access to underlying inputs used to generate outputs to support transparency and collaboration.