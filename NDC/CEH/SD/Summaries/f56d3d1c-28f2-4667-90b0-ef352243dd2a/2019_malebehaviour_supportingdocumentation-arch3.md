# SUPPORTING DOCUMENTATION:

- Purpose and scope
  - Document outlining how data on male cricket behavior around burrows was collected, processed, and managed.
  - Aims to enable collaboration and reuse of the data; notes a point of contact (Tom Tregenza) before working with the data.

- Collection methods
  - Behaviour monitored via 140 infrared cameras around burrows, recording 24/7.
  - Videos used to extract behavioural data; temperature included as a covariate.

- Nature and units of recorded values
  - Target behaviours quantified as time spent (minutes) during observation.
  - Temperature recorded (ºC) and used as a covariate.

- Quality control
  - Video data checked for consistency using Access queries to detect errors (e.g., same cricket recorded at two burrows simultaneously).

- Data structure and content
  - Three data files:
    - 2019_MaleBehaviour: observations with fields such as Tag, Pop, Burrow, Behav (Outside, Feeding, Calling, Fleeing, Inside, SunAvailable, InSun), Date, Duration, Temp.
    - 2019_Populations: population metadata (origin altitude, locality, coordinates).
    - 2019_Specimens: individual specimen data (Population, Tag, Sex, Mass, Released).

- Experimental design
  - Males collected from 10 locations in Asturias; females collected from three meadows.
  - Crickets marked with two-character tags, released into randomly assigned artificial burrows; cages used to limit movement initially.
  - 140 cameras installed to monitor burrows; non-videoed burrows covered by direct observations.

- Field work and instrumentation
  - IR cameras (Vivotek IP8330) linked to five computers with motion-activated recording software.
  - Weather data collected via a Davis Vantage Pro2 station and six surface sensors placed around the meadow.

- Calibration and values
  - Time measured by computer clocks; weather station factory calibrated; no additional calibration steps for other equipment.

- Analytical methods
  - Two-stage video analysis:
    - First pass to identify burrows in use across a day (group of cameras monitored, then hidden as activity found).
    - Second pass: detailed review of identified periods, recording events into a spreadsheet, then importing into MS Access.
  - Observers were partitioned by altitude groups to minimize inter-observer differences.

- Data provenance and reuse
  - Data is described with supporting datasets and structured fields to enable replication and secondary analysis.
  - Collaboration encouraged; data creators offer additional information and expertise to potential analysts.

- References
  - Rodríguez-Muñoz, R., et al. (2010). "Natural and sexual selection in a wild insect population." Science 328:1269-1272.