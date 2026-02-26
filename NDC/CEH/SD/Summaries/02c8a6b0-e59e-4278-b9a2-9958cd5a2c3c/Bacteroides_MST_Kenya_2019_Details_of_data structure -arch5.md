# Details of data structure

- Six CSV files comprise the dataset, each with specific information on sampling locations, isolation steps for Bacteroides hosts, and measurements of fecal indicator markers.
- The dataset covers sampling locations, the early and final steps of isolating Bacteroides hosts over two weeks (week of 10-06-2018 and 17-06-2018), and detection of FIB and MST markers in water sources.

## File-by-file descriptions

- LocationOfFaecalSampling.csv
  - Purpose: Provides the sampling locations for human and faecal samples used to isolate Bacteroides spp. markers.
  - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude (decimal degrees); Longitude (decimal degrees); Altitude (metres).

- IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - Purpose: Initial steps for isolating Bacteroides spp. markers during the week starting 10 June 2018.
  - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor (per gram of faecal sample); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsWeek10-6-18StepB.csv
  - Purpose: Final steps for isolating Bacteroides spp. markers during the week starting 10 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - Purpose: Initial steps for isolating Bacteroides spp. markers during the week starting 17 June 2018.
  - Columns: Location name from faecal sample collection; Latitude (decimal degrees); Longitude (decimal degrees); Altitude (metres); Faecal sample origin; Dilution factor (per gram of faecal sample); Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU).

- IsolationBacteroidesHostsweek17-6-18StepB.csv
  - Purpose: Final steps for isolating Bacteroides spp. markers during the week starting 17 June 2018.
  - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive Esculin reaction and Anaerobic (CFU); Negative Esculin reaction and Anaerobic (CFU); Positive Esculin reaction and Aerobic (CFU); Negative Esculin reaction and Aerobic (CFU); Gram staining information; Status; Code and origin of Bacteroides spp. hosts selected.

- DetectionOfFIB&MSTmarkers.csv
  - Purpose: Measurements of fecal indicator bacteria and bacteriophages in drinking water sources and wastewater effluents.
  - Columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/1 mL); Phages of Bacteroides fragilis GB124 (PFU/1 mL); Phages of potential human Bacteroides spp. (codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3) (PFU/1 mL); Phages of potential cattle Bacteroides spp. (codes KN.1, KN.2, KN.3, KN.8, SIN.19) (PFU/1 mL).

## Linkages between files

- IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; matching should be done using Column A: Location name from faecal sample collection, though the two files are not in the same order or quantity.
- IsolationBacteroidesHostsWeek17-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek17-6-18StepA; matching should be done using Column A: Location name from faecal sample collection, with potential differences in order and entry counts.

## Data governance and stewardship considerations

- Provenance and lineage
  - Clear week-based sequences (StepA then StepB) with explicit location-based matching should be preserved to maintain traceability of isolation work.
- Metadata and data dictionary
  - Ensure definitions for all columns (units, scope of measurements, coding for isolate codes) are documented.
  - Note the mapping of isolate codes to locations (e.g., LU.2 = Luawk location isolate 2) for interpretability.
- Geospatial data
  - Latitude/Longitude are in decimal degrees; ensure consistent coordinate reference and preserve precision.
  - Altitude in metres; maintain unit consistency across records.
- Data integration
  - When linking StepA and StepB files, enforce the matching on the Location name from faecal sample collection.
  - Be aware of potential duplicates, missing entries, or misalignments due to the separate weekly files.
- Access, privacy, and sharing
  - Document any sharing restrictions or embargoes; maintain appropriate metadata to support discoverability without exposing sensitive identifiers.
- Interoperability and long-term storage
  - Store as stable CSVs with a central metadata record; consider a data dictionary and a data catalog entry to support discoverability by data users.

## Practical data quality considerations and challenges

- Inconsistent naming/casing (e.g., “week17” vs “Week17”) across files may affect joins.
- Different entries counts between paired StepA/StepB files require robust matching logic beyond simple row-by-row joins.
- The dataset relies on location-based codes that map to sample origins; ensure these mappings are preserved and properly documented for reuse.
- Large and multi-file structure requires careful versioning and update mechanisms to keep linked records consistent.

## Recommended next steps for effective stewardship

- Create a consolidated metadata record and data dictionary detailing each file, its purpose, and all columns with units and allowed values.
- Establish a formal join key strategy for linking StepA and StepB files, including handling of mismatches and missing values.
- Preserve and publish the location-to-code mappings (e.g., LU.2, SIN.19, KN.1) to ensure reproducibility.
- Store datasets in a data portal with clear provenance, versioning, and change-tracking, and set up a process for updates and re-validation of links.