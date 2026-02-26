# Pontbren Database Catalogue

- Purpose and scope
  - Describes the Pontbren Database, including instrumentation, data organization, and quality assurance.
  - Aims to enable consistent, time-series assessment of environmental health and policy performance.
  - Emphasizes standardized outputs (reports, maps, charts) and storage of datasets in appropriate portals.

- Data structure and access
  - Data files are organized into directories with descriptions where needed.
  - Most data are in .txt format, typically split into six-month blocks (January–June and July–December).
  - File names indicate covered dates; appendices provide supplementary information for users.

- Core data domains and instrumentation
  - AWS (Automatic Weather Station)
    - Located at the Bowl; sensors sampled every 1 minute; outputs include daily and 10-minute averages.
    - Measurements cover incident radiation, wind speed/direction, soil temperature, humidity, air temperature, net radiation.
    - 2009 updates added for improved humidity/temperature readings due to sensor changes.
  - Bowl study site runoff and soil water tension
    - Runoff and tensiometer data from bowl runoff weir boxes, drain/overland flow, tipping bucket data, and tensiometer arrays (10 cm, 30 cm, 50 cm).
    - Weir boxes log water height; flow inferred from changes; flow units in litres per second.
  - Groundwater (boreholes)
    - 5 boreholes with Diver pressure transducers and BaroDiver compensation; groundwater height and temperature recorded.
    - Locations and logs detailed in appendices.
  - Hillslope study site runoff and soil water tension
    - Runoff data from hillslope weir boxes, tensiometers, and tree shelterbelt overland flow data.
    - Some overland flow measurements affected by rodent-related data quality issues.
  - Llyn Hir study site soil water tension
    - Tensiometer arrays (10 cm, 30 cm, 50 cm) with adjustable sampling frequency (every 10–15 minutes).
  - Land use manipulation plots
    - Four plots with three replicates each; treatments: Ungrazed, Grazed, Trees.
    - Each plot includes tensiometers and overland flow measurements; replicate locations mapped and layout shown in figures.
  - Neutron probe soil moisture
    - Measurements at multiple sites (bowl, hillslope, manipulation plots, tree areas, Llyn Hir); profiles typically 10 cm to 120 cm depth.
    - Calibration uses a linear relation; peat layering noted at Llyn Hir.
  - Rain gauge data
    - Tipping bucket and storage gauges across several sites; data reported as mm/day and mm respectively.
  - Streamflow
    - Sites 1–13 and Site 10/11 monitored with Starflow acoustic Doppler or pressure transducers and v-notch weirs.
    - Starflow provides minute-by-minute data; calibration against spot measurements via y = αx + β; site-specific parameters (Table 3) and low-flow depth thresholds documented (unreliable below 50 mm).
  - Field diaries
    - Word documents documenting field notes, location instrumentation, and context for data issues.

- Data quality, metadata, and QA
  - QA framework described in Appendices.
  - Appendix A: QA coding system (e.g., Good quality 1x; calibration issues 3x; logger failures 6x; other x-codes for tensiometers, rainfall, streamflow, etc.).
  - Appendices B–C: Borehole logs and neutron probe logs provide site-specific drilling, geology, and measurement details.
  - Field diaries document anomalies, gaps, or instrument problems (e.g., rodent damage, partial data loss).
  - Site-specific issues such as low-flow calibration validity (<50 mm depth) and quality concerns are explicitly noted.

- Data formats, calibration, and processing notes
  - Instrument outputs and calibration
    - Streamflow: Starflow estimates calibrated against manual spot measurements using site-specific α and β; low-flow depth thresholds identified as not suitable for calibration.
    - Neutron probe: Uses linear calibration with soil_count/water_count; clay calibration parameters; peat noted at Llyn Hir.
    - Weir/tipping bucket: Flow derived from pressure transducers and volume changes; notes on sampling times and equipment changes.
    - Groundwater: Barometric compensation via BaroDiver; groundwater height relative to soil surface; temperature data included.
    - AWS: Outputs include daily maxima/minima, daily averages, and wind-direction standard deviation; sensor updates acknowledged (2009).
  - Use and applicability
    - Provides a multi-site, multi-parameter dataset essential for evaluating hydrological responses to land-use, rainfall, evaporation, and groundwater dynamics.
    - Supports trend analyses, policy assessment, and cross-site comparisons through standardized formats and QA codes.
    - Designed for external access and integration with other data sources beyond Pontbren.

- Particular challenges for analysts
  - Increasing dataset value by integrating with other relevant data (avoiding single-use outputs).
  - Enabling access to underlying data used to generate final outputs to ensure transparency and reproducibility.

- Endnotes and supplemental resources
  - Figures illustrate instrument locations and plot designs (Pontbren site, Bowl instrumentation, tree shelterbelt layout).
  - Appendices provide detailed QA codes, borehole logs, and neutron probe access tube logs to aid interpretation and quality assessment.