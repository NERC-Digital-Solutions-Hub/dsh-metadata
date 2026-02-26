# Monthly atmospheric ammonia, acid gas, inorganic aerosols and base cation concentrations from Northern Ireland DELTA gas and aerosol monitoring network, 2019-2020

- Overview
  - Describes monthly atmospheric concentrations of inorganic, water-soluble gases and aerosols measured with the UKCEH DELTA® method at four sites across Northern Ireland for 2019 and 2020.
  - Target species: gases — ammonia (NH3), nitric acid (HNO3), sulfur dioxide (SO2); aerosols — ammonium (NH4+), nitrate (NO3−), sulfate (SO4^2−), chloride (Cl−), sodium (Na+), calcium (Ca^2+), magnesium (Mg^2+).
  - Network jointly operated by AFBI and UKCEH; funded by DAERA.

- Experimental design and monitoring purpose
  - DELTA® network expands NI spatial coverage to study spatial variability and seasonal trends; enables concurrent gas and aerosol measurements to assess relationships (e.g., NH3 with interacting acid gases).
  - Datasets support testing atmospheric transport models and estimating annual budgets of reduced vs oxidised nitrogen and of sulfur.

- Monitoring sites
  - Four NI sites (with confidential coordinates reported to two decimals):
    - Hillsborough (AFBI25) — start 05/03/2019
    - Ballynahone (AFBI26) — start 07/03/2019
    - Coleraine (UoU) AFBI27 — start 06/03/2019
    - Sandholes (AFBI28) — start 07/03/2019
  - Inlet height: 1.5 m
  - Site information includes latitude/longitude and site identifiers; exact coordinates are withheld at full precision.

- UKCEH DELTA® method and sampling regime
  - Low-volume diffusion denuder system for long-term monitoring of NH3, HNO3, SO2 and related aerosols.
  - Sampling rate: 0.2–0.4 L min−1; monthly integrated sampling with time-referenced exposure periods.
  - Sample handling: monthly site visits for sample exchange; gas meter readings record sampled air volume for concentration calculations.
  - Sample processing: denuders and filters extracted in deionised water; analysis performed at UKCEH Lancaster lab.

- Analytical methods and species
  - Gases (DC1+DC2): NO3−, SO4^2− via IC; NH3 via SEAL-AA3; HNO3 and SO2 represented in various denuder arrangements (DC1+DC2, DH, DA, etc.).
  - Particles/aerosols (PT, FPH, FPA): NH4+, NO3−, SO4^2−, Cl−; Na+, Ca2+, Mg2+ via IC and ICP-OES; NH4+ also measured by SEAL-AA3 in some extracts.
  - Typical limits of detection (LOD) provided per ion for monthly (volume 15 m^3) exposure.

- Nature and units of recorded values
  - Concentrations are time-integrated averages expressed in µg m−3.
  - Calculated from measured mass divided by sampled air volume (gas meter readings).
  - Data include flags indicating detection limits and data quality.

- Data structure and contents
  - Each row corresponds to one site, one month, and one parameter, with fields including:
    - site_id, site_name, network_id (AFBI)
    - parameter_id (e.g., delta_NH3_g, a_NH4_p, etc.)
    - measurement_start_date/time and end_date/time
    - measurement (µg m−3)
    - Less_than flag (LOD indicator)
    - verification_id, Unit_id (µg m−3)
    - Data_capture (0 missing/rejected, 100 accepted)
    - Validity_id (1 valid, -1 invalid)
    - EMEP_code (data status flags)
    - MONTH, YEAR, Comments
  - Ratified outputs are time-stamped, versioned, and finalized after review.

- Data processing, quality control, and ratification
  - Data stored in an Oracle-based AAGA database; automated and manual processing via a ShinyApp.
  - Three-stage quality control:
    - Stage 1: Automated QC with EBAS/EMEP flags (date overlaps, exposure duration, flow rate checks, outliers, missing samples).
    - Stage 2: Manual review and flagging (laboratory blanks, ion balance checks, sampling malfunctions, outliers both low and high, data validity).
    - Stage 3: Expert/project manager review considering site context, expected trends, cross-site comparability, and gas-aerosol relationships.
  - Final output is a time-stamped, versioned, “Ratified” dataset with all values and appropriate flags.

- Data flags and interpretation
  - Uses EBAS/EMEP flag system (groups 0–9) for data status, including:
    - Missing data, unspecified reasons, contamination, instrumental or sampling anomalies, incorrect coatings or analyses, and data outside expected ranges.
    - Examples include: missing data (799, 798, 999), sampling period anomalies (653, 654), instrument or flow issues (663, 664, 666), contamination or coating issues (591, 534), and corrected or accepted irregular data (110, 111, 147, etc.).
  - Flags are harmonised with European monitoring standards to support cross-network data sharing.

- Data governance and references
  - Supporting information aligned with AGANet and NAMN protocols; long-standing methodological basis (since 1999 for AGANet).
  - References and EBAS flag resources provided for data submission and flag interpretations.
  - Resource locators available for network information, NAMN/ALPHA DELTA protocols, and EBAS flag definitions.

- Relevance and usage
  - Provides robust, quality-assured monthly concentrations of ammonia, acid gases, and inorganic aerosols for NI.
  - Supports atmospheric transport modeling, nitrogen and sulfur budgets, and intercomparison with co-located networks (e.g., NAMN/ALPHA).
  - Data ready for analysis in policy-relevant air quality and environmental assessments.