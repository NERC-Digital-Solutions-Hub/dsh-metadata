# IM Protocol

- Purpose and scope
  - Standardized protocol to collect and identify daily macrolepidoptera (large moths) using Rothamsted Insect Survey (RIS) light traps.
  - Supports long-term environmental monitoring with an existing national database accumulated over ~25 years.
  - Data are intended to enable trend analysis of moth populations and environmental change.

- Rationale
  - Butterflies and moths are good indicator taxa due to their ecological characteristics and sensitivity to environmental change.
  - Protocol aligns with RIS methodology to ensure consistency and comparability over time.

- Equipment
  - Standard RIS light trap: ~1.2 m stand, 1.5 m overall height, 0.6 m width/depth.
  - Light source: 200 W clear tungsten lamp powered by mains electricity, on a solar dial time-switch.
  - Safety/handling: Residual Current Device (RCD) protection; trap designed for daily operation and sample collection.

- Location and site considerations
  - Positioned for easy daily emptying; near TSS when possible, often near laboratories, houses, or farms.
  - Shelter by vegetation when possible; ideally >20 m from artificial light sources.

- Sampling protocol
  - Ideally daily sampling year-round; if not possible, accumulate samples (e.g., weekends).
  - Samples posted to Rothamsted for identification unless local expertise is available.
  - For large sites, multiple traps may be used if operators can be found.
  - Time commitment: approximately 40 minutes per trap per week for emptying; 15 minutes per site per year for experienced identifiers.

- Procedures (daily operations)
  - Step-by-step checks before collection: confirm RCD status, correct clock/time (GMT), lamp functioning, and jar setup.
  - Collect sample into pre-dosed jars containing ~5 ml tetrachloroethane; prevent exposure to vapour.
  - Transfer insects to tissue-lined pill boxes in a well-ventilated area; re-dose jar for next use.
  - Label each box with site name and date range (e.g., 14–15 June 1995; or 27/30 January 1995 for a weekend run).
  - If two boxes are used, mark as 1/2 and 2/2; report any non-operational nights.

- Preservation and safety
  - Insect samples are preserved and immobilized quickly using tetrachloroethane (toxic; hazardous handling required).
  - Safety precautions include avoiding inhalation, skin/eye contact, using PPE, and ensuring ventilation; handle spills with appropriate measures.
  - Electrical safety: disconnect power before bulb replacement; regular testing of RCD; contact electricians for faults.

- Data capture and recording conventions (GIS-ready data fields)
  - Core schema for ECN sites; key fields required for each sampling occasion:
    - Site Identification Code (e.g., T05) – unique ECN Site code.
    - Core Measurement Code (e.g., PC) – identifies the measurement type.
    - Location Code (e.g., 01) – sampling location code within the site.
    - Sampling Date/Time – date (and time if sampling frequency exceeds daily).
  - Core measurements for invertebrates – moths (IM Protocol):
    - Species code; Species name; Number caught; Units = RIS code.
    - Optional: genus and full taxonomic details.
  - Data recording conventions reference Heslop (1964) coding system; data support and transfer documentation available in ECN datasets.
  - Notes on data capture:
    - Sampling Date is the date the catch is collected after overnight recording.
    - Report nights when the trap did not operate (e.g., lamp failure).
    - If samples are accumulated over several nights, date reflects trap set and date emptied.

- Data use and integration
  - Data stored in RIS database and ECN database; available datasets follow ECNCCU data transfer documentation.
  - Format supports GIS analyses and map-based visualizations of spatial patterns and temporal trends.
  - Field definitions and codes are designed to enable integration into broader environmental monitoring systems.

- Appendices and references
  - Appendix I: Daily operation details for RIS light trap (equipment setup and step-by-step workflow).
  - Foundational literature and project references (Rothamsted Insect Survey history, light trap methodology, and related ecological studies).