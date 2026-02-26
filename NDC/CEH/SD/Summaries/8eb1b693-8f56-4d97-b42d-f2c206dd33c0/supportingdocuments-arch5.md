# Data structure

- The dataset captures growth responses of ectomycorrhizal (ECM) fungi across multiple isolates under nine nutrient treatments.
- Measurements include growth rate (mm per day) and biomass (g dry weight per cm2) collected over a prolonged period, with colony diameter measured daily.

## Overview

- Focus: Growth of 7 ECM fungal isolates under nine nutrient treatments formed by nitrogen (N) and phosphorus (P) sources.
- Treatments vary the form of N (inorganic N, organic N, or no N) and P (inorganic P, organic P, or no P).
- Two primary response variables are recorded: growth rate and biomass.
- Data collection spans roughly 57 days for diameter measurements; growth rate is described as over 52 days in the design, with diameter tracked daily for 57 days.

## Experimental design

- Fungal isolates used:
  - Laccaria bicolor (lb101B)
  - Laccaria amethystina (la56)
  - Paxillus involutus (Pi47)
  - Piloderma byssinum (PbUP185)
  - Suillus bovinus (O96)
  - Suillus viscidus (Sv171)
  - Suillus viscidus (SvAFST1)
- Culture conditions:
  - Growth on a 1 L control Melin-Norkrans (MMN) nutrient agar
  - Temperature: 18°C
  - pH: 5.5
  - Carbon source: glucose
  - Trace elements added (Mg, Ca, Fe, NaCl)
- Nine MMN treatments differed only in nitrogen and phosphorus sources, while all other components remained as in the base MMN formulation.

## Data schema and variables

- Columns (as per the data table design):
  - B: Isolate/agar composition code (reference name of ECM fungal isolate)
  - C: Nitrogen source code (InN, OrgN, NoN)
  - D: Phosphorus source code (InP, OrgP, NoP)
  - E: Measured growth rate (mm per day)
  - F: Biomass (g dry weight per cm2)
- Isolate references include lb101B, la56, Pi47, PbUP185, O96, Sv171, SvAFST1.
- The nine treatments are defined by combinations of N and P forms through the codes C and D.
- Units:
  - Growth rate: millimeters per day (mm/day)
  - Biomass: grams dry weight per square centimeter (g dwt per cm2)

## Treatments and media composition

- Nitrogen sources (N):
  - Inorganic N: ammonium nitrate (NH4NO3) at 175 mg/L
  - Organic N: glycine at 82 mg/L, glutamines at 78 mg/L, glutamic acid at 161 mg/L, phenylalanine at 181 mg/L
  - No nitrogen: NoN
- Phosphorus sources (P):
  - Inorganic P: monopotassium phosphate (KH2PO4) at 1.6 g/L
  - Organic P: phytic acid dipotassium salt at 1.44 g/L
  - No phosphorus: NoP
- Media base:
  - MMN agar prepared with glucose as carbon source
  - pH adjusted to 5.5
  - Trace elements included (MgSO4·7H2O, CaCl2·2H2O, FeCl3·6H2O, NaCl with specified concentrations)

## Measurements

- Colony diameter measured daily over a 57-day period.
- Biomass determined by:
  - Harvesting mycelia
  - Freeze-drying
  - Weighing to obtain g dry weight per cm2

## Data quality and stewardship considerations

- Metadata and provenance:
  - Clear linkage between isolate codes (B), nitrogen (C), phosphorus (D), and measured responses (E, F) to enable reproducibility.
  - Maintain a mapping table to connect abbreviations with full species names and treatment details.
- Standards and interoperability:
  - Ensure consistent units across datasets (mm/day for growth rate; g dwt per cm2 for biomass).
  - Document exact MMN formulation and any deviations to support cross-study comparisons.
- Data governance and sharing:
  - Versioning of dataset to capture updates or corrections.
  - Clear guidance on data reuse, especially given multiple isolates and treatment combinations.
  - Consider uploading to appropriate data portals with standardized metadata to support discoverability by data users.
- Data quality checks:
  - Validate that growth rate corresponds to the diameter time series (noting the potential discrepancy between “52 days” in design and “57 days” in measurements).
  - Verify consistency of isolate IDs, treatment codes, and corresponding metadata across records.
- Practical challenges for stewardship:
  - Handling and harmonizing data from multiple systems/ formats if integrated with other datasets.
  - Managing large, time-series measurements (daily diameter across 57 days) and associated biomass data.