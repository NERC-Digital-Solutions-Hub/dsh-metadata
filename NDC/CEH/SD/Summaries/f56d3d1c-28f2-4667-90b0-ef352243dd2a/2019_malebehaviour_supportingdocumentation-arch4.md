# SUPPORTING DOCUMENTATION:

- Purpose and collaboration
  - Open invitation to collaborate with anyone interested in analyzing these data.
  - If planning to analyse, the authors can provide additional information and expertise.
  - Contact Tom Tregenza before working with the data.

- Collection methods
  - Behaviour of male crickets monitored via 140 infrared cameras around burrows, recording 24/7.
  - Videos manually reviewed to extract behavioural data.

- Nature and units of recorded values
  - Target behaviours quantified as time spent (minutes) during observation.
  - Temperature (ºC) recorded as a covariate.

- Quality control
  - Consistency checks performed on video data using Access queries to detect errors (e.g., a cricket recorded at two burrows simultaneously).

- Data structure (three data files)
  - 2019_MaleBehaviour
    - Fields include: Tag, Pop, Burrow, Behav, Date, Duration, Temp, and other observation details.
    - Observed behaviours: Outside, Feeding, Calling, Fleeing, Inside, plus SunAvailable and InSun indicators.
    - Data sorted by individual, burrow, and start time.
  - 2019_Populations
    - Contains population identity codes, locality names, altitude, and coordinates.
  - 2019_Specimens
    - Contains Population, Tag, Sex (MA/female FA), Mass at release, Release date.

- Experimental design
  - Female crickets collected from multiple sites; males from 10 locations (balanced altitudes).
  - Crickets reared in controlled boxes, marked with unique two-character IDs, released into artificial burrows in the meadow.
  - 140 IR cameras installed; burrows monitored continuously; non-videoed burrows periodically observed.
  - Field setup includes marking, burrow identification, and cage coverage to limit movement post-release.

- Field work and instrumentation
  - IR cameras: Vivotek IP8330; motion-activated recording via i-Catcher software.
  - Weather data collected with a Davis Vantage Pro2 station and six additional ground sensors (temperature sensors in meadow and simulated burrows).

- Calibration and measurements
  - Weather station factory-calibrated; time is the primary measured value; no other calibration steps beyond standard equipment.

- Analytical methods
  - Data extraction performed in two passes:
    - First pass: rough identification of burrow activity across 16 cameras for each hour.
    - Second pass: detailed per-camera analysis to determine start times of behaviours; events recorded to a spreadsheet, then imported into MS Access.
  - Videos assigned to nine observers to reduce inter-observer differences across altitudes.
  - Data management structured to facilitate subsequent processing and analysis.

- Data usage and governance
  - Emphasis on collaborative use and potential access to supplementary information.
  - Clear provenance and structured data lifecycle (collection, quality control, processing, and storage) to support reproducibility and reuse.

- References
  - Rodríguez-Muñoz, R., et al. (2010). "Natural and sexual selection in a wild insect population." Science 328:1269-1272.