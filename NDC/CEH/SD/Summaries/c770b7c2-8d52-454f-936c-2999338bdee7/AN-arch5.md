# AN Protocol ATMOSPHERIC CHEMISTRY - NITROGEN DIOXIDE Version 1.1 (previously AC Protocol, updated Jan 2001)

- Purpose
  - Detect and define changes in periodic mean atmospheric concentrations of nitrogen dioxide (NO2).
  - Focus on NO2 due to health and ecosystem effects; NO and NO2 originate from natural and man-made NOx sources.
  - Use passive diffusion tubes as the measurement method; low capital cost, no on-site power, replicates needed due to tube variation.

- Measurement method and sampling design
  - Diffusion tubes: stainless steel mesh discs absorbent in a plastic tube; prepared as specified or using ready-made tubes/discs.
  - Deployment: three diffusion tubes (experimental) and three blanks mounted in clips at about 1.5 m above ground, near a meteorological enclosure if available.
  - Sampling interval: two weeks per sampling period.
  - Handling: white caps removed before deployment; tubes collected after two weeks; caps re-fitted prior to removal; blanks transported to site but not exposed.
  - Location and setup: tubes attached to bulk precipitation collector pole or a post; ensure consistent siting and enclosure when applicable.

- Data labeling and identifiers
  - Unique labelling scheme for each tube: experimental tubes E1, E2, E3; blanks B1, B2, B3.
  - Site and location codes, sampling date, and a unique reference code must accompany analytical results for transfer to the ECN database.
  - Example coding: ECN Site ID, ECN Site Code (e.g., Moor House 04), Location Code (01), tube code, sampling date (e.g., 01-Jan-1996).

- Analytical procedure and quality control
  - Absorbent analysis provides total NO2 absorption over the sampling period; calculate mean NO2 concentration for that period.
  - Laboratory protocol requires gloves, specific reagents, and fresh preparation of reagents each day.
  - Colorimetric determination using sulphanilamide, N-1-naphthylethylene-diamine dihydrochloride (NEDA), and reagents X and Y; absorbance read at 542 nm.
  - Calibration: prepare working standards daily; construct calibration curve to report NO2 mass (µg) and convert to NO2 concentration (ppb) based on exposure time and tube geometry.
  - File and store: samples and standards prepared and analyzed with strict handling; maintain refrigerated storage for samples; ensure analyte integrity.

- Data structure and recording conventions
  - Core measurement: atmospheric chemistry - nitrogen dioxide (AN Protocol).
  - Required core fields for each sampling occasion (fortnightly per site): 
    - Site Identification Code (e.g., T05)
    - Core Measurement Code (e.g., PC)
    - Location Code (e.g., 01)
    - Setting out date and time (GMT)
    - Sampling date and time (GMT)
    - Tube code (e.g., E1, E2, E3, B1, B2, B3)
    - Weight NO2 (units in micrograms, reported to three significant figures)
  - Data formats: reference to ECNCCU data transfer documentation and restricted-extranet site managers’ documentation for ECN dataset formats; data transfer includes a unique combination of site, measurement, location, and timestamp.

- Documentation, forms, and equipment
  - Standard field recording form available from CCU (example provided in Appendix II).
  - Appendix I describes analytical reagents and preparation steps; Appendix II lists equipment details (diffusion tubes, colored and clear caps, mesh discs, supplier details).
  - Reagents and stock solutions prepared freshly; use of gloves; follow safety notes for harmful reagents.

- Data governance and stewardship considerations
  - Data stewardship tasks aligned with dataset usability: ensure appropriate metadata, consistent coding (Site, Core Measurement, Location), and precise timing information for discoverability and reuse.
  - Ensure up-to-date dataset formats and transfer documentation for interoperability and long-term preservation.
  - Maintain traceability from field deployment through laboratory analysis to final NO2 concentration results; preserve the association between tube codes, sampling events, and analytical outcomes.
  - Coordinate with ECN Central Coordination Unit (CCU) for data standards, transfer procedures, and contact (ecnccu@ceh.ac.uk) to obtain access to data formats and additional documentation.

- Scope of applicability
  - Currently focused on NO2 measurement using diffusion tubes; consideration of extending ECN programmes to ammonia, SO2, and ozone has been reviewed, but no reliably passive methods established at present.