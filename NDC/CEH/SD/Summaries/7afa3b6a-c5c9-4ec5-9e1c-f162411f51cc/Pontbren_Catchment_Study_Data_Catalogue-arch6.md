# Introduction to the DATABASE Catalogue

## Overview
- Describes the Pontbren Database, its instrumentation, data organization, and metadata.
- Data are stored in directories with quality assurance (QA) codes; QA details are provided in appendices.
- Most data are in .txt files, typically organized in 6-month blocks; filenames indicate collection dates.
- Appendices offer supplementary information useful to database users.

## Database framework and content
- Data categories and sites include:
  - Automatic Weather Station (AWS) data from the bowl site with minute-level sampling; daily and 10-minute averages; post-2009 sensor adjustments.
  - Bowl study site: runoff and soil water tension datasets (weirs, tipping buckets, tensiometers at multiple depths).
  - Groundwater: borehole data with Diver/barometric compensation; height and temperature; interval changes over time.
  - Hillslope study site runoff and soil water tension data.
  - Llyn Hir study site soil water tension data.
  - Land-use manipulation plots: Grazed, Ungrazed, Trees; tensiometers and overland flow measurements.
  - Neutron probe soil moisture data across multiple sites with depth resolution; calibration details and site notes.
  - Rain gauge data across sites (tipping bucket and storage gauges).
  - Streamflow data from several sites with Starflow and other calibration methods; site-specific calibrations included.
  - Field Diaries (word docs) containing field notes and data-issue references.
  - Appendices (QA codes, borehole logs, neutron probe logs).
- Cross-site, multi-method framework supports comprehensive environmental data (hydrology, soil moisture, groundwater, land-use impacts) with attention to data provenance and context.

## Data collection, formats, and usage notes
- Sampling and formats:
  - AWS: 1-minute sensor data; daily and 10-minute averages; some additional columns after 2009.
  - Runoff/tensiometer data: various logging intervals; units include litres/second (flow) and cm H2O (tensiometers).
  - Groundwater: height (cm), temperature; corrections applied.
  - Rain gauges: tipping bucket (mm/day) and storage gauges (mm).
  - Streamflow: metered spot measurements calibrated against manual readings; site-specific linear calibrations (y = αx + β).
- Quality considerations:
  - Evaporation effects in weir boxes; QA codes annotate data quality issues.
  - Known issues in some plots (rodent damage, equipment issues) noted in QA; field diaries provide data-context.
- Documentation and metadata:
  - Folders include descriptive notes, instrument locations, and figures.
  - Tables for Tables/Figures; appendices provide QA codes and borehole/probe logs.
- Outputs and usability:
  - Catalogue explains organization, naming, and outputs (dashboards, self-serve analyses, reports).
  - QA codes help assess data suitability for calibration and modelling.
  - Guidance on folder content descriptions and the importance of field diaries for understanding data issues.

## Quality assurance and documentation
- QA codes defined in Appendix A (e.g., good quality, problems, calibration issues, logger or instrument faults).
- Appendices B–C provide borehole and neutron probe logs with location, depth, soil description, and installation details.
- Quality notes accompany many data files, especially where data quality is uncertain (e.g., tree shelterbelt, some hillslope data).

## Access, usage, and outputs
- The catalogue provides guidance on data discovery, QA assessment, and building self-serve data products across topics (hydrology, soil moisture, groundwater, land-use impacts).
- Emphasizes transparency through detailed logs, calibration parameters, and QA annotations to aid reliability assessments and reproducibility.
- Describes folder structure, naming conventions, and outputs available (dashboards, self-serve analyses, reports).

## Relevance to Data Support archetype
- Provides a comprehensive, navigable framework to locate and interpret multi-disciplinary environmental data.
- Supports data discovery, quality assessment, and creation of data products for a broad audience.
- Enables cross-site comparisons and calibration through site-specific parameters and QA metadata.
- Promotes reproducibility and transparency via detailed instrument logs, calibration parameters, and QA annotations.

## Equipment & Methods highlights (examples from the dataset)
- Borehole logging uses hand augers, AQ drill rods, guide tubes, pneumatic hammer, and rotary drills; logging performed by a contractor (e.g., Groundwater Monitoring and Drilling Ltd).
- Example borehole datasets (NP20–NP23) include:
  - Site locations (e.g., PEN-TAL-Y-CEIN LLANFAIR CAEREINION; COED CWM-Y-LLWYNOG)
  - N-probes and manipulation plots (sites 3.1–3.3, S3)
  - Grid references (e.g., SJ 07360 06833; SJ 07426 06920)
  - Soil descriptions (various silty/clay soils with mottling) and depths
  - Completion details (16 gauge aluminium access tubing)
  - Sampling depths and dates (e.g., Date 14/05/06; samples 0.80–1.60 m)
- Documentation entries reflect field procedures, sediment descriptions, and multi-depth sampling across several boreholes and monitoring probes.