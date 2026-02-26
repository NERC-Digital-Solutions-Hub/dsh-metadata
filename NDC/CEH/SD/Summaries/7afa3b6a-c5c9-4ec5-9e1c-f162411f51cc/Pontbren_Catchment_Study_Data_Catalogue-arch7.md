# Pontbren Database Catalogue

## Overview
- Comprehensive collection describing the Pontbren Database, including instrumentation, data content, organization, and user-focused guidance.
- Emphasizes map-based data products, GIS-friendly context, and guidance for data discovery, access, quality assessment, and interpretation.

## Data structure & Access
- Data organized into directories by data type and site (e.g., AWS, bowl study site, hillslope, Llyn Hir, land-use plots, groundwater, neutron probe, rain gauges, streamflow, field diaries).
- Data files are primarily text (.txt), commonly split into six-month blocks; file names indicate collection date ranges.
- Each data point may carry a quality assurance (QA) code; Appendix materials provide QA details.
- Appendices offer supplementary information (QA coding, borehole logs, neutron probe logs, streamflow calibrations, field notes).

## Instrumentation & Data Categories (high-level)
- AWS (Automatic Weather Station): 1-minute sensor data; outputs include daily and 10-minute averages, daily max/min, and wind statistics; post-2009 sensor changes add extra columns.
- Bowl study site: Runoff and soil water tension data from weirs, tipping buckets, tensiometers.
- Groundwater: Multiple boreholes with transducer readings; barometric correction; expressed as height relative to soil surface plus temperature.
- Hillslope study site: Runoff, tensiometers, and overland flow data.
- Llyn Hir study site: Soil water tension data; sampling frequency adjusted to manage data volume.
- Land-use manipulation plots: Four sites with treatments (Ungrazed, Trees, Grazed); tensiometer arrays and overland flow measurements.
- Neutron probe soil moisture: Depth profiles (typically every 10 cm to ~120 cm) across multiple sites; includes calibration model.
- Rain gauges: Tipping bucket and storage gauges across several sites; units in mm/day or mm.
- Field Diaries: Site-specific notes describing data issues and events.
- Streamflow: Site-specific instrumentation (Starflow acoustic Doppler or transducers/weirs) with calibration tables linking estimates to manual measurements.

## Data Quality & QA
- QA coding system defines quality categories and fault types (Good, questionable, calibration issues, logger faults, sensor damage, environmental damage).
- Some data have known issues (e.g., rodent damage, outages, sampling timing differences); QA codes enable filtering or weighting for GIS analyses.

## Calibration & Site Processing
- Streamflow calibration uses site-specific linear relationships between Starflow estimates and manual measurements (alpha x + beta; site-dependent).
- Neutron-probe data use a calibration equation relating counts to water content, with site-specific adjustments for certain soil layers (e.g., peat).
- Low-flow data are often excluded from calibration due to reliability considerations.
- Calibration parameters include uncertainty (e.g., standard deviations).

## Spatial Context & GIS Relevance
- Figures illustrating instrument locations support GIS mapping and spatial analysis.
- Data include precise location descriptors (grid references, site names, typical coordinates) to enable spatial joins and mapping of instruments, boreholes, and hydrological features.
- Designed for integration into map-based visualizations and multi-site comparisons (e.g., comparing tensiometer responses, overlaying rainfall, streamflow, and soil moisture).

## Appendices & Metadata
- Appendix A: QA coding system (detailed fault and quality codes for all data streams).
- Appendices B–C: Groundwater borehole logs and neutron-probe logs (structure, depths, materials, references).
- Appendix D: Streamflow gauging site calibration and field-measured data (spot measurements).

## Practical Guidance for GIS Specialists
- Expect 1-minute AWS data with derived 10-minute and daily summaries; post-2009 changes may introduce extra columns.
- Runoff and soil tension datasets are organized by instrument type and site; anticipate patchy data and varying sampling intervals.
- Data are text-based; build robust parsers and handle six-month blocks or custom date ranges.
- Use QA codes to filter data for analyses requiring consistent data quality.
- Apply site-specific calibration parameters when converting flow or neutron-probe readings to comparable hydraulic quantities.
- Reference maps, borehole logs, and instrument layouts are essential for accurate spatial alignment and GIS joins.

## Summary Takeaway
- The Pontbren Database Catalogue provides a QA-focused, site-wide compilation of hydrological, soil moisture, and meteorological data with rich instrumentation metadata, calibration parameters, and field notes, all organized to support map-based GIS visualizations and spatial analyses.