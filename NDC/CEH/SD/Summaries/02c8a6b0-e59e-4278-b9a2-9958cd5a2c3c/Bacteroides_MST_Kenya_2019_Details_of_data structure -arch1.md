# Details of data structure

- The document describes a dataset comprising six CSV files that together capture sampling locations, isolation steps for Bacteroides hosts, and marker detection in water sources.
- The data are organized by two sampling weeks (week of 10 June 2018 and week of 17 June 2018) and by two processing steps (Step A and Step B) for the Bacteroides host isolation, plus a separate file for detection of fecal indicator bacteria and related phages.

## Files and contents

- LocationOfFaecalSampling.csv
  - Provides geographic and sample-identifying information for human and faecal samples used in isolation.
  - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude (decimal degrees); Longitude (decimal degrees); Altitude (metres).

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Initial steps of isolation for week commencing 10 June 2018.
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram of faecal sample); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Final steps of isolation for week commencing 10 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Initial steps of isolation for week commencing 17 June 2018.
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram of faecal sample); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Final steps of isolation for week commencing 17 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- DetectionOfFIB&MSTmarkers.csv
  - Information about levels of fecal indicator bacteria and related phages in drinking water sources and wastewater effluents.
  - Columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/1 mL); Phages of Bacteroides fragilis strain GB124 (PFU/1 mL); Phages of potential human Bacteroides spp. codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3 (PFU/1 mL each); Phages of potential cattle Bacteroides spp. codes KN.1, KN.2, KN.3, KN.8, SIN.19 (PFU/1 mL each).

## Linkages between files

- IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; the two files should be matched by the Location name from faecal sample collection (column A), despite differing order and entry counts.
- IsolationBacteroidesHostsWeek17-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek17-6-18StepA; similarly, match by Location name from faecal sample collection (column A).

## Codes and interpretation

- In DetectionOfFIB&MSTmarkers, the codes for potential human Bacteroides spp. isolates (e.g., LU.2, TIB.1, TIA.1, WAA.1) and cattle Bacteroides spp. (KN.1, KN.2, KN.3, KN.8, SIN.19) encode location-based isolate numbers.
- The notes indicate these codes correspond to the initials of sampling locations plus isolate numbers (e.g., LU.2 = Luawk primary school pit latrine, isolate 2).

## Practical implications for analysts

- The dataset supports integrated analysis of sampling location, geospatial context, and laboratory isolation results across two time windows and processing steps.
- Key join keys for merging: Location name from faecal sample collection (shared across Step A/B files within each week) and the location metadata from LocationOfFaecalSampling.csv.
- The DetectionOfFIB&MSTmarkers.csv file enables correlation of environmental water quality markers with Bacteroides-host isolation results and could inform assessments of contamination or host distributions.
- Awareness of potential dataset scale and integration challenges is important, given multiple files with similar location references and the need to align by location names across different weeks and steps.