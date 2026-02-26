# Pontbren Database Catalogue

## Overview
- A comprehensive, multi-site environmental monitoring dataset designed to scrutinise environmental health indicators, support policy evaluation, and inform future decisions.
- Aimed at researchers, policy managers, and data custodians requiring discoverable, interoperable data with clear documentation and QA checks.

## Purpose and audience
- Enables policy scrutiny of environmental health indicators and informs decision-making.
- Targets readers needing transparent data governance, metadata, and open sharing of underlying data where appropriate.

## Data framework and structure
- Data organized into directories by data category and study site.
- Each data point can carry a quality assurance (QA) code; QA details provided in appendices.
- Primarily stored as .txt files, grouped in six-month intervals (Jan–Jun, Jul–Dec); filenames indicate collection period.
- Appendices cover QA coding schemes and field notes to aid interpretation and provenance.
- Framework supports data description, metadata augmentation, and public sharing where feasible.

## Data domains and key components
- Automatic Weather Station (AWS)
  - Location: bowl on instrumented hillslope.
  - Sensors sampled every minute; outputs include daily and 10-minute averages; includes daily max/min and wind direction std dev.
  - Post-2009 sensor upgrade added Ave Humidity/Temp.

- Bowl study site runoff and soil water tension
  - Runoff and tensiometer data with instrumentation map (weir boxes, drain flow, overland flow, tunnel/tensiometer arrays, neutron probes, boreholes).

- Groundwater monitoring (boreholes)
  - Five locations with Diver/barometric compensation.
  - Height of water (cm) relative to soil surface; groundwater temperature; variable sampling frequency.
  - Individual boreholes described with location and logs.

- Hillslope study site runoff and soil water tension
  - Tree shelterbelt hillslope measurements; overland flow traps, drain flow, tensiometers.
  - Weir-box data (1-minute sampling, then 5-minute averages).
  - Tree shelterbelt overland flow and tensiometer arrays; notes on data quality (e.g., rodent damage).

- Llyn Hir study site soil water tension
  - Tensiometer array at multiple depths (10, 30, 50 cm); data at 10-minute cadence (adjusted to 15 minutes in Sept 2009).

- Land use manipulation plots
  - Four sites (Rhos1, Rhos2, Tyn Fron, Penllwyn) with three replicate plots each (Ungrazed, Trees, Grazed) in randomized layout.
  - Tensiometer depths at 10/30/50 cm; overland flow data on 10 m × 2.5 m plots (mm/h).
  - Detailed treatment mappings and plot layouts; plot-specific tensiometer and overland flow data per plot.

- Neutron probe soil moisture
  - Profiles across bowl, hillslope, manipulation plots, tree areas, and Llyn Hir; depths 10–120 cm where possible.
  - Calibration: y = α × (soil_count / water_count) + β with α = 0.96, β = -0.01 (peat/site adjustments noted).

- Rain gauge data
  - Tipping bucket and storage gauges across multiple sites (Bowl, Hirrhos Uchaf, Llyn Hir, Penllwyn, Quarry, Rhos1, etc.).
  - Output in mm per day (tipping buckets); storage gauges in mm.

- Field diaries
  - Field notes capturing context, issues, and data conditions for monitoring locations.

- Streamflow
  - Starflow bed-mounted acoustic Doppler systems at several sites; other sites use pressure transducers or v-notch weirs.
  - Data logged every minute; site-specific calibration with spot measurements; parameters include depth, temperature, velocity, cross-sectional area, and flow rate.
  - Calibration relationships (y = αx + β) used to align estimates with manual measurements; low-flow data treated as unreliable for calibration.

## Appendices and quality assurance
- Appendix A: Quality assurance coding system
  - Detailed QA codes for tensiometers, rain gauges, groundwater, starflow, weir plates, tipping buckets, AWS, and manipulation plots.
  - Codes cover good data, questionable quality, detector/collection issues, calibration concerns, and site-specific problems (e.g., rodent damage, power loss, sensor failure).

- Appendix B: Groundwater borehole logs
  - Equipment, methods, and borehole logs with stratigraphy, depths, and completion details.

- Appendix C: Neutron probe access tube logs
  - Logs describing locations and access tubes.

- Appendix D: Streamflow gauging sites flow metered spot measurements
  - Site-specific flow measurements with start/finish times, flow estimates, and calibration notes.

## Data usage, accessibility, and challenges
- Metadata quality and QA are central to usability; QA codes help assess reliability.
- Data sharing is encouraged but can be constrained by data sensitivity, metadata completeness, and governance requirements.
- Common challenges across the dataset:
  - Data gaps or data not meeting “good enough” standards.
  - Data access limitations and timeliness.
  - Siloed information within and between organisations.
  - Public sharing requirements that may hinder use of some data.
  - Keeping datasets up to date and maintaining metadata quality.
  - Data formatting and transformation needed for cross-site analyses.
  - Communicating complex findings clearly to varied audiences.
  - Establishing and maintaining data governance for storage, sharing, and updates.

## Visuals and documentation
- Figures and tables accompany the catalog to support interpretation (e.g., instrument locations, study site layouts, calibration parameters).
- Field diaries and site reports provide contextual insights for data quality and anomalies.

## Bottom line
- The Pontbren Database Catalogue consolidates a multi-site, multi-instrument environmental monitoring dataset with comprehensive documentation, QA coding, metadata, and governance guidance to support robust policy evaluation and informed decision-making.