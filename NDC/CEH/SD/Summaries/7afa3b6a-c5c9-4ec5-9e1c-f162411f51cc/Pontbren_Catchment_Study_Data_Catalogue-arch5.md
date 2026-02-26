# Pontbren Database Catalogue

## Aim
- Describes the Pontbren Database to support discovery, reuse, and governance of datasets.
- Ensures datasets meet standards, are stored and shared appropriately, and kept up to date for use by others.
- Designed for organisations/networks with large numbers of datasets, emphasising data governance and usability for data creators and users.

## Data structure and governance
- Data organized into directories with folder descriptions; quality assurance (QA) codes recorded for data points; QA details stored in Appendices.
- Most data provided as .txt files, typically in six-month blocks; file names indicate collection dates.
- A database framework illustrates folders/subfolders for data holdings.
- Appendices provide supplementary information to aid users (QA system; borehole logs; neutron probe logs; field diaries; streamflow calibration; etc.).

## Data categories (high level)
- AWS (Automatic Weather Station)
- Bowl study site runoff and soil water tension data
- Groundwater (boreholes)
- Hillslope study site runoff and soil water tension data
- Llyn Hir study site soil water tension data
- Land use manipulation plots
- Neutron probe soil moisture data
- Rain gauge data
- Field diaries
- Streamflow data

## Data categories and instrumentation (key points)

- AWS
  - Sensors sampled every minute; outputs include daily and 10-minute averages; includes daily max/min, daily mean, wind speed/direction, soil temperature, humidity, air temperature, net radiation.
  - In 2009, new columns added to improve RH and temperature sensing.

- Bowl study site (runoff and soil water tension)
  - Runoff data from weir boxes and tipping buckets; tensiometers at depths 10, 30, 50 cm.
  - Weir box flows reported in litres/second; some periods affected by evaporation or non-operation.
  - Tensiometer data per array with reconfiguration noted.

- Groundwater (boreholes)
  - Five boreholes monitored with Diver pressure transducers; barometric pressure corrections applied.
  - Data presented as water height relative to soil surface plus temperature; sampling cadence changed over time.

- Hillslope study site
  - Includes hillslope runoff weirs (drain/overland flow), tensiometers, and tree shelterbelt overland flow data.
  - Some data gaps due to rodent damage; QA codes reflect data quality concerns.
  - Tensiometer arrays at multiple depths; installations/removals/reconfigurations occurred.

- Llyn Hir study site
  - Tensiometers at multiple depths; sampling interval changed from 10 to 15 minutes in Sept 2009.

- Land use manipulation plots
  - Four plots with three replicates each; treatments: Grazed, Ungrazed, Trees (restoration/afforestation).
  - Replicates include tensiometers (10, 30, 50 cm) and overland flow measurements (mm/h).
  - Detailed documentation of plot locations and treatment mapping; plot 4 includes additional site data.

- Neutron probe soil moisture
  - Spatially distributed across bowls, hillslope, plots, tree areas, and Llyn Hir.
  - Profile measurements typically every 10 cm to depths up to 120 cm.
  - Provided with calibration approach and site-specific parameters.

- Rain gauge data
  - Data from multiple gauges (tipping bucket and storage gauges where available).
  - Units: tipping bucket in mm/day; storage gauges in mm.
  - Site locations correspond to figures and field sites.

- Field diaries
  - Word documents detailing field notes for locations/instrumentation; useful for explaining data issues.

- Streamflow
  - Starflow bed-mounted acoustic Doppler at Sites 1–9 and 13; Site 10–12 use a mix of pressure transducers and v-notch weirs.
  - Starflow data logged every minute; calibrated against manual spot measurements via site-specific linear calibration (y = αx + β).
  - Calibration excludes very low-flow events (<50 mm water depth) for reliability.

## Quality assurance and metadata

- Appendices A–C cover data governance and QA detail:
  - Appendix A: QA coding system
    - Codes describe data quality categories (Good, questionable, calibration issues, threshold breaches, logger failures, etc.) and instrument-specific issues (tensiometers, rain gauges, tipping buckets, AWS sensors, Starflow, etc.).
    - Provides guidance on potential problems (rodent damage, calibration issues, sensor faults, power or logging problems).
  - Appendix B: Borehole logs
    - Detailed equipment/methods, borehole logs, groundwater tests, and logs from multiple boreholes (depths, soil descriptions, completions).
  - Appendix C: Neutron probe access tube logs
    - Logs for neutron probe tubes with location and access details.
- Data points carry QA codes; field notes document issues and ongoing data quality considerations.
- Some data are not suitable for calibration or site-wide analyses due to gaps, patchy collection, or equipment issues (e.g., rodent damage, sensor failures).

## Calibration and site-specific parameters

- Starflow streamflow calibration
  - Site-specific calibration: y = αx + β, where y is calibrated flow (L/s) and x is Starflow estimate (L/s).
  - Parameters α and β (with associated standard deviations) are provided per site (Sites 1–13); low-flow data excluded from calibration.

## Practical implications for Data Stewards

- Data governance and usability
  - Clear folder structure and descriptive content support discoverability and interoperability.
  - Standardised metadata and QA enable reproducibility and informed data reuse.
  - Embargo/stewardship considerations embedded via QA codes and field diaries.

- Metadata and documentation
  - Appendices provide essential metadata for boreholes, neutron probes, QA codes, and field methods.
  - Site-specific instrumentation layouts (figures) and treatment details for manipulation plots provide context for analyses.

- Data maintenance and updates
  - Catalogue emphasises ongoing data availability, updates, and acknowledgement of data limitations (e.g., incomplete user needs, data transfer challenges, multi-system interoperability, and bespoke solutions due to legacy databases).