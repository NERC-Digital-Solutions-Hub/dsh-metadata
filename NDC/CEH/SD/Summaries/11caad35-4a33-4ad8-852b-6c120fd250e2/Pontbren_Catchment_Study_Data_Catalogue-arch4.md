# Pontbren Database Catalogue

- Purpose and scope
  - Describes the Pontbren Database: instrumentation, data organization, quality assurance, access, and reuse.
  - Emphasizes directory-based data organization with site-specific metadata, QA codes, and descriptions to support discoverability and cross-site collaboration.
- Core governance approach for data leaders
  - Systems view of the data landscape: instrumentation, collection methods, data flows, QA, and metadata.
  - Standardized file naming, folder descriptions, and QA codes to communicate data suitability and limitations.
  - Clear data assets and structure: datasets organized by site and function, with appendices providing context for quality and methodology.
  - Emphasis on discoverability, metadata interoperability, and ongoing user-aligned product iteration.

## Key features for Data Leaders

- Systems view and governance
  - Holistic perspective on data system, including QA codes and contextual appendices.
  - Mechanisms to communicate data suitability and caveats for reuse.
- Data assets and structure
  - Directory-based storage, often partitioned into six-month blocks, grouped by instrument type and site (e.g., AWS, groundwater, hillslope, Llyn Hir, manipulation plots, neutron probe, rain gauges, field diaries, streamflow).
  - Appendices provide supplementary context (QA coding, borehole logs, neutron probe logs).
- Data quality and metadata
  - QA coding (Appendix A) documenting data quality issues, sensor problems, calibration status, and anomalies.
  - Site-specific calibration notes (e.g., streamflow site-station adjustments) and AWS data headings.
  - Metadata elements include sensor types, sampling intervals, units, locations, and instrument configurations.
- Data accessibility and reuse
  - Descriptions of data files with headings, units, and data block structures (e.g., 1-minute AWS readings, 10-minute averages, daily summaries).
  - Explicit caveats and limitations (gaps, instrument changes, calibration caveats, and field conditions) to aid interpretation.
  - Field diaries and appendices provide contextual information to support reuse.

## Dataset components and their significance

- AWS (Automatic Weather Station)
  - Location: bowl within instrumented hillslope.
  - Temporal resolution: 1-minute samples with daily and 10-minute averages; updated sensor columns post-2009.
  - Typical headings: incident radiation, wind, soil/air temperatures, humidity, net radiation.
- Bowl study site data (runoff and soil water tension)
  - Runoff from weir boxes and tipping buckets; flow in litres/second.
  - Tensiometer measurements at multiple depths; array and logger configurations described.
- Groundwater
  - Five boreholes with water height relative to soil surface and groundwater temperature; barometric pressure compensation.
  - Borehole and site logs provided in appendices.
- Hillslope study site, Llyn Hir, and tree shelterbelt data
  - Runoff, drain flow, overland flow data; tensiometer arrays; neutron probe moisture data across multiple plots and locations.
- Land use manipulation plots
  - Four plots with three replicates each; treatments (Grazed, Ungrazed, Trees) assigned; tensiometer and overland flow data collected.
- Rain gauge data
  - Tipping bucket and storage gauges across multiple sites; data reported as mm/day or mm.
- Neutron probe and borehole logs
  - Detailed logs describing soil profiles, moisture measurements, borehole construction, and calibration notes.
- Field diaries and streamflow
  - Field notes documenting data collection issues.
  - Streamflow data from Starflow systems with site-specific calibration to estimate flow.
- Borehole logs (example content from text)
  - Location details, grid references, datum levels, lithology (soils, clays, gravels), depths, completion tubes, and sampling intervals.
- Streamflow gauging and metered data
  - Time-stamped flow metered estimates across numerous sites, with start/finish times and flow values (ls-1 or equivalent).

## Data governance and usage guidance for Data Leaders

- Data discovery and stewardship
  - Use folder structure, site labels, instrument types, and measurement periods to locate data.
  - Refer to QA codes (Appendix A) to assess reliability and caveats prior to analysis.
- Data quality and calibration
  - Apply calibration relationships (e.g., streamflow calibrations, AWS metadata) to interpret measurements.
  - Account for known data gaps, sensor changes, and field conditions described in diaries and QA notes.
- Metadata and interoperability
  - Maintain site-specific metadata: locations, depths, units, sampling intervals for cross-site analyses.
  - Use borehole and neutron probe appendices to ensure consistent interpretation.
- Collaboration and reuse
  - Catalogue supports cross-network data use with standardized structure, descriptions, and QA codes.
  - Facilitates partnerships and data-sharing across networks and communities of practice.
- Gaps and challenges
  - Data are scattered, with potential protection barriers and inconsistent standards.
  - QA codes and documentation mitigate gaps; ongoing need for sector coordination to improve standards and reduce duplication.

## Endnotes and supplementary context

- Emphasis on accessibility through well-described folders, contents, and file naming.
- Appendices provide essential context for data quality, borehole structure, and neutron probe methods.
- Overall aim: robust data management, transparent quality assessment, and collaborative data use across the Pontbren study network.