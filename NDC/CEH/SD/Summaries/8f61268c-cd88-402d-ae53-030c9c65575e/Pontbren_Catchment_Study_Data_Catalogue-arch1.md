# Introduction to the Database Catalogue

## Purpose and Audience
- Describes the Pontbren Database, its instrumentation, data organization, quality assurance, and descriptive metadata to support data-driven analysis and modelling.
- Intended for researchers and analysts who will extract data, assess quality, build models, or validate findings with supporting metadata.

## Data Organization and Access
- Data are organized in directories with a documented framework; files typically stored as .txt blocks, often split into six-month periods (Jan–Jun, Jul–Dec).
- Each data point may have an associated QA code; QA codes and their meanings are detailed in Appendices.
- Appendices provide supplementary information (QA coding, borehole logs, neutron probe logs, streamflow calibration data, etc.).
- The catalogue references instrument locations, layouts, and study-site schematics.

## Data Coverage and Instrumentation (by dataset)
- Automatic Weather Station (AWS)
  - Location: bowl on instrumented hillslope; sensors logged every 1 minute; data supplied as daily and 10-minute averages; some measurements include daily max/min and wind-direction standard deviation.
  - Variables: incident radiation, wind speed/direction, soil temperature, relative humidity, air temperature, net radiation; post-2009 sensor changes added Ave Humidity 2 and Ave Air Temp 2.
- Bowl study site runoff and soil water tension data
  - Excludes AWS, tipping bucket rain gauge, boreholes, and neutron probe data.
  - Split into Bowl runoff (weir boxes) and Bowl tensiometers (arrays at 10, 30, 50 cm).
- Bowl runoff
  - Weir boxes measure water height above a 90-degree weir via pressure transducers; flow in L/s; sampling started every 10 s, then 5-minute averages; evaporation can produce negative height when no flow.
  - Bowl drain and overland flow weirs cover drainage areas of 0.44 ha and 0.36 ha respectively; QA notes include rodent damage affecting data quality for some traps.
- Bowl tipping bucket data
  - Drain flow and overland flow tipping buckets; flow in L/s; sampling times occasionally changed due to logger limitations and bucket-size changes.
- Bowl tensiometers
  - Arrays at 10, 30, and 50 cm depth; data initially on a single logger, later distributed across loggers; units in cm H2O; data coverage until March 2008 with some sensor removals.
- Groundwater
  - Five boreholes monitored with Diver pressure transducers; BaroDiver for barometric correction; data expressed as height of water (cm) relative to soil surface and groundwater temperature (°C).
  - Sampling: every 10 minutes initially, then every 30 minutes (timing adjusted over time).
- Hillslope study site runoff and soil water tension (tree shelterbelt hillslope)
  - Runoff (overland flow traps), drain flow, and overland flow data from hillslope above tree areas; tensiometer arrays with location-specific depths and removal events noted in 2008.
  - Tree shelterbelt overland flow: two 5 m × 5 m plots; initially cumulative flow between site visits, later switched to tipping buckets with data logged every 10 minutes (flow rate in L/s).
- Llyn Hir study site soil water tension
  - Tensiometer array at 10 cm, 30 cm, and 50 cm depths; sampling every 10 minutes (later 15 minutes to reduce site visits).
- Land use manipulation plots
  - Four plots (Rhos1, Rhos2, Tyn Fron, Penllwyn) with three replicate subplots (Ungrazed, Trees, Grazed) per plot; plots randomized.
  - Each replicate has tensiometers at 10, 30, and 50 cm; overland flow measured per replicate (mm/h).
- Neutron probe soil moisture
  - Measured across bowl, hillslope, manipulation plots, tree areas, and Llyn Hir; profiles typically 10 cm increments to depths down to 120 cm.
  - Neutron counts converted to volumetric moisture content using a linear calibration (y = α × Soil_count/Water_count + β; α = 0.96, β = -0.01 by default; peat-layer adjustments at Llyn Hir may use different parameters).
  - Location-specific access tubes detailed.
- Rain gauge data
  - Tipping bucket gauges and storage gauges across multiple sites (Bowl, Hirrhos Uchaf, Llyn Hir, Penllwyn, Quarry, Rhos1, etc.).
  - Data include rainfall totals in mm (tip buckets in mm/day; storage gauges in mm); gauges at varied heights above ground with grid surrounds.
- Field Diaries
  - Word documents with field notes describing site issues; useful for data interpretation and quality checks.
- Streamflow
  - Starflow acoustic Doppler monitoring at Sites 1–9 and 13; Sites 10–12 use pressure transducers and v-notch weirs.
  - Data recorded every minute and averaged to every 15 minutes.
  - Site-specific calibration to relate Starflow estimates to manual measurements: y = αx + β with site-specific α and β; low-flow data (<50 mm water depth) deemed unacceptable for calibration.
- Calibration parameters and site details
  - Site-specific calibration parameters listed (Sites 1–9 and 13) with α*, β*, and standard deviations.

## Quality Assurance and Data Quality
- Appendices detail QA coding system (Appendix A) with codes for data quality categories (Good, questionable, calibration issues, data gaps, logger failures, instrument damage, etc.) across tensiometers, tipping buckets, rainfall, groundwater, Starflow, and site manipulations.
- Appendix A includes codes describing equipment faults, data collection anomalies, calibration issues, and site-specific problems (e.g., rodent damage, sensor drift, blockages).
- Appendices B–D provide borehole logs, neutron probe logs, and additional groundwater context to support interpretation and QA.
- Field diaries provide contextual information for data interpretation and quality checks.

## Data Specifics for Modelling and Analysis
- Data designed for multi-scale analysis across bowls, hillslopes, shelterbelts, and manipulation plots to study catchment-scale flood risk and hydrological responses to land-use change.
- Key relationships and calibration approaches:
  - AWS: standard meteorological variables with sensor recalibration in 2009.
  - Streamflow: Starflow estimates require site-specific calibration against spot measurements; low-flow data may be excluded from calibration.
  - Neutron probe: moisture content derived from counts via linear calibration; peat-layer adjustments applied where needed.
- Acknowledges data gaps and scale mismatches (rodent-related gaps, differing sampling frequencies, and alignment challenges across sites and instruments).

## Appendices and Additional Resources
- Appendix A: Quality assurance coding system (comprehensive quality codes for tensiometers, tipping buckets, rain gauges, groundwater, Starflow, and site manipulations; links to data corrections).
- Appendix B: Borehole logs (equipment, methods, locations, soil stratigraphy, groundwater levels, borehole channels).
- Appendix C: Neutron probe logs (location metadata and logging conventions).
- Appendix D: Field and instrumentation context (site-specific notes for data interpretation).

## Endnotes for Analysts
- Expect variability in data density and quality; QA codes guide data filtering and cleaning.
- When linking datasets (e.g., AWS meteorology with downstream hydrological measurements), account for different sampling frequencies and calibration offsets.
- Use site-specific calibration parameters for Starflow; exclude low-depth measurements if flagged as unsuitable for calibration.
- Leverage Appendices to understand borehole/neutron probe configurations and to clarify data provenance and measurement conditions for robust analysis.

## Equipment & Methods (Borehole Logs)
- The borehole logs document drilling and monitoring setup for N-probes at multiple sites with detailed soil descriptions, depths, and sampling logs.
- Drilling equipment used includes hand augers, AQ drill rods, guide tubes, pneumatic hammers, Atlas Copco RAB/Leopard drills.
- Specific borehole identifiers (e.g., NP20, NP21, NP22, NP23) and locations (e.g., PEN-TAL-Y-CEIN LLANFAIR CAEREINION; COED CWM-Y-LLWYNOG; site S3) are recorded with grid references and completion details (16-gauge aluminium access tubes), depths, soil textures, and sample intervals.
- Documentation dates (e.g., 14/05/06) and completion details are provided to support data provenance and replication.

## Streamflow Gauging Sites and Data
- Streamflow gauging includes flow metered spot measurements with precise start/finish times and flow estimates.
- Data span multiple sites (e.g., Site 7–13) with diverse measurement times and flow values, used for calibrating Starflow and validating hydrological models.