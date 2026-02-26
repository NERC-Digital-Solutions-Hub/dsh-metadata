# AN Protocol ATMOSPHERIC CHEMISTRY - NITROGEN DIOXIDE Version 1.1 (previously AC Protocol, updated Jan 2001)

## Aim
- Detect and define changes in periodic mean atmospheric concentrations of nitrogen dioxide (NO2).
- Emphasize NO2 due to health and ecosystem effects; NO is a precursor; major urban sources include vehicle exhaust, power generation, heating, and industry.
- Use diffusion tubes as a low-cost, well-researched passive method; replicate tubes to account for individual tube variation; monitor long-term trends.

## Measurement Method and Data Generation
- Method: passive diffusion tubes with NO2 absorbent; replicate three experimental tubes and three blanks per site.
- Data outputs: mean NO2 concentrations over sampling periods, with linkage to site and sampling metadata.
- Scope for extension: consideration to include other gases, but currently no reliably passive methods.

## Sampling Protocol and Location
- Placement: three diffusion tubes per site mounted at 1.5 m above ground; can be attached to bulk precipitation collector pole or a post; siting inside a meteorological enclosure if available.
- Deployment and collection: tubes deployed for two weeks; collected, caps replaced, and blanks handled identically but not exposed.
- Labeling and identification: each tube coded E1–E3 (exposed) or B1–B3 (blank); site code examples (e.g., Moor House 04); location code (01); sampling date (e.g., 01-Jan-1996). Unique reference accompanies analytical results for ECN database transfer.

## Analytical Procedure and Reagents
- Analytical approach: colorimetric determination of NO2 absorbed on discs; absorbance read at 542 nm against a water blank.
- Reagents and safety: use AR grade chemicals; sulphanilamide and N-1-naphthylethylene-diamine dihydrochloride (NEDA); hazardous materials with required handling (gloves, refrigeration, safe disposal).
- Calculation: convert absorbance to NO2 mass (µg) via calibration; NO2 concentration in ppb calculated from exposure time, tube geometry, and recovered NO2.
- Quality controls: fresh preparation of reagents daily; standard curves prepared each day; blanks and exposed tubes analyzed together.

## Equipment and Materials (Appendices)
- Appendix I: Detailed reagents, standard preparations, and step-by-step procedure for analysis.
- Appendix II: Equipment specifics, including discs, diffusion tubes, caps, and supplier details.

## Data Management, Metadata, and Recording Conventions
- Core dataset requirements: accurate temporal and spatial identifiers plus tube-specific data.
- Core variables (fortnightly per site): 
  - Site Identification Code (unique ECN site code)
  - Core Measurement Code (e.g., PC for this core measurement)
  - Location Code (replicate position)
  - Setting out date/time (GMT, to 1-minute precision)
  - Sampling date/time (GMT, to 1-minute precision)
  - Tube code (E1/E2/E3 or B1/B2/B3)
  - Weight NO2 (µg, 3 s.f.)
- Data transfer: datasets conform to ECN database formats; documentation available via restricted ECN extranet; contact ECNCCU for access.
- Recording forms: standard field forms provided; explicit guidance on coding and data capture.

## Quality Assurance and Challenges for Data Leaders
- Replication and blanks help quantify tube-to-tube variability and data reliability.
- Data governance: ensure consistent metadata, proper dataset formats, and traceability from field to ECN database.
- Potential expansion: assess feasibility of adding other pollutants; current passive methods for some gases are not yet acceptably reliable.
- Operational considerations: careful cleaning, storage of tubes and reagents, and rigorous labeling to maintain data integrity across sites and sampling periods.