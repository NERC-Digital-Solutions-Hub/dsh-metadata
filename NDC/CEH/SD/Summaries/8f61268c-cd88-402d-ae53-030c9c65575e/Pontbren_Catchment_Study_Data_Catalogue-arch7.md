# Introduction to the DATABASE Catalogue

- A comprehensive, multi-site hydrological database (Pontbren) designed to enable understanding, discovery, and reuse of site-specific environmental data.
- Aims to provide map-like, navigable data products with clear metadata to support GIS-based analysis and visualisation for policy makers, clients, and the public.
- Emphasises audience-oriented documentation to help GIS users locate, interpret, and integrate datasets across sites and instruments.

## Data Organization and Access

- Data organized into directories reflecting the database framework; each data point can have a QA code; descriptions of folders/files provided where needed.
- File formats mainly .txt, divided into six-month blocks (January–June, July–December) to accommodate common data handling limits; file names indicate collection dates.
- Documentation and QA: Appendices cover QA coding schemes and detailed instrument logs to aid data quality assessment.
- Accessibility features: Tables of contents, figure references, and appendices guide users to instrument locations, site layouts, and data quality notes.
- Spatial context: Figures illustrate instrument locations to aid GIS interpretation of spatial relationships.

## Data Content by Site and Instrumentation

- AWS (Automatic Weather Station) at Bowl site: 1-minute sensor sampling; provides daily and 10-minute averages for variables like radiation, wind, temperatures, humidity, and net radiation; sensor updates noted.
- Bowl site hydrological data: Runoff (weir boxes, tipping-bucket) and soil water tension arrays; units include litres/second and cm H2O.
- Groundwater (Tyn y Bryn Hillslope): 5 locations with barometric-compensated transducers; data include water height and temperature; sampling intervals vary from 10 to 30 minutes.
- Hillslope study runoff and soil tension: Weir data for runoff; tensiometers at multiple depths; overland flow data for tree shelterbelt plots; units in litres/second and cm H2O; some data reorganization noted.
- Llyn Hir: Soil water tension arrays with 10/30/50 cm depths; sampling intervals adjusted over time.
- Land use manipulation plots: Four plots with three treatments each; tensiometer arrays and overland flow data; layout documented.
- Neutron probe soil moisture: Profiles typically every 10 cm to depths up to ~120 cm; raw counts converted to volumetric moisture with calibration parameters; special considerations for peat/organic-rich soils.
- Rain gauge data: Multiple sites with tipping bucket and storage gauges; units in mm/day or litres/second; site elevations/context provided.
- Field diaries: Word documents with field notes on monitoring locations and instrumentation to inform data quality.
- Streamflow: Mixed gauging approaches (Starflow Doppler systems and fixed-profile gauging); Starflow yields stage, velocity, cross-sectional area, and flow rate; site-specific linear calibrations (y = αx + β) with reported α and β values and uncertainties.
- Calibration and metadata: Site- and instrument-specific calibrations for streamflow and neutron probe data; QA codes and notes for GIS workflows.

## Data Formats, Time Resolution, and GIS Relevance

- Time-stamped time series with metadata designed for temporal GIS analyses; coordinates/maps included for spatial joins.
- Temporal resolution ranges from 1-minute to 10-minute sensor data; some data aggregated to daily, 5-minute, or hourly values depending on instrument.
- Spatial context: Instrument location figures and site maps facilitate understanding relationships between sensors, plots, and hydrological features.
- Calibration and QA: Site-specific calibration models for streamflow and neutron data; QA codes and notes to guide data filtering in GIS workflows.

## Calibration, Quality, and Metadata Details

- Site-specific streamflow calibrations use linear relationships between Starflow estimates and manual measurements; multiple sites have distinct α and β values with uncertainties.
- QA coding system: Appendix A provides QA codes for various data streams (tensiometers, rain gauges, overland flow, groundwater, starflow, etc.) to support data curation in GIS analyses.
- Appendices B–D: Borehole logs, neutron probe access tube logs, and additional field/equipment metadata to support reproducibility and metadata completeness.

## Appendices and Supporting Documentation

- Appendix A: Quality assurance coding system with detailed codes for data quality, instrument status, and potential issues (e.g., instrument faults, calibration problems, field disturbances).
- Appendix B: Groundwater monitoring borehole logs with equipment, methods, and log details.
- Appendix C: Neutron probe access tube logs.
- Appendix D: Field/groundwater/streams related logs and data quality notes.
- Streamflow gauging site details and calibration records embedded within the documentation.

## GIS Specialist Takeaways

- Rich, well-documented, multi-site hydrological dataset with extensive instrument inventories, site maps, and QA guidance suitable for GIS-based analysis and map-based data products.
- Comprehensive metadata enables spatial joins and layered analyses across weather, runoff, soil moisture, groundwater, and streamflow for integrated hydrological modelling and policy-relevant visualization.
- Calibration models and QA codes provide essential data filters for GIS workflows, including site-specific streamflow calibrations and neutron-probe moisture content transformations.