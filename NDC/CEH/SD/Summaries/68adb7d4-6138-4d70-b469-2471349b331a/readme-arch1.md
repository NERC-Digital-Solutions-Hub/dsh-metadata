# Supporting documentation for plant biomass and leaf-level functional traits from four different genotypes of sugarcane plants grown under a range of ozone conditions

## Overview
- Experimental study on the impacts of ozone (O3) on four Saccharum sugarcane genotypes using a gradient of O3 exposures.
- Conducted at the TropOz facility (Open Top Chambers) in Cairns, Australia, with nine independently controlled chambers.
- Key approach: ozone dose–response functions for biomass, using both concentration-based (AOT40) and flux-based (PODy) metrics.
- Two experimental runs with slightly different environmental conditions to enable comparison and regional modelling via DO3SE.
- Data deposit complements the Cheesman et al. (2023) paper and related research.

## Experimental facility and design
- Location: TropOz facility at Nguma-bada campus, JCU, Cairns; collaboration between University of Exeter and James Cook University.
- Setup: Nine OTCs (volume ~22.2 m3 each) with charcoal-filtered air; ozone generated on site and delivered to chambers 8:00–17:00.
- O3 gradient: Approximately nine exposure levels, yielding daytime mean concentrations from ~15 to 120 ppb.
- Monitoring: O3 concentrations measured ~22-minute intervals; meteorology (temperature, VPD, PAR) recorded every five minutes at a central station.
- Rationale: Gradient design reduces nonlinearity issues and improves detection of dose–response relationships.

## Plant material and experimental runs
- Genotypes: Badila (Saccharum officinarum), Mandalay (S. spontaneum), Q240, and CTC4.
- Source and propagation: Germplasm from SRA; ~60 one-eye sets per genotype propagated under controlled conditions before transplant to pots.
- Growth conditions: Uniform irrigation, high organic-matter potting mix, and biweekly fertilization.
- Experimental timing:
  - Three genotypes (Badila, Q240, CTC4) exposed beginning 13 Nov 2021 for 96 days.
  - Mandalay exposure began 28 Mar 2022 due to slower early growth, for 100 days.
- Environmental differences between runs: Acknowledged and accounted for in O3 flux–dose calculations.

## Measurements and data collection
- Biomass and tissue traits:
  - Harvested plants with oven-dried biomass to constant mass; biomass partitioned into leaves, stems, and roots.
  - Leaf-level data: L+1 leaf collected for leaf area and leaf mass per area (LMA).
- Gas exchange and stomatal conductance:
  - g_s measured on multiple genotypes with porometer; additional Leaf-level gas exchange data from Li-6400XT for control plants.
  - Data converted to Relative Stomatal Conductance (RSC) for model fitting.
- O3 dose metrics:
  - DO3SE model v3.1 used to compute PODy (mmol m-2) across thresholds y (0–8 nmol m-2 s-1).
  - Two thresholds used for regional modelling: POD0 and POD2, plus a PODy series derived from porometer and LiCor data.
  - Calibration of DO3SE using gas-exchange data; g_o3 = 0.663 × g_s; model fits validated against observed daylight g_s (R2 0.59–0.83 across genotypes).
- Dose–response modelling:
  - Relative biomass decline modeled against PODy; maximum biomass used as the y-intercept from chamber-level regression (n=4).

## Data processing and quality control
- Meteorology: Sensor data cross-checked against local station; calibrated instruments used throughout.
- O3 concentrations: Monitored against zero-air standards for each sampling round.
- Biomass data: Final measurements verified with annually calibrated scales; outliers reweighed after further drying as needed.
- Data provenance: Detailed documentation of data sources, processing steps, and calibration procedures.

## Data files in the deposit
- Sugarcane_O3.csv: O3 concentration data for nine chambers during the first experiment; columns for date and Chamber_1–Chamber_9 (ppb).
- Sugarcane_Mandalay_O3.csv: O3 concentration data for nine chambers during the second experiment (Mandalay); same structure as above.
- Sugarcane_Met_5min.csv: Environmental conditions (5-minute averages) for the first experiment (AirTC_Avg, RH, PAR_Den_Avg, Datetime).
- Sugarcane_Mandalay_Met_5min.csv: Environmental conditions (5-minute averages) for the Mandalay experiment.
- Calculated_PODy.csv: PODy values (14 columns) across genotypes and chambers for thresholds 0–8; includes fields Cham_ID, Genotype, and POD values for porometer and LiCor data.
- Sugarcane_Biomass.csv: Final biomass and leaf-level traits for four genotypes; includes Genotype, Plant_ID, Chamber_ID, Date, New/Old leaf lengths, weights, areas, LMA, Tillers, Final_height, AGB, Biomass, and a Flagged indicator for outlier removal.

## Interpreting and applying the data
- Dose–response relationships enable understanding of O3 impact on biomass across genotypes, accounting for stomatal regulation via PODy.
- Flux-based PODy metrics facilitate cross-environment comparisons and integration with regional vegetation models that include soil moisture and temperature.
- Data can support predictions of sugarcane yield loss under varying ozone regimes, and inform breeding or management strategies for ozone tolerance.
- The deposit should be used in conjunction with Cheesman et al. (2023) for broader context on sugarcane production under ground-level ozone.

## Related work and references
- Cheesman et al. (2023). Impacts of ground-level ozone on sugarcane production.
- DO3SE model and related methodology (Emberson; Jarvis; Hayes et al.).
- Agathokleous & Saitanis (2020); Agathokleous et al. (2019) on ozone susceptibility and dose–response concepts.
- Braga Junior et al. (2021) and related varietal census for Brazilian sugarcane.
- Additional methodological references on dose–response modelling and nonlinear experimental design (Kreyling et al. 2018; Pleijel et al. 2022).