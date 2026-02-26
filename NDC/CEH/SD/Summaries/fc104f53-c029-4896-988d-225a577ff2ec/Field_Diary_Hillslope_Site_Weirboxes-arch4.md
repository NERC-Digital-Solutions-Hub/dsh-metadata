# This file is for the weir boxes that are measuring drain and overland flow in the bowl.

## Overview
- Logs for two weir boxes measuring drain (DRAIN) and overland flow (OLF) in the bowl.
- Installed on 01/11/2006; data collection spans through 2008.
- Includes measurements, site adjustments, equipment issues, and data download notes.

## Equipment and measurements
- DRAIN flow weir box positioned ~23.33 mm above the v-notch.
- OLF weir box positioned ~106 mm below the v-notch.
- V-notch measurements:
  - DRAIN: average V length 212.5 mm; CV 2.99%.
  - OLF: average V length 211 mm; CV 1.3%.
  - Water depth measured at the edge to avoid drawdown effects; example: average depth 112 mm; water depth above V-notch 37.3 mm (DRAIN ~111 mm).
- Internal area measurements (to determine flow capacity):
  - DRAIN: ~75.2 cm × 69.2 cm → ~0.5204 m².
  - OLF: ~74.5 cm × 69.1 cm and 75.1 cm × 69.2 cm → AV ~0.5172 m².
- Noted measurement caveats:
  - 9 mm difference in V-notch length on DRAIN sides indicating V notch not perfectly vertical.
  - Evaporation and other factors can affect measured water levels.

## Timeline of key events and maintenance
- 08/11/2006: Download; OLF leak observed.
- 14/11/2006: OLF weir box stilling removed to investigate leak.
- 22/11/2006: OLF weir box pressure transducer reinstalled.
- 23/11/2006: Leak attributed to OLF weir box; box removed and dried for repair.
- 27/11/2006: Data downlink indicated drain flow issue (wire had come loose); repaired.
- 03/01/2007: OLF weir box essentially at 0 mm above V-height during download.
- 08/03/2007: Plastic guiding material extended to near end of trench; noted crumbly soil; extension incomplete.
- 29/03/2007: Data download issue due to logger/battery handling.
- 03/04/2007–04/05/2007: Further extension and pegging of guiding material; soil crumbly but secured.
- 07/06/2007: Weir box dimensions measured to confirm internal area.
- 30/08/2007: Drain not flowing.
- 17/09/2007: OLF near V-notch crest; minor blockage causing small water dam.
- 12/12/2007: Sediment accumulation in OLF gutter; down pipe cleared.
- 23/01/2008: Data appears lower than observed; puddle in cabinet housing logger dried; cabinet appeared dry.
- 30/01/2008: Blockage in OLF down pipe cleared.
- 13/03/2008: Data gap between 03/03/2008 and 13/03/2008; downloaded file shows duplicate data.
- 15/08/2008: Data drop noted after last download on 30/07/2008.

## Data quality, gaps, and anomalies
- Leaks and structural issues:
  - OLF leak observed and investigated; leak likely around the stilling box attachment.
  - Repeated maintenance to prevent leaks and ensure stable readings.
- Measurement integrity concerns:
  - V-notch misalignment (9 mm difference) suggests potential bias in flow estimation.
  - Evaporation causing water level decline in OLF box; evaporation corrections may be needed.
- Blockages and sediment:
  - Blockage in OLF down pipe (cleared 30/01/2008); occasional sediment buildup in OLF gutter (12/12/2007).
- Data continuity and reliability:
  - Multiple logger-related interruptions (battery changes, mis-handling) leading to data gaps and potential duplicates (03/03–13/03/2008).
  - 30/08/2007: drain not flowing; 17/09/2007: minor blockage; 23/01/2008: low data relative to observed flows.
- Observational inconsistencies:
  - Observed overland flow at the bowl appeared higher than what the hill slope drain weirs recorded; possible blockage or measurement bias contributing to discrepancy.

## Data management implications for Data Leaders
- Data provenance and metadata needs:
  - Clear documentation of V-notch geometry, depths, measurement edge methods, and sensor placements.
  - Recording of internal area calculations and units for reproducibility.
- Quality assurance requirements:
  - Routine checks for leaks, blockages, and alignment of V-notches.
  - Procedures to handle evaporation effects and to distinguish true flow from instrumental drift.
  - Regular verification of logger health, battery handling procedures, and data integrity to minimize gaps.
- Data completeness and governance:
  - Track data gaps (e.g., 03/03–13/03/2008) and data anomalies (duplicate downloads) for transparent analyses.
  - Maintain logs of maintenance events (repairs, cleaning, adjustments) to contextualize data quality.
- Operational considerations:
  - Implement preventive maintenance schedules and automated alerts for leaks or sensor faults.
  - Consider redundancy or cross-validation with observed field measurements to reconcile discrepancies between observed flows and recorded data.

## End status and implications
- The dataset spans late 2006 to mid-2008 with multiple maintenance interventions, several data gaps, and some sensor-related anomalies.
- For data-driven decision-making, treat readings with caution given leak issues, potential V-notch misalignment, blockages, and data discontinuities.
- Robust metadata, ongoing quality checks, and documented maintenance actions are essential to improve reliability and usability of the data moving forward.