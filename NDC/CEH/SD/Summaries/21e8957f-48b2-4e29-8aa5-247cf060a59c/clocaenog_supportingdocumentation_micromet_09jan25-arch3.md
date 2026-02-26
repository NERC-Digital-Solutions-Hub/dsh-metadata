# Climoor field site in Clocaenog forest. Supporting documentation for data

## 1) Data access
- Data available via the Environmental Information Data Centre (EIDC).
- Dataset reference: Daily plot-level (micro-meteorological) data at Climoor field site in Clocaenog Forest (CLM_AWS_2024_summaryQA.csv) with 28 columns and 367 rows.
- Access link: https://catalogue.ceh.ac.uk/documents/66aed381-44b9-4661-a6ca-fa196732f66b

## 2) Data structure and quality notes
- Core file: CLM_AWS_2024_summaryQA.csv
  - Includes measurements such as soil temperatures at multiple depths and plots, soil moisture, and related variables.
  - NA marks missing data; faulty data replaced by -9999.
- Data organization: Date column (YYYY-MM-DD) and per-plot measurements (e.g., TSoil5cm_Plot1_degC, Soil_moisture_Plot1_m3_per_m-3, etc.).
- Data quality approach:
  - Data QC primarily via manual visual inspection and basic checks; not strictly enforced automated QC in all cases.
  - Metadata and data provenance may require contact with dataset originators for full context.

## 3) Site overview
- Location: Clocaenog Forest, North East Wales, UK; upland moorland habitat.
- Establishment: 1998; automated drought and warming climate-change manipulation experiments.
- Habitat and vegetation: Dominated by Calluna vulgaris (heather); bryophytes are prominent; soil type humo-ferric podzol with horizon variability.
- Baseline climate (1997–2014): mean air temp ~8.0°C; mean soil temp in control plots ~7.5°C; mean annual rainfall ~1411 mm; total N deposition ~20–25 kg N ha^-1 yr^-1.
- Vegetation and soil metrics captured include litterfall, biomass for key species, C, N, nutrient contents, and soil chemical/horizon properties.

## 4) Climate change treatments and experimental design
- Treatments: drought and warming, each with three replicated plots (4 m × 5 m) plus three control plots (n=9 total).
- Drought: retractable polyethylene roof reducing rainfall during May–Sept (historically) by ~20% (up to ~80% of rain excluded in practice due to sensor limits); period has varied over years (since 2012 April–October; wind events occasionally disrupts operation).
- Warming: retractable aluminium mesh curtains over plots at night, reflecting infrared radiation and reducing heat loss; rain sensors retract warming roofs when rain detected to limit rainfall exclusion.
- Maintenance: frames/roofs required refurbishments; new frames installed on top of old in 2017 to minimize vegetation disturbance.
- Timeline context: dataset includes drought/warming operation details, rainfall reductions by year, and growing-degree-day (GDD) calculations for warming vs control.

## 5) Equipment, protocols and data processing
- On-site equipment:
  - Automated weather station (AWS) for meteorological data; additional plot-based sensors for micro-meteorology.
  - Rainfall gauges (site-level) and plot-level throughfall collectors.
  - A suite of measurements: soil/air temperatures, soil moisture, rainfall chemistry, soil respiration, trace gas fluxes (CH4, N2O), net ecosystem CO2 exchange, photosynthesis, vegetation biomass, canopy reflectance, phenology, litter, root biomass, microbial biomass, nitrogen mineralisation, SOM/SOC, soil solution/leachate chemistry.
- Data cadence:
  - AWS: daily meteorological data; sensors sample every minute with hourly averages.
  - Micro-met data: daily plot measurements; soil temperature at 5, 10, 20 cm; soil moisture measured with TDR sensors since 2008.
  - Rainfall/throughfall: rainfall biweekly; throughfall data collected biweekly with separate plots.
  - Other datasets: periodic (infrequent) measurements (e.g., vegetation surveys, chemistry, litter, root biomass).
- Data governance and availability:
  - Not all data are stored in the EIDC; for detailed or infrequent datasets, contact with site researchers (Sabine Reinsch, Bridget Emmett) is advised.
  - Data processing notes emphasize transparency about methods, but some processing decisions (e.g., use of visual QC) reflect practical site constraints.

## 6) Micro-meteorological data - plot level
- Instruments and depths:
  - Soil temperature at 5 cm, 10 cm, 20 cm; soil moisture via TDR sensors (m3 m-3) installed since 2008.
- Data handling:
  - Measurements logged per minute; converted to hourly (pre-2016) and half-hourly averages (post-2016).
  - Quality control relies on visual checks rather than strict automated thresholds.

## 7) Rainfall data and rainfall chemistry
- Site-level rainfall:
  - Ground-level rain gauge (12.7 cm funnel) storing rainfall biweekly; preferred for robustness against logger/power issues.
- Throughfall:
  - Plot-level rainfall collected biweekly via funnels and bottles; data quality can be affected by equipment loss or damage (e.g., funnels, bottles, overflows).
  - Treatment-level rainfall changes are derived as percent differences from site rainfall and applied to site totals; plots with compromised data may be excluded from treatment means.

## 8) Appendix and site layout
- Figures and layout descriptions provided:
  - Site layout and quadrat arrangement shown to contextualize plot-level measurements.

## 9) Data limitations and notes for monitoring planners
- Notable data gaps/interruptions:
  - Drought roofs stopped during 2016 due to refurbishments and later water accumulation on roofs affecting operation.
  - Rainfall sensor malfunction since Jan 2018.
  - COVID-19 restrictions limited field visits in 2020–2021, affecting data collection.
- Data availability caveats:
  - Some years or datasets are not fully archived in EIDC; researchers should contact originators for complete metadata and data beyond the primary CSV.
  - Data processing decisions (e.g., manual QC, infilling decisions) may influence reproducibility and require metadata to interpret.

## 10) Contacts
- Primary contacts for further details: Sabine Reinsch and Bridget Emmett (enquiries@ceh.ac.uk).