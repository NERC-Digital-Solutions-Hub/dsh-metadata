# Pontbren Database Catalogue

## Overview
- Comprehensive inventory of Pontbren data, detailing instrumentation, data structure, and how to use the data for analysis and mapping.
- Data organized by site and data type, with extensive metadata, QA codes, and appendices to support data quality assessment and reuse.
- GIS-ready references: precise geolocations, instrument layouts, and site maps to support map-based data products.

## Data organization and access
- Files are structured in site- and data-type folders, under a Quality Assured framework.
- Data points carry QA codes; QA guidance is provided in appendices.
- Data delivered as plain text files (.txt) in six-month blocks (January–June, July–December). Filenames reflect collection dates.
- Appendices provide context for QA, borehole logs, and neutron probe logs; field diaries document field conditions and data reliability.

## Data categories and GIS relevance
- Automatic Weather Station (AWS)
  - High-frequency meteorological data (1-minute sampling; daily and 10-minute averages).
  - Variables include radiation, wind, temperature, humidity; enables temporal weather layers and interpolation to non-AWS sites.
- Bowl study site (runoff and soil water tension)
  - Runoff and tensiometer data; flow in litres/second; evaporation and sensor issues noted.
  - Weir boxes, tipping buckets, and tensiometer arrays across depths (e.g., 10 cm, 30 cm, 50 cm).
- Groundwater
  - 5 boreholes with water height and groundwater temperature; barometric corrections applied.
- Hillslope study site (runoff and soil water tension)
  - Includes multiple weir boxes, tensiometers, and overland flow plots; data require admission of evaporation effects and sampling frequencies.
- Llyn Hir study site
  - Tensiometer arrays with regular sampling; soil moisture context for GIS layers.
- Land use manipulation plots
  - Four plots with varied treatments; tensiometers and overland flow data by plot and replicate; useful for comparative GIS analyses.
- Neutron probe soil moisture
  - Profiling across depth (≈10 cm increments to ~120 cm); counts converted to volumetric moisture with calibration constants.
- Rain gauge data
  - Tipping bucket and storage gauges across multiple sites; site-specific gauge configurations documented.
- Field Diaries
  - Contextual notes to support data interpretation and quality assessment.
- Streamflow
  - Sites 1–13 with site-specific instrumentation and calibration; starflow devices, pressure transducers, and v-notch weirs; includes calibration relationships to align with manual measurements.

## Spatial layout and metadata
- Instrument locations and site maps referenced (Figures 1–3) to support GIS layering.
- Precise grid references (examples: SJ 04760 05725, SJ 06921 06704, etc.) enable accurate georeferencing of boreholes, probes, and gauges.
- Spatial integration supports layering meteorological, hydrological, soil moisture, and streamflow data in GIS applications.

## Temporal structure and data fusion
- Varied sampling frequencies: 1 minute (AWS), 10 minutes (some soil/stream data), 15–60 minutes (streamflow and groundwater), and daily summaries.
- Six-month data blocks require time alignment when merging datasets from different sensors and sites.
- QA codes facilitate data curation before GIS visualization or hydrological modeling.
- Neutron probe and soil moisture data include calibration parameters to translate raw counts to meaningful moisture values.

## Data quality, metadata, and appendices
- Appendices A–C cover:
  - A: Quality assurance coding system for tensiometers, rain gauges, starflow, groundwater, etc.
  - B: Borehole logs (equipment, drilling methods, logging details).
  - C: Neutron probe access tube logs (location, depth, deployment details).
- Field diaries document field observations and data reliability.
- Appendix D provides streamflow gauging site flow metered spot measurements for calibration and validation.

## GIS-specific use-cases and workflows
- Multi-layer GIS maps
  - Overlay AWS climate data with rainfall/runoff, groundwater depth, soil moisture, and streamflow data.
- Time-series mapping
  - High-frequency AWS and streamflow data enable event-driven maps; drought/flood mapping using tensiometer and rainfall series.
- Site-specific calibration surfaces
  - Apply calibration parameters (e.g., streamflow alpha/beta) to starflow outputs for comparison with manual measurements.
- Data fusion and harmonization
  - Spatially referenced data from multiple sites require careful temporal alignment and QA-driven filtering before integration into a single GIS dataset.

## End-to-end considerations for GIS professionals
- Prepare GIS layers by site and data type, incorporating QA status and metadata from appendices.
- Use grid references to georeference all boreholes, probes, and gauges for accurate spatial analyses.
- Maintain temporal synchronization across datasets to enable reliable event analysis and hydrological modeling.
- Leverage site maps and instrument layouts to create intuitive, explorable map-based data products.

## Summary of key points
- The Pontbren Database Catalogue provides a thorough inventory of instrumentation, data structure, and usage guidance for GIS-enabled analysis.
- Data are organized by site and data type, with rich metadata, QA codes, and appendices to support quality assessment and reuse.
- For GIS applications, the Catalogue offers precise geolocation details, instrument placement, and a pathway to integrate diverse hydrological, meteorological, soil moisture, and streamflow data into map-based data products.