# SUPPORTING DOCUMENTATION:

## Overview
- Document communicates the data collection, structure, quality control, and analytical methods for a cricket behavior study.
- Encourages collaboration and offers additional information/expertise; contact Tom Tregenza before using the data.

## Data collection and scope
- Behavior of male crickets monitored via 140 infrared day/night cameras around burrows, recording continuously (24/7).
- Field period: 2019; study conducted in Asturias, North Spain.
- Weather data collected via a central weather station and six surface sensors (temperature measurements integrated into observations).

## Data types and units
- Target behaviors quantified as time spent in minutes within observation periods; temperature (ºC) included as a covariate.
- Data files (three datasets):
  - 2019_MaleBehaviour: per-event observations with fields including Tag, Pop, Burrow, Behav, Date, Duration, Temp, etc.
  - 2019_Populations: population identifiers, locality name, altitude, coordinates.
  - 2019_Specimens: individual metadata (Population, Tag, Sex, Mass, Released).

## Quality control and data provenance
- Quality control checks on video data using Access queries to detect inconsistencies (e.g., same cricket recorded as using two burrows simultaneously).
- Data processing and validation performed to ensure accurate event timing and behavior recording.

## Data structure details
- 2019_MaleBehaviour: records per observed behavior event; key fields include:
  - Tag (unique two-character ID)
  - Pop (high altitude 'H' or low altitude 'L')
  - Burrow (location of observation)
  - Behav (Outside, Feeding, Calling, Fleeing, Inside, SunAvailable, InSun)
  - Date and Time of onset
  - Duration (minutes)
  - Temp (mean ground-level temperature during behavior)
- 2019_Populations: links individuals to populations with locality, altitude, and coordinates.
- 2019_Specimens: subject metadata (Sex, Mass, Released date).

## Experimental design and field instrumentation
- Ballpark: 132 male crickets from 10 locations (5 under 160 m a.s.l.; 5 over 1,200 m a.s.l.); 127 adult females from three meadows within 5 km.
- Males and females reared separately before release; crickets marked with unique two-character IDs.
- Artificial burrows established; one cricket per burrow; burrows caged briefly post-release.
- 140 IR cameras deployed over burrows; direct night-time/diurnal observations supplement camera coverage.
- Cameras and burrows monitored across the breeding season with direct observations for non-videoed burrows.

## Field work and laboratory instrumentation
- Cameras: Vivotek IP8330, connected to five computers with motion-activated recording software (i-Catcher).
- Weather: Davis Vantage Pro2 station with additional ground sensors (six total) at various meadow locations and simulated burrows.

## Calibration steps and values
- Weather station data factory-calibrated; no additional equipment calibration required beyond standard computer timekeeping.

## Analytical methods
- Data extraction in two steps per day:
  - First pass: broad screening to separate active burrows from empty ones (multi-camera view management to minimize bias).
  - Second pass: detailed per-camera analysis, back-and-forth playback to identify event onsets, then forward playback at workable speed to record events.
- Data recorded to MS Excel and imported into MS Access for processing.
- Observers assigned to nine groups to reduce inter-observer differences and artifact between altitudes.

## Governance and collaboration
- Researchers open to collaboration; a potential collaborator should contact Tom Tregenza before using the data.
- Additional information and expertise may be available to assist with analyses and interpretation.

## References
- Rodríguez-Muñoz, R., et al. (2010). "Natural and sexual selection in a wild insect population." Science 328: 1269-1272.