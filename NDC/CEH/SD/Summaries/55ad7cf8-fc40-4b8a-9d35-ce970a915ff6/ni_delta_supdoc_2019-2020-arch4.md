# EIDC Supporting information  
Monthly atmospheric ammonia, acid gas, inorganic aerosols and base cation concentrations from Northern Ireland DELTA gas and aerosol monitoring network, 2019-2020

- Overview
  - Presents monthly atmospheric concentrations of inorganic water-soluble reactive gases and aerosols measured with the UKCEH DELTA® method at four sites in Northern Ireland for 2019 and 2020.
  - Gases: ammonia (NH3), nitric acid (HNO3), sulphur dioxide (SO2). Aerosols: ammonium (NH4+), nitrate (NO3-), sulphate (SO4^2-), chloride (Cl-), sodium (Na+), calcium (Ca2+), magnesium (Mg2+). HONO collection is recorded but not reported.
  - Joint operation by Agri-Food and Bioscience Institute (AFBI) and UK Centre for Ecology & Hydrology (UKCEH); funded by DAERA, Northern Ireland.
  - Data support atmospheric transport modeling and nitrogen/sulphur budgeting for Northern Ireland.

- Data scope and nature
  - Timeframe: 2019 and 2020.
  - Sites: 4 monitoring sites across NI (Hillsborough, Ballynahone, UoU Coleraine, Sandholes).
  - Units: concentrations reported as µg m-3; values are time-integrated monthly averages (exposure period aligned to calendar months ±5 days).
  - Data files: File 1 (2019) and File 2 (2020) with monthly concentration data for the four sites.

- Experimental design and monitoring network
  - DELTA® gas and aerosol monitoring network expands spatial coverage in NI to characterize spatial variability and seasonal trends.
  - Concurrent measurement of gas and aerosol components enables assessment of NH3 with interacting acid gases (HNO3, SO2) and inorganic particulate composition.
  - Data valuable for testing atmospheric transport models and estimating annual budgets of reduced nitrogen (NH3, NH4+) vs oxidised nitrogen (NO3-, HNO3) and sulphur.

- Monitoring sites and DELTA® method
  - Sites and metadata: four NI sites with monthly sampling; coordinates withheld to two decimal places for confidentiality.
  - UKCEH DELTA® method: low-volume diffusion denuder sampling (0.2–0.4 L min-1) with downstream aerosol filters; monthly exposure cycles; gas meter readings to calculate air volume.
  - Sample handling: denuders and filters extracted in deionised water; chemical species analysed by IC, SEAL-AA3, and ICP-OES.
  - Haul and analysis workflow: field sampling by AFBI operators; laboratory analysis at UKCEH Lancaster; data aggregated in an Oracle-based AAGA database and processed through a ShinyApp.

- Ion species and analytical details
  - Gases captured: NH3, HNO3, SO2; additional HONO collected but not reported.
  - Aerosols/particulates captured: NH4+, NO3-, NO3-/Cl- mixture (FPH), NH4+ (FPA), and major cations/ions (Na+, Ca2+, Mg2+).
  - Analytical methods:
    - DC1/DC2: NO3-, SO4^2- by Ion Chromatography (IC)
    - DH: SO4^2-, NO3- by IC
    - DA: NH4+ by SEAL-AA3
    - PT: NH4+, NO3-, SO4^2-, Cl- by IC; Na+, Ca2+, Mg2+ by ICP-OES
    - FPH: NO3-, Cl- by IC
    - FPA: NH4+ by SEAL-AA3
  - Typical limits of detection (per month exposure; ~15 m^3 sampled): NH4+, NO3-, SO4^2-, Cl- (IC/SEAL-AA3); Na+, Ca2+, Mg2+ (ICP-OES); NH3 and related species have explicit LODs listed.

- Data quality and processing
  - Long-standing method linked to AGANet (since 1999); standardised and peer-reviewed.
  - Data management: staged QA pipeline in AAGA with staged flags modeled on EBAS/EMEP conventions.
  - Stage 1: automated QC in AAGA (date overlaps, exposure duration, flow rate checks, outlier rejection, missing samples handling).
  - Stage 2: manual review (laboratory blanks, ion balance checks, sampling malfunctions, outliers review, data invalidation when appropriate).
  - Stage 3: expert/project manager review (site knowledge, expected concentrations/trends, cross-site/year comparisons, gas-vs-aerosol relationships, episode impacts).
  - Output: final ratified dataset with time-stamped, versioned files and a status of Ratified.

- Data structure and content
  - Each row corresponds to one month of data for a single site.
  - Key fields (examples): site_id, site_name, network_id (AFBI), parameter_id (e.g., delta_NH3_g, a_NH4_p, etc.), measurement_start_date/time, measurement_end_date/time, measurement value (µg m-3), below-LOD flag, verification_id, unit_id (µg m-3), data_capture, validity_id, EMEP_code, month, year, comments.
  - Data flags: EBAS/EMEP-style flags categorize data as valid, provisional, missing, suspected issues, or specific mechanical/chemical problems.
  - Ratified data: produced from AAGA in a standard template, time-stamped with version control.

- Access and references
  - Data and flags align with EBAS/EMEP standards; flags list available at the EBAS/NILU flags portal.
  - Supporting resources and network information:
    - AGANet: UK-air Defra network page
    - NAMN/ALPHA and DELTA protocols: NI NH3 monitoring networks
    - EBAS flags: NILU project flags page

- Key takeaway for data leadership
  - The document describes a robust, quality-controlled data pipeline for high-value atmospheric chemistry data across NI, spanning 2019–2020, with clearly defined methodologies, data structures, QA stages, and standardized flagging to enable reliable data provisioning for modelling, policy support, and cross-network collaboration.