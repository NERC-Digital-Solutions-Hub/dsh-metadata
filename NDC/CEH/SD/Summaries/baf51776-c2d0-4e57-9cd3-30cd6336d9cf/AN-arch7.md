# AN Protocol ATMOSPHERIC CHEMISTRY - NITROGEN DIOXIDE Version 1.1 (previously AC Protocol, updated Jan 2001)

- Purpose and context
  - Detect and define changes in periodic mean atmospheric concentrations of nitrogen dioxide (NO2).
  - NO2 is a key health and ecosystem pollutant, largely produced by urban fuel combustion.
  - Method used: passive diffusion tubes; low capital cost and minimal on-site power requirements; replicates needed due to tube variability.
  - Consideration for extension to other gases (ammonia, SO2, ozone) noted; currently no reliably passive methods for those.

- Field deployment and sampling design
  - At each ECN site: three exposed diffusion tubes (E1, E2, E3) and three blank tubes (B1, B2, B3).
  - Tubes mounted on a post at about 1.5 m above ground, attached to bulk precipitation collector pole or within a meteorological enclosure if present.
  - Deployment cycle: 2-week sampling periods; tubes collected, white caps re-fitted before removal.
  - Blanks are carried to site and returned to lab without exposure; stored refrigerated during the sampling period.

- Tube construction, preparation and handling
  - Diffusion tubes consist of stainless steel mesh discs inside plastic tubes with absorbent for NO2.
  - Pre-use cleaning: acid wash, Decon 90 rinse, ultrasonic cleaning for discs; handle with forceps.
  - Absorbent preparation: two dry discs per cap, 30 µL of 10% triethanolamine solution in each cap.
  - Storage: prepared tubes stored refrigerated; freshly prepared diluted absorbent prior to use.

- Analytical procedure (lab)
  - Absorbent analyzed to determine total NO2 absorbed over the sampling period; compute mean NO2 concentration for the period.
  - Reagents for colorimetric analysis prepared fresh; includes sulphanilamide and N-1-Naphthylethylene-diamine dihydrochloride (NEDA).
  - Calibration: stock standards prepared; readings taken at 542 nm against a water blank; results reported as µg NO2 and converted to NO2 concentration (ppb) using tube geometry and exposure duration.
  - Safety: gloves required during analysis; cap removal and handling procedures specified to minimize contamination.

- Data, labeling and metadata standards
  - Key identifiers for each data record:
    - Site Identification Code (e.g., T05)
    - Core Measurement Code (unique code for this core measurement)
    - Location Code (e.g., 01)
    - Sampling/Setting dates and times (GMT, with precise timing)
    - Tube code (E1–E3 for exposed; B1–B3 for blanks)
    - Weight of NO2 collected (µg, reported to 3 sig. figures)
  - Data are collected fortnightly for each site and each of the three exposed and three blank tubes.
  - Data transfer follows ECNCCU data transfer documentation; dataset formats specified in restricted Site Managers’ extranet.
  - A standard field recording form is provided (Appendix II); all data must be traceable to unique site and tube codes.

- Practical notes and references
  - Typical workflow: deploy tubes, maintain field records, collect and transport back to lab the same day for analysis of blanks and exposed tubes.
  - Documentation and references provided for methodology and quality assurance (e.g., Hargreaves 1989; UNEP/WHO 1994).
  - Associated equipment and consumables listed (Gradko International Ltd) and described in Appendix II.

- Outputs and data products
  - Generated NO2 concentrations (ppb) per 2-week sampling period per tube.
  - Data are structured to support spatial analyses and map-based GIS products, with standardized location, timing, and measurement codes to enable aggregation and comparison across sites.