# Details of data structure

- This document describes a six-file CSV dataset used for monitoring environmental health metrics related to Bacteroides markers and fecal indicator organisms in water sources and fecal samples.
- The dataset combines sampling locations, isolation steps for Bacteroides hosts, and detection of FIB/MST markers to enable temporal and spatial assessment of environmental health.

## The six CSV files

- LocationOfFaecalSampling.csv
  - Purpose: Provides information on where human and fecal samples were collected for Bacteroides marker isolation.
  - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude; Longitude; Altitude.

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Purpose: Initial steps of isolation of Bacteroides markers for the week of 10 June 2018.
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Purpose: Final steps of isolation for the week of 10 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Purpose: Initial steps of isolation of Bacteroides markers for the week of 17 June 2018.
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Purpose: Final steps of isolation for the week of 17 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- DetectionOfFIB&MSTmarkers.csv
  - Purpose: Levels of faecal indicator bacteria (FIB: intestinal enterococci, total coliforms, E. coli), somatic coliphages, phages infecting Bacteroides fragilis GB124, and phages for potential Bacteroides hosts in drinking water and wastewater effluents.
  - Columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/mL); Phages of B. fragilis GB124 (PFU/mL); Phages of potential human Bacteroides spp. codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3, KN.1, KN.2, KN.3, KN.8, SIN.19 (PFU/mL).

- Note on codes
  - The codes for newly isolated Bacteroides spp. markers combine location initials with isolate numbers (e.g., LU.2; SIN.19).

## Linkages between files

- IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; entries should be matched by Location name from faecal sample collection.
- IsolationBacteroidesHostsWeek17-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek17-6-18StepA; entries should be matched by Location name from faecal sample collection.

## Data integration and use for monitoring

- The dataset supports:
  - Mapping environmental sampling locations to Bacteroides markers and CFU counts.
  - Integrating fecal sampling data with water quality indicators (FIB/MST markers) for a comprehensive view of environmental health.
  - Temporal analysis by week (10 Jun and 17 Jun 2018) to assess changes in marker presence and concentrations.

## Data quality, handling, and storage

- Data align with standardised column structures across files to facilitate verification, cleaning, and transformation.
- When using, consider:
  - Merging StepA and StepB files by matching Location name.
  - Merging Week10 and Week17 sets similarly to construct complete isolation histories per location.
  - Ensuring geographic coordinates are consistent (Latitude/Longitude/Altitude) and units are standardized.
- It is recommended to store and upload the consolidated datasets to appropriate data portals for accessibility and transparency, in line with environmental monitoring practices.