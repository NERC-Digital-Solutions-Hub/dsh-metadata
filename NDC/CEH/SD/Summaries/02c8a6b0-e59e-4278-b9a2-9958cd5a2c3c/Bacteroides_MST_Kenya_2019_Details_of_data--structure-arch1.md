# Details of data structure

- A six-file CSV dataset describing sampling locations, isolation of Bacteroides spp. markers, and detection of fecal indicator bacteria and related phages collected in 2018.
- Designed for analyses of spatial and temporal patterns in sampling, isolation outcomes, and environmental markers, with explicit field mappings and codes for cross-file integration.

## Files in the dataset

- LocationOfFaecalSampling.csv
  - What it contains: Info on where human and faecal samples were collected.
  - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude; Longitude; Altitude (m).

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - What it contains: Initial steps of isolating Bacteroides spp. markers for the week of 10 June 2018.
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - What it contains: Final steps of isolating Bacteroides spp. markers for the week of 10 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - What it contains: Initial steps of isolating Bacteroides spp. markers for the week of 17 June 2018.
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - What it contains: Final steps of isolating Bacteroides spp. markers for the week of 17 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- DetectionOfFIB&MSTmarkers.csv
  - What it contains: Levels of fecal indicator bacteria and related markers in drinking water sources and treated wastewater.
  - Columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/mL); Phages of Bacteroides fragilis GB124 (PFU/mL); Phages of potential human Bacteroides spp. markers (multiple codes: LU.2, TIB.1, TIA.1, WAA.1, ONA.3, KN.1, KN.2, KN.3, KN.8, SIN.19) (PFU/mL).

## Linkages and integration notes

- Cross-file continuation:
  - IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA.
  - IsolationBacteroidesHostsweek17-6-18StepB is a continuation of IsolationBacteroidesHostsWeek17-6-18StepA.
- Matching key between StepA and StepB files:
  - The information in column A (Location name from faecal sample collection) should be matched between StepA and StepB files, even though the entries are not in the same order or quantity.
- Location-code conventions:
  - Codes for Bacteroides-host isolates encode location initials plus isolate number (e.g., LU.2 = Luawk primary school pit latrine; SIN.19 = Sinogo water pan shoreline).
- Data integration goal:
  - Link sampling locations, their geographic coordinates, and the isolation outcomes across the two weeks (10–16 June and 17 June) to enable spatial-temporal analyses and correlation with FIB/MST marker detections.

## Data use notes and considerations

- Units and measurements:
  - CFU: colony-forming units; CFU/gram for faecal samples; CFU/100 mL for water samples; PFU/mL for phages.
- Spatial-temporal scope:
  - Two distinct weeks in June 2018 with both initial (StepA) and final (StepB) isolation steps, plus environmental marker data from drinking water sources.
- Analyst considerations:
  - Ensure proper matching of StepA and StepB entries by location names.
  - Maintain the linkage between faecal sampling locations and subsequent Bacteroides isolates.
  - Use the location codes to map environmental markers (in DetectionOfFIB&MSTmarkers) to the corresponding sampling sites.
  - Be aware of potential data gaps where entries differ in quantity or order between Week 10 and Week 17 files.
- Potential analyses:
  - Spatial distribution of isolation outcomes and CFU counts by location.
  - Temporal comparison of StepA vs StepB results within each week.
  - Associations between fecal sample origins, dilution factors, and isolation success.
  - Correlations between environmental FIB/MST markers and presence of specific Bacteroides hosts or their phages.