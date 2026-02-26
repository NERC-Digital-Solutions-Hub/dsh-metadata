# Climoor field site in Clocaenog forest. Supporting documentation for data

- The Climoor/Clocaenog field site is a climate change manipulation experiment (initiated in 1998) using automated roof technology to create drought and warming treatments reflecting 20–30 year climate projections.
- Data described here are from a daily plot-level micro-meteorological dataset and supporting site information, stored and accessible via the Environmental Information Data Centre (EIDC).

## Data access

- Data are available from the Environmental Information Data Centre (EIDC) under Data collection: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest.
- Link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

## Data structure

- The dataset comprises one spreadsheet: CLM_AWS_2022-2023_summaryQA.csv
- Specifications: 28 columns, 731 rows
- Data quality marks: missing data as "NA"; faulty data replaced by "-9999"

## Site information

### 3.1 Clocaenog climate change experimental site characteristics
- Automated manipulation site producing potential climate change for upland moorland over several decades.
- Location: Clocaenog Forest, North East Wales (53°03′19″N, -03°27′55″W)
- Habitat: upland west-atlantic moorland dominated by Calluna vulgaris (heather); additional species listed includes Vaccinium myrtillus, Empetrum nigrum, mosses and bryophytes.
- Growing season: June–August; shoulder seasons April–May and September–October; winter dormancy November–February.
- Soil: humo-ferric podzol with horizons (E and Bh) variably visible; typical E horizon at 6–17 cm depth.

### 3.1.1 Climate (1997–2014)
- Mean air temperature: 8.0 °C
- Mean soil temperature (control plots): 7.5 °C
- Mean annual rainfall: 1411 mm
- Total nitrogen deposition: 20–25 kg N ha⁻¹ yr⁻¹

### 3.1.2 Soil
- Soil type: humo-ferric podzol; parent material: Ordovician/Silurian shale or mudstone
- Depths, nutrients, and basic soil properties across horizons (examples: LF, Oh, Eg, Bh horizons with %N, %C, C:N, cations, base saturation, etc.)
- Cation Exchange Capacity (CEC) and base saturation vary by horizon (LF, Oh, Eg, Bh)

### 3.1.3 Vegetation
- Ecosystem type: Wet upland heath
- Dominant shrubs/graminoids: Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa
- Bryophytes present (indicated with asterisks)
- Annual litterfall (mean): 177 g m⁻²
- 1998 baseline vegetation cover/biomass for major groups (Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes)

### 3.1.4 Chemistry
- Vegetation elemental data provided (C, N) for several plant species and litter
- Additional chemical indicators (P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) for major plants and litter

## Climate change treatment information

- Treatments: drought and warming, each with three replicates (4 m × 5 m). Three control plots with scaffolding to mimic shading effects; total of nine plots.
- Drought treatment: retractable polyethylene roof reduces rainfall by ~20% during May–September (originally) and later April–October; some rainfall missed due to sensor limits; since 2016, heavy rain events caused roof accumulation preventing full retraction.
- Warming treatment: retractable aluminium mesh curtains reduce nighttime heat loss (reflects 96–97% of infrared radiation; night-time warming ~64% reduction in heat loss); operates with a light sensor and a tipping bucket sensor to retract during rain; annual rainfall reduction ~14% due to partial rain exclusion.
- Wind constraints: roofs do not operate in winds >10 m s⁻¹ to prevent damage.
- Frame maintenance: frame upgrades installed in June 2017 (new frames on top of old ones) to reduce vegetation disturbance; ongoing maintenance and equipment challenges noted (e.g., frame wear, water trapping on drought roofs).
- Historical annual rainfall reductions per year (drought) and growing-degree-days (GDD) changes due to warming are documented (Tables 6a and 6b); GDD calculations are described and referenced.

## Equipment, protocols and data processing methodology

- On-site automated weather station (AWS) plus plot-level micro-meteorological sensors; abiotic and biotic measurements collected within plots.
- Summary of data types collected (Table 7): meteorology, soil/air temperature, soil moisture, rainfall (site-level and throughfall), water table depth, soil respiration, trace gases (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation surveys, canopy reflectance, phenology, vegetation chemistry, litter, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC, soil solution chemistry, etc.
- Data storage: not all datasets stored in EIDC after June 2015; contact organizers for details.
- Micro-meteorological data (plot-level): measurements since 1998, soil temperature at 5, 10, and 20 cm; soil moisture measured by TDR probes (since 2008; earlier theta probe); data logged as minute-by-minute readings, with hourly averages pre-2016 and half-hourly averages post-2016.
- AWS sensors: mounted on a secure mast (4 m) after 2007 due to thefts; sensors include air temperature, relative humidity, solar radiation, PAR, net radiation, barometric pressure, rainfall (tipping bucket), wind speed/direction.
- Data quality control: basic graphical QA in Excel; acknowledges limitations of automated quality checks and the value of human interpretation.
- Rainfall data: two primary sources
  - Site-level storage rain gauge: robust, collected biweekly; preferred when hourly data not required
  - Throughfall collectors: plot-level rainfall collected biweekly; data adjusted to provide seasonal/annual values and percent differences between treatments
  - Data gaps and exclusions noted when throughfall data are compromised (e.g., funnel detachment, overflow)
- Throughfall methodology: percent-change approach applied to ground-level rainfall to estimate treatment rainfall; excluded plots if data loss occurred; infilling with average reductions used in some years.

## Appendix and figures

- Appendix includes site layout and quadrat arrangement, illustrating plot configuration and measurement areas.

## Data usage notes and practical considerations

- Data are suitable for standardized environmental health assessments and long-term policy performance analyses across climate manipulation experiments.
- The dataset CLM_AWS_2022-2023_summaryQA.csv provides a near-daily snapshot of plot-level micro-meteorology with QA annotations; researchers should be aware of missing values and adjustments (e.g., -9999 markers, NA).
- For datasets not stored in EIDC or post-2015 details, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) for access.
- The documentation emphasizes value in integrating this site’s data with other datasets to enhance interpretability and policy relevance, aligning with the Analysts Monitoring the Environment aim to demonstrate environmental condition through consistent, scrutinizable formats.