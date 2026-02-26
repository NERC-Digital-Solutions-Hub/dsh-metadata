# Supporting documentation - Ozone effects in high sugar grass pasture

## Purpose and scope
- Documents a phytometer-style mesocosm study assessing the effects of ozone on a high-sugar pasture system combining Lolium perenne (AberMagic) and Trifolium repens (Crusader).
- Aims to generate data on biomass production, tissue injury, nitrogen fixation, and canopy gas exchange under controlled ozone exposures to inform environmental health monitoring and policy decisions.

## Experimental design and setup
- Plant material: Lolium perenne cv. AberMagic and Trifolium repens cv. Crusader sourced from commercial seeds.
- Growth system: Pots in a CEH solardome facility (six hemispherical glasshouses, 3 m diameter) with uniform soil and inoculated soil microbial community.
- Treatments: Six solardomes each receiving multiple ozone treatments in a randomised design; ambient temperature and moisture monitored in one dome.
- Exposure regime: Episodic ozone profiles based on rural monitoring data; 16-week exposure period (11/06/2013–01/10/2013).
- Replication concerns: Ozone treatments were not replicated within domes (justified by prior validation of the solardome facility for similar experiments).
- Environmental monitoring: Continuous measurements of temperature, soil moisture, PAR, relative humidity; routine watering to field capacity.

## Measurements and data collected
- Biomass:
  - Above-ground shoot biomass collected every 4 weeks; components pooled per ozone treatment.
  - Root biomass and nodule mass measured at the 16-week harvest; nodules excised for Crusader roots.
  - Injury assessment of leaves (injured and senesced leaves categorized; expressed as a percentage of affected area for comparison).
- Nitrogen fixation:
  - Acetylene reduction assay (ARA) conducted every 4 weeks prior to maintenance cuts to estimate nitrogenase activity.
- Forage quality:
  - Near-infrared reflectance (NIR) analysis for nutritive characteristics; calculations of Relative Feed Value (RFV) and Consumable Feeding Value (CFV).
- Canopy gas exchange and productivity:
  - Whole-canopy hourly CO2 fluxes measured with a bell chamber and infrared gas analyser to derive Net Primary Production (NPP), canopy respiration (Rtot), and Gross Primary Production (GPP).
  - Deposition/dependent ozone flux calculated using the DO3SE model; stomatal conductance data used to parameterise model for Crusader (AberMagic used default parameters due to limited data).
  - Accumulated ozone flux values tied to POD thresholds (POD 6 for AberMagic; POD 1 for Crusader) to relate flux to biomass and injury outcomes.
- Additional measurements:
  - Leaf area index (derived from biomass).
  - Whole-plot canopy-level injury and performance data used in regression analyses.
- Data and datasets:
  - Acetylene reduction assays (4, 8, 12, 16 weeks): acetylene_reduction_assay_4week.csv, acetylene_reduction_assay_8week.csv, acetylene_reduction_assay_12week.csv, acetylene_reduction_assay_16week.csv.
  - Biomass (shoot and root) by week: week4shootbiomass.csv, week8shootbiomass.csv, week12shootbiomass.csv, week16shootbiomass.csv; week4rootbiomass.csv, week8rootbiomass.csv, week12rootbiomass.csv, week16rootbiomass.csv.
  - Injury data by week: week4injury.csv, week8injury.csv, week12injury.csv, week16injury.csv.
  - All measurements summary and environmental data: allmeasurements.csv; AOT40_and_climate_variables.csv.
  - Gaseous exchange and climate variables: Gs file (contained in allmeasurements.csv).
  - AOT40 and climate data include ozone exceedance above 40 ppb, PAR, temperature, VPD, etc.

## Data processing, analysis, and reporting
- Data handling: Biomass, injury, and N-fixation variables analyzed with linear regression against accumulated POD values (POD 6 for AberMagic, POD 1 for Crusader); seasonal analyses for shoot biomass.
- Canopy gas exchange: ANOVA across ozone treatments, with week included as a random factor; post-hoc Tukey tests for treatment differences.
- Data transformations: Injury data arcsine-transformed prior to analysis; relative values computed against a zero-POD baseline.
- Software: All analyses performed in R (Version 3.1.1).

## Data governance, metadata, and openness considerations
- Metadata and data quality: The dataset comprises detailed measurements and environmental conditions, with explicit variable definitions described in the accompanying documentation (e.g., column descriptions within each CSV).
- Data sharing and provenance: The documentation notes that sharing underlying data can be a barrier in some monitoring contexts and that metadata quality and data governance are important for reuse; datasets are organized with clear naming conventions and week-by-week structure to facilitate traceability.
- Data usability for monitoring frameworks: The suite of measurements (biomass, N-fixation via ARA, injury scoring, forage quality, and canopy gas exchange) alongside environmental context (AOT40, PAR, temperature, VPD) provides a robust set of indicators for evaluating ozone-related environmental health effects and informing policy decisions.

## Relevance for monitoring frameworks and policy decisions
- Key environmental health measures:
  - Biomass production and allocation (shoot, root, and clover/grass composition) under ozone exposure.
  - Nitrogen fixation activity as influenced by ozone (ARA-derived).
  - Tissue injury and recovery indicators in clover and grass species.
  - Canopy-level gas exchange metrics (NPP, GPP, Rtot) and total canopy respiration.
  - Ozone deposition fluxes and dose-response relationships via POD metrics.
  - Forage quality indices (RFV, CFV) linked to productivity and nutritional value.
- Data richness and governance:
  - Rich, multi-dimensional dataset enabling dose–response analyses and cross-parameter correlations.
  - Clear documentation of data structure enhances reproducibility and comparability across monitoring initiatives.
  - Integration of environmental condition data (AOT40, PAR, climate variables) with biological responses supports policy-relevant risk assessment and scenario analysis.
- Considerations for future monitoring:
  - Replication of ozone treatments could strengthen statistical robustness.
  - Expanded metadata and data-sharing practices can improve accessibility for policy evaluation and cross-study synthesis.