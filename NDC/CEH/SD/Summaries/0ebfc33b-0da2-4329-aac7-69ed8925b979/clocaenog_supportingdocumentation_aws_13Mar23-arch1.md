# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access and citation
  - Data available at https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
  - Licensing: Open Government Licence; cite: Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily automatic weather station (AWS) data from Climoor fieldsite in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979

- Data structure and quality
  - Dataset: CLM_AWS_2016-2021_summaryQA.csv
  - Contains 10 columns; missing data recorded as NA and faulty data replaced by -9999
  - Columns (Date and meteorological variables):
    - Date
    - Mean_air_temperature_degC
    - Minimum_air_temperature_degC
    - Maximum_air_temperature_degC
    - Rainfall_mm
    - Air_pressure_mbar
    - Solar_radiation_kW_per_m2
    - Photosynthetic_active_radiation_umol_per_m2_per_sec
    - Wind_speed_m_per_sec
    - Wind_direction_degrees
  - Data format: Date in Year-Month-Day; hourly/daily resolution with quality checks performed via basic spreadsheet review

- Site overview
  - Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, 03°27'55"W)
  - Ecosystem: upland west-atlantic moorland
  - Dominant vegetation: Calluna vulgaris (heather) >60% of biomass; presence of Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes among others
  - Soil: humo-ferric podzol with horizon variability; depth and horizons Eg, Bh described; soil chemistry and C/N dynamics provided for multiple horizons
  - Growing season: June–August; shoulders April–May and September–October; winter dormancy Nov–Feb
  - Baseline climate (1997–2014): mean air temp ≈ 8.0°C; mean soil temp in control ≈ 7.5°C; mean annual rainfall ≈ 1411 mm; N deposition ≈ 20–25 kg N ha−1 yr−1

- Climate change treatments
  - Experimental design: two treatments (drought and warming) plus three control plots; 3 replicates per treatment and 3 control plots (9 plots total)
  - Drought treatment
    - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor
    - Effect: around 20% reduction in annual rainfall; greater reduction (up to ~80% of detectable rainfall) during growing season
    - Operational window: May–September (historically); since 2012 May–October; since 2016 affected by rainfall accumulation on roofs and later by maintenance issues
  - Warming treatment
    - Mechanism: retractable aluminum mesh curtains to reduce infrared heat loss at night
    - Effect: roughly 14% reduction in annual rainfall within warming plots due to rain retraction timing
    - Operational window: night-time activation; retraction upon rainfall detected; sometimes rainfall excluded due to response lag
  - Infrastructure notes
    - Frames and mechanisms required refurbishment: new frames installed on old structure in June 2017 to minimize vegetation disruption
    - High winds (>10 m/s) temporarily prevent curtain operation to protect equipment
  - Additional treatment data
    - Table 6a (Drought) lists annual precipitation, dates of drought, and percent reductions (varied yearly, e.g., 1999: 28% annual, 79% growing season; 2010: 30% annual, 67% growing season)
    - Table 6b (Warming) provides growing degree days (GDD) calculations and year-by-year warming changes; notes on years with NA or incomplete data due to sensor or logistical issues
    - COVID-related interruptions and sensor issues noted (2016 refurbishment, 2018 broken rainfall sensor, 2020–2021 reduced field activity)

- Equipment, protocols and data processing
  - Data collection framework
    - Automated Weather Station (AWS) for meteorological data (daily to hourly granularity)
    - Micro-met plot sensors for plot-scale soil and air temperature and soil moisture (daily; hourly to half-hourly post-2016)
    - Rainfall: storage rain gauge (biweekly collection; used as robust rainfall source) and plot-level throughfall collectors (biweekly)
    - Throughfall data used to estimate plot-level rainfall by applying percent-change adjustments to site-level rainfall; occasionally plots are excluded if data are compromised
  - Data types and coverage (examples)
    - AWS meteorological data: relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed and direction; measurements logged every minute; hourly averages
    - Micro-meteorological data: soil temperature (5, 10, 20 cm), soil moisture (TDR sensors since 2008); data logged frequently; quality checks via visual inspection
    - Rainfall data: ground-level rain gauge (biweekly) and plot-level throughfall (fortnightly)
    - Additional data types available within the site: soil respiration, trace gas measurements (CH4, N2O), net ecosystem CO2 exchange, vegetation surveys, canopy reflectance, phenology, litter chemistry and biomass, soil solution chemistry, etc. Note: not all data are stored in the Environmental Information Data Centre (EIDC); inquiries discouraged for access details after 2015
  - Data processing and quality control
    - Data quality control performed via basic Excel tools, emphasizing interpretability and memory of site conditions
    - Throughfall data processing involves adjusting plot rainfall by observed percentage changes relative to site rainfall; data gaps lead to plot exclusion or infilling with average reductions
  - Accessibility and contact
    - Primary contact for additional datasets: Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk)

- Supplemental material and figures
  - Appendix includes site layout and quadrat arrangement; 0.5 m² quadrats used for vegetation measurements
  - Figures referenced for the framing changes and rainfall roof issues (e.g., water accumulation on roofs affecting retraction)

- Practical implications for analysts
  - Data are designed for correlating weather/climate manipulation with ecological responses across drought and warming treatments
  - Expect data gaps due to sensor faults, frame refurbishments, and COVID-related interruptions; treatment effect calculations rely on plot-level adjustments via throughfall data
  - Rich, multi-sensor time-series enable cross-validation between AWS data and plot-level measurements; however, some datasets are not uniformly stored in the central data centre and may require direct contact for access
  - Metadata and careful citation are essential given the complex treatment histories and instrument changes over time