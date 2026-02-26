# Details of data structure

## Overview
- Dataset consists of six CSV files related to sampling, isolation, and detection of Bacteroides markers.
- Emphasizes geospatial data suitable for map-based visualization: several files include explicit latitude, longitude, and altitude.
- Intended to support GIS-enabled analysis of sample collection sites, lab processing steps, and marker detections.

## File-by-file summaries
- LocationOfFaecalSampling.csv
  - Provides sampling locations and context for human/faecal samples.
  - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude; Longitude; Altitude.

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Initial steps in isolating Bacteroides markers for the week starting 10 June 2018.
  - Columns include: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; CFU counts for positive/negative esculin reactions (anaerobic and aerobic).

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Final steps in isolation for the week starting 10 June 2018.
  - Columns include: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; CFU data by esculin reaction and environment; Gram staining; Status; Code and origin of Bacteroides hosts.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Initial steps in isolating Bacteroides markers for the week starting 17 June 2018.
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; CFU counts (esi) for anaerobic/aerobic conditions.

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Final steps in isolation for the week starting 17 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; CFU counts by esculin reaction (anaerobic/aerobic); Gram staining; Status; Code and origin of Bacteroides hosts.

- DetectionOfFIB&MSTmarkers.csv
  - Detection levels of fecal indicator bacteria and related markers in drinking water and WWTP effluent.
  - Columns: Date of water sampling; Water source name; Intestinal enterococci; Total coliforms; Escherichia coli; Somatic coliphages; Phages for GB124; Phages for various potential human Bacteroides spp. codes; Each code (LU.2, TIB.1, etc.) represents phages detected in specific isolates.
  - Note: Codes in this file combine location-name initials and isolate numbers (e.g., LU.2 = Luawk primary school pit latrine, isolate 2; SIN.19 = Sinogo water pan shoreline, isolate 19).

## Linkages and data integration
- Cross-file matchings to form a cohesive dataset:
  - IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; entries should be matched by Location name from faecal sample collection (Column A), though ordering and entry counts differ.
  - IsolationBacteroidesHostsWeek17-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek17-6-18StepA; match via Location name from faecal sample collection.
- These linkages enable stitching together sampling locations, initial and final isolation steps, and later detection results for GIS-enabled timelines or multi-layer maps.

## Geospatial and data quality considerations for GIS
- Spatial attributes:
  - LocationOfFaecalSampling provides precise coordinates (latitude, longitude) and altitude for mapping sample sites.
- Data quality considerations:
  - Potential inconsistencies in location naming across StepA/StepB files; different orders and entry counts.
  - Multiple datasets require careful cleaning and standardization (e.g., date formats, unit consistency, categorical codes).
  - Integration relies on a shared key: Location name from faecal sample collection.
- Data processing implications:
  - Prepare layered GIS products: points for sampling sites, lineages or workflows for isolation steps, and point/area markers for detection results.
  - Consider time-enabled mapping to reflect weekly sampling windows (10-6-2018 and 17-6-2018).

## GIS visualization and analysis opportunities
- Visualize sampling locations and sampling dates on a map to identify geographic patterns.
- Show progression from Step A to Step B for each week to illustrate laboratory workflows spatially.
- Map detection markers (FIB and MST markers) alongside water sources and WWTP effluents to assess correlations or contamination hotspots.
- Use the codes in the detection file to link phage presence to specific isolates and locations for traceability.

## Data management notes and recommendations
- When preparing GIS products, create consistent attribute schemas across files and establish a robust join key (Location name from faecal sample collection).
- Validate and reconcile mismatches between StepA and StepB files before integration.
- Maintain documentation of code origins (e.g., LU.2, SIN.19) to support interpretation and reproducibility.
- Given the stated challenges, implement data cleaning, standardization, and modular, map-friendly layers to facilitate end-user exploration.