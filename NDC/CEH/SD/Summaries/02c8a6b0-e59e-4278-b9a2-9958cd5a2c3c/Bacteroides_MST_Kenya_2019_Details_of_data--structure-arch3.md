# Details of data structure

- Purpose and scope
  - A six-file CSV dataset detailing sampling locations, isolation steps for Bacteroides spp. markers, and detection of fecal indicator bacteria (FIB) and MST markers in water sources and waste outputs.
  - Designed to support environmental health monitoring, linking field sampling with laboratory isolation results and marker detections.

- Files and their contents
  - LocationOfFaecalSampling.csv
    - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude; Longitude; Altitude.
  - IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
    - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; Positive/Negative Esculin reaction and CFU (Anaerobic); Positive/Negative Esculin reaction and CFU (Aerobic).
  - IsolationBacteroidesHostsWeek10-6-18StepB.csv
    - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive/Negative Esculin reaction and CFU (Anaerobic); Positive/Negative Esculin reaction and CFU (Aerobic); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.
  - IsolationBacteroidesHostsWeek17-6-18StepA.csv
    - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; Positive/Negative Esculin reaction and CFU (Anaerobic); Positive/Negative Esculin reaction and CFU (Aerobic).
  - IsolationBacteroidesHostsweek17-6-18StepB.csv
    - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive/Negative Esculin reaction and CFU (Anaerobic); Positive/Negative Esculin reaction and CFU (Aerobic); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.
  - DetectionOfFIB&MSTmarkers.csv
    - Columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/mL); Phages of Bacteroides fragilis GB124 (PFU/mL); Phages of potential human Bacteroides spp. codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3, KN.1, KN.2, KN.3, KN.8, SIN.19 (PFU/mL).

- Linkages between files
  - IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; entries should be matched by Location name from faecal sample collection (Column A).
  - IsolationBacteroidesHostsWeek17-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek17-6-18StepA; entries should be matched by Location name from faecal sample collection (Column A).

- Data quality and metadata considerations
  - Some datasets require careful alignment across files via location-based keys.
  - The sixth file includes codes that map to locations and isolate numbers (e.g., LU.2, SIN.19), which should be cross-referenced with sampling locations.
  - The dataset supports temporal (week-of-collection) and spatial (lat/long) analysis for environmental health monitoring.

- Implications for monitoring frameworks
  - Provides structured, chaptered data suitable for creating dashboards and reports on FIB/MST markers and Bacteroides-related indicators.
  - Enables assessment of contamination patterns across time and space, linking field sampling to laboratory results.
  - Highlights the need for robust data governance and harmonization when integrating multiple files, including consistent location identifiers and clear provenance for isolates and marker detections.