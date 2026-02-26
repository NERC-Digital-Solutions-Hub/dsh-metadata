# Introduction to the Database Catalogue

- Presents the Pontbren Database, detailing instrumentation, data structure, and quality assurance practices to support consistent environmental monitoring and scrutiny of health and policy performance over time.
- Aims to provide well-documented, standardised data outputs that enable long-term environmental assessment.

## Data structure and access

- Data organized into directories by data domain and site; quality assured (QA) data flagged with QA codes.
- Most data stored as plain text (.txt) files, typically split into 6-month blocks (January–June and July–December).
- File names indicate covered dates; folders describe content; appendices provide supplementary metadata (QA coding, borehole logs, neutron probe logs, gauge measurements, etc.).
- Includes a Table of Tables, a Table of Figures, and instrument-location figures to aid navigation.

## Data domains and content

- AWS (Automatic Weather Station): minute-scale sensors; outputs include daily and 10-minute averages; added sensors in 2009 with new temp/RH columns.
- Bowl study site runoff and soil water tension: includes weir/runoff measurements, tipping bucket data, and tensiometers at multiple depths; some data patchiness due to equipment.
- Groundwater (boreholes): five groundwater locations; water height relative to soil surface and temperature; barometer-compensated measurements; sampling intervals.
- Hillslope study site runoff and soil water tension: overland and drain flow, tensiometers, and plot-level data for upland management effects.
- Llyn Hir study site soil water tension: tensiometers at multiple depths; frequent sampling.
- Land use manipulation plots: Grazed, Ungrazed, Trees treatments with replicates; tensiometers and overland flow data per plot.
- Neutron probe soil moisture data: multiple sites with profiles to ~1 m; calibration equations provided; peat at some sites requires special handling.
- Rain gauge data: tipping bucket and storage gauges; site-specific placements described.
- Field diaries: site notes and data quality considerations.
- Streamflow: multiple sites with various gauging methods (Starflow acoustic Dopplers, transducers, v-notch weirs); high-frequency data with calibration equations.
- Tables and figures: data headings, treatment locations, calibration parameters, and instrument layouts.

## Quality assurance and calibration

- Appendix A documents a QA coding system for data quality and instrument faults (e.g., tensiometers, tipping buckets, rain gauges, Starflow, groundwater).
- Codes distinguish Good quality, questionable data, calibration issues, instrument faults, and site-specific problems.
- Calibration details include Starflow-based linear relationships (y = αx + β) with site-specific parameters; low-flow data (depth < 50 mm) excluded from calibration.
- Appendices B–D provide borehole logs and neutron probe logs to support quality interpretation and metadata.

## Appendices and metadata

- Appendix B: Borehole logs (groundwater monitoring and drilling details, equipment, sampling logs across sites).
- Appendix C: Neutron probe access tube logs (locations, depths, and logs).
- Appendix D: Neutron probe and site-specific documentation.
- Figures and tables present instrument locations, calibration parameters, and site layouts.

## Data usage and accessibility

- Data are produced to enable consistent environmental health monitoring and policy performance evaluation over time.
- Emphasises data provenance, QA, and the ability to link raw counts to calibrated outputs.
- Aims to enable others to access underlying data used to produce outputs, increasing dataset value through integration with other data sources.