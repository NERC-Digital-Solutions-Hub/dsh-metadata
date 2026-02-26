# Pontbren Database Catalogue

- Overview: A comprehensive catalogue describing the Pontbren Database, its instrumentation, data files, folder structure, and metadata. It explains how data are collected, stored, quality-assured, and described to support GIS-based analysis and map-style data products.
- Purpose for GIS specialists: Provides spatially referenced, instrumented datasets needed for map-based visualisations, trend analyses, and flood/soil-moisture modelling across multiple study sites.

## Data structure, access and file organisation

- Data are organized into directories with a defined framework; quality-assured data include QA codes at each data point.
- Files are typically plain text (.txt), divided into six-month blocks (e.g., January–June, July–December) or other intervals as needed.
- Filenames indicate collection dates; folders describe contents; appendices provide supplementary information (QA coding schemes, borehole logs, neutron/probe logs).
- The database structure is hierarchical (e.g., AWS, Groundwater, Hillslope, Llyn Hir, Land use plots, Neutron probes, Rain gauges, Streamflow, Field Diaries, Appendices).

## Data categories and instrumentation

- AWS (Automatic Weather Station)
  - Located at the bowl within the instrumented hillslope.
  - Sensors sampled every 1 minute; data provided as daily, 10-minute, and higher-frequency averages.
  - Includes incident radiation, wind, soil and air temperatures, humidity, net radiation; sensor replacement notes add columns from 2009 onward.

- Bowl study site runoff and soil water tension
  - Includes runoff and tensiometer datasets; features weir boxes (drain/overland flow) and tipping-bucket data.
  - Weir boxes measure water height above a 90-degree weir; flow calculated in litres/second.
  - Tensiometers deployed at 10, 30, 50 cm depths; data in cm H2O.

- Groundwater (Boreholes)
  - Monitored at five locations with Diver pressure transducers (BaroDiver corrections for barometric pressure).
  - Data expressed as height of water (cm) relative to soil surface, plus groundwater temperature.
  - Borehole logs provide detailed construction descriptions for each site.

- Hillslope study site runoff and soil water tension
  - Data from the tree shelterbelt hillslope (runoff, drain flow, overland flow) and tensiometers.
  - Weir box data: 1-minute sampling, 5-minute data logging; evaporation can affect water height.
  - Tree shelterbelt overland flow recorded on plots, later replaced with tipping-bucket systems (continuous, 10-minute logging).

- Llyn Hir study site soil water tension
  - Tensiometer array near Llyn Hir; three tensiometers at 10, 30, 50 cm; data every 10 minutes (sometimes 15 minutes).

- Land use manipulation plots
  - Four plots with three replicates each (treatments: Ungrazed, Trees, Grazed).
  - Tensiometer data at 10, 30, 50 cm; overland flow measured on plots (10 m × 2.5 m).
  - Replicate plot treatment locations and designs documented in accompanying tables/figures.

- Neutron probe soil moisture
  - Data from bowl, instrumented hillslope, manipulation plots, tree areas, Llyn Hir.
  - Profiles down to ~120 cm; soil moisture content derived from neutron counts with calibration parameters.

- Rain gauge data
  - Tipping bucket and storage gauge data from multiple sites; measurements reported as mm per day (tipping buckets) and storage gauges.

- Streamflow
  - Varied gauging techniques (Starflow acoustic Doppler for most sites; some sites with pressure transducers and v-notch weirs).
  - Starflow outputs include stage height, velocity, and flow rate; calibration relationships provided per site.

- Field diaries
  - Word documents detailing field observations and issues affecting data quality.

## Data quality, calibration, and QA

- Appendix A: Quality assurance coding system
  - Codes describe data quality: Good (1x), questionable (2x), not suitable for calibration (3x), plus site- and sensor-specific fault codes (tensiometers, rain gauges, starflow, groundwater, etc.).
  - Includes issues like rodent damage, sensor miscalibration, logger faults, and calibration anomalies.

- Appendix B and C
  - Borehole logs and neutron probe logs provide detailed equipment/methods, locations, access tubes, and depth references.
  - Logs cover coordinates, datum levels, lithology, sampling intervals, and completion details.

- Data quality notes
  - Some datasets patchy due to issues such as rodent damage (noted for hillslope overland flow traps), evaporation effects, and logger limitations.
  - Starflow calibration parameters are site-specific; low-flow caveats noted; calibration against spot measurements recommended.

## Calibration, mappings and GIS relevance

- Spatial information
  - Instrument locations are depicted in site layout figures; many boreholes and probes have precise grid references (e.g., SJ grid references in logs).
  - Data integration with GIS is supported by embedded location data in field logs, borehole logs, and site maps.

- Temporal resolution and data richness
  - High-temporal-resolution data (1-minute to 10-minute intervals) enable dynamic, map-based visualisations of hydrological processes.
  - Six-month blocks help manage large datasets within GIS workflows; site-specific calibration datasets (Starflow) support consistent flow estimation.

- Data product readiness
  - Metadata and QA context enable creation of map-based data products (e.g., rainfall-runoff maps, soil moisture isopleths, groundwater depth maps, streamflow distributions) while flagging data quality limitations for GIS analyses and modelling.

## Appendices and metadata resources

- Appendices include:
  - Appendix A: QA coding system
  - Appendix B: Borehole logs
  - Appendix C: Neutron probe access tube logs
- Field diaries and calibration tables
  - Field diaries document site-specific issues; calibration parameters (e.g., Starflow) and site-specific notes support GIS-based hydrological analyses.

## End notes and caveats

- Data are comprehensive but have site- and instrument-specific limitations (e.g., rodent damage, sensor replacements, variable sampling frequencies, data gaps).
- Users should consult QA codes, site-specific calibration parameters, and field diaries when aggregating data for GIS analyses or when performing hydrological modelling across Pontbren study sites.