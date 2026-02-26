# Pontbren Database Catalogue

- A description of the Pontbren Database and the instrumentation used to generate the data.
- Data files are organized into directories following a framework; QA codes are provided for quality-assured data.
- Data are primarily stored as .txt files, typically split into six-month blocks (January–June, July–December) with file names reflecting the collection dates.
- Appendices include supplementary information useful for database users.

## Database framework and structure

- Data organized into main folder groups:
  - AWS (Automatic Weather Station)
  - Bowl study site runoff and soil water tension data
  - Groundwater
  - Hillslope study site runoff and soil water tension data
  - Llyn Hir study site soil water tension data
  - Land use manipulation plots
  - Neutron probe soil moisture data
  - Rain gauge data
  - Field Diaries
  - Streamflow
- Each group contains subfolders by instrument/site (e.g., Bowl runoff weir box, Bowl drain flow tipping bucket, Bowl tensiometers; Site1–Site13 streamflow; etc.).
- Quality assured data entries include a QA code and a description in Appendices.
- Figures referenced illustrate spatial layouts of the study sites.

## Key data categories and what they contain

- AWS (Automatic Weather Station)
  - Sensors sampled every 1 minute; data provided as daily and 10-minute averages.
  - Measurements include incident radiation, wind speed/direction, soil temperature, relative humidity, air temperature, net radiation.
  - Extra columns introduced after 2009 due to additional sensors for humidity and temperature.

- Bowl study site runoff and soil water tension data
  - Contains runoff data (weirs and tipping buckets) and tensiometer data.
  - Runoff data are organized by weir boxes and tipping buckets; flow is reported in litres/second.
  - Water height in weir boxes used to estimate flow; evaporation can cause negative water height, indicating no flow.
  - Tensiometer arrays at 10 cm, 30 cm, and 50 cm depths; data files may be split by array/logger after March 2008.

- Groundwater
  - Data from five groundwater monitoring locations using Diver pressure transducers with barometric compensation.
  - Outputs include groundwater height (cm) relative to soil surface and groundwater temperature.
  - Sampling frequency varied (every 10 minutes initially, later every 30 minutes).

- Hillslope study site runoff and soil water tension data
  - Data from the tree shelterbelt hillslope, including weir boxes for drain flow and overland flow, tensiometers, and tree shelterbelt overland flow measurements.
  - Data quality notes include rodent damage issues affecting overland flow data.
  - Tensiometer arrays similar to Bowl site (depths and logger arrangements vary).

- Llyn Hir study site soil water tension data
  - Tensiometer arrays at 10 cm, 30 cm, and 50 cm depths; sampling initially every 10 minutes, later 15 minutes.

- Land use manipulation plots
  - Four manipulation plots (Rhos1, Rhos2, Tyn y Fron, Penllwyn) with three replicates per plot.
  - Treatments include Ungrazed, Trees, and Grazed, randomly assigned to replicates.
  - Data include tensiometer readings (cm H2O) and overland flow (mm/h) for each replicate plot.

- Neutron probe soil moisture data
  - Neutron probe measurements across bowls, hillslope, manipulation plots, trees, Llyn Hir.
  - Profiles typically provide data every 10 cm down to ~120 cm.
  - Calibration uses a linear equation y = alpha * soil_count / water_count + beta; calibration constants provided (alpha ≈ 0.96, beta ≈ -0.01, with site-specific notes).

- Rain gauge data
  - Tipping bucket and storage gauge data across multiple sites (Bowl, Hirrhos Uchaf, Llyn Hir, Penllwyn, Quarry, Rhos1, etc.).
  - Data reported as mm per day (or mm for storage gauges).

- Field Diaries
  - Word documents containing field notes for monitoring locations/instrumentation, describing issues affecting data quality.

- Streamflow
  - Streamflow data from various gauging sites using bed-mounted Starflow systems ( Sites 1–9, 13) or alternative gauges (Sites 10–12).
  - Starflow data include stage height, velocity, water depth, water temperature, battery status, cross-sectional area, and flow rate; calibration with site-specific equations to align with manual spot measurements.
  - Low-flow data (< 50 mm depth) often excluded from calibration.

## Tables and calibration notes

- Table 1 (AWS headings) lists sensor measurements and units for AWS data.
- Table 3 (Starflow calibration parameters) provides site-specific linear calibration coefficients (alpha*, beta*) used to convert Starflow estimates to calibrated flow in litres/second.
- Calibration is site-specific; low-flow data may be deemed unacceptable for calibration.

## Quality assurance (Appendix A) and documentation (Appendix B, C)

- Appendix A defines a comprehensive QA coding system for different data streams:
  - Tensiometers, Rain Gauges, Tipping Buckets, Groundwater, Starflow, Weir plates, Calibration issues, and Site manipulations.
  - Codes denote good data, questionable quality, calibration or collection issues, rodent damage, transmission gaps, and other anomalies.
- Appendix B provides borehole logs (equipment/methods, location, water strikes, reduced levels, soils, and completion details).
- Appendix C provides neutron probe access tube logs (location, logs, depth, and materials).

## GIS and data usage considerations

- The catalogue is designed to support GIS-based data products by clarifying instrument locations, data resolutions, and the relationships between multiple datasets (e.g., tensiometers aligned with weir or streamflow sites).
- Spatial interpretation is aided by Figures showing instrument locations and study site layouts.
- Data are suitable for creating map-based visualizations of hydrological processes, soil moisture, groundwater dynamics, and land-use impacts on runoff.
- Users should reference QA codes and site-specific calibration details to ensure appropriate interpretation of the data in GIS analyses.

## Practical notes for users

- File organization and naming conventions reflect collection dates; check folder descriptions for content when exploring data.
- Be mindful of data quality issues noted in field diaries and QA codes (e.g., rodent damage to overland flow systems, sensor calibration issues, differences between Starflow estimates and spot measurements).
- For hydrological and soil moisture modeling in GIS, leverage site-specific calibration parameters and ensure proper handling of six-month data blocks and potential data gaps.

## Appendices overview (referred materials)

- Appendix A: QA coding system for data streams (good, questionable, calibration issues, transmission gaps, etc.).
- Appendix B: Borehole logs (equipment/methods, location, water strikes, soils, and completion details).
- Appendix C: Neutron probe access tube logs (location, logs, depth, materials).

## Additional context from equipment & methods documentation (N-probe & borehole details)

- Detailed borehole logs and N-probe manipulations provide site-specific soil descriptions, depths, and completion information to support data interpretation and calibration.
- Location references, datums, and lithology descriptions accompany borehole records to enhance spatial data integration in GIS workflows.