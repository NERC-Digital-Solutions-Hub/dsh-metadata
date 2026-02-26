# Experimental crop biomass and gas flux (methane, nitrous oxide, and ammonia) data from continuous and intermittently flooded rice fields, India, month-month 2016

- A dataset from a 2016 rice field experiment in Delhi, comparing continuous flooding (CF) and intermittent flooding (IF) with five fertilizer treatments.
- Focuses on emissions of methane (CH4), nitrous oxide (N2O), and ammonia (NH3), plus nitrogen use efficiency (NUE) and crop yield.
- Data collected to support environmental monitoring of irrigation practices, fertiliser strategies, and their trade-offs for greenhouse gas emissions and rice production.

## Site, design, and management

- Location: Indian Agricultural Research Institute (IARI), New Delhi, India (IARI_ND; site ID IARI_rice_kharif_2016).
- Coordinates: 28°40' N, 77°12' E; altitude 228 m.
- Climate: subtropical, semi-arid; mean temps July–Oct ~35°C max / ~18°C min.
- Soil: silty clay loam (Typic Ustochrept), bulk density 1.38 g cm-3, pH 8.01, organic carbon 4.2 g/kg, total N 0.24 g/kg.
- Experimental setup: split-plot design with two irrigation regimes (CF and IF) and five fertiliser treatments, each with three replicates; plot size 6 x 7 m.
- Crop: rice variety Pusa 44; transplanting 12–13 July 2016; harvest 3–5 October 2016.
- Agronomy specifics: basal P, K, Zn applications; irrigation via basin method; CF had 25 irrigations, IF had 15; IF irrigation triggered by surface cracks.

## Treatments

- Table 2 Fertiliser Treatments (N application in kg N ha-1)
  - CON: Control, 0 N
  - FYM: 50% N through farmyard manure + 50% N through neem-coated urea (NCU); total 120 kg N ha-1
  - LCC: Leaf Colour Chart (LCC) based NCU application; total 120 kg N ha-1
  - NCU: 100% N through neem-coated urea; total 120 kg N ha-1
  - PRI: 100% N through prilled urea; total 120 kg N ha-1

- Fertiliser timing and methods vary by treatment (e.g., NCU and LCC strategies with split applications; basal P, K, Zn applied across all treatments).

## Measurements and sampling

- Gas flux sampling (GHG: CH4 and N2O) using static chambers; chamber dimensions: 50 cm x 30 cm x 100 cm; measurements at 0, 30, and 60 minutes.
  - Analysis: CH4 by gas chromatography with flame ionization detector; N2O by GC with electron capture detector.
  - Flux calculation uses changes in concentration over time, chamber volume, and soil area.

- Ammonia volatilisation sampling
  - Uses transparent static chambers (18 cm x 18 cm x 30 cm) with boric acid capture and titration to quantify NH3-N.
  - Fluxes below 1 g NH3-N ha-1 d-1 discounted (treated as zero flux).

- Soil and plant measurements
  - Soil NO3-N and NH4-N; soil properties; root- and shoot-based nitrogen content through Kjeldahl analysis.
  - Crop biomass and yield: biomass measured as dried mass; grain and straw separated and dried; grain moisture measured; NUE calculated relative to control within the same irrigation regime.

- Weather and site data
  - Weather data collected at the site (temperature, rainfall, humidity, sunshine, evapotranspiration, wind) and used for context and potential normalization.

## Data files and contents

- irrigation.csv: daily water depth for CF and IF plots; water table heights.
- weather.csv: daily meteorological data (dates, Tmin, Tmax, rainfall, Tmean, RH, Sunshine, ET, wind).
- site_properties.csv: plot-level properties (Irrigation regime, Fertiliser Treatment, Replicate, soil pH, total N, total C, bulk density, texture percentages).
- NH3.csv: NH3 flux data by date, irrigation regime, treatment, and replicate.
- N2O_CH4.csv: N2O and CH4 flux data by date, irrigation regime, treatment, and replicate.
- soil_NO3_NH4.csv: soil NO3-N and NH4-N concentrations (dry weight) by date, irrigation, treatment, replicate.
- crop_biomass_N.csv: biomass data (grain and straw) with dry weights, and nitrogen concentrations for grain and straw.
- Metadata and references: notes on data processing rules, availability, and citations to supporting literature.

## Data processing, quality, and standards

- Data verification and cleaning follow standardised methods; outputs designed for clear interpretation and cross-study comparability.
- Ammonia data are discounted when flux measurements are below methodological detection limits (1 g NH3-N ha-1 d-1), with zero flux assigned in the dataset.
- Data are organized to support replicable calculation of NUE and related metrics; dataset storage and portal uploads implied.

## Relevance to environmental monitoring and policy

- Enables assessment of trade-offs between water-saving irrigation (IF) and greenhouse gas emissions (CH4, N2O, NH3) in rice systems.
- Provides standardized, traceable measurements and datasets suitable for integration with other environmental datasets and policy performance monitoring.
- Supports evaluation of nitrogen use efficiency under different irrigation and fertiliser strategies, contributing to sustainable agriculture and climate-smart farming analyses.

## References

- Key methodological and contextual references for GHG measurements, soil nitrogen analysis, NUE calculations, and related rice-system emissions research, including:
  - Bhatia et al. (2005, 2016)
  - Bremner (1965)
  - Cowan et al. (2021)
  - Pathak et al. (2002, 2003)
  - Page et al. (1982)