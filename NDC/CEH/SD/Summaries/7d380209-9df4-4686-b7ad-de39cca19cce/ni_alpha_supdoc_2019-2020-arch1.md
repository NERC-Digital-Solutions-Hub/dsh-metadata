# Monthly atmospheric ammonia concentration data from Northern Ireland ALPHA ® Ammonia Monitoring Network, 2019-2020

- Purpose and context
  - Provides monthly atmospheric NH3 concentrations from 25 NI ALPHA® sites for 2019 and 2020.
  - Data used for model validation and calibration of modeled NH3 concentrations (e.g., FRAME) and for deriving UK nitrogen deposition estimates via CBED.
  - Aims to increase confidence and reduce uncertainty in NH3 modelling to assess policy scenario impacts.
  - Includes co-located ALPHA® and DELTA® measurements at one site to enable inter-comparison.
  - NH3 data contribute to validating emissions inventories and understanding local vs. background emissions across NI.

- Experimental design and network scope
  - ALPHA® network expands spatial coverage across Northern Ireland to improve spatio-temporal NH3 data.
  - UK NAMN long-term context provides three NI sites; the 25 ALPHA® sites were chosen to broaden coverage.
  - Monitoring is monthly with time-integrated sampling over each period.
  - DELTA® sampling at four NI sites supplements NH3 data and is reported in a companion submission.
  - Hillsborough site specifically included to evaluate local farm emission sources.

- Monitoring sites and sampling method
  - 25 ALPHA® sites (24 rural, 1 urban) across NI, data by AFBI and UKCEH.
  - Site details include site name, start dates from Feb–Mar 2019, ongoing end dates, coordinates (reported to 2 decimal places for confidentiality).
  - Sampling method: UKCEH ALPHA® high-sensitivity passive samplers (citric acid-coated filters) deployed at ~1.5 m height.
  - Monthly sampling with time-integrated exposure; samples exchanged by trained local operators.

- ALPHA® method specifics and measurements
  - NH3 concentration (µg NH3 m-3) derived from NH4+ on filters, scaled by air volume sampled (m3) using annual uptake rate (m3 h-1).
  - Uptake rates used: 0.0031665 m3 h-1 (2019) and 0.0031277 m3 h-1 (2020).
  - Limit of detection (LOD) set at 0.03 µg NH3 m-3 for monthly exposures.
  - Analysis performed by UKCEH Lancaster lab; NH4+ measured colorimetrically (modified salicylate).

- Data handling, quality control, and processing
  - Data managed in an Oracle-based database (AAGA) with a ShinyApp for NH3 concentration calculations.
  - Multi-stage QA/QC protocol:
    - Stage 1: Automated QC by UKCEH (auto-flagging per EBAS/EMEP flags), including date overlaps, sampling duration flags, replicate precision (CV > 15% flagged), outlier handling, and missing samples (-9999 or -1 flags).
    - Stage 2: Manual review of monthly blanks, sampling malfunctions, outliers (low or high), and corrective actions; invalid data flagged accordingly.
    - Stage 3: Expert/project manager review considering site knowledge, modelling expectations, seasonal patterns, and cross-site comparisons; final “Ratified” output with timestamp and versioning.
  - Data outputs are time-stamped with version control; final ratified dataset contains all values with appropriate flags.

- Data structure and contents
  - Each row corresponds to one month of data for a single site.
  - Key fields include: site_id, site_name, network_id (AFBI), parameter_id (alpha_NH3_g), measurement_start_date/time, measurement_end_date/time, measurement (NH3 concentration in µg m-3), Less_than flag (LOD), verification_id, Unit_id (µg m-3), Data_capture, Validity_id, EMEP_code, Month, Year, and Comments.
  - Data are time-integrated monthly averages of NH3 concentrations.

- Data flags and compatibility
  - Uses EMEP data flags grouped into three categories: V (Valid), I (Invalid), M (Missing).
  - Flags cover issues such as missing data, contamination, instrument/flow problems, sampling and lab issues, and estimates.
  - Co-located DELTA data and cross-checks with other NI projects help support data validity.
  - Confidentiality: site coordinates are reported with limited precision (two decimals).

- Related resources and references
  - Data submission and flag handling align with EBAS/EMEP standards; flags and documentation available via NILU project resources.
  - Supporting information links include NAMN, FRAME modelling, CBED deposition, EBAS flag lists, and EN 17346 (2020) standard for diffusive NH3 samplers.
  - References provide methodological validation and context for diffusive samplers and NH3 modelling.

- Output and usage
  - Final ratified NH3 concentration dataset suitable for model validation and deposition modelling, inter-site comparisons, and assessing policy scenario impacts on NH3.
  - Data are designed to be discoverable and usable within UK air-quality modelling frameworks and cross-network harmonisation efforts.