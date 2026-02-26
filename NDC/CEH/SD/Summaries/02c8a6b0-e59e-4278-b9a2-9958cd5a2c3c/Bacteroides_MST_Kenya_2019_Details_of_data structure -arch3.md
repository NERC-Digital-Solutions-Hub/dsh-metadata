# Details of data structure

## Overview
- Dataset describing six CSV files related to sampling, isolation of Bacteroides hosts, and detection of fecal indicator bacteria and related markers in water sources.
- Data are organized to support environmental health monitoring, including sampling locations, methods, organism isolation steps, and marker detection.

## Data Files and Contents
- 1. LocationOfFaecalSampling.csv
  - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude (decimal degrees); Longitude (decimal degrees); Altitude (metres).
- 2. IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram of faecal sample); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).
- 3. IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.
- 4. IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Columns: Location name from faecal sample collection; Latitude (decimal degrees); Longitude (decimal degrees); Altitude (metres); Faecal sample origin; Dilution factor (per gram of faecal sample); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).
- 5. IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.
- 6. DetectionOfFIB&MSTmarkers.csv
  - Columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/1 mL); Phages of Bacteroides fragilis strain GB124 (PFU/1 mL); Phages of potential human Bacteroides spp. codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3 (PFU/1 mL); Phages of potential cattle Bacteroides spp. codes KN.1, KN.2, KN.3, KN.8, SIN.19 (PFU/1 mL).
  - Note on codes: newly isolated Bacteroides spp. marker codes combine location initials and isolate number (e.g., LU.2 = Luawk primary school pit latrine, isolate 2; SIN.19 = Sinogo water pan shoreline, isolate 19).

## Data Linkages and Integration
- File "IsolationBacteroidesHostsWeek10-6-18StepB" is a continuation of "IsolationOfBacteroidesHostsWeek10-6-18StepA"; entries are not in the same order or quantity, but the A column (Location name from faecal sample collection) should be matched between the two.
- Similarly, "IsolationBacteroidesHostsWeek17-6-18StepB" continues "IsolationOfBacteroidesHostsWeek17-6-18StepA"; the A column should be matched across these paired files.

## Variables and Units
- Geospatial: Latitude and Longitude are in decimal degrees; Altitude in metres.
- Microbiological measurements: CFU (colony-forming units) for Esculin reactions (anaerobic/aerobic) and other markers; PFU (plaque-forming units) for phages.
- Timepoints: Sampling dates for faecal and water samples; two separate weeks (10-6-18 and 17-6-18) for isolation steps.

## Relevance for Monitoring Frameworks
- Provides a structured data pipeline from sampling location to lab-based isolation results and water quality markers.
- Supports assessment of environmental health indicators (FIB, MST markers) and potential pathogen indicators in water sources.
- Enables monitoring framework authors to define data provenance, reproducibility, and linkage across sampling events and analytical steps.

## Data Quality, Access, and Governance Considerations
- Metadata gaps may hinder data verification; some fields rely on precise sample origin descriptions and lab methods.
- Data may be subject to sharing constraints; public dissemination of underlying datasets should be aligned with governance and openness standards.
- Data transformation and harmonization may be required to integrate across weeks and steps; attention needed for consistent location naming and indexing.

## Practical Guidance for Reuse
- When integrating files, align by Location name from faecal sample collection to pair StepA and StepB data for each week.
- Use DetectionOfFIB&MSTmarkers to assess water quality alongside fecal sampling results for comprehensive environmental health monitoring.
- Reference the coding scheme for isolates to interpret marker origins and cross-link with location data.