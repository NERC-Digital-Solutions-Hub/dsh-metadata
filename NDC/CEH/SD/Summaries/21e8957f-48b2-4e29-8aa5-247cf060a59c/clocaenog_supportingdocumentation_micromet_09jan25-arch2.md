# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access
  - Available from the Environmental Information Data Centre (EIDC) under Data collection: Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest
  - URL: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

- Data structure
  - Single data file: CLM_AWS_2024_summaryQA.csv
  - Size: 28 columns, 367 rows
  - Data coding: NA = not recorded; -9999 = faulty data
  - Contents include: date, soil temperature at 5 cm for warming/control/drought plots, soil temperature at 20 cm, soil moisture for plots, and related metadata

- Site information
  - Location: Clocaenog Forest, North East Wales, UK (53°03'19"N, -03°27'55"W)
  - Environment: upland moorland with evergreen heathland vegetation; typical species include Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum and bryophytes
  - Soil: humo-ferric podzol with variable eluvial (E) and illuvial (Bh) horizons; C, N, pH and other properties described in detailed tables
  - Climate (1997–2014 context): mean air temp ~8.0 °C; mean control soil temp ~7.5 °C; mean annual rainfall ~1411 mm; N-deposition ~20–25 kg ha^-1 yr^-1
  - Vegetation and litter: shrub-dominated community; mean annual litterfall ~177 g m^-2; bryophyte cover substantial
  - Ecosystem type: wet upland heath; soil and vegetation characterized for climate manipulation context

- Climate change treatment information
  - Treatments: drought and warming, each with three replicated plots, plus three control plots (total 9 plots)
  - Drought treatment
    - Mechanism: retractable polyethylene roof triggered by rainfall sensor
    - Timing: May–Sept (1999–2011), moved to Apr–Oct since 2012
    - Effect: approximately 20% reduction in annual rainfall; up to ~80% reduction in growing-season rainfall due to sensor limits
    - Operational notes: roofs do not operate in winds >10 m s^-1; since 2016 roof performance affected by rainwater accumulation
  - Warming treatment
    - Mechanism: retractable aluminium mesh curtains that reduce infrared loss at night
    - Rainfall interaction: roof retraction occurs after 15 minutes of darkness and rain detection to minimize rainfall loss; average annual rainfall reduction ~14%
    - Operational notes: curtains not used in high winds; some rainfall exclusion during activation; separate from drought plots
  - Frame and maintenance
    - In 2016–2017, original frames refurbished/replaced; new frames installed on top of old frames to minimize vegetation disturbance
  - Climate metrics
    - Growing Degree Days (GDD) used to quantify warming effect; calibration based on plot-specific air temperatures
    - Detailed yearly GDD changes and percentage warming provided (Table 6b)

- Equipment, protocols and data processing
  - On-site automated weather station (AWS) for meteorological data; additional plot-level sensors for micro-meteorology
  - Data types (Table 7 summary): AWS meteorology (temp, RH, rainfall, pressure, radiation, PAR, wind), plot-based soil/air temp and soil moisture, rainfall (site and throughfall), water table depth, soil respiration, trace gases, net ecosystem CO2 exchange, photosynthesis, vegetation surveys, litterfall, root and microbial biomass, soil organic carbon, and soil solution chemistry
  - Data collection cadence
    - AWS: daily measurements
    - Micro-met plot data: daily
    - Rainfall and throughfall: monthly to fortnightly
    - Vegetation, chemistry, and other biogeochemical data: infrequent to annual
  - Data accessibility and QA
    - Not all data are stored in the EIDC; some datasets are stored or catalogued separately; contact details provided for inquiries
    - Quality control described as visual/manual checks alongside basic data cleaning (e.g., handling of NA and -9999)

- Micro-meteorological data specifics
  - Soil temperature: measured at 5, 10, and 20 cm depths using Campbell Scientific sensors
  - Soil moisture: current TDR sensors (CS616) since 2008; earlier manual theta probes
  - Temporal resolution: measurements every minute; hourly averages initially, half-hourly averages after 2016
  - Data handling: quality control via visual inspection and trend checks

- Rainfall data and throughfall
  - Rainfall measurement: ground-level rain gauge (funnel 12.7 cm) with biweekly collection; preferred over AWS in case of logger/power interruptions
  - Throughfall: plot-level rainfall captured biweekly with funnels/bottles; data quality issues (overflow, loss) accounted for in data processing
  - Rainfall data processing: throughfall percent change used to derive treatment-specific rainfall estimates; missing data in a plot leads to exclusion from treatment means; occasional infilling with average reductions across years

- Appendix and site layout
  - Figures detailing site layout, quadrat arrangement, and measurement areas accompany the documentation

- Practical notes for analysts
  - The dataset provides plot-level micro-meteorological data aligned with drought and warming treatments, suitable for analyses of climate manipulation effects on soil and vegetation parameters
  - Data can be integrated with broader environmental health datasets, with explicit documentation on data structure and QA
  - Consider the treatment-specific adjustments and gaps (e.g., roof operation gaps due to wind, rainwater accumulation, and COVID-related interruptions) when designing analyses or interpreting long-term trends

- Contact
  - For inquiries about additional datasets beyond the CLM_AWS_2024_summaryQA.csv, contact Sabine Reinsch or Bridget Emmett at enquir ies@ceh.ac.uk (UKCEH Bangor)