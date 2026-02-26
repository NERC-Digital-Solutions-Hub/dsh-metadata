# Supporting documentation for plant biomass and leaf-level functional traits from four different genotypes of sugarcane plants grown under a range of ozone conditions

- This data deposit documents experimental conditions and results on how ozone (O3) exposure affects four Saccharum genotypes, with the aim of developing and applying ozone dose–response metrics to support environmental health monitoring and regional-scale vegetation modelling.
- Accompanied by an associated paper (Cheesman et al., 2023) and should be interpreted alongside those results.

## Experimental facility and design

- Location and facility: TropOz, a joint UoE–JCU research facility in Cairns, Australia, with nine independently controlled Open Top Chambers (OTCs; internal volume 22.2 m3 each).
- O3 exposure gradient: Each chamber delivered a different daytime O3 level to create a semi-continuous gradient across nine exposures (approx. 15–120 ppb), enabling assessment of nonlinear responses.
- Measurement regime:
  - O3 concentrations: Monitored ~every 22 minutes per chamber using UV-absorption analyzers.
  - Environmental variables: Temperature, vapor pressure deficit, and PAR recorded every five minutes from a central meteorological station.
- Experimental runs and conditions:
  - Two experimental runs due to a delayed start for Mandalay; environmental conditions differed between runs and are accounted for in dose–response calculations.

## Plant material and experimental setup

- Genotypes studied (four sugarcane lines): Badila (S. officinarum), Mandalay (S. spontaneum), Q240, and CTC4.
- Source and propagation: Material obtained from SRA germplasm collection and propagated under controlled nursery conditions before transplantation into 30-L pots with standard fertilization.
- Exposure: ~10 cm tall plants allocated to each of the nine OTCs; Badila, Q240, and CTC4 began exposure in November 2021; Mandalay began exposure in March 2022 (longer exposure window).
- Growth conditions: Full sun, no drought stress, maintained near field capacity through drip irrigation.

## O3 dose–response and metrics

- Biomass assessment: Harvested plants were oven-dried and partitioned into leaves, stalks, and roots; a recent leaf (L+1) was analyzed for leaf area and leaf mass per area (LMA).
- Concentration-based metric: AOT40 (ppm h) used as a reference exposure metric.
- Flux-based dose metric: Used DO3SE v3.1 to estimate PODy (mmol m-2; nmol O3 m-2 s-1 threshold y) accounting for stomatal conductance and environmental conditions.
  - Stomatal conductance: g_s measured on L+1 leaves; g_o3 = 0.663 × g_s; relative stomatal conductance (RSC) used in DO3SE.
  - Model calibration: DO3SE parameters tuned using porometer data and Li-6400XT gas-exchange data; r2 values ranged from 0.59 (CTC4) to 0.83 (Mandalay) when predicting daylight g_s.
  - Thresholds used: PODy calculated for y = 0–8 nmol m-2 s-1; two thresholds selected for regional simulations: POD0 and POD2.
- Dose–response function: Relative biomass decline (across genotypes and chambers) modeled against PODy values; a linear regression between mean chamber biomass and PODy provided the intercept for maximum biomass.
- Rationale: Flux-based POD metrics enable cross-condition comparisons and integration with regional vegetation models that incorporate soil moisture and temperature.

## Data quality control and methods

- Meteorological data: Collected with factory-calibrated sensors and validated against a local met station.
- O3 concentration checks: Regular zero-air standard checks to ensure measurement integrity.
- Biomass and trait measurements: Weight scales annually calibrated; outliers re-weighed after additional drying to verify data accuracy.
- Data validation: Modelled g_s vs. observed g_s compared to verify DO3SE parameterization.

## Data files deposited

- Sugarcane_O3.csv: O3 concentration data for nine OTCs during the first experiment (date and Chamber_1…Chamber_9 readings).
- Sugarcane_Mandalay_O3.csv: O3 concentration data for the Mandalay experiment (date and Chamber_1…Chamber_9 readings).
- Sugarcane_Met_5min.csv: Environmental conditions (5-minute averages) for the first experiment (AirTC_Avg, RH, PAR_Den_Avg, Datetime).
- Sugarcane_Mandalay_Met_5min.csv: Environmental conditions (5-minute averages) for the Mandalay experiment.
- Calculated_PODy.csv: Phytotoxic ozone dose (PODy) calculations for four genotypes across chambers, with thresholds 0–8 nmol m-2 s-1 and using both porometer and Li-Cor data; includes POD2_Porometer, POD6_Porometer, POD0_Licor, POD1–POD8_Licor, AOT40, Cham_ID, Genotype.
- Sugarcane_Biomass.csv: Final biomass data and leaf-level functional traits for four genotypes across chambers; includes Plant_ID, Height, leaf lengths, fresh/dry weights, leaf areas, LMA, tiller counts, biomass components (AGB, roots), total biomass, and QC flag.

## Metadata, governance, and usage notes

- Data provenance: Links to experimental methods, DO3SE modelling approach, and underlying literature; deposit designed to support cross-study comparisons and regional-scale modelling of ozone impacts on crops.
- Openness and reuse: Data described with explicit variables and measurement methods; intended for public sharing with transparent data handling and standardization.
- Considerations for use in monitoring frameworks:
  - Provides a robust example of combining concentration- and flux-based ozone metrics to derive dose–response functions relevant to policy-relevant monitoring.
  - Demonstrates integration of detailed, instrument-level data (O3, meteorology, gas exchange) with biomass and leaf-trait outcomes to support model validation and scenario analysis.
- Key references: Cheesman et al. (2023) for sugarcane ozone impacts; foundational DO3SE and stomatal conductance modelling literature; and related methodological papers on nonlinear responses and POD metrics.

## References

- Agathokleous et al. (2019, 2020)
- Braga Junior et al. (2021)
- Cheesman et al. (2023)
- Emberson (2020)
- Kreyling et al. (2018)
- Pleijel et al. (2022)