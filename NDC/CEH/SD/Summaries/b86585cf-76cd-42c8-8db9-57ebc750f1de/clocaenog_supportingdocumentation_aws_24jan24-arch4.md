# Climoor field site in Clocaenog forest. Supporting documentation for data

## 1. Data access
- Data available from the Environmental Information Data Centre (EIDC) under the dataset: Daily automated weather station (AWS) data from Climoor field site in Clocaenog forest.
- Access link: https://catalogue.ceh.ac.uk/documents/198980ac-8f5e-4a16-b1c0-bc6d61516b99

## 2. Data structure
- File: CLM_AWS_2022-2023_summaryQA.csv
- Columns: 10
- Rows: 731
- Data quality markings: NA indicates missing data; faulty data replaced by -9999

Column details (Date and meteorological variables with units)
- Date, Year-Month-Day
- Mean_air_temperature_degC, unit: °C
- Minimum_air_temperature_degC, unit: °C
- Maximum_air_temperature_degC, unit: °C
- Rainfall_mm, unit: mm
- Air_pressure_mbar, unit: mbar
- Solar_radiation_kW_per_m2, unit: kW m^-2
- Photosynthetic_active_radiation_umol_per_m2_per_sec, unit: μmol m^-2 s^-1
- Wind_speed_m_per_sec, unit: m s^-1
- Wind_direction_degrees, unit: degrees

## 3. Site information
- Location: Clocaenog Forest, North East Wales, UK (53°03'19''N, -03°27'55''W)
- Habitat: upland moorland dominated by Calluna vulgaris (heather); other species include Vaccinium myrtillus, Empetrum nigrum, and bryophytes
- Environment: automated climate manipulation site with drought and warming treatments; powered by solar and wind
- History: established 1998; replicated drought and warming treatments plus controls
- Soil: humo-ferric podzol with variable horizons (E and Bh not always visible)
- Vegetation cover/biomass (1998 baseline): Calluna vulgaris ~98% cover, Vaccinium myrtillus ~66%, Empetrum nigrum ~25%, Deschampsia flexuosa ~13%, bryophytes ~73%
- Climate (1997–2014): mean air temp ~8.0°C; mean soil temp ~7.5°C (control); mean annual rainfall ~1411 mm; total N-deposition ~20–25 kg N ha^-1 yr^-1

## 4. Climate change treatment information
- Treatments: two main treatments (drought and warming) with three replicate plots each, plus three control plots (total n=9 plots)
- Drought treatment
  - Operated May–Sept (1999–2011); extended to April–October from 2012; suspended or altered due to issues since 2016
  - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor; reduces annual rainfall by ~20% (site is very wet)
  - Limitations: some small rain events missed; occasional full exclusion of ~80% of rain during drought periods
  - Frame/control changes: 2016–2017 frame replacement with new anchoring frames installed on top of old ones to minimize vegetation disturbance
- Warming treatment
  - Night-time warming using retractable aluminium mesh curtains; reflects 96–97% of infrared radiation
  - Activation: based on light level; retracts during rain to avoid rainfall exclusion
  - Rainfall exclusion: average site rainfall reduction ~14%
  - Wind constraints: curtains do not operate in winds > 10 m s^-1
  - Interaction with drought: warming roofs can operate together or independently of drought roofs
- Treatment timing and performance
  - Tabled yearly details show varying reductions in rainfall and growing degree days (GDD), with annual summaries and notes on weather-related disruptions
  - From 2016 onward, drought roofs were often inoperative due to refurbishment and water accumulation; COVID-19 also affected fieldwork
- Known issues
  - Roof frames exposed to environment leading to maintenance needs
  - Rainfall sensor on site broken since 04 Jan 2018
  - Data gaps or reduced visits during certain years (e.g., 2018–2021)

## 5. Equipment, protocols and data processing methodology
- Automated Weather Station (AWS)
  - Measures: relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
  - Data cadence: minute-level measurements aggregated to hourly averages
  - Quality control: visual checks in Excel due to preference for contextual interpretation over strict automated limits
- Micro-meteorological plot data
  - Plot-level soil and air temperature; soil moisture measured with TDR sensors (CS616) installed from 2008; earlier data collected with Theta probe
  - Data cadence: minute-level; post-2016 logged as hourly or half-hourly averages
- Rainfall data
  - Site-level rainfall: storage rain gauge (2-week accumulation; biweekly data preferred for robustness)
  - Throughfall data: plot-level rainfall collected with funnels and bottles (biweekly); data require adjustments to compare with annual/site rainfall
  - Data processing: percent difference in throughfall applied to site rainfall to estimate plot-level rainfall; data losses lead to exclusion of affected plot means or infilling with averages
- Data catalog and contacts
  - Not all data are stored within EIDC (some smaller or post-2015 datasets)
  - For further details, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)

## 6. Data quality, gaps and limitations
- Data completeness
  - Some years have incomplete datasets (e.g., gaps due to equipment issues, COVID-19, and site access limitations)
  - 2018 onward: rainfall sensor failure; drought roofs not always operable
- Data processing caveats
  - Throughfall data may require exclusion or infilling when measurement devices fail or data are compromised
  - Use of hourly/half-hourly aggregations may vary by year; macro-scale summaries (e.g., GDD) are calculated from plot data
- Metadata and provenance
  - Dataset includes detailed site and treatment metadata, sensor specifications, and data processing notes
  - Appendix includes site layout figures and plot quadrat information

## 7. Additional notes
- The dataset is part of a long-term climate manipulation experiment with ongoing data collection across abiotic and biotic measurements
- Appendix materials include figures illustrating site layout and quadrat arrangements
- Version: AWS - 24 Jan 2024; Author: Sabine Reinsch

## 8. Practical takeaways for data leadership
- The Climoor dataset provides rich, multi-year, plot-level climate manipulation data with explicit treatment metadata and robust, though imperfect, sensor networks
- Data governance considerations:
  - Document data provenance, sensor specifications, and processing steps (hourly/daily aggregations, QA practices)
  - Track data gaps, equipment maintenance, and accessibility changes (e.g., COVID-era impacts)
  - Maintain clear handling rules for missing values (NA) and swapped or backfilled values (-9999)
  - Ensure crosswalks between site-level and plot-level rainfall data via documented processing steps
- Access and governance:
  - Data are accessible via EIDC; maintain contact channels for data inquiries and updates
  - Given the complexity and potential data gaps, establish a data quality flag system to communicate reliability year-by-year and plot-by-plot