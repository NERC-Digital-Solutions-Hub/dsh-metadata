# Pontbren Database Catalogue

- Comprehensive repository describing Pontbren hydrological and soil data, instrumentation, and data products.
- Data organized into datasets with quality assurance (QA) codes applied to data points; most data provided as text files split into six-month blocks to manage sizes and Excel limitations.
- Appendices provide supplementary information useful for data users (QA coding, borehole logs, neutron probe logs, site diaries).

## Data Organization and Content

- Core data groups
  - AWS (Automatic Weather Station): 1-minute observations; outputs include daily and 10-minute averages, daily max/min, wind direction statistics.
  - Bowl study site runoff and soil water tension: bowl runoff (weir boxes, tipping buckets) and tensiometer arrays.
  - Groundwater: borehole height data with barometric compensation; includes groundwater temperature.
  - Hillslope study site runoff and soil water tension: weir box runoff, overland flow traps, drain flow, tensiometers, tree shelterbelt data.
  - Llyn Hir study site: soil water tension data from tensiometers; sampling cadence evolved over time.
  - Land use manipulation plots: four plots with tensiometers and overland flow plots; treatments include Ungrazed, Trees, and Grazed; replication within plots.
  - Neutron probe soil moisture: multi-site soil water content profiles (0–120 cm, often every 10 cm); includes soil and water counts for moisture calculation.
  - Rain gauge data: tipping-bucket and storage gauge data from multiple locations.
  - Streamflow: site measurements from Starflow (acoustic Doppler) gauges and other sites with pressure transducers or v-notch weirs; calibrated flow via site-specific relationships.
  - Field Diaries: notes describing issues/events affecting data collection.
  - Appendices: QA coding, borehole logs, neutron probe logs, and additional documentation.

- Specific measurement and data characteristics
  - AWS: incident radiation, wind speed/direction, soil/air temperatures, relative humidity, net radiation; sensor upgrades added columns.
  - Runoff: flow in litres per second; weir-box measurements use water height relative to a 90-degree weir; tipping buckets provide supplementary flow estimates.
  - Tensiometers: depths typically 10, 30, 50 cm; data in cm H2O; some arrays logged on separate loggers after hardware changes.
  - Groundwater: borehole water height with BaroDiver correction; includes groundwater temperature.
  - Neutron probe: soil moisture content from counts, calibrated with a linear model per site.
  - Rain gauges: tipping bucket data in mm/day; storage gauge data where available.
  - Streamflow: calibrated site-specific relationships; low-flow data excluded from calibration.
  - QA and site notes: field diaries capture operational notes explaining anomalies or gaps.

## Data Quality and QA

- QA framework
  - Appendix A defines hierarchical QA codes for data streams (Tensiometers, Rain Gauges, Tipping Buckets, Starflow, Groundwater, Weir data, etc.).
  - Codes indicate quality levels, questionable data, data unsuitable for calibration, out-of-range values, logger failures, sensor issues, calibration problems, biological interference, and other faults.
  - Each data point/file annotated with QA codes to guide cleaning and interpretation.
- Common data issues
  - Patchy/damaged data due to rodent damage, equipment failures, or blocked collection systems.
  - Differences in sampling times and bucket sizes in tipping buckets.
  - Gaps or degradation from tensiometer de-gassing, sensor calibration, or power/communication problems.
- How to use QA
  - Filter/flag data using QA codes during analyses, calibrations, or data fusion.
  - Cross-reference with Field Diaries and Appendix A for code meanings and implications.

## Calibration and Modelling Notes

- Starflow streamflow calibration
  - Site-specific linear calibration: y = α × x + β, where x is Starflow estimate and y is calibrated flow (ls-1).
  - Coefficients and standard deviations provided per site; low-flow data (depth < 50 mm) excluded from calibration.
- Neutron probe calibration
  - Moisture content derived from counts via y = α × (soil_count / water_count) + β.
  - Catalogue parameters: α = 0.96, β = -0.01 (with site-specific considerations near peat/surface layers).

## Access and Reference Details

- File and folder structure
  - Data files organized by dataset (AWS, Bowl, Groundwater, Hillslope, Llyn Hir, Land use plots, Neutron probe, Rain gauges, Streamflow) with site-specific subfolders.
  - Appendices reference calibration tables, instrument locations, and other supplementary documentation.
- File formats and naming
  - Text-based data files, often named to reflect the data collection date range.
  - Some datasets split across multiple loggers or files due to instrument layout and data volume.

## Practical Guidance for Data Support

- When exploring data
  - Rely on QA codes to assess reliability before integrating datasets.
  - Cross-check with Field Diaries for context on data collection issues or anomalies.
  - Apply site-specific calibration parameters (Starflow) and neutron probe moisture models when converting raw measurements to physical quantities.
- When combining datasets
  - Align timestamps across datasets (e.g., AWS vs. streamflow, tensiometers vs. rainfall) and account for cadence changes.
  - Consider measurement methods (weir boxes vs. tipping buckets) and potential evaporation losses or instrument downtime.
- Data quality and reuse
  - Outputs are annotated with QA codes and supported by logs (boreholes, N-probes) to facilitate replication and modeling.

## Borehole Logs and Equipment (Equipment & Methods)

- The accompanying equipment notes illustrate drilling and logging practices used for N-probes.
  - Methods include hand auger, AQ drill rod/guide tube, pneumatic hammer, Atlas Copco RAB and Leopard rotary/percussive drills.
  - Borehole logs provide site-specific details (grid references, site names, and NP identifiers), depths, soil descriptions, completion tubing, sampling intervals, and dates (e.g., 14/05/06).
  - Examples cover multiple N-probe sites (e.g., Pen-Tal-Y-Cein Llanfair Caereinion; Site S3 eastern/central/western; COED CWM-Y-LLWYNOG; Trees/edge of wood) with detailed lithology and sampling records.

- Practical implications
  - Borehole logs support calibration and validation of soil moisture measurements from neutron probes.
  - Site-specific soil descriptions and depths inform data quality assessments and interpretation of moisture signals.

## Streamflow Gauging and Spot Measurements

- Appendix D provides streamflow gauging site flow metered spot measurements.
- Includes start/finish times and flow estimates for numerous measurements across multiple sites and dates, illustrating extensive field verification data to support calibration and validation of continuous streamflow estimates.