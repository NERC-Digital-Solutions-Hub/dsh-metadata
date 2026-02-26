# Details of data structure

- Overview
  - A dataset comprising six CSV files that document sampling, isolation, and detection related to Bacteroides markers.
  - Includes geospatial sampling data, bacterial isolation steps (two weeks, two steps per week), and detection of faecal indicator bacteria and related phages.
  - Data types include dates, locations (lat/long/altitude), CFU counts, dilution factors, test results (Esculin reactions, Gram staining), and sample codes.

- File descriptions
  - LocationOfFaecalSampling.csv
    - Columns: Date of sample collection; Faecal sample number and origin; Name of faecal sample sources; Latitude; Longitude; Altitude.
    - Purpose: geolocated sampling events and sample origins.
  - IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
    - Columns: Location name; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; Positive/Negative Esculin reactions with Anaerobic/Aerobic CFU.
    - Purpose: initial isolation steps for Week 10 (June 2018).
  - IsolationBacteroidesHostsWeek10-6-18StepB.csv
    - Columns: Location name; Faecal sample origin; Bacterial Isolate code; Positive/Negative Esculin reactions with Anaerobic/Aerobic CFU; Gram staining information; Status; Code and origin of hosts.
    - Purpose: final isolation steps for Week 10.
  - IsolationBacteroidesHostsWeek17-6-18StepA.csv
    - Columns: Location name; Latitude; Longitude; Altitude; Faecal sample origin; Dilution factor; Positive/Negative Esculin reactions with Anaerobic/Aerobic CFU.
    - Purpose: initial isolation steps for Week 17 (June 2018).
  - IsolationBacteroidesHostsweek17-6-18StepB.csv
    - Columns: Location name; Faecal sample origin; Bacterial Isolate code; Positive/Negative Esculin reactions with Anaerobic/Aerobic CFU; Gram staining information; Status; Code and origin of hosts.
    - Purpose: final isolation steps for Week 17.
  - DetectionOfFIB&MSTmarkers.csv
    - Columns: Date of water sampling; Water source name; Intestinal enterococci; Total coliforms; Escherichia coli; Somatic coliphages; Phages targeting Bacteroides fragilis GB124; Phages for various potential human Bacteroides spp. codes (LU.2, TIB.1, TIA.1, WAA.1, ONA.3); Phages for potential cattle Bacteroides spp. codes (KN.1, KN.2, KN.3, KN.8, SIN.19).
    - Note: Codes map to location initials plus isolate numbers (e.g., LU.2 = Luawk primary school pit latrine, isolate 2).
    - Purpose: measurements of faecal indicator bacteria and phage indicators in drinking water sources and wastewater effluents.

- Linkages and data integration
  - Week 10: IsolationBacteroidesHostsWeek10-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek10-6-18StepA; join on Location name (though entries are not in the same order or quantity).
  - Week 17: IsolationBacteroidesHostsWeek17-6-18StepB is a continuation of IsolationOfBacteroidesHostsWeek17-6-18StepA; join on Location name (order and counts may differ).

- Data governance considerations for Data Leaders
  - Data richness across spatial, temporal, and experimental dimensions enables end-to-end tracing from sampling to host isolation and marker detection.
  - Key quality questions:
    - Consistency of Location name matching across StepA/StepB files and across weeks.
    - Completeness and standardization of CFU counts, dilution factors, and test results.
    - Clarity and consistency of sample origin codes and isolate codes.
    - Metadata availability for dates, sources, and methods to support discoverability.
  - Opportunities for improving data strategy:
    - Establish a canonical key for each sampling event to simplify cross-file joins.
    - Create a unified metadata schema (definitions, units, and data standards) to reduce ambiguity (e.g., Esculin reaction interpretations, CFU units).
    - Ensure documentation of data lineage and versioning to support reproducibility and collaboration across teams or partners.