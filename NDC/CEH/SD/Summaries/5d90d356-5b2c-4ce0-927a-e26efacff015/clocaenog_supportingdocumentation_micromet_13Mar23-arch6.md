# Climoor field site in Clocaenog forest. Supporting documentation for data

- Access and licensing
  - Data available at the DOI: https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015
  - Licensing: Open Government Licence; users must cite Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015

- Data structure
  - Single main data file: clm_micromet_2016-2021_summaryqa.csv with 28 columns
  - Missing data indicated as "NA"; faulty data replaced by -9999
  - Example fields include: Date (Year-Month-Day); soil temperature at 5 cm depth for multiple plots (TSoil5cm_PlotX_degC); soil temperature at 20 cm depth (TSoil20cm_PlotX_degC); soil moisture per plot (Soil_moisture_PlotX_m3_per_m-3)
  - Data layout described and formatted for end-user self-service

- Site information
  - Location: Clocaenog Forest, North East Wales, UK; upland moorland habitat
  - Ecosystem and vegetation: dominated by Calluna vulgaris (heather) with Vaccinium myrtillus, Empetrum nigrum, and bryophytes; shrub and bryophyte cover high; growing season June–August; winter dormancy
  - Soil: humo-ferric podzol with variable horizons (Eg/Bh, E horizon depth 6–17 cm in apparent cases)
  - Climate (1997–2014): mean air temp ~8.0°C; mean control soil temp ~7.5°C; mean annual rainfall ~1411 mm; total N-deposition ~20–25 kg N ha-1 yr-1
  - Vegetation characteristics: biomass and cover data for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes
  - Table 2 and Table 3 summarize soil properties and vegetation metrics, including C, N, C:N ratios, and nutrient content by horizon and litter

- Climate change treatment information
  - Experimental design: two treatments (drought and warming) plus three control plots; 9 plots total arranged as three replicates per treatment
  - Treatments specifics:
    - Drought: retractable polyethylene roof reduces rainfall by ~20% (May–Sept historically; extended Apr–Oct since 2012); some rainfall events missed due to sensor limits; roofs not operated in high winds
    - Warming: retractable aluminium mesh curtains reduce night-time heat loss; curtains retracted when rain detected to prevent rainfall loss; some rainfall exclusion occurs due to delay in roof retraction
    - Frames and hardware: original frames installed in 1998; new frames installed on top of old ones in June 2017 due to wear and weathering
    - Maintenance: increased maintenance burden over years; 2016 refurbishments; 2017 frame upgrade
  - Treatment timing and effectiveness: annual and seasonal rainfall reductions documented per year; growing degree days (GDD) calculated for control vs warming; changes in treatment operation during certain years (e.g., off during COVID-19)
  - Rainfall data notes: in some years, rainfall sensors or site access issues affect measurement completeness

- Equipment, protocols and data processing methodology
  - On-site equipment: automated weather station (AWS) plus plot-level sensors for micro-meteorology; extensive data types collected
  - Data types and sensors (summarized in Table 7)
    - AWS meteorological data: relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction
    - Micro-meteorological (plot-level) data: soil and air temperature, soil moisture
    - Rainfall valves: ground-level rain gauge; throughfall collectors (plot-level rainfall)
    - Water table depth, soil respiration, trace gases, net ecosystem CO2 exchange, vegetation surveys, canopy reflectance, vegetation phenology, litter chemistry, etc.
  - Data collection frequency and timing
    - Sensors typically sample every minute; hourly averages used initially, then half-hour averages after 2016
    - Vegetation and chemistry data collected annually or on defined campaigns
  - Data quality control
    - Visual QA using basic Excel-based checks; acknowledges trade-offs between strict automated QA and human memory/context
  - Data storage and processing notes
    - Some data not stored in the Environmental Information Data Centre (EIDC) after June 2015; contact for details
  - Rainfall measurement and rainfall chemistry
    - Site-level rainfall via storage rain gauge (biweekly samples)
    - Throughfall data collected biweekly; calculations to convert to plot-level rainfall using percent differences relative to site rainfall
    - Handling of data gaps: plot-level means may use fewer than three replicates when data are missing; infilling with average reductions over years in some cases

- Micro-meteorological data – plot level
  - Plot-level measurements since 2008; soil temperature measured at 5, 10, 20 cm depths using Campbell Scientific sensors
  - Soil moisture measured with TDR sensors (CS616) installed since 2008; prior measurements used Theta probes
  - Data granularity: measurements every minute; hourly averages (pre-2016) and half-hour averages (post-2016)
  - QA approach: manual visual checks; explicit limitations acknowledged

- Storage rain gauge data and rainfall chemistry
  - Rainfall measured with a ground-level rain gauge (12.7 cm funnel); rainfall collected biweekly
  - Considered more robust than AWS data due to logger/power reliability; used as primary rainfall dataset when hourly data not required

- Throughfall data (plot-level rainfall)
  - Throughfall captured with plot-level funnels/bottles; data used to compute seasonal and annual rainfall for each plot
  - Calculation method: apply plot-level percent changes to site-level rainfall to derive plot rainfall; exclude plots with missing data; occasional data infill with year-average reductions

- Appendix and site layout
  - Figures illustrating site layout, quadrat arrangement, and measurement areas (e.g., quadrats of 0.5 m^2)
  - Layout details relevant to experimental plots and instrumentation placement

- Summary of key uses and caveats
  - Data support aim: enables exploration of climate manipulation effects on upland moorland ecosystems; enables self-service data access across multiple data streams (micro-meteorological, rainfall, throughfall, vegetation, and chemistry)
  - Caveats to consider when using the data: incomplete yearly rainfall data for some years; sensor and maintenance interruptions; data gaps in certain datasets or years; imputation strategies described for specific cases
  - Contact for additional details: Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) for non-stored data or infrequently collected datasets