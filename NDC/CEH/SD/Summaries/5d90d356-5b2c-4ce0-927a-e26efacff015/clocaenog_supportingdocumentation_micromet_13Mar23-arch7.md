# Climoor field site in Clocaenog forest. Supporting documentation for data

- Data access and citation
  - Data available at https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015
  - License: Open Government Licence; cite Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre.
  - Use of data requires compliance with licensing terms and proper citation.

- Data structure
  - Primary dataset: clm_micromet_2016-2021_summaryqa.csv (28 columns)
  - Example variables: TSoil5cm_Plot1_degC, TSoil5cm_Plot2_degC, TSoil20cm_Plot1_degC, Soil_moisture_Plot1_m3_per_m-3, and corresponding plots 1–9
  - Data quality marks: NA for unrecorded values; faulty data replaced by -9999
  - Data format: Date in Year-Month-Day; soil temperature and soil moisture measurements for multiple plots; site-level soil moisture and related metrics
  - Note for GIS use: data are plot-based time series suitable for linking with spatial plot geometries and visualizing temporal trends across the field site

- Site information
  - Location: Clocaenog Forest, North East Wales, UK (53°03'19''N, -03°27'55''W)
  - Ecosystem: upland west-atlantic moorland; dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum present
  - Vegetation and structure: detailed species list; bryophytes indicated; typical seasonal growth pattern (growing season June–August; dormancy Nov–Feb)
  - Soil: humo-ferric podzol with horizon variability; E and Bh horizons variably visible; horizon depths and chemical properties provided (N, C, C:N, H, Ca, Mg, Na, K, Al, CEC, base saturation)
  - Climate (1997–2014 overview): mean air temp 8.0°C; mean soil temp in control plots 7.5°C; mean annual rainfall 1411 mm; total N deposition 20–25 kg N ha-1 yr-1
  - Vegetation and litter: annual litterfall ~177 g m-2; detailed biomass data for Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum, Deschampsia flexuosa, bryophytes

- Climate change treatment information
  - Experimental design: two treatments (drought and warming) with three replicates each, plus three control plots; total of 9 plots
  - Drought treatment: retractable polyethylene roof during May–Sept (1999–2011), later April–October (from 2012); roof reduces ~20% of annual rainfall, excluding ~80% of events due to sensor limits; high-wind periods (>10 m/s) suspend operation
  - Warming treatment: retractable aluminium mesh curtains; reflects 96–97% of IR; reduces nocturnal heat loss; roof operation triggered after 15 minutes of darkness; rainfall is prevented from reducing warming if detected, but some rainfall is excluded due to lag
  - Coordination with drought: roofs can operate together or separately
  - Maintenance notes: frames refurbished with new frames installed on top of old ones in June 2017 to minimize vegetation disruption; occasional roof water accumulation issues noted
  - Long-term data considerations: 2016–2021 notes include failures, COVID-19 disruptions, and sensor issues; some years show incomplete data or unavailable rainfall measurements

- Equipment, protocols and data processing
  - Automated Weather Station (AWS): provides meteorological data; mounted on a secured mast (4 m above ground after thefts)
  - Micro-meteorological plot sensors: soil and air temperature, soil moisture; data logged at high frequency (per-minute measurements, averaged hourly; later half-hourly averages after Jan 2016)
  - Rainfall measurement: site-level storage rain gauge (biweekly collection; preferred when available); plot-level throughfall data collected biweekly using funnels and bottles; data used to derive plot-specific rainfall by applying percent-change adjustments to site rainfall
  - Sensor suites (AWS and plot sensors): includes air temperature, relative humidity, rainfall (tipping bucket), solar radiation, PAR, net radiation, barometric pressure, wind speed/direction; plant-related measurements include vegetation surveys, canopy reflectance, phenology, and chemistry
  - Data quality control: manual inspection in Excel for trend validation; ongoing quality considerations acknowledged
  - Data storage and accessibility: not all data are stored within the Environmental Information Data Centre (EIDC); contact Sabine Reinsch or Bridget Emmett for further details

- GIS-relevant notes for data integration
  - Spatial layout: Appendix includes site layout and quadrat-based measurement areas; 0.5 m² quadrats indicate fine-scale spatial sampling
  - Plot-level and site-level data: enables linking environmental variables (temperature, soil moisture, rainfall, etc.) with plot locations for spatial analysis and map-based visualization
  - Temporal dimension: dataset supports time-series GIS analyses and change detection across drought and warming treatments over multiple years

- Appendix and visualization
  - Figures include site layout, quadrat arrangement, and motor box locations; 0.5 m² quadrats used for measurement areas

- Practical considerations for GIS workflows
  - Ensure alignment of plot identifiers (1–9) with spatial plot polygons or shapefiles
  - Integrate climate treatment metadata (drought vs warming vs control) to enable thematic mapping of treatment effects
  - Account for missing years and sensor outages in temporal analyses; document data gaps and data provenance
  - Use throughfall, site rainfall, and rainfall chemistry data to derive treatment-specific rainfall estimates for spatial comparisons

- Contact for data inquiries
  - For additional datasets beyond the micromet CSV (post-June 2015 and infrequently stored data), contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) in UKCEH Bangor