# IM Protocol

## Overview
- A standardized protocol to collect and identify daily collections of macrolepidoptera (butterflies and moths) using light traps.
- Based on the Rothamsted Insect Survey (RIS) methodology, leveraging 25+ years of centralized data to analyse population trends.
- Serves as a long-term environmental monitoring framework with potential policy evaluation and decision-support applications.

## Aim and Rationale
- Aim: Systematically sample macrolepidoptera with a standard light trap to monitor environmental change indicators.
- Rationale: Lepidoptera are well-known taxonomically and biologically and their larval phytophagy makes them good indicators of environmental change; RIS provides a robust, expert-backed, long-running data resource.

## Method
### Equipment
- Standard Rothamsted light trap (Williams 1948) requiring a continuous power supply.

### Location
- Site near the TSS (trap site) with accessibility for daily emptying; near laboratories, houses, or farms if possible.
- Shelter the trap with vegetation if possible; place >20 m from artificial light sources when feasible.

### Sampling and Data Handling
- Frequency: Ideally daily all year; if not possible, samples can be accumulated (e.g., weekends).
- Identification: Samples posted to Rothamsted for identification unless local expertise exists.
- Data storage: All data stored in the RIS database and the ECN database.
- Scale: For large sites, multiple traps are desirable if suitable operators are available.
- Operational detail: Emptying a trap takes about 40 minutes per trap per week, plus travel.

### Appendix I – Trap Description and Daily Operation
- Trap structure: Approximately 1.2 m stand, 1.5 m overall height; 0.6 x 0.6 m footprint.
- Light source: 200 W clear tungsten lamp, mains powered; solar dial time-switch adjusts for daylength; RCD provides safety.
- Collection medium: Insects collected in a jar lined with plaster and dosed with about 5 ml tetrachloroethane to immobilize specimens.
- Daily routine: Check RCD, clock accuracy, lamp operation, replace jar and re-dose with tetrachloroethane, annotate site and date on boxes, and report any non-operational days.

### Safety and Hazards
- Tetrachloroethane: toxic; precautions include avoiding inhalation/skin contact, working in well-ventilated areas, wearing safety gear, and proper spill management.
- Electricity: Ensure power is disconnected before changing bulbs; follow professional electrical guidance and maintain RCDs.

## Data Recording and Standards
### Recording Conventions
- Core dataset requirements (ECN Site, ECN core measurement, location, sampling date/time) to uniquely identify each sampling event.
- Core measurement: invertebrates – moths (IM Protocol).
- Data fields include:
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Date trap set
  - Sampling date
  - Species code and species name
  - Number caught (RIS code)
- Data handling guidance:
  - Sampling date denotes the date catch is collected after overnight recording.
  - Report any nights the trap did not operate (e.g., lamp failure).
  - Coding follows Heslop (1964); refer to accompanying Data Transfer documentation for ECN data formats.
- Data storage: Data are lodged in RIS and ECN databases; access to transfer documentation is available via ECNCCU.

### Notes and References
- The protocol cites foundational RIS literature (e.g., Taylor 1986; Woiwod & Harrington 1994; Woiwod et al. 1990–1994) and ensures traceability through standardized references.
- The Heslop (1964) coding system is the basis for dataset coding.

## Relevance to Monitoring Frameworks
- Demonstrates how a long-running, standardized protocol yields consistent time-series data suitable for policy evaluation and environmental health monitoring.
- Emphasizes data standardization, clear metadata, and robust data governance (data quality assurance, storage in centralized databases, and explicit data transfer documentation).
- Highlights the importance of accessible underlying data for transparency and decision-making, while balancing safety and operational constraints.

## Challenges and Considerations for Authors of Monitoring Frameworks
- Data gaps and data quality: relies on daily, year-round sampling; interruptions (lamp failures, access, weather) create gaps requiring clear reporting.
- Access and sharing: data must be publicly shareable, yet some barriers may exist due to safety, proprietary concerns, or metadata completeness.
- Silos: data collocated within RIS and ECN databases; cross-organizational data integration may require governance to avoid silos.
- Metadata adequacy: thorough metadata (dates, trap settings, location codes) is essential for verifiability and reuse.
- Data transformation: raw trap data must be cleaned and transformed into standardized formats for analysis and comparison.
- Governance and openness: need for data management standards, versioning, and transparent sharing policies to enable reuse and policy use.