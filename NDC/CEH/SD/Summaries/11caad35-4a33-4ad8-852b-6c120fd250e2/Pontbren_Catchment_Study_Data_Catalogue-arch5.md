# Pontbren Database Catalogue

## Purpose and Scope
- Describes the Pontbren Database, detailing instrumentation and data provisions to support discovery, sharing, and reuse.
- Data are organized in directories with metadata and quality assurance information; includes appendices for supplementary context.

## Data Organization and Framework
- Data files are structured in a hierarchical directory framework by site and data type (e.g., AWS, Bowl runoff, Groundwater, Streamflow).
- Quality assured (QA) data are labeled and documented; QA codes are provided in Appendices.
- Most data are stored as .txt files, typically split into six-month blocks; file names reflect collection date ranges.
- Descriptions of folder contents accompany the catalogue to aid navigation and reuse.

## Data Categories and Instrumentation
- AWS (Automatic Weather Station)
  - Data sampled every 1 minute; daily and 10-minute averages produced; includes daily max/min, daily mean, and wind direction standard deviation.
  - Sensor upgrades post-2009 led to improved humidity and temperature measurements.
- Bowl study site runoff and soil water tension
  - Subfolders for Bowl runoff (weir boxes, tipping buckets) and Bowl tensiometers (arrays at depths 10/30/50 cm).
  - Weir box measurements estimate flow; occasional negative height indicates no flow.
- Groundwater
  - Five boreholes monitored with Diver pressure transducers and barometric compensation; data expressed as groundwater height plus temperature; sampling cadence changed over time.
- Hillslope study site runoff and soil water tension
  - Data from tree shelterbelt hillslope: weirs (drain/overland flow), tensiometers (multiple depths), and tree shelterbelt overland flow data.
- Llyn Hir study site soil water tension
  - Tensiometer arrays at 10/30/50 cm; sampling cadence adjusted over time.
- Land use manipulation plots
  - Four plots with three replicates each; treatments Ungrazed, Trees, Grazed; tensiometers and overland flow within plots.
- Neutron probe soil moisture
  - Raw counts across multiple sites; moisture derived via calibration; depth profiles up to 120 cm with peat affecting calibration.
- Rain gauge data
  - Tipping bucket and storage gauges at multiple sites; data reported as mm per day; site elevations and drainage features noted.
- Field diaries
  - Field notes describing instrumentation, monitoring locations, data issues, and site conditions.
- Streamflow
  - Monitored with Starflow acoustic Doppler systems (and some conventional methods); calibrated against manual spot measurements using site-specific relationships.

## Data Quality, Metadata, and Calibration
- Quality Assurance (QA) coding system
  - Appendix A defines QA codes for data quality (good, questionable, calibration/measurement issues, logger failures, instrument-specific problems, etc.) across AWS, tensiometers, rainfall, groundwater, and streamflow.
  - Codes cover field issues such as rodent damage and sensor miscalibration.
- Calibration and site-specific notes
  - Streamflow calibration uses linear relationships (y = αx + β) with parameters provided; low-flow data may be excluded from calibration.
- Data quality caveats
  - Some datasets are patchy (e.g., rodent damage affecting tree shelterbelt data) and certain datasets are unsuitable for calibration or flagged as questionable.
  - Documented data gaps and changes in sampling cadence to inform interpretation and analyses.

## Appendices and Supporting Materials
- Appendix A: Quality assurance coding system (extensive codes for AWS, tensiometers, rain gauges, tipping buckets, groundwater, weir boxes, and calibration issues).
- Appendix B: Groundwater borehole logs (equipment, method, locations, lithology, depths, water strikes, and casing details).
- Appendix C: Neutron probe access tube logs (locations and logs).
- Appendix D: Field notes and logs (field diaries, site references, calibration/measurement context) and streamflow gauging site data.

## Data Governance and Stewardship Considerations
- The catalogue provides a comprehensive governance framework for data storage, metadata, QA, and updates to support discoverability and reuse.
- Users should note instrument-specific issues (e.g., rodent damage, sensor upgrades, cadence changes) and consult field diaries and QA codes when assessing data quality.
- Data stewardship implications include maintaining consistent metadata standards, updating calibration parameters, and documenting corrections or exclusions.

## Practical Guidance for Data Discovery and Reuse
- Use the directory structure to locate data by site and data type (e.g., AWS, Bowl runoff, Groundwater, Streamflow).
- Consult Table 1 and Table 3 for data headings and site-specific calibration parameters, respectively.
- Check Appendices A–D for quality codes, borehole logs, neutron probe logs, and field context to inform data suitability for calibration, modelling, or longitudinal analyses.
- Be aware of data limitations (patchy data, occasional sensor failures, and historical cadence changes) when performing longitudinal analyses or cross-site comparisons.