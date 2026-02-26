# Details of data structure

- This dataset comprises six CSV files describing sampling locations, isolation of Bacteroides hosts, and detection of fecal indicator bacteria and related markers.

## File-by-file overview

- LocationOfFaecalSampling.csv
  - Purpose: location information for where human and faecal samples were collected.
  - Key columns: Date of sample collection; Faecal sample number and origin; Source name; Latitude; Longitude; Altitude.

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Purpose: initial steps of isolating Bacteroides spp. markers for the week starting 10 June 2018.
  - Key columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Purpose: final steps of isolating Bacteroides spp. markers for the week starting 10 June 2018.
  - Key columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Purpose: initial steps of isolating Bacteroides spp. markers for the week starting 17 June 2018.
  - Key columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Purpose: final steps of isolating Bacteroides spp. markers for the week starting 17 June 2018.
  - Key columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- DetectionOfFIB&MSTmarkers.csv
  - Purpose: levels of fecal indicator bacteria and related markers in drinking water sources and wastewater effluent.
  - Key columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/mL); Phages of Bacteroides fragilis GB124 (PFU/mL); Phages of potential human Bacteroides spp. markers (codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3, KN.1, KN.2, KN.3, KN.8, SIN.19) with PFU/mL.

## Cross-file linkages

- Week 10-6-18: IsolationOfBacteroidesHostsWeek10-6-18StepA.csv should be linked to IsolationBacteroidesHostsWeek10-6-18StepB.csv via matching Location name from faecal sample collection (column A). Entries are not in the same order or quantity, so careful matching is required.
- Week 17-6-18: IsolationBacteroidesHostsWeek17-6-18StepA.csv should be linked to IsolationBacteroidesHostsweek17-6-18StepB.csv in the same way (Location name from faecal sample collection).

## Codes and interpretation notes

- In DetectionOfFIB&MSTmarkers.csv, codes for Bacteroides spp. host markers (e.g., LU.2, SIN.19) correspond to the initials of the location names where fecal samples were collected plus the isolate number. This allows tracing isolate origins (e.g., LU.2 = Luawk primary school pit latrine, isolate 2).

## Data use considerations (for Data Support)

- The dataset provides a broad view of sampling locations, sample origins, and the outcomes of isolation steps (CFU counts, Gram staining, isolate codes). It also includes water-quality markers (FIB and MST markers) across water sources and treatment plant effluents.
- Where weeks contain continuation files (StepA vs StepB), ensure proper reconciliation by matching on the shared location name field, mindful of potential mismatches in order or entry counts.
- Potential data products to support end users:
  - Location-based explorer showing sampling sites with coordinates and CFU/marker levels over time.
  - Time-series dashboards for FIB/MST markers across water sources and dates.
  - Joinable views linking fecal sample origins to final Bacteroides isolates via StepA/StepB codes for traceability.
- Suggested data quality actions:
  - Standardize location naming across StepA and StepB to ease joins.
  - Validate that each StepA entry has a corresponding StepB entry for the same location where applicable.
  - Document units (CFU/100 mL, PFU/mL) consistently across files.