# Supporting documentation for plant biomass and leaf-level functional traits from four different genotypes of sugarcane plants grown under a range of ozone conditions

## Overview
- Deposit of experimental conditions and results examining the impacts of ozone (O3) on four Saccharum genotypes grown under controlled gradient exposures.
- Associated with Cheesman et al (2023) and TropOz/O3 field synthesis; data intended for use in dose–response analyses and regional modelling of ozone effects on sugarcane.

## Experimental facility and design
- Location: TropOz facility, joint University of Exeter (UoE) and James Cook University (JCU) in Cairns, Australia.
- Setup: Nine independently controlled Open Top Chambers (OTCs), each ~22.2 m3, with charcoal-filtered air and on-site O3 generation.
- O3 gradient: Semi-continuous gradient across nine chambers (approx. 15–120 ppb daytime average) to explore nonlinear dose responses.
- Monitoring: O3 concentrations read ~3 times per hour per chamber; environmental variables (air temperature, vapor pressure deficit, PAR) recorded every five minutes from a central meteorological station.
- Experimental runs: Two runs with slightly different environmental conditions; both exposed full sunlight and no drought stress.

## Plant material and experimental setup
- Genotypes: Badila (Saccharum officinarum L.), Mandalay (Saccharum spontaneum), Q240 and CTC4 (commercial hybrids).
- Source and handling: Germplasm from SRA; plants germinated under controlled conditions, potted, and fertilized regularly.
- Exposure: Three genotypes (Badila, Q240, CTC4) started ~10 cm tall in November 2021; Mandalay started March 2022 due to slower initial growth.
- Replication: Four individuals per genotype per chamber; nine chambers total, enabling a split across genotypes and O3 levels.
- Environmental note: Delays and two separate runs mean environmental conditions differed between runs; these differences are accounted for in downstream dose–response calculations.

## Measurements and derived metrics
- Biomass and traits: Biomass partitioned into leaves, stalks, and roots; leaf area and leaf mass per area (LMA) measured on the most recently emerged leaf (L+1).
- Gas exchange and stomatal conductance: g_s measured on L+1 leaves (abaxial and adaxial surfaces for some genotypes) using porometry; additional Li-6400XT measurements on controls; data converted to Relative Stomatal Conductance (RSC) and used to parameterize DO3SE.
- O3 dose–response metrics: DO3SE v3.1 used to calculate PODy (mmol O3 m−2 projected leaf area per second) integrating stomatal conductance; y-thresholds (0–8 nmol m−2 s−1) tested to reflect resistance and sensitivity differences.
- Exposure metrics: Concentration-based AOT40 and flux-based PODy used to relate biomass decline to O3 exposure.
- Data processing: DO3SE parameters calibrated with gas-exchange data; model validation against observed g_s; two PODy thresholds (POD0 and POD2) selected for regional simulations.

## Data products deposited
- Sugarcane_O3.csv: O3 concentration time series for nine chambers during the first experiment (date, Chamber_1–Chamber_9).
- Sugarcane_Mandalay_O3.csv: O3 concentration time series for the second experiment (Mandalay) across chambers.
- Sugarcane_Met_5min.csv: Five-minute averaged environmental conditions for the first experiment (AirTC_Avg, RH, PAR_Den_Avg, Datetime).
- Sugarcane_Mandalay_Met_5min.csv: Five-minute environmental conditions for the second experiment (same variables as above).
- Calculated_PODy.csv: Calculated PODy values for four genotypes across chambers, with POD thresholds (0–8 nmol m−2 s−1) and methods (Porometer vs. Licor), including AOT40 and PODx metrics.
- Sugarcane_Biomass.csv: Final biomass and leaf traits for four genotypes, including plant IDs, chamber IDs, date harvested, leaf dimensions, LMA, tiller counts, biomass components (AGB, roots), total biomass, and flags/notes.

## Data quality, provenance, and governance
- Quality controls: Meteorological data cross-checked against local station; O3 concentrations checked with zero-air standards; biomass measurements performed with annually calibrated scales; outliers re-weighed after extended drying.
- Provenance: Experimental setup, genotypes, and measurement protocols documented; data linked to TropOz facility with detailed methodology to enable reproducibility.
- Limitations and considerations for reuse: 
  - Two experimental runs with differing environmental conditions; users should account for run-specific effects when comparing across genotypes.
  - Mandalay data had some g_s measurements not collected with porometer; control measurements used Li-Cor data for g_s where possible.
  - Some environmental differences between runs may influence POD-based comparisons; DO3SE calibration uses gas-exchange data to mitigate this.
- Licensing and access: Plant material supplied under licence by SRA; data and deposit are linked to published work (Cheesman et al., 2023) and broader ozone–vegetation literature.

## Reuse and potential applications
- Enables development and validation of O3 dose–response functions for sugarcane, including
  - biomass decline as a function of PODy and AOT40
  - genotype-specific sensitivity (Badila, Mandalay, Q240, CTC4)
  - flux-based modelling that can be integrated with regional vegetation models under variable environmental conditions
- Useful for:
  - cross-dataset comparisons of ozone sensitivity in tropical crops
  - informing crop management and breeding programs targeting ozone resilience
  - informing risk assessments and policy-relevant ozone exposure guidelines for sugarcane production areas

## References and related resources
- Cheesman, A. W., et al. (2023). Impacts of ground-level ozone on sugarcane production. Science of the Total Environment, 904, 166817.
- Emberson, L. (2020); Kreyling et al. (2018); Agathokleous et al. (2019, 2020); Pleijel et al. (2022) – methodological context for POD and DO3SE approaches.