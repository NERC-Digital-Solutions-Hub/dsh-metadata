# Supporting documentation for plant biomass and leaf-level functional traits from four different genotypes of sugarcane plants grown under a range of ozone conditions

## Overview
- Deposited dataset and methods from ozone (O3) exposure experiments on four sugarcane genotypes to develop O3 dose–response functions for biomass and leaf traits.
- Experimental work conducted at the TropOz facility in Cairns, Australia, with a semi-continuous gradient of nine O3 exposures.
- Data include O3 concentrations, meteorological variables, biomass partitioning, leaf traits, and modeled phytotoxic O3 dose (POD) metrics.
- Intended to complement Cheesman et al. (2023) and enable regional-scale applications and vegetation-model integration.

## Experimental facility and design
- Location: TropOz facility (JCU/UoE) on Nguma-bada campus, Cairns, Australia.
- Facility features: nine independently controlled Open Top Chambers (OTCs), internal volume 22.2 m3 each; charcoal-filtered air with on-site O3 generation; daytime exposure from 08:00–17:00.
- O3 gradient: distinct exposure levels across chambers to create a semi-continuous gradient (roughly 15–120 ppb daytime concentrations), enabling nonlinear response analysis.
- Monitoring: O3 measured ~every 22 minutes per chamber; environmental variables (air temperature, VPD, PAR) via a central meteorological station with 5-minute averaging.
- Runs: two experimental runs with different environmental conditions; Mandalay run started later than others, affecting direct comparisons but accounted for in dose–response calculations.

## Plant material and experimental setup
- Genotypes: Badila (Saccharum officinarum L.), Mandalay (Saccharum spontaneum), Q240 (commercial hybrid), CTC4 (commercial hybrid).
- Source: SRA germplasm (Meringa, Qld, Australia); ~60 one-eye sets per line.
- Establishment: germinated under ambient shadehouse; transplanted to 30-L pots with high organic matter mix; regular irrigation and fortnightly fertilization.
- Exposure: four plants per genotype per OTC (total 9 OTCs), with exposure initiated when plants reached ~10 cm height (except Mandalay delayed to 28 March 2022).
- Duration: Badila, Q240, CTC4 – ~96 days; Mandalay – ~100 days.

## Data types and measurements
- Biomass: harvested and oven-dried; partitioned into leaf, stalks, and roots; leaf area and leaf mass per area (LMA) measured from latest emergent leaf (L+1).
- Gas exchange and stomatal data: stomatal conductance (gs) measured on L+1 leaves using porometer for most genotypes; supplementary Li-Cor Li-6400XT data for control plants; gs data converted to Relative Stomatal Conductance (RSC) and used to parameterize DO3SE.
- O3 dose metrics: accumulated O3 flux estimated with DO3SE model (v3.1) to compute PODy (mmol m-2) across thresholds y (0–8 nmol m-2 s-1); two flux thresholds (0 and 2) used for regional simulations; AOT40 also calculated (ppm h).
- Model calibration: DO3SE parameters fitted using observed gs data; modelled gs vs observed daylight gs shows strong correspondence (R2 0.59–0.83 across genotypes).
- Dose–response: biomass decline (relative) modeled against PODy values to derive biomass-based dose–response functions; y-intercept of chamber-mean biomass vs PODy used to estimate maximum biomass.

## Data quality and quality control
- Meteorological data validated against local station data; O3 checks performed against zero-air standards every sampling round.
- Final biomass determinations validated with annually calibrated scales; suspected outliers reweighed after additional drying time.

## Data deposited (files and structure)
- Sugarcane_O3.csv: O3 concentration data for nine OTCs during the first experiment (date, Chamber_1…Chamber_9).
- Sugarcane_Mandalay_O3.csv: O3 concentration data for nine OTCs during the Mandalay experiment (date, Chamber_1…Chamber_9).
- Sugarcane_Met_5min.csv: Environmental conditions (5-minute averages) for the first experiment (AirTC_Avg, RH, PAR_Den_Avg, Datetime).
- Sugarcane_Mandalay_Met_5min.csv: Environmental conditions for the Mandalay experiment (same columns).
- Calculated_PODy.csv: Phytotoxic O3 dose (PODy) values across genotypes, chambers, and flux thresholds (POD2, POD6, AOT40, etc.) with separate columns per genotype and chamber.
- Sugarcane_Biomass.csv: Final biomass partitioning and leaf-level traits for all genotypes (Genotype, Plant_ID, Chamber_ID, Date, New/Old Leaf Length, FW/DW, Area, LMA, Stems, Final_height, Biomass, AGB, Flagged, Notes).
- Additional supporting notes and references accompanying the data.

## GIS and data product implications
- Geospatial relevance: nine spatially co-located exposure chambers provide a controlled, gradient-based dataset ideal for linking O3 exposure with biomass and leaf traits across genotypes.
- Potential map-based outputs:
  - Spatially resolved O3 exposure gradients (per chamber) over time.
  - Dose–response surfaces linking PODy to biomass decline for each genotype.
  - Regional-scale integrations using PODy thresholds (0 and 2 nmol m-2 s-1) with environmental covariates (temperature, PAR, humidity) to drive vegetation models.
- Data integration: combines environmental variables, gas-exchange-derived physiology, and end-point biomass metrics, enabling GIS workflows that explore spatial patterns of ozone susceptibility across sugarcane genotypes.
- Data standards and reusability: well-documented CSV structure with explicit variable definitions; validated against multiple measurement modalities; suitable for ingestion into GIS analyses, environmental impact assessments, and crop-ozone interaction mappings.

## Notes and caveats
- Two experimental runs experienced different ambient environmental conditions; the dataset accounts for these differences in dose–response calculations.
- Mandalay’s delayed start resulted in differing environmental conditions between runs; these differences are accounted for via DO3SE calibration and model fitting.
- Threshold selection (POD0 and POD2) facilitates comparison with prior studies and regional modelling efforts.

## References
- Agathokleous et al., 2019; 2020; Emberson et al., 2020; Kreyling et al., 2018; Pleijel et al., 2022.
- Cheesman et al., 2023. Impacts of ground-level ozone on sugarcane production. Science of the Total Environment, 904, 166817.