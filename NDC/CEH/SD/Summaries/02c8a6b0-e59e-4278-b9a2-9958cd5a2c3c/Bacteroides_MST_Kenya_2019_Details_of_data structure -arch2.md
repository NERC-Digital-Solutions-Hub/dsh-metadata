# Details of data structure

- The dataset comprises six CSV files:
  1. LocationOfFaecalSampling
  2. IsolationOfBacteroidesHostsWeek10-6-18StepA
  3. IsolationBacteroidesHostsWeek10-6-18StepB
  4. IsolationBacteroidesHostsWeek17-6-18StepA
  5. IsolationBacteroidesHostsweek17-6-18StepB
  6. DetectionOfFIB&MSTmarkers

- Purpose across files
  - Documents where human and faecal samples were collected for Bacteroides spp. marker isolation.
  - Describes the initial (Step A) and final (Step B) steps of isolating Bacteroides hosts for two sampling weeks.
  - Reports environmental drinking water quality indicators and markers (FIB and MST) in water sources and wastewater effluents.

- Detailed content by file
  - LocationOfFaecalSampling.csv
    - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude; Longitude; Altitude.
    - Purpose: geolocate sampling sites and origins.
  - IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
    - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; Positive/Negative Esculin reaction and CFU (Anaerobic and Aerobic).
    - Purpose: initial isolation data for the week starting 10 June 2018.
  - IsolationBacteroidesHostsWeek10-6-18StepB.csv
    - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive/Negative Esculin reaction and CFU (Anaerobic and Aerobic); Gram staining information; Status; Code and origin of Bacteroides hosts selected.
    - Purpose: final isolation data for the week starting 10 June 2018.
  - IsolationBacteroidesHostsWeek17-6-18StepA.csv
    - Columns: Location name from faecal sample collection; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; Positive/Negative Esculin reaction and CFU (Anaerobic and Aerobic).
    - Purpose: initial isolation data for the week starting 17 June 2018.
  - IsolationBacteroidesHostsweek17-6-18StepB.csv
    - Columns: Location name from faecal sample collection; Faecal sample origin; Bacterial Isolate code; Positive/Negative Esculin reaction and CFU (Anaerobic and Aerobic); Gram staining information; Status; Code and origin of Bacteroides hosts selected.
    - Purpose: final isolation data for the week starting 17 June 2018.
  - DetectionOfFIB&MSTmarkers.csv
    - Columns: Date of water sampling; Water source name; Intestinal enterococci (CFU/100 mL); Total coliforms (CFU/100 mL); Escherichia coli (CFU/100 mL); Somatic coliphages (PFU/mL); Phages of Bacteroides fragilis GB124; Phages of various potential human Bacteroides hosts (codes LU.2, TIB.1, TIA.1, WAA.1, ONA.3, KN.1, KN.2, KN.3, KN.8, SIN.19); other phage codes as listed.
    - Purpose: quantify FIB and MST markers and bacteriophage indicators in drinking water sources and wastewater effluents.
    - Note on codes: codes for new Bacteroides spp. hosts combine location initials and isolate number (e.g., LU.2 = Luawk primary school pit latrine, isolate 2).

- Data integration and linking guidance
  - The Week10-6-18 StepB data continues from Week10-6-18 StepA; entries should be matched via Column A (Location name from faecal sample collection), though the two files are not in the same order or quantity.
  - Similarly, Week17-6-18 StepB continues from Week17-6-18 StepA with matching by Location name from faecal sample collection.
  - When combining datasets, align and deduplicate using the Location name from faecal sampling to ensure continuity of site-level observations across steps.

- Relevance for environmental monitoring
  - Supports standardized reporting of sampling locations, sample origins, and isolation outcomes over two mid-June weeks.
  - Enables cross-referencing environmental microbiological indicators (FIB and MST markers) with Bacteroides host isolation data.
  - Provides structured data suitable for producing maps, charts, and reports to assess environmental health and treatment-related water quality.

- Data quality and stewardship considerations
  - Ensure proper QA/QC when merging StepA and StepB files for each week due to non-aligned ordering.
  - Maintain clear provenance by preserving site codes and location names for traceability across steps and markers.
  - Store and upload resulting datasets to appropriate portals as part of standard monitoring data workflows.