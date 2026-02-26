# SUPPORTING DOCUMENTATION

- We welcome collaboration with anyone interested in these data and may provide additional information and expertise. Please contact Tom Tregenza before working with the data.

## Overview
- Documents the data collection, structure, and analysis workflow for a cricket behavioural study.
- Aims to enable researchers to understand behaviour relative to environmental factors and to promote data reuse.

## Data collection and instrumentation
- Behaviour of male crickets recorded with 140 infrared cameras around burrows, operating 24/7.
- Video footage analyzed to extract behavioural data.
- Field measurements include a central weather station with ten-minute interval logging and six surface temperature sensors (three outside, three inside simulated burrows).

## Nature and units of recorded values
- Target behaviours quantified as time spent (minutes) during observation.
- Temperature (ºC) recorded as a covariate.

## Quality control
- Video data checked for consistency using Access queries to detect errors (e.g., a cricket recorded as occupying two burrows simultaneously).

## Data structure (three data files)
- 2019_MaleBehaviour
  - Fields: Tag, Pop, Burrow, Behav, Date, Duration, Temp, plus identifiers for time and observation context.
  - Behaviours include Outside, Feeding, Calling, Fleeing, Inside, SunAvailable, InSun.
- 2019_Populations
  - Fields: Population (origin code; 'H' high altitude, 'L' low altitude), Locality name, Altitude, Coordinates.
- 2019_Specimens
  - Fields: Population, Tag, Sex (MA: male; FA: female), Mass (g), Released (date).

## Experimental design
- Spring 2019: 132 male crickets collected from 10 locations in Asturias (5 under 160 m, 5 over 1,200 m); 127 adult females from three meadows within 5 km.
- Males were reared separately by population; females kept together in fewer boxes.
- Crickets marked with unique two-character tags; artificial burrows established prior to release based on long-term burrow positions.
- One cricket released per burrow; cages initially placed to discourage movement, removed after 2–4 days.
- 140 IR cameras installed over burrows; video recording continued through the breeding season; non-videoed burrows monitored by direct observation every 1–2 days.

## Field work and instrumentation
- Cameras: Vivotek IP8330, connected to five computers with motion-activated recording software (i-Catcher).
- Weather station: Davis Vantage Pro2; additional ground sensors placed around the meadow.

## Calibration and measurement
- Time is the primary measured value, recorded via computer clock.
- Weather station is factory-calibrated; no other calibration steps beyond standard computer timing.

## Analytical workflow
- Data extraction occurs in two daily steps:
  - Step 1: Quick pass across 16 cameras simultaneously to identify active burrows for a given hour.
  - Step 2: Detailed per-camera review, starting from identified active periods, to record events in a spreadsheet.
- Data are imported into MS Access for processing.
- To ensure consistency across observers, videos from different groups of cameras were assigned to nine observers.

## Collaboration and access
- The authors express openness to collaboration and may provide additional information or expertise to assist analyses. Interested researchers should contact Tom Tregenza prior to data use.

## References
- Rodríguez-Muñoz, R., et al. (2010). Natural and sexual selection in a wild insect population. Science 328:1269-1272.