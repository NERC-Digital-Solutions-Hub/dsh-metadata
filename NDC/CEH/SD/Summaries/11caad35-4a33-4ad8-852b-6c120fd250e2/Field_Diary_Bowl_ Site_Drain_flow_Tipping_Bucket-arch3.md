# Drain flow data log and weir box/tipping bucket calibration notes (2005-2009)

## Overview
- Document chronicles a drain-flow monitoring setup using a tipping bucket (TB) system, a weir box, transducer, and TinyTag data logger, spanning 2005–2009.
- Monitoring interval was reset from 10-minute to 5-minute intervals to align with the overland flow trap and various calibration activities.
- The dataset relies on multiple hardware components (TBs, weir boxes, magnets, batteries, seals) and requires careful QA to ensure data integrity.

## Monitoring setup and data collection
- Key components:
  - Tipping bucket system for flow measurement
  - Weir box for drain flow measurement
  - Transducer and TinyTag logger; occasional battery/desiccant changes and seal maintenance
  - Magnets and mechanical mounting (notably TB magnet issues identified)
- Data handling practices:
  - Calibration events and maintenance logs are embedded in the time series records
  - Time stamps sometimes required alignment across GMT/BST; several instances of timestamp adjustments
  - Periods of calibration or maintenance are flagged to be ignored in analysis or treated separately

## Calibration events and data quality actions
- 07/06/2007: Calibration performed with ~30 L through the TB, yielding 10 tips; established tip volume as 2.91 L per tip (subsequent observations noted drift)
- 15/08/2007: Magnet reattached to TB; recalibration confirmed; inappropriate tips during 2:30–3:30 BST were to be ignored
- 30/04/2007 and 21/08/2006: Battery/desiccant/seal and weir box maintenance; TB restarted and connection issues resolved
- 14/11/2008 and 17/11/2008: Calibration adjustments introduced
  - 17/11/2008: Applied linear incremental adjustment to tip volume to reconcile differences between 07/06/2007 and 14/11/2008 calibrations
  - 30.66 L recorded as 11 tips (2.79 L per tip) after recalibration
- Regular maintenance and issues:
  - TB/bucket dislodgement (e.g., 08/11/2006) and calibration reinstallation
  - Leaks and seal issues (e.g., 06/12/2006)
  - Weir box and PT checks, sediment clearing, and water diversion during calibrations (e.g., 22/04/2009, 29/04/2009)
  - System freezes affecting data (e.g., 01/01/2009)
  - Periods of non-flow or non-collection identified (e.g., 30/08/2007; 25/02/2009)

## Data handling, metadata, and governance
- Data quality assurance is intertwined with calibration logs; calibration periods are explicitly annotated and sometimes excluded from analysis.
- Time alignment is essential due to DST changes (GMT/BST), requiring corrections in the analysed data files.
- Documentation of data provenance is present through detailed event notes (calibrations, repairs, and anomalies), highlighting the need for robust metadata to support data reuse and auditing.
- Public sharing of underlying data is a potential barrier noted in broader monitoring governance contexts; keeping transparent, well-documented data and calibration records helps mitigate governance challenges.

## Challenges and implications for monitoring frameworks
- Data gaps and access:
  - Periods with missing or unreliable data due to TB calibration, maintenance, or hardware failures
- Metadata and data provenance:
  - Incomplete or scattered metadata requires explicit calibration and maintenance logs to interpret data accurately
- Data transformation and standardization:
  - Variability in tip volume over time necessitated recalibration and possible application of time-varying correction factors
- Communication of complex findings:
  - Calibration events and data exclusions must be clearly represented in dashboards/reports to avoid misinterpretation
- Data governance needs:
  - Clear protocols for sharing datasets, including documenting calibration periods and data exclusions, to enable transparency and reuse

## Key takeaways for authors of monitoring frameworks
- Embed calibration and maintenance records within the primary dataset and as shared metadata to preserve data quality context.
- Implement time synchronization and DST handling as a standard data processing step; explicitly annotate time-related corrections.
- Treat instrument-specific changes (e.g., TB tip volume, magnet position) as data correction factors that should be versioned and justified in the data lineage.
- Establish clear data exclusion rules for calibration periods and provide理由 (reasons) and timestamps for those exclusions.
- Promote openness of underlying data while balancing practical constraints; ensure that data governance processes are in place to support data sharing and reuse.
- Maintain additive QA procedures that include routine hardware checks, calibration verifications, and transparent logging of anomalies (e.g., leaks, bucket misalignment, clogs, or frosting effects).
- Design dashboards and reports to distinguish raw measurements from post-calibration, corrected values, and to flag any data flagged as unreliable due to maintenance events.