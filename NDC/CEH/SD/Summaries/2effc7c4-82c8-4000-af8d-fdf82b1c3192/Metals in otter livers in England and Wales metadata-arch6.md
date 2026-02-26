# Otter Liver Tissue Data Dictionary (Predatory Bird Monitoring Scheme; Cardiff University Otter Project)

- Overview
  - A dataset of otter findings with unique identifiers from two sources: CEH Ref (Predatory Bird Monitoring Scheme) and UWC Ref (Cardiff University Otter Project).
  - Records include when and where the otter body was found (Month Found, Year Found, County) and basic metadata (Sex, AgeClass).
  - Biological metric: Condition coefficient (K) referenced to Kruuk & Conroy (1991) mortality study.
  - Spatial data: X-coordinate and Y-coordinate positions.
  - Tissue composition: % dry matter of the liver.
  - Chemical analysis: Dry weight concentrations (mg/kg) of numerous elements in liver tissue, with statuses for each metric (ND = not detected; NA = not analysed).

- Fields and Definitions
  - CEH Ref: Unique numeric identifier (Predatory Bird Monitoring Scheme).
  - UWC Ref: Unique numeric identifier (Cardiff University Otter Project).
  - Month Found; Year Found: Temporal context of finding.
  - County: Location within England or Wales.
  - Sex: Female or Male.
  - AgeClass: Juvenile, Sub-adult, or Adult.
  - Condition coefficient (K): Body condition metric; defined per Kruuk & Conroy (1991).
  - X-coordinate; Y-coordinate: Spatial positioning data.
  - % Dry matter: Proportion of liver mass that is dry matter (determined from drying a 0.5 g sample at 70°C for 48 hours).
  - Al, Mn, Fe, Co, Ni, Cu, Zn, Se, Sr, Mo, Cd, Sb, Pb, Hg, Cr, As, V, Ag: Dry weight concentrations in mg/kg of liver tissue.
  - ND/NA: ND = not detected; NA = not analysed.

- Data quality and interpretation
  - ND indicates non-detection; NA indicates not analysed.
  - Data may be patchy and come from multiple systems, requiring harmonisation.
  - Formats and completeness vary across records; careful quality assurance and integration are needed.
  - Interpreting the Condition coefficient (K) may require domain-specific understanding.

- Potential data uses and products
  - Enable self-serve exploration through dashboards, pivot tables, and charts.
  - Generate reports with guidance on data usage and interpretation.
  - Combine with other datasets (cross-dataset analyses) using the unique identifiers.
  - Identify opportunities to improve data collection and consistency across systems.

- Particular challenges and recommended actions for Data Support
  - Time spent understanding the ask due to limited upfront data consideration.
  - Managing patchy data across a wide range of formats and systems.
  - Communicating complex information in a clear, accessible way.
  - Promoting outputs to maximize sharing and reuse.
  - Actions: clarify requirements, verify data sufficiency, clean and transform data, promote outputs, seek topic experts, and advocate for better data creation practices.