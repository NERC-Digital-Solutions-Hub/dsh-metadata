# AN Protocol

- Aim and context
  - Detect and define changes in periodic mean atmospheric concentrations of nitrogen dioxide (NO2).
  - NO2 is a key pollutant from urban combustion sources with health and ecosystem implications; NO is the precursor.
  - Current method uses passive diffusion tubes; extension to other gases (ammonia, SO2, ozone) is under review but none are currently reliably measured with passive methods.

- Measurement approach
  - Use diffusion tubes with NO2 absorbent discs; replicate tubes to account for tube-to-tube variation.
  - Three diffusion tubes per sampling location (E1–E3) and three blanks (B1–B3).
  - Sampling cadence: two-week exposure periods.
  - Height and placement: mounted in clips at about 1.5 m above ground; location near bulk precipitation collector or in a meteorological enclosure if present.
  - Deployment protocol: remove white cap before deployment; collect after two weeks; re-fit white caps after collection; blanks prepared and transported identically but not exposed.
  - Data coding: unique site and sample identifiers; essential dataset fields described below.

- Field equipment and preparation
  - Diffusion tube components: stainless steel mesh discs (1 cm diameter) with NO2 absorbent, plastic tubes, coloured and clear caps.
  - Cleaning and assembly: rigorous cleaning (acid wash, Decon 90, rinsing); handle discs with forceps; prepare as per protocol.
  - Storage: prepared tubes stored refrigerated; fresh absorbent mixture prepared just before use.

- Analytical procedure (Appendix I)
  - Analytical approach: measure total NO2 absorbed over the sampling period; convert to mean NO2 concentration.
  - Reagents and Hazards: sulphanilamide, N-1-naphthylethylene-diamine dihydrochloride (NEDA); prepare daily reagents and standards with specified stock solutions.
  - Procedure: reagents Y for samples and X for standards; develop colorimetric response; measure absorbance at 542 nm against a water blank; calculate NO2 weight from calibration and convert to ppb using diffusion tube geometry and exposure time.
  - Sample handling: operator must wear gloves; rinse diffusion tubes after analysis to avoid cross-contamination.

- Data handling and recording conventions
  - Core measurement code for this protocol: AN (atmospheric chemistry - nitrogen dioxide).
  - Required dataset fields (fortnightly for each location, three exposed tubes and three blanks):
    - Site Identification Code (unique ECN site)
    - Core Measurement Code (AN)
    - Location Code (replicate 01…)
    - Setting out date and time (GMT)
    - Sampling date and time (GMT), with appropriate precision
    - Tube code (E1, E2, E3 for exposed; B1, B2, B3 for blanks)
    - Weight NO2 (µg) per tube, reported with three significant figures
  - Data transfer: dataset formats are specified in ECNCCU data transfer documentation; data to be stored with metadata and made discoverable via ECN databases; contact ecnccu@ceh.ac.uk for access.

- Documentation, QA, and replication
  - Field recording form provided (Appendix II); ensures consistent capture of all sampling events and tube identifiers.
  - Experimental tubes and blanks are used to assess background and methodological variability; replication is essential for robust meanNO2 estimation.

- Appendix II: Equipment details
  - Detailed listing of discs, diffusion tubes, and caps; supplier information for materials used in field deployment and analysis.

- Practical notes and cautions
  - Analytical chemicals are hazardous; follow safety and storage requirements.
  - Strict labeling and coding are required to ensure traceability from field to ECN database.
  - The protocol acknowledges potential extension to other pollutants but notes lack of reliable passive methods for ammonia, SO2, and ozone at present.