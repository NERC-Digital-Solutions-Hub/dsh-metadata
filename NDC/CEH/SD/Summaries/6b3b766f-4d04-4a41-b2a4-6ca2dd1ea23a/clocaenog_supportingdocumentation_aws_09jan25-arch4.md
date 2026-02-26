# Climoor field site in Clocaenog forest. Supporting documentation for data

## 1 Data access
- Data are accessible via the Environmental Information Data Centre (EIDC) under the dataset: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest. Link: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99

## 2 Data structure
- Dataset: CLM_AWS_2024_summaryQA.csv
- Size: 1 spreadsheet, 10 columns, 367 rows
- Missing/faulty data: NA indicates missing values; -9999 replaces faulty data
- Columns (Date in Year-Month-Day format; measurements in respective units):
  - Mean_air_temperature_degC
  - Minimum_air_temperature_degC
  - Maximum_air_temperature_degC
  - Rainfall_mm
  - Air_pressure_mbar
  - Solar_radiation_kW_per_m2
  - Photosynthetic_active_radiation_umol_m-2_s-1
  - Wind_speed_m_per_sec
  - Wind_direction_degrees
- Descriptions provided for each variable

## 3 Site information
- Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, -03°27'55"W)
- Purpose: Automated climate manipulation site producing drought and warming treatments to reflect predicted climate changes
- Habitat: upland moorland dominated by Calluna vulgaris (heather); bryophyte presence noted
- Establishment: 1998; solar and wind powered; replicated drought and warming treatments
- Vegetation baseline (1998): Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes
- Soil: humo-ferric podzol with variable horizons (Eg, Bh); C, N, C:N, base cations and CEC characterized across horizons
- Growing season: June–August; shoulder seasons April–May and September–October; winter dormancy
- Litter and biomass: Annual litterfall ~177 g m-2; baseline biomass data for major species and bryophytes provided

### 3.1 Clocaenog climate change experimental site characteristics
- Ecosystem type: Wet upland heath
- Mean climate (1997–2014): Mean air temp 8.0 °C; Mean soil temp in control 7.5 °C; Mean annual rainfall 1411 mm; Total N deposition 20–25 kg N ha-1 yr-1
- Vegetation and soils: Detailed species list including bryophytes; annual litterfall and 1998 baseline biomass values; soil chemical properties across horizons (N, C, C:N, base cations, H+, CEC)
- Canopy and litter chemistry: Species- and litter-level C, N, C:N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates

#### 3.1.1 Climate
- Location coordinates repeated; climate data summarized above for the period 1997–2014

#### 3.1.2 Soil
- Soil type: Humic ferric podzol; horizon details (Eg, Bh) and depths
- Additional soil chemistry data across horizons (N, C, C:N, H+, Ca, Mg, Na, K, Al, CEC, base saturation)

#### 3.1.3 Vegetation
- Ecosystem type and dominant species
- 1998 baseline shrub and bryophyte metrics (cover and biomass)
- Bryophyte-specific notes indicated by asterisks

#### 3.1.4 Chemistry
- Species- and litter-level carbon and nitrogen concentrations
- Ratios and element concentrations (P, K, Ca, Mg) across plant species and litter
- Lignin, tannin, alpha-cellulose, and carbohydrate contents for multiple species and litter

## 4 Climate change treatment information
- Treatments: Drought and warming; 3 replicate plots each + 3 control plots (total 9 plots)
- Drought treatment
  - Timing: May–September (1999–2011); since 2012 April–October; early 2016 adjustments
  - Mechanism: Retractable polyethylene roof triggered by tipping bucket rainfall sensor; reduces annual rainfall by ~20% and excludes ~80% of rain during drought months
  - Limitations: Some small rain events missed; in 2016–2017, rainfall accumulation on roof affected retraction
- Warming treatment
  - Mechanism: Retractable aluminium mesh curtains to reduce infrared radiation at night; roof retracted when rain detected to prevent rainfall reduction in warming plots
  - Rainfall impact: ~14% annual rainfall reduction on average
  - Operation: Controlled by light sensor; considerations for wind (>10 m s-1) preventing curtain operation
  - Interaction: Roofs can function together or separately with drought roofs
- Maintenance and changes
  - 2017: Replacement planning; new frames installed June 2017 (on top of old frames) to minimize vegetation disturbance
  - 2016–2018: Equipment wear and rainfall issues led to partial and intermittent operation
  - 2018 onward: Rainfall sensor on site broken since Jan 2018
  - 2020–2024: COVID-19 related disruptions; some operations Off or partial
- Table 6 summary notes
  - Drought: Yearly precipitation reductions and dates listed; several years show substantial reductions; 2016 Off; 2017 partial operation; 2018–2024 not always measured due to equipment/conditions
  - Warming: GDD (Growing Degree Days) changes calculated; operation years and windows vary; 2016 onward partial operation with specific dates; 2018–2024 operational details noted
- Figure references
  - Figures illustrating frame designs and effects on vegetation; layout schematic in Appendix

## 5 Equipment, protocols and data processing methodology
- Instrumentation overview: Automated weather station (AWS) with a suite of sensors; additional plot-level micro-met sensors; diverse abiotic and biotic data collected
- Data storage and archival
  - Not all data stored in EIDC after June 2015; contact project leads for full data details
  - Data types include meteorological, soil/biogeochemical, vegetation, litter, and ecosystem flux measurements
- 5.1 AWS Micro-meteorological data
  - Sensors and measurements: Air temp (HMP 45C), relative humidity (HMP 45C), solar radiation (Skye SP1110), PAR (SKP215), net radiation (NR-Lites), barometric pressure (CS100), rainfall (ARG100 tipping bucket), wind (Windsonic 2D)
  - Logging: Measurements every minute; hourly averages (and, since 2016, half-hour averages)
  - Data quality: Visual QC in Excel; human-centric approach noted for context beyond rigid automated limits
- 5.2 Storage rain gauge data (site-level rainfall) and rainfall chemistry
  - Method: Ground-level rainfall gauge with 12.7 cm funnel; rain collected biweekly; preferred when hourly data are unavailable due to reliability
- 5.3 Throughfall data (plot-level rainfall)
  - Method: Plot-level rainfall captured with funnels and 3 L bottles; biweekly collection
  - Data processing: Compute seasonal/annual plot rainfall by applying plot-specific percent differences to site-level rainfall; exclude plots with missing/compromised data; infilling by average reductions used sparingly
- Appendix and figures
  - Site layout and quadrat map provided to contextualize measurement locations

Overall, the document details a long-running climate manipulation experiment at Climoor (Clocaenog) with drought and warming treatments, extensive baseline soil/vegetation data, and a comprehensive, though sometimes disrupted, data collection and processing framework accessible via EIDC.