# Introduction to the Pontbren Database Catalogue

- Purpose: Describe the Pontbren Database, detailing instrumentation, data organization, and quality assurance to support consistent long-term environmental monitoring and policy-related scrutiny.
- Audience: Organisations with established monitoring duties and analysts who rely on standardized data products, QA, and clear documentation.

## Data framework and organization
- Data organized into directories with a described framework; datasets typically stored in 6-month blocks (with some exceptions).
- Each data point in QA-enabled files carries a quality assurance (QA) code; QA details provided in appendices.
- Descriptive notes and appendices accompany datasets to aid users.
- Interface includes navigational elements (tables of contents, tables, figures) to orient users.

## Core data categories and instrumentation (sites and data streams)
- Automatic Weather Station (AWS) data at Bowl site: 1-minute sampling; daily and 10-minute averages; standard meteorological variables; sensor-change notes.
- Bowl study site: runoff and soil-water tension (tensiometers); weir boxes, drain/overland flow data; tipping bucket data.
- Groundwater: five boreholes at Hillslope site; Diver transducers with barometric compensation; height and temperature data; varying sampling intervals.
- Hillslope study site (tree shelterbelt area): runoff, tensiometer data across depths, overland flow plots; notes on data quality and rodent issues.
- Llyn Hir site: soil-water tension data from tensiometers; proximity to streamflow gauges; sampling frequency adjustments.
- Land-use manipulation plots (Rhos1, Rhos2, Tyn Fron, Penllwyn): four plots with replicates; treatments include Grazed, Ungrazed, Trees; tensiometers at 10, 30, 50 cm; overland flow within plots; dedicated datasets per plot.
- Neutron probe soil moisture: multi-site measurements across bowls, hillslope, plots, tree areas, Llyn Hir; profile measurements typically every 10–120 cm; calibration described.
- Rain gauges: tipping bucket and storage gauges across multiple sites; units/location context provided.
- Field diaries: notes documenting site-specific issues and data anomalies.
- Streamflow: Starflow (acoustic Doppler) gauging at most sites; some sites use bed-mounted Starflow or alternative instruments; calibration relations to spot measurements documented.

## Measurement details and data handling
- Data frequency/format:
  - AWS: 1-minute samples; daily and 10-minute averages; post-2009 sensor-upgrade columns added.
  - Runoff/tensiometer: high-frequency logging (often 1–5 minutes) with QA flags.
  - Groundwater: height (cm) and temperature; variable sampling intervals with barometric correction.
  - Rain gauges: tipping bucket (mm/day); storage gauge (mm).
  - Streamflow: Starflow outputs with site-calibrated relationships to spot measurements; low-flow data flagged as less reliable.
- Flow estimation and calibration:
  - Bowl weirs: flow derived from water height relative to weir bottom; primary measurement in L/s; evaporation corrections acknowledged.
  - Weir boxes/tipping buckets used for cross-validation of drain/overland flow.
  - Starflow: site-specific calibration lines against manual measurements; alpha/beta parameters documented with uncertainties.
- Neutron probe data: soil moisture via linear calibration; site-specific notes (e.g., surface peat at Llyn Hir).
- Data quality and issues:
  - QA codes track logger failures, sensor problems, physical damage (e.g., rodents); Hillslope data show patchy datasets due to rodent damage.
- Quality assurance and documentation:
  - Appendices provide QA coding system (Appendix A) covering tensiometers, rain gauges, tipping buckets, starflow, groundwater, etc.
  - Borehole logs and neutron probe logs (Appendices B–D) provide contextual notes.
  - Field diaries summarize issues and may explain anomalies in the dataset.

## Quality assurance, calibration, and data availability
- QA codes enable users to assess data reliability and decide on calibration or exclusion for analysis (Appendix A).
- Site-specific calibration parameters (e.g., starflow vs. spot measurements) are documented (Table 3) to ensure transparent cross-site comparability.
- Emphasis on storing and uploading created datasets to appropriate portals for long-term accessibility and reuse.

## Practical notes and limitations
- Some datasets are patchy or compromised by environmental factors (e.g., rodent damage, equipment upgrades, sampling-frequency changes).
- Data files may vary in structure due to equipment changes, logger reorganizations, or sampling constraints; users should consult the catalogue for file descriptions and QA codes.
- The catalogue is designed to support meta-analyses and cross-site data integration by providing standardized terminology, QA labeling, and calibrated relationships across multiple study sites and data streams.