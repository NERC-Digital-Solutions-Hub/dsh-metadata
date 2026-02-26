# Climoor field site in Clocaenog forest. Supporting documentation for data

## 1 Data access, use and citation
- Data are accessible via DOI: https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015
- Licensing terms: Open Government Licence; users must comply with terms.
- Required citation: Reinsch, S.; Brooks, M.; Emmett, B.A. (2022). Daily plot level (micro meteorological) data at Climoor field site in Clocaenog Forest 2016-2021. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/5d90d356-5b2c-4ce0-927a-e26efacff015
- Note: Not all data are stored within the Environmental Information Data Centre (EIDC); for infrequently collected or post-2015 datasets, contact Sabine Reinsch or Bridget Emmett (enquiries@ceh.ac.uk) for details.

## 2 Data structure
- Single data file: clm_micromet_2016-2021_summaryqa.csv with 28 columns.
- Data completeness/flags:
  - NA marks missing data.
  - -9999 marks faulty data (quality replaced).
- Example variables include:
  - Date (YYYY-MM-DD)
  - Soil temperature: TSoil5cm_Plot1_degC, TSoil5cm_Plot2_degC, …, TSoil20cm_Plot9_degC
  - Soil moisture: Soil_moisture_Plot1_m3_per_m-3, … Plot9
  - Descriptions and units are provided as part of the dataset metadata.
- Structure highlights:
  - Soil temperatures measured at multiple depths (5 cm and 20 cm) across plots.
  - Plot-level soil moisture measurements.
  - Designed to support climate manipulation and environmental monitoring analyses.

## 3 Site information
- Purpose: Automated climate change manipulation site to simulate drought and warming for upland moorland over multiple decades.
- Location: Clocaenog Forest, North East Wales, UK (53°03'19''N, -03°27'55''W); typical upland west-atlantic moorland with dominance of Calluna vulgaris (heather).
- Establishment: 1998; replicated drought and warming treatments using automated roof technologies powered by solar and wind.
- Vegetation and soil:
  - Dominant vegetation: Calluna vulgaris; bryophytes notable among species.
  - Soil: humo-ferric podzol with horizon variability (E and Bh not always visible); typical horizon depths and characteristics described.
- Climate data (1997-2014):
  - Mean air temperature: 8.0°C; mean soil temperature in control plots: 7.5°C
  - Mean annual rainfall: 1411 mm
  - Total N-deposition: 20–25 kg N ha-1 yr-1
- Vegetation, litterfall, and soil chemistry data summarized (e.g., litterfall ~177 g m-2; various C, N, P, K, Ca, Mg, lignin, tannin values by species/horizon).
- Soil characteristics (selected): LF and Oh horizons, C, N, C:N, H, Ca, Mg, Na, K, Al, CEC, base saturation, with values varying by horizon.

## 3.1 Clocaenog climate change experimental site characteristics
- Treatments and layout:
  - Two climate manipulation treatments: drought and warming, each with three replicate plots (4 m x 5 m).
  - Three control plots with scaffolding to mirror shading effects; total plots: 9.
- Drought treatment:
  - Implemented May–Sept (1999–2011); extended to Apr–Oct since 2012.
  - Mechanism: retractable polyethylene roof triggered by rainfall sensor; reduces annual rainfall by ~20% (approx. 80% of rain excluded due to sensor thresholds).
  - Operational caveats: high wind limits; occasional rainwater accumulation on roof since 2016 affected roof retraction.
- Warming treatment:
  - Night-time warming via retractable aluminium mesh curtains; reflects 96–97% IR, reducing heat loss at night by ~64%.
  - Controlled by light sensor; rain detected triggers retraction to prevent rainfall loss; some rainfall exclusion persists due to lag.
  - Wind restrictions apply; separate from drought roofing when needed.
- Maintenance and upgrades:
  - Frame aging led to more frequent maintenance; new frames installed on top of old ones in June 2017 to minimize vegetation disruption.
- Data integrity notes (Table 6 summary):
  - Drought and warming years include varying reductions in annual and growing-season rainfall (percent reductions listed per year).
  - 2016: drought roofs not in operation due to refurbishments and later water accumulation on roofs (affecting drought operation).
  - 2020–2021: COVID-19 restrictions affected field work; some data collection impacted.
  - Rainfall sensor issues: 2018 rainfall sensor on-site broken since Jan 2018.
  - Some years show incomplete data (marked as ** or NA) for rainfall and related metrics.

## 4 Climate and data processing methodology
- Data collection framework:
  - Automated Weather Station (AWS) for meteorological data (daily) and plot-based micro-meteorological sensors (daily).
  - A broad suite of abiotic and biotic data collected within plots; not all data are stored in the EIDC.
- Micro-meteorological data (plot-scale) specifics:
  - Soil temperature: measured at 5, 10, and 20 cm depths using Campbell Scientific sensors.
  - Soil moisture: measured using TDR sensors (CS616) since 2008; earlier manual theta probe measurements.
  - Data cadence: sensors sampled every minute; hourly averages prior to Jan 2016; half-hour averages thereafter.
  - Data quality control: mainly visual QC in Excel; acknowledges limitations of automated QC that might miss event-specific anomalies.
- AWS meteorological data:
  - Sensors for air temperature, relative humidity, rainfall (tipping bucket), solar radiation, PAR, net radiation, wind speed/direction, barometric pressure.
  - Initial AWS height: 1 m; elevated to 4 m after thefts; measurements recorded every minute and reported as hourly averages.
  - Data QC approach similar to plot data (visual inspection in Excel).
- Rainfall measurement and throughfall data:
  - Site rainfall: stored in a ground-level rain gauge, providing robust, low-maintenance data (biweekly collection; two-week accumulation).
  - Throughfall rainfall: plot-level rainfall collected biweekly using funnels and bottles; data processed to align with site-scale rainfall for annual/seasonal comparisons; data exclusions and infill rules applied when data are compromised or lost.
  - Provisions for data reconciliation:
    - Throughfall percent differences used to derive treatment-specific rainfallAdjustments.
    - Exclusion of plots from treatment means when data are compromised; occasional infilling with average reductions across years.
- Data availability and processing notes:
  - Appendix figures illustrate site/quadrat layout and measurement areas.
  - The dataset includes detailed documentation on measurement methodology, temporal scales, and data processing steps to enable reproducibility and reuse by data stewards and researchers.

## 5 Practical considerations for data stewardship
- Governance and provenance:
  - Clear licensing and citation requirements; dataset DOI provided and citation guidance explicit.
  - Some data remain outside EIDC; contact points provided for access to non-EIDC data.
- Metadata and discoverability:
  - Comprehensive site description, treatment details, and measurement methodologies included in the supporting documentation.
  - Data file includes field names and units; NA/-9999 flags indicate quality and missingness for data users.
- Data quality and completeness:
  - Acknowledgement of gaps due to equipment failures (rainfall sensor, wind-related operational limits) and COVID-19 disruptions.
  - Data processing rules for throughfall and site rainfall enable consistent cross-year analyses despite occasional data loss.
- Recommended use for data stewards:
  - Preserve and surface metadata about treatments, frame upgrades, and operational constraints impacting data continuity.
  - Ensure licensing terms are respected and users are directed to the appropriate contact points for access to all relevant data holdings.
  - Maintain guidance on data processing steps (e.g., handling NA/-9999, throughfall adjustment methodology) to support reproducible analyses.