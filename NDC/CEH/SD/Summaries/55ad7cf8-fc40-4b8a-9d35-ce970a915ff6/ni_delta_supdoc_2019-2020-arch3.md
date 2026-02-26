# EIDC Supporting information
Monthly atmospheric ammonia, acid gas, inorganic aerosols and base cation concentrations from Northern Ireland DELTA gas and aerosol monitoring network, 2019-2020

- The document describes two data files (2019 and 2020) from the Northern Ireland DELTA® Gas and Aerosol Monitoring Network, covering monthly concentrations of inorganic, water-soluble reactive gases and aerosols at four NI sites.
- Gases measured: ammonia (NH3), nitric acid (HNO3), sulfur dioxide (SO2).
- Aerosols measured: ammonium (NH4+), nitrate (NO3-), sulfate (SO4 2-), chloride (Cl-), sodium (Na+), calcium (Ca2+), magnesium (Mg2+).
- The network was operated by AFBI and UKCEH, funded by DAERA NI.

- Purpose and relevance
  - Provides data to test atmospheric transport models and estimate annual budgets of reduced (NH3/NH4+) vs oxidised nitrogen (HNO3/NO3-) and sulfur (SO2/SO4 2-).
  - Aids understanding of spatial variability and seasonal trends in NI, facilitating assessment of NH3 interactions with acid gases and inorganic particulate matter.

- Experimental design and monitoring sites
  - DELTA® gas and aerosol method used with four NI sites (AFBI25 Hillsborough, AFBI26 Ballynahone, AFBI27 UoU Coleraine, AFBI28 Sandholes).
  - Sampling: monthly, continuous time-integrated sampling; site coordinates reported with limited precision for confidentiality.
  - DELTA® system: low-volume diffusion denuder for reactive gases and downstream aerosol filters; sampling rate 0.2–0.4 L min-1; monthly gas meter readings to compute concentrations (µg m-3).

- UKCEH DELTA® method overview
  - Selective removal of gases on denuders; aerosols collected on filters.
  - Analyzed species and analytical methods (IC, SEAL-AA3, ICP-OES) for various components.
  - Typical detection limits provided (per month exposure, volume 15 m3).

- Data collection, processing and quality control
  - Data stored in an Oracle-based AAGA database; automated calculation of concentrations via a ShinyApp.
  - Multi-stage QC process:
    - Stage 1: automated checks (date overlaps, exposure duration, flow rate consistency, outlier rejection, missing samples).
    - Stage 2: manual data checks (laboratory blanks, ion balance, sampling malfunctions, outliers, data validity).
    - Stage 3: expert/project manager review considering site knowledge, expected trends, inter-site comparisons, and gas–aerosol relationships.
  - Ratified outputs produced with time-stamping and version control.

- Data structure and content
  - Each dataset row represents one month of data for a single site.
  - Key fields include site_id, site_name, network_id (AFBI), parameter_id (e.g., NH3_g, a_NO3_p), measurement_start/end dates and times, measured concentration, unit (µg m-3), detection flags, data_capture status, validity, and EMEP codes.
  - Reported concentrations are time-integrated averages in µg m-3; values may be flagged for detection limits or data quality.

- Data flags and governance
  - Data flags follow EBAS/EMEP conventions (valid, invalid, missing; multiple flag groups for mechanical, chemical, extreme values, etc.).
  - Flags cover issues such as instrument problems, sampling anomalies, contamination, coating errors, flow deviations, and outliers.
  - Flag system supports data provenance, traceability, and harmonization with other European networks.
  - Data are prepared for submission to EBAS; site coordinates and metadata are structured for consistency and comparability across networks.

- Implications for Monitoring Frameworks
  - Demonstrates a robust, multi-layer data governance approach: defined sampling protocol, standardized analytical methods, structured QC, and transparent flagging.
  - Highlights the importance of metadata completeness, data versioning, and public sharing of underlying data to support policy scrutiny and decision-making.
  - Provides a concrete example of aligning field measurements (NH3, HNO3, SO2, inorganic aerosols) with modeling needs and nutrient/atmospheric deposition budgets.

- References and resources
  - EN 17346: ambient air – diffusion sampler method for ammonia.
  - EBAS/NILU data flags and UK-AIR network flag conventions.
  - DELTA method and AGANet/NAMN documentation for context and harmonization.