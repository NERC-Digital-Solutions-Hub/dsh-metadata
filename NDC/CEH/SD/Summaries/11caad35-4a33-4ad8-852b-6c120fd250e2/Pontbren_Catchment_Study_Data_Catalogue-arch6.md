# Introduction to the Database Catalogue

- Purpose: A comprehensive metadata and data-management resource to enable discovery, combination, and analysis of Pontbren study data, supporting self-serve use through dashboards, reports, or charts.
- Audience and use: Intended for end users across diverse topics (environmental monitoring, hydrology, soil moisture, streamflow, etc.) who need to locate, assess quality, and integrate datasets for analysis and modeling.
- Scope: Documents data organisation, QA, instrumentation, data types, calibration parameters, site notes, and data-quality considerations across Pontbren study sites.

## Data structure, organisation, and accessibility

- Hierarchical folder structure organized by data type and study site.
- Data files typically stored as .txt files in 6-month blocks (e.g., Jan–Jun, Jul–Dec); file names indicate date ranges.
- Appendices provide supplementary information, metadata, and user guidance.
- QA codes accompany data records to signal reliability and suitability for calibration, modeling, or trend analysis.

## Data categories and instrumentation

- AWS (Automatic Weather Station): 1-minute cadence with daily/10-minute averages; includes incident radiation, wind, temperature, humidity, net radiation; sensor upgrades added columns over time.
- Bowl study site runoff and soil water tension: multiple subfolders for weirs, tipping buckets, drains, tensiometers; flows in litres per second; evaporation impacts noted.
- Groundwater (piezo-monitoring): Diver pressure transducers with BaroDiver corrections; outputs water height and groundwater temperature; sampling frequency adjusted over time.
- Hillslope and Llyn Hir study sites: runoff, tensiometers, and soil moisture data with various logging configurations; some quality concerns (e.g., rodent damage) noted.
- Land use manipulation plots: replicated plots with treatments (Ungrazed, Trees, Grazed); tensiometers at multiple depths; overland flow measurements.
- Neutron probe soil moisture: depth-profile measurements (0–120 cm typically); calibration using standard model; adjustments for peat/organic layers.
- Rain gauge data: multiple locations with tipping bucket and storage gauges; data expressed as mm/day or mm.
- Field diaries: notes on field conditions and instrumentation issues affecting data quality.
- Streamflow: multiple sites using Starflow bed-mounted AD devices (minute-scale data) and some sites with transducers or v-notch weirs; site-specific calibration relationships for converting to discharge; filtering criteria for low-flow data.
- Tables and figures: instrument locations, QA calibration parameters, and site layouts.

## Quality assurance, metadata, and documentation

- Appendix A: QA coding system (Good quality = 1x; questionable = 2x; not suitable for calibration = 3x) with fault codes for tensiometers, rain gauges, tipping buckets, groundwater, starflow, and weir boxes.
- Appendix B: Borehole logs; Appendix C: Neutron probe logs; Appendix D: Streamflow gauging sites and flow-measured records.
- Field diaries provide context on data collection issues and events that influence interpretation.
- Outputs may include QA codes alongside measurements to indicate data reliability and calibration suitability.

## Data usage, integration, and cross-site analysis

- Designed to enable discovery, combination, and cross-site comparison across rain, runoff, soil moisture, streamflow, groundwater, tensiometer, and neutron probe datasets.
- Users should consult QA codes to determine data suitability for calibration, modeling, or trend analyses.
- Documentation highlights how to integrate diverse data streams and apply site-specific calibration parameters.

## Known data quality issues and caveats

- Rodent damage to Hillslope overland flow traps; peat layers affecting neutron calibration; variability in sampling intervals across sites.
- Data quality codes help identify data suitable for calibration versus exploratory analyses.
- Endnotes emphasize comprehensive metadata, calibration parameters, and site-specific notes to support robust interpretation.

## Text-specific insights: equipment, site logs, and data granularity

- Borehole logging and drilling details indicate depth-specific lithology descriptions, datum levels, and completion details (e.g., NP20–NP23 logs, motor/drill configurations, and 16-gauge aluminium access tubing).
- Logs capture grid references, soil textures, moisture-related measurements, and depth intervals, illustrating the depth-resolved data that feed neutron probe and groundwater datasets.
- Appendix D provides site-by-site streamflow gauging data with flow metered estimates and time stamps, demonstrating the integration of field measurements with instrument-based records.

## Endnotes and metadata completeness

- The catalogue is intended to be comprehensive, offering calibration parameters, site notes, and metadata to enable robust data use, combination, and interpretation across Pontbren study sites.
- Emphasises cross-site comparability and transparent documentation of data quality and collection conditions.