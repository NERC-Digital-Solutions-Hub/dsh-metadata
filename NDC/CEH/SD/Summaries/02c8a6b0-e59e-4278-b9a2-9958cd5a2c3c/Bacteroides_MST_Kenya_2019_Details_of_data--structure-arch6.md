# Details of data structure

- This dataset comprises six CSV files that document sampling, isolation, and detection processes related to Bacteroides spp. markers, with a focus on two sampling weeks in June 2018 and associated fecal and water samples.
- Files cover: locations of faecal sampling, initial and final steps of isolation of Bacteroides hosts, and detection of fecal indicator bacteria and bacteriophages in water sources and wastewater effluents.
- Codes for isolates are derived from sampling location initials plus an isolate number (e.g., LU.2, SIN.19, KN.1).

## File descriptions

- LocationOfFaecalSampling.csv
  - Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude; Longitude; Altitude.

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- DetectionOfFIB&MSTmarkers.csv
  - Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/mL); Phages of Bacteroides fragilis GB124 (PFU/mL); Phages of potential human Bacteroides spp. markers (codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3) (PFU/mL); Phages of potential cattle Bacteroides spp. markers (codes KN.1, KN.2, KN.3, KN.8, SIN.19) (PFU/mL).

## Linkages between files

- IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; match entries by Location name from faecal sample collection (A column). Order and entry counts may differ.
- IsolationBacteroidesHostsWeek17-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek17-6-18StepA; match entries by Location name from faecal sample collection (A column). Order and entry counts may differ.

## Data integration considerations

- Primary linkage key: Location name from faecal sample collection (as used across StepA/StepB files).
- Expect potential formatting inconsistencies across files; careful matching is required when merging.
- The detection data includes multiple marker types with distinct codes for human and cattle Bacteroides markers, enabling cross-reference to isolates from the sampling weeks.

## Practical data use for the Data Support archetype

- Generate geospatial dashboards mapping sampling locations (lat/long) and associated CFU counts for fecal indicators and phages.
- Create end-user self-serve reports showing isolation progress from StepA to StepB by location.
- Link water quality markers (FIB/MST) with Bacteroides isolates to explore associations between environmental markers and isolates.
- Build reference tables for the isolate codes (LU.2, SIN.19, KN.x) to trace origins and sample context across datasets.

## Data quality and integration notes

- Be mindful of potential mismatches in file order and entry counts between StepA and StepB files; rely on the location-based matching column for integration.
- Cross-file consistency is essential when creating dashboards or reports that combine isolation results with sampling locations and environmental markers.