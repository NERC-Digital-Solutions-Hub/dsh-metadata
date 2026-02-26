# Introduction to the Database Catalogue

## Purpose and scope
- Describes the Pontbren Database, including instrumentation, data provisioning, data organization, QA coding, and documentation.
- Explains data structure, directory layout, and QA coding used to document data quality.
- Notes data are stored as text files (TXT) in 6-month blocks with filenames indicating collection periods; appendices provide metadata and QA guidance.

## Database structure and contents
- Data organized into thematic directories with appendices for QA and instrument logs.
- Main data categories (folders) include:
  - AWS (Automatic Weather Station)
  - Bowl study site runoff and soil water tension data
  - Groundwater (boreholes)
  - Hillslope study site runoff and soil water tension data
  - Llyn Hir study site soil water tension data
  - Land use manipulation plots
  - Neutron probe soil moisture data
  - Rain gauge data
  - Field Diaries
  - Streamflow
- Each category contains subfolders for specific instruments or sites (e.g., Bowl runoff weir boxes, tensiometers at multiple depths, Site1..Site13 for streamflow).

## Data collection, frequency, and formats by dataset
- AWS
  - Sensors sampled every 1 minute; outputs include daily and 10-minute averages.
  - Measurements include incident radiation, wind, soil and air temperatures, humidity, net radiation, etc.
  - Post-2009 updates added RH and air temperature columns for new sensors.
- Bowl study site runoff and tensiometers
  - Runoff from weir boxes and tipping bucket systems; flow in litres per second.
  - Tensiometer arrays at 10 cm, 30 cm, and 50 cm depths; data in cm H2O.
- Groundwater (boreholes)
  - 5 boreholes with Diver pressure transducers; data as water height and temperature with barometric correction.
  - Sampling cadence changed over time (from every 10 minutes to every 30 minutes).
  - Borehole journal logs included in appendices.
- Hillslope study site runoff and soil water tension
  - Runoff data from weir boxes (drain and overland flow) and tensiometers; flow in L/s; multiple depths for tensiometers.
  - Some overland flow data patchy due to rodent damage affecting quality.
- Llyn Hir study site
  - Tensiometer arrays at multiple depths; sampling cadence adjusted over time (e.g., 10 to 15 minutes).
- Land use manipulation plots
  - Four sites with three replicate plots each; treatments Ungrazed, Trees, and Grazed.
  - Data include tensiometer arrays (three depths) and overland flow (mm/h) on isolated plots.
- Neutron probe soil moisture
  - Profile moisture data from bowl, hillslope, manipulation plots, tree areas, and Llyn Hir; depths down to ~120 cm at 10 cm intervals where possible.
  - Calibration uses site-specific parameters or CEH-provided parameters.
- Rain gauges
  - Tipping bucket and storage gauge data across multiple sites; units in mm and mm/day.
- Field Diaries
  - Word documents with field notes for monitoring locations and instrumentation; describe issues and data context.
- Streamflow
  - Sites 1–9 and 13 use bed-mounted Starflow systems (flow, depth, velocity) logged every minute and averaged to 15-minute intervals.
  - Sites 10–12 use pressure transducers and v-notch weirs with calibration to spot measurements; site-specific calibration equations published in tables.
- Appendices and documentation
  - Appendices include QA coding system (Appendix A) and borehole/neutron probe logs and groundwater documentation (Appendices B–D).
  - Field diaries and site figures referenced throughout.

## Quality assurance and metadata
- QA codes accompany data points; Appendix A lists codes for good data and common issues (logger failures, sensor calibration, flow measurement issues, rodent damage, etc.).
- Field diaries provide context for data quality events and instrumentation issues.
- Metadata explains data file structure, headings, and calibration relationships (e.g., Starflow with spot measurements, neutron probe calibration parameters).

## Notable data issues and cautions
- Data gaps and patchy data in some sub-systems, notably Hillslope overland flow due to rodent damage.
- Data quality varies by site and time; QA codes are essential for interpreting data reliability.
- Calibration and site-specific parameters are crucial for accurate streamflow and neutron-probe conversions; readers should consult calibration tables and notes.

## Appendices and detailed documentation
- Appendix A: QA coding framework for interpreting data quality at the point level.
- Appendices B–D: Borehole and neutron probe logs, groundwater monitoring documentation, methodology, site references, and sampling details.
- Field diaries and site figures support data provenance and reuse.

## Practical implications for data governance and reuse
- Supports cross-site data integration through standardized structure, QA coding, units, and sampling frequencies.
- Enhances data discovery, validation, and reuse across networks and partners via clear instrumentation documentation and site layouts.
- Provides a comprehensive, multi-parameter view of hydrology and soil moisture dynamics, enabling policy-facing data leadership and cross-disciplinary analytics.