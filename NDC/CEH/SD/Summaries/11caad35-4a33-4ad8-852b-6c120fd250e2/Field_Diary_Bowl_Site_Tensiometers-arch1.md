# The data in this folder is data downloaded from the Delta-t logger in the bowl study area.

- Scope of data
  - Data collected from Delta-t loggers in the bowl study area.
  - Tensiometers deployed at multiple depths (notably 10 cm, 30 cm, 50 cm) across several transect points.
  - Time period spans from at least 2004 to 2009, with numerous maintenance and operational entries within that window.
  - Regular notes on degassing, vent exposure, and data downloads accompany the measurements.

- Key events and maintenance
  - 15/03/04: Tensiometers degassed; initial deployment notes for T2.1, T2.3, T2.2, T2.4, T1.2, T1.4 with various depths.
  - 27/04/05 & 10/05/05: Vents exposed to the atmosphere on several tensiometers; subsequent updates on vent status.
  - 2004–2007: Frequent degassing, vent checks, grass cutting, and cage maintenance; sheep and mole activity repeatedly affect cages/tubes; several tensiometers damaged or reinstalled.
  - 16/04/07: Wiring changes to the delta-T logger to invert polarity so negative mV reads correspond to negative pore-water pressure values.
  - 2007–2008: Reinstallation and reconfiguration of tensiometers; routine degassing and vent checks; addressing data integrity and hardware issues.
  - 26/08/2008 – 16/10/2008: Recalibration and adjustment of installation geometry (tilt ~15°) and depths; introduced depth/angle-related offset handling.
  - 25/11/2008: Offset updated from -4.8 cm to 0 in the aftermath of installation geometry changes; offsets subsequently embedded in logger program.
  - 2009: Continued grass cutting and degassing; a non-responsive bottom tensiometer in July 2009 noted.

- Data quality issues and data gaps
  - 11–15 April 2006: Data missing due to logger auto-wrap during download; start of sampling period data lost.
  - 03/11/08: Top-cage data download problem leading to corrupted data; data not available.
  - Various instances of device or loggers going offline, battery issues, and communication problems (e.g., 16/06/2008 timing drift, 25/07/2008 battery/logging issues).

- Equipment and environmental challenges
  - Repeated vent burial or exposure due to earthworms, grass growth, and other disturbances; vents buried or partially covered requiring exposure and re-degassing.
  - Sheep, mole activity, and occasional wire/tube damage leading to reinstallation or replacement of tensiometers and tubing.
  - Delta-T logger issues: need for overwriting data, clock synchronization, and calibration updates; multiple notes about logger misreads, battery changes, and program adjustments.

- Data processing notes and offsets
  - 26/08/2008: Installation modified to angle 15°; an offset of -4.8 cm was initially applied to account for the porous cup depth vs. pressure transducer.
  - 25/11/2008: Offset changed to 0 cm to reflect updated installation geometry; offset handling incorporated into the logger program by subsequent downloads.
  - 02/09/2008: Acknowledgement that offsets need to be reflected in spreadsheets due to different installation geometry; subsequent 16/10/2008 update confirms offset consolidation.
  - 16/10/2008 and 24/10/2008: Replacements and calibration adjustments for bottom and other tensiometers; noted impact on data interpretation.

- Implications for analysis and provenance
  - Data quality is mixed with several gaps, corrupted downloads, and recurring equipment issues; thorough provenance and careful data cleaning are required.
  - Offsets due to installation geometry are critical for accurate interpretation of depth-related pore-water pressures and must be consistently applied.
  - Cross-referencing tensiometers across depths, transects, and timepoints is necessary to maintain coherence given reinstallation events and gear changes.
  - Environmental disturbances (grass cutting, animal activity) and vent management must be considered when aligning time-series with external covariates.