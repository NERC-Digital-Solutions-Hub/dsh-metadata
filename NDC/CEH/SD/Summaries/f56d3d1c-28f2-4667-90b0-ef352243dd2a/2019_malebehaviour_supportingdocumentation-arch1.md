# SUPPORTING DOCUMENTATION:

## Overview
- Invitation to collaborate with researchers on these data; contact Tom Tregenza before working with the data.
- Indicates potential access to additional information and expertise to assist analysis.

## Data collection and target variables
- Behaviour of male crickets monitored via 140 infrared cameras around burrows, recording 24/7.
- Target behaviours quantified as time spent (minutes) during observation; temperature included as a covariate.

## Data files and structure
- Three data files:
  - 2019_MaleBehaviour: per-record observations with fields such as Tag, Pop, Burrow, Behav (Outside, Feeding, Calling, Fleeing, Inside), SunAvailable, InSun, Date, Duration, Temp.
  - 2019_Populations: population identifiers, locality name, altitude, coordinates.
  - 2019_Specimens: Population, Tag, Sex, Mass, Released.
- Data are organized to align individual crickets with their populations and observed behaviours over time.

## Experimental design
- Collection in Asturias (North Spain) during April 2019:
  - 132 male adults from 10 locations (5 below 160 m, 5 above 1200 m).
  - 127 adult females from three meadows within ~5 km of the study site.
- After collection, crickets reared in boxes; Males from different populations kept separate; females grouped in three boxes.
- On release (22–29 April), each cricket tagged with a two-character code and released into a randomly chosen artificial burrow.
- Burrows covered with cages for 2–4 days; cages removed, and 140 IR cameras installed over burrows.
- Direct observations conducted for burrows without cameras.
- Burrow identifiers tracked throughout the breeding season; observations supplemented by video.

## Field work and instrumentation
- IR cameras: Vivotek IP8330; connected to five computers with motion-activated recording software (i-Catcher).
- Weather data: Davis Vantage Pro2 weather station plus six temperature sensors (three on the meadow surface, three inside simulated burrows in PVC pipes) distributed across the meadow.
- Time-stamped recordings and weather data collected to support analyses.

## Calibration and data handling
- Weather station factory calibrated; no additional equipment calibration beyond standard timekeeping.
- Time was the primary measured variable; no other calibration requirements noted.

## Analytical methods
- Data extraction in two steps per day:
  - Step 1: Rough pass across 16 cameras simultaneously to identify burrow activity.
  - Step 2: Detailed viewing of each active period; playback to determine start times of events; events recorded in MS Excel, then imported into MS Access.
- To minimize bias, nine observers were organized into groups to standardize recording across altitudes.
  
## Collaboration and data accessibility
- Clear emphasis on collaboration; researchers welcome inquiries and offer to share additional information and expertise.
- Data and metadata management practices suggested to improve discoverability and usability of resulting datasets.

## Reference
- Rodriguez-Muñoz, R., et al. (2010). Natural and sexual selection in a wild insect population. Science 328:1269-1272.