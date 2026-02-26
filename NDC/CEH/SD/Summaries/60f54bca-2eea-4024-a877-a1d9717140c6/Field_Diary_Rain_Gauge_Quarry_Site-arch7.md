# Quarry Rain gauge

## Overview
- Rain gauges located at the Quarry at Tyn y Bryn Farm (originally RG2).
- 0.2 mm tipping bucket rain gauge positioned at ground level.
- Long operational log spanning 2005–2009 detailing floods, blockages, sensor faults, calibrations, and maintenance.

## Data Characteristics
- Primary measurement: rainfall via tipping bucket mechanism; data often referenced as tips and conversions to rainfall (e.g., 113 tips equivalent to 1 L).
- Adjacent storage gauge used for cross-checks and discrepancy detection.
- References to related data sources and notes (e.g., RG2.xls) indicating the existence of supplementary data files.

## Data Quality Issues and Anomalies
- Frequent flooding of the pit housing the gauge and water in the collection funnel, affecting measurements.
- Sensor components failing or requiring replacement (tiny tag failures, rusty or submerged connections, potential short circuits).
- Data inconsistencies between tipping bucket readings and the adjacent storage gauge (e.g., February 2006: storage gauge 92.5 mm vs tipping bucket 189.2 mm; questions about data quality).
- Timestamp and timing problems (logger data out by ~52 minutes in early 2007; needs reset).
- Blocked tipping bucket funnel and other blockages (soil blockage, leaf collector issues) leading to under/overestimation.
- Environmental conditions causing irregularities (snow in February 2007 affecting data; drainage concerns and flooding).
- Maintenance events sometimes aimed at correcting anomalous data (tests, draining, recalibration, cleaning).

## Maintenance, Calibration, and Procedures
- Regular cleaning and rebalancing of the tipping bucket system.
- Replacement of tiny tags and batteries; use of desiccants.
- Physical interventions to improve drainage (draining channels, draining the pit, spiking soil for drainage).
- Documentation of test procedures (e.g., applying 1 L and counting tips) to verify system response.
- Instances of repairing or replacing components (leaf collector gauze, rusty connections, drainage adjustments).

## Data Provenance and Metadata Considerations
- Data tied to a specific field instrument and location (RG2 at Quarry).
- Logs contain sequential maintenance and fault events with dates, observations, and corrective actions.
- Noted dependencies on supplementary data (RG2.xls) for details on questionable periods.
- Evidence of data quality concerns requiring explicit tagging in datasets (e.g., “data dodgy” for certain months).

## Implications for GIS Visualisations and Data Products
- Variable data quality over time necessitates quality flags and provenance metadata for each time period.
- Cross-validation with the adjacent storage gauge is important to identify reliable intervals.
- Potential biases from environmental conditions and maintenance events must be accounted for in maps and analyses.
- Gaps and anomalies may require data cleaning, imputation, or exclusion from certain GIS analyses.

## Recommendations for GIS Workflows
- Attach detailed QA/QC flags to rain gauge time series, including notes on known issues (flooding, blockages, timestamp drift).
- Maintain a metadata layer documenting maintenance events, sensor status, and data quality assessments.
- Integrate cross-checks with the storage gauge data to validate tipping bucket measurements.
- Develop protocols for handling periods labeled as dodgy or questionable (exclude or treat with uncertainty).
- Create visual indicators of data reliability (quality tiers) to accompany map-based rainfall displays.
- Archive and reference supplementary documents (e.g., RG2.xls) used for resolving data questions during analysis.