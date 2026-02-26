# Details of data structure

- A dataset comprising six CSV files related to sampling, isolation of Bacteroides hosts, and detection of fecal indicator markers (FIB) and MST markers.

## File-by-file summaries

- LocationOfFaecalSampling.csv
  - 6 columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude (decimal degrees); Longitude (decimal degrees); Altitude (metres).

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - 10 columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram of faecal sample); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - 10 columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - 10 columns: Location name from faecal sample collection; Latitude (decimal degrees); Longitude (decimal degrees); Altitude (metres); Faecal sample origin; Dilution factor (per gram of faecal sample); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - 10 columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- DetectionOfFIB&MSTmarkers.csv
  - 16 columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/1 mL); Phages of Bacteroides fragilis GB124 (PFU/1 mL); Phages of potential human Bacteroides spp. codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3 (PFU/1 mL); Phages of potential cattle Bacteroides spp. codes KN.1, KN.2, KN.3, KN.8, SIN.19 (PFU/1 mL). Note: codes correspond to location names plus isolate numbers.

## Linkages between CSV files

- IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; match entries by Location name from faecal sample collection (column A).
- IsolationBacteroidesHostsweek17-6-18StepB is a continuation of IsolationBacteroidesHostsWeek17-6-18StepA; match entries by Location name from faecal sample collection (column A).
- These cross-file alignments enable combined analysis of initial and final isolation steps for each sampling location across the two weeks.