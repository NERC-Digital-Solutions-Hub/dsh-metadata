# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access and licensing
  - Data available at https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
  - License: Open Government Licence; citation required: Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily automatic weather station (AWS) data from Climoor fieldsite in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/0ebfc33b-0da2-4329-aac7-69ed8925b979
  - Purpose: Supporting documentation for data accompanying the Climoor climate change manipulation experiment.

- Data structure
  - One data file: CLM_AWS_2016-2021_summaryQA.csv with 10 columns.
  - Data quality/format notes:
    - Missing data marked as NA.
    - Faulty data replaced by -9999.
  - Columns and units (Date format: Year-Month-Day):
    - Mean_air_temperature_degC (degC)
    - Minimum_air_temperature_degC (degC)
    - Maximum_air_temperature_degC (degC)
    - Rainfall_mm (mm)
    - Air_pressure_mbar (mbar)
    - Solar_radiation_kW_per_m2 (kW m^-2)
    - Photosynthetic active radiation_umol_per_m2_per_sec (µmol m^-2 s^-1)
    - Wind_speed_m_per_sec (m s^-1)
    - Wind_direction_degrees (degrees)

- Site context
  - Location: Clocaenog Forest, North East Wales, UK (approx. 53°03'19"N, -03°27'55"W)
  - Habitat: upland moorland with Calluna vulgaris (heather) as a dominant biomass component; bryophytes and other vascular species present.
  - Soil: humo-ferric podzol with variable horizons (Eg, Bh; depth ~6–17 cm where apparent); parent material Ordovician/Silurian shale or mudstone.
  - Climate (1997–2014 snapshot): mean air temp ~8.0°C; mean soil temp in control ~7.5°C; mean annual rainfall ~1411 mm; total N-deposition ~20–25 kg N ha^-1 yr^-1.
  - Vegetation metrics: annual litterfall ~177 g m^-2; detailed cover/biomass data for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa and bryophytes (various values from 1998 baseline).

- Climate change treatment information
  - Experimental design: two manipulated treatments (drought and warming) plus three replicated control plots, total 9 plots (3 per treatment, 3 controls).
  - Drought treatment
    - Mechanism: retractable polyethylene roof triggered by tipping-bucket rainfall sensor; reduces annual rainfall by ~20% (site in wet region).
    - Operational window: May–September (1999–2011); since 2012, April–October; adjustments after 2016 due to rainfall patterns and sensor issues.
  - Warming treatment
    - Mechanism: retractable aluminum mesh curtains trapping infrared radiation; night-time warming; roof retracted upon rainfall to protect rainfall regimes.
    - Rainfall reduction: ~14% annual rainfall reduction; timing controlled by a light sensor and rainfall detection with delays.
  - Operational constraints
    - Roofs disabled during high winds (>10 m s^-1) to prevent damage.
    - Structural refurbishment: 2017 replacement of frames mounted atop original supports; minimal vegetation disturbance.
  - Treatment performance data
    - Table 6 (a) drought: annual dates and percent reduction in rainfall and growing season rainfall from 1997–2015; 2016–2011 years show varying activity and reductions.
    - Table 6 (b) warming: growing degree days (GDD) comparisons between control and warming plots; GDD differences documented from 1999–2021, with notes on periods when warming roofs operated separately or together with drought roofs.
  - Practical notes
    - Some years show data gaps due to sensor or equipment issues; 2016–2017 refurbishment and 2018 rainfall sensor failure noted.
    - During COVID-19, site access restrictions impacted data collection.

- Data collection, sensors, and processing (equipment and protocols)
  - AWS meteorological data (on-site automated weather station)
    - Measured variables: relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed and direction.
    - Sensor suite and brands: e.g., HMP 45C (air temp, RH), Skye SP1110 pyranometer (solar), SKP215 Q Sensor (PAR), NR-Lites (net radiation), ARG100 tipping bucket (rainfall), Windsonic anemometer (wind).
    - Temporal resolution: measurements every minute; hourly averages stored.
    - Data quality control: manual visual checks in Excel.
  - Micro-meteorological plot data
    - Soil temperature: 5, 10, 20 cm depths (T107 sensors, Campbell Scientific).
    - Soil moisture: TDR sensors (CS616) after 2008; earlier manual theta probe measurements.
    - Data logging: hourly averages up to Jan 2016; post-2016 data logged as half-hour averages.
  - Rainfall data (site-level rainfall and rainfall chemistry)
    - Site rainfall: ground-level storage rain gauge (12.7 cm funnel); rainfall accumulated biweekly; preferred when hourly logger data is suspect or logger downtime occurs.
    - Throughfall data: plot-level rainfall collected biweekly using funnels and bottles; throughfall percentages used to adjust plot rainfall relative to site-level rainfall; periods of data loss lead to plot exclusion or infilling with average reductions.
  - Data processing notes for data users
    - Data quality checks rely on visual QC rather than automated hard limits.
    - Throughfall-derived rainfall adjustments allow cross-plot comparability with site-level rainfall data.
    - Some datasets stored outside EIDC; contact details provided for additional data requests (Sabine Reinsch, Bridget Emmett).

- Accessibility and further details
  - The document mentions Appendix figures (site layout, quadrat layout) for spatial context.
  - For additional or non-EIDC data collected up to 2015, contact the project leads (Sabine Reinsch or Bridget Emmett).

- Practical data products for data support
  - Potential self-serve datasets: AWS met data (1999–present), micro-met plot data (1998–present), rainfall and throughfall datasets, and derived metrics such as plot-level rainfall changes and growing degree days.
  - Metadata and lineage suitable for dashboards or data products: treatment assignments, plot mappings, sensor configurations, data quality notes, and data processing steps to reproduce throughfall adjustments and GDD computations.