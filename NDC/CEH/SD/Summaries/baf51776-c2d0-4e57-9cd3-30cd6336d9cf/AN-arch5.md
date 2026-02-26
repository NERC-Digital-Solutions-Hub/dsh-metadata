# AN Protocol Aim ATMOSPHERIC CHEMISTRY - NITROGEN DIOXIDE Version 1.1 (previously AC Protocol, updated Jan 2001)

- Purpose and scientific context
  - Detect and define changes in periodic mean atmospheric concentrations of nitrogen dioxide (NO2).
  - NO2 is a key urban pollutant from combustion sources; it affects health and ecosystems and participates in smog and acid rain formation.
  - Uses passive diffusion tubes for low-cost, reliable long-term monitoring; extension to other gases (ammonia, SO2, ozone) is under review but currently not reliably passive.

- Measurement design and field procedures
  - Sampling uses diffusion tubes with NO2 absorbent discs; three active tubes and three blanks per site.
  - Tubes deployed for two weeks; collected and re-sealed for transport to the lab.
  - Locations: three diffusion tubes mounted at 1.5 m above ground, on posts or within a meteorological enclosure if available.
  - Labelling and tracking: unique reference codes combining Site ID, Location Code, Tube Code (E1–E3 for exposed, B1–B3 for blanks), collection date, and sampling time.
  - Tube codes and handling: strict cleaning and preparation protocols for components; samples stored refrigerated and analyzed promptly.

- Core data elements and dataset structure
  - Core measurement code for this protocol: AN (nitrogen dioxide).
  - Required data fields for each sampling occasion:
    - Site Identification Code (unique ECN Site code, e.g., T05).
    - Core Measurement Code (AN).
    - Location Code (e.g., 01) for replicate sampling points at a site.
    - Setting out date and time (GMT, 24‑h clock; time precision 1 minute).
    - Sampling date and time (GMT; time precision 1 minute).
    - Tube Code (E1, E2, E3 for exposed; B1, B2, B3 for blanks).
    - Weight NO2 (micrograms; reported with three significant figures).
  - Data products and interpretation:
    - From the measured NO2 weight and sampling details, compute mean NO2 concentration over the exposure period (ppb) using tube geometry and exposure duration.
    - Experimental tubes provide the NO2 concentration; blank tubes help assess background/contamination.
    - Data are intended for transfer to the ECN database with a unique reference accompanying analytical results.

- Analytical procedure and QA/QC
  - Absorbent analysis yields total NO2 absorbed over the sampling period; convert to mean concentration over that period.
  - Reagents and standards prepared fresh daily; measurements performed by spectrophotometry at 542 nm.
  - QA considerations include handling blanks, replication (triplicate tubes), and proper calibration against standards.
  - Operators must wear gloves during analysis; tubes are rinsed after analysis to avoid cross-contamination.

- Documentation, provenance and data sharing
  - A standard field recording form is provided to ensure consistent data capture (including core identifiers and timing).
  - A dedicated data transfer framework (ECNCCU) governs the dataset format and transfer to the ECN database; contact ECNCCU for access to the data specifications.
  - Clear referencing and coding conventions are required to support data discoverability, traceability, and re-use.

- Appendices and supporting materials (data governance relevance)
  - Appendix I: Analytical reagents and preparation steps for the colorimetric NO2 determination.
  - Appendix II: Equipment details (diffusion tubes, caps, mesh discs, suppliers).
  - These sections document the exact materials and methods needed to reproduce the data generation, important for metadata completeness and reproducibility.

- Practical considerations for data stewards
  - Ensure the presence of four core identifying fields for each data entry (Site ID, Core Measurement Code, Location Code, Sampling Date/Time) and the three replication tube codes (E1–E3, B1–B3).
  - Capture both raw (Weight NO2) and derived (NO2 concentration in ppb) values, plus sampling duration and tube geometry used in calculations.
  - Preserve the linkage between sample data and the accompanying lab analysis (calibration details, reagents, standards) for full provenance.
  - Maintain alignment with the ECN data transfer documentation to facilitate discovery and reuse across systems.