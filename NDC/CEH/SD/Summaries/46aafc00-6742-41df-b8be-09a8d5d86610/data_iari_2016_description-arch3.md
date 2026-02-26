# Experimental crop biomass and gas flux (methane, nitrous oxide, and ammonia) data from continuous and intermittently flooded rice fields, India, month-month 2016

## Data scope and purpose
- Describes data from a rice paddy experiment in Delhi, India (2016) comparing continuous flooding (CF) and intermittent flooding (IF) with five nitrogen fertiliser treatments.
- Aimed at understanding environmental tradeoffs: methane (CH4), nitrous oxide (N2O), and ammonia (NH3) emissions, nitrogen use efficiency (NUE), and yield.
- Data intended to support monitoring frameworks by providing traceable, multi-variable environmental health indicators linked to irrigation practices and fertiliser strategies.

## Experimental design and site information
- Location: Indian Agricultural Research Institute (IARI), New Delhi, India; site IARI_ND, altitude 228 m, 28°40' N 77°12' E.
- Soil: silty clay loam (Typic Ustochrept); alluvial parent material.
- Climate: subtropical, semi-arid; long-term avg temp and rainfall cited (750 mm).
- Design: split-plot with CF and IF irrigation as main factor; five fertiliser treatments (CON, FYM, LCC, NCU, PRI) as sub-plots; three replicates; plot size 6 x 7 m.
- Crop management: rice cultivar Pusa 44; transplanting 12–13 July 2016; harvesting 3–5 October 2016; basal P, K, Zn applied; CF vs IF irrigation events (CF: 25 irrigations; IF: 15 irrigations).

## Measurements and data collection
- Gas fluxes: CH4, N2O (via static chambers and GC analyses) and NH3 (ammonia volatilisation via boric acid trapping and titration).
- Other data collected: irrigation depths, soil properties, meteorological conditions, crop yield, and soil nitrogen content.
- Sampling details:
  - CH4 and N2O: gas samples at 0, 30, 60 minutes per chamber; CH4 measured by GC-FID; N2O by GC-ECD.
  - NH3: volatilisation measured with static chambers; NH3-N quantified titrimetrically; fluxes discounted below 1 g NH3-N ha−1 d−1.
- Flux calculation: F = (dC/dt) × (ρ × V / A), where dC/dt is rate of concentration change, ρ is air density, V is chamber volume, A is ground area.
- Data formats and quality notes: biomass and nitrogen analyses via Kjeldahl method; data quality controls include reporting zero flux for below-threshold NH3 measurements.

## Fertiliser treatments and data context
- Table 2 (described in text) details five treatments:
  - CON: no nitrogen
  - FYM: 120 kg N ha−1 via 50% farmyard manure and 50% neem-coated urea (NCU)
  - LCC: Leaf Colour Chart guided NCU (30 kg N ha−1 applied based on LCC readings)
  - NCU: 100% N via neem-coated urea (120 kg N ha−1)
  - PRI: 100% N via prilled urea (120 kg N ha−1)
- All treatments received basal phosphorus, potassium, and zinc.

## Data products (files)
- irrigation.csv: water depth measurements and water table heights for CF and IF plots.
- weather.csv: daily meteorological data (T min/max, rainfall, Tmean, relative humidity, sunshine, evapotranspiration, wind speed).
- site_properties.csv: irrigation type, fertiliser treatment, replicate, soil pH, totalN, totalC, bulk density, and soil texture metrics.
- NH3.csv: NH3 flux data by date, irrigation regime, treatment, and replicate.
- N2O_CH4.csv: N2O and CH4 flux data by date, irrigation regime, treatment, and replicate.
- soil_NO3_NH4.csv: soil nitrate and ammonium concentrations by date, irrigation regime, and replicate.
- crop_biomass_N.csv: biomass data (grain and straw) and nitrogen content for harvested crops, including dry weights and N concentrations.

## Data quality, limitations, and governance
- Data quality considerations:
  - Flux measurements filtered by methodology threshold; sub-threshold NH3 fluxes set to zero.
  - Some site metadata (e.g., texture NA for some replicates) indicates incomplete metadata across all replicates.
- Data accessibility and openness:
  - Data are organized into clearly described CSV files with explicit variable definitions and measurement units.
  - Metadata describe measurement methods and experimental conditions; sharing of underlying data is facilitated by file-level documentation, though some metadata gaps exist.
- Potential data-use considerations for monitoring:
  - One-location study (IARI, Delhi) with CF vs IF and five fertiliser treatments; results may need regional validation for broader policy application.
  - Data enable assessment of environmental health indicators: CH4, N2O, NH3 emissions, NUE, and yield under different irrigation and fertiliser regimes.
  - Useful for policy analyses on water management, fertiliser strategies, and emission mitigation in rice systems.

## Relevance for monitoring environmental health and policy
- Provides a comprehensive, multi-parameter dataset linking irrigation regime, fertiliser strategy, and environmental health indicators (GHG and NH3 emissions) with agronomic outcomes (yield, NUE).
- Enables monitoring framework practitioners to:
  - Define and track metrics such as CH4 and N2O fluxes, NH3 volatilisation, NUE, and grain/straw yields.
  - Assess data quality, provenance, and governance requirements (metadata completeness, data sharing, transparent methods).
  - Compare policy-relevant practices (CF vs IF, different nitrogen inputs) to inform water use efficiency and greenhouse gas mitigation strategies in rice production.
- The dataset can support lifecycle or scenario analyses and benchmarking across similar agroecosystems, with clear methodological documentation for reproducibility and governance.