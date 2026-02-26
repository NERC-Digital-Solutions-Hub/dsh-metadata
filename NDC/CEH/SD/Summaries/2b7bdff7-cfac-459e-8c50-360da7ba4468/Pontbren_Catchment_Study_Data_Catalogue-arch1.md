# Introduction to the Database Catalogue

- The Pontbren Database Catalogue describes instrumentation, data organization, and quality assurance to support data-driven analysis and modeling.
- Scope covers multiple data streams from Pontbren study sites, plus documentation and metadata to enable discovery and reuse.
- Key message for analysts: the catalogue explains what data exist, how they were collected, how they are stored, how quality is assessed, and how to calibrate and combine datasets for analysis and modeling.

## Data Structure and Framework

- Data are organized into directories by data type and site, with clear folder names and descriptions.
- Quality assured data are tagged with QA codes; appendices describe these codes.
- Most data are provided as .txt files, typically split into six-month blocks (Jan–Jun and Jul–Dec).
- File naming generally reflects the dates spanned by the data.
- Appendices provide supplementary information useful for dataset users (QA coding, borehole logs, neutron probe logs, streamflow site measurements).

## Instrumentation and Datasets by Theme

- Automatic Weather Station (AWS)
  - Location: bowl within the instrumented hillslope
  - Sampling: sensors at 1-minute intervals; daily and 10-minute averages produced
  - Variables: incident radiation, wind speed/direction, soil temperature, relative humidity, air temperature, net radiation
  - 2009: two extra columns added for humidity and temperature sensors

- Bowl study site runoff and soil water tension
  - Runoff measured via bowl runoff weir boxes; includes drain and overland flow paths
  - Flow measurement: water height above 90° weir; flow in litres/second
  - Tipping bucket systems for drain and overland flow; tensiometer arrays at 10, 30, 50 cm depths

- Groundwater (boreholes)
  - 5 groundwater locations monitored with Diver pressure transducers; BaroDiver for barometric compensation
  - Data as height of water (cm) and groundwater temperature
  - Sampling frequency: primarily every 10 minutes, later 30 minutes for some sites
  - Borehole details provided in appendices (locations and logs)

- Hillslope study site runoff and soil water tension
  - Runoff measured via hillslope weir boxes (drain and overland flow)
  - Tensiometers: arrays at specified depths; some sensors removed in 2008
  - Tree shelterbelt overland flow: two 5 m × 5 m plots; progressed from cumulative measurements to continuous tipping-bucket data

- Llyn Hir study site soil water tension
  - Tensiometers at 10, 30, 50 cm; sampling typically every 10 minutes, later 15 minutes

- Land use manipulation plots
  - Four plots with three replicates each (1–3 within a plot)
  - Treatments: Grazed (control), Ungrazed (no sheep), Trees (trees planted and sheep removed)
  - Replicates include tensiometers (10, 30, 50 cm) and overland flow plots (mm/h)

- Neutron probe soil moisture
  - Datasets from bowl, hillslope, manipulation plots, tree areas, and Llyn Hir
  - Profile measurements typically every 10 cm down to 120 cm
  - Moisture content calculated with a calibration equation; peat considerations at some sites

- Rain gauge data
  - Tipping bucket gauges and storage gauges across multiple sites
  - Data reported as mm/day (tip data) and mm (storage data)

- Field Diaries
  - Word documents with field notes for monitoring locations and instrumentation
  - Document issues potentially explaining data anomalies

- Streamflow
  - Monitored across multiple sites via Starflow bed-mounted Doppler systems; some sites use v-notch weirs with pressure transducers
  - Data: stage height, velocity, depth, temperature, cross-sectional area, and flow rate; calibration per site against manual measurements
  - Site-specific calibration: y = αx + β; low-flow data (< 50 mm depth) not used for calibration

## Calibration and Data Processing

- Flow calibration
  - Site-specific linear relationships (y = αx + β) between Starflow estimates and manual measurements
  - Low-flow data below 50 mm depth are not used for calibration

- Neutron probe calibration
  - Moisture content computed via a line equation using soil_count and water_count
  - Calibration parameters: α ≈ 0.96, β ≈ −0.01 (clay-based; peat considerations at some sites)

- Data handling
  - Datasets stored with metadata and quality codes; some flagged for issues such as rodent damage or equipment problems
  - Some data are patchy or partially reliable due to field conditions

## Quality Assurance and Documentation

- Appendix A: QA coding system
  - Codes for overall data quality (Good, questionable, not suitable for calibration, etc.)
  - Specific codes for tensiometers, rainfall gauges, tipping buckets, starflow, groundwater, calibration issues, and other faults
  - Codes cover manipulation, plots, and instrumentation issues

- Appendices B–C
  - Appendix B: Borehole logs (equipment, drilling details, lithology, water strikes, datum levels, borehole completion)
  - Appendix C: Neutron probe logs (access tubes and logs across sites)

- Metadata and site descriptions
  - Instrument location figures; Table of Tables and Table of Figures
  - Field diaries provide context for data quality and site conditions

## Challenges and Considerations for Analysts

- Data availability and scale
  - Local-scale data may be sparse for some variables or sites
  - Data stored across journals, reports, and multiple local authorities; accessibility issues noted

- Data access and discoverability
  - Datasets may be known only within niche circles; access may require significant effort and domain expertise

- Data integration and standardization
  - Unifying data from multiple sources and formats; variable quality and differing spatial/temporal scales
  - Data protection and privacy considerations for public health-related data

- IT and workflow constraints
  - Administrative rights, legacy software, and heavy computational demands can impede analysis

- Promoting impact and usability
  - Challenges in translating findings into actionable insights and ensuring datasets are discoverable and usable by others

- Detail gaps
  - Some data lack useful details such as administrative boundaries; field conditions can introduce gaps

- Suitability for calibration and modeling
  - Calibration constraints due to data gaps, low-flow periods, or degraded measurement periods

- Usage guidance
  - Use QA codes to assess data quality prior to calibration or modeling
  - Refer to site-specific calibration parameters for Starflow and neutron probe conversions
  - Use Appendices for borehole logs and neutron probe logs to support interpretation