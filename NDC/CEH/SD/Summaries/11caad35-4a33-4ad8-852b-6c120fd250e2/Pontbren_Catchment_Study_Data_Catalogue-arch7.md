# Introduction to the DATABASE Catalogue

## Purpose and scope
- Describes the Pontbren Database, detailing instrumentation and data produced.
- Provides a structured, directory-based framework for accessing diverse hydrological, meteorological, and soil data.
- Includes quality assurance (QA) codes and appendices to aid data interpretation and reuse in GIS and map-based analyses.

## Data organization and access
- Data files are arranged into directories by site and dataset type, with consistent naming to indicate collection dates.
- Most data are stored as text files (.txt), typically split into 6-month blocks (January–June, July–December) or adjusted for data frequency.
- Appendices describe QA codes, borehole logs, neutron probe logs, and related metadata.
- The catalogue includes Tables (Table of Tables, Table of Figures) and site maps illustrating instrument locations.

## Core datasets and instrumentation (by site)
- Automatic Weather Station (AWS): minute sampling; outputs include daily and 10-minute averages; includes temperature, radiation, humidity, etc., with updates after 2009.
- Bowl study site: runoff data from weir boxes; soil moisture via tensiometers at 10, 30, 50 cm.
- Groundwater: boreholes with water height and groundwater temperature; barometric correction; varying sampling frequency.
- Hillslope study site: runoff, tensiometers, and overland flow plots.
- Llyn Hir study site: tensiometer arrays for soil water tension at 10/30/50 cm.
- Land use manipulation plots: grazed, ungrazed, trees; tensiometers; overland flow measurements.
- Neutron probe soil moisture: profiles (0–120 cm, 10 cm increments) across multiple areas; water content derived from counts with calibration.
- Rain gauges: tipping-bucket and storage gauges across multiple sites; units in mm/day.
- Field diaries: site observations and data caveats.
- Streamflow and alternative methods: bed-mounted Starflow devices; site-specific calibration to convert Stage/Velocity/Area/Temperature to calibrated flow; includes calibration parameters per site and notes on low-flow data exclusion.
- GIS relevance: instrument locations and layouts support spatial visualization and GIS-based analyses; data cover multiple hydrological and soil variables with high temporal resolution.

## Data quality, standards, and interpretation
- QA codes accompany data to indicate quality status (e.g., good quality, questionable, not suitable for calibration), with specific codes for tensiometers, tipping buckets, rain gauges, and groundwater data.
- Field notes document instrument issues, damage, and data caveats.
- Appendix materials include borehole logs and neutron probe logs with drilling details, lithology, depths, and completions.
- Site maps illustrate instrument locations, aiding GIS-based representation and analysis.

## Calibration and site-specific notes (for GIS and analysis)
- Streamflow calibration: site-specific α* and β* values link Starflow estimates to calibrated flow (L/s); low-flow data may be excluded from calibration.
- Neutron probe data: linear calibration y = α(S_count/W_count) + β, with α ≈ 0.96 and β ≈ -0.01, plus site-specific caveats for topsoil/peat differences.
- Calibration details enable consistent integration of multiple measurement methods within GIS workflows.

## Map-ready and GIS-relevant considerations
- Instrumentation locations and site layouts are provided graphically to support spatial visualization and integration with GIS workflows.
- Data layers span precipitation, runoff, soil moisture, groundwater height, streamflow, and tensiometer readings, enabling multi-layer mapping and spatial analyses across scales.
- Data are time-series with high temporal resolution and are partitioned (e.g., by site, dataset, and time block) for GIS-friendly processing and large dataset management.

## Practical usage notes
- Expect occasional data gaps due to equipment issues (e.g., rodent damage, logger failures, calibration adjustments), as indicated by QA codes.
- Folder contents and data collection methodologies are described to support reproducible GIS analyses and data integration.
- The dataset emphasizes clear metadata, site maps, and calibration references to facilitate map-based interpretation and cross-site comparisons.

## Text (Equipment & Methods and borehole logs) — GIS-relevant details
- Equipment and methods documented for borehole drilling and logging, including:
  - Hand auger, AQ drill rod, guide tubes, pneumatic hammer, rotary drills; borehole logs with site references (e.g., PEN-TAL-Y-CEIN LLANFAIR CAEREINION; Site S3 variations; grid references such as SJ 07360 06833).
  - N-probe (neutron probe) manipulations across multiple plots and sites; various NP numbers (NP20–NP23) with corresponding borehole logs detailing soil types, depths, and sample intervals.
  - Datum levels, depths (mBGL), soil descriptions (e.g., dark yellow brown silty clay; humic soils), and lithology (clay, sandstone/mudstone, gravelly layers).
  - Completion details (16 gauge aluminium tubing), sample intervals (e.g., 0.25–1.60 m), and dates (e.g., 14/05/06).
  - Locations include edges of woodland and manipulation plots (e.g., N-probe Tyn y Fron Trees, Edge of wood).
- Streamflow gauging sites and flow metered spot measurements (Appendix D) provide start/finish times and measured flows at numerous sites, enabling calibration and cross-validation for GIS-based hydrological modeling.