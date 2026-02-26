# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- Purpose and scope
  - Comprehensive metadata and data dictionary for dissolved chemical concentrations in water samples collected at multiple sites within a catchment.
  - Documents pre-concentration and analysis procedures intended to improve detection limits prior to analytical measurement.

- Analyte coverage and data structure
  - Wide range of inorganic and some organic species (e.g., Aluminium, Ammonium, Arsenic, Boron, Bromide/Br, Cadmium, Caesium, Calcium, Cerium, Chloride, Chromium, Cobalt, Conductivity, Copper, Dissolved Organic Carbon, DON, Fluoride, Nitrogen species (Nitrate, Nitrite, Ammonium, Total Dissolved Nitrogen), Iodine, Iron, Lanthanum, Lead, Lithium, Magnesium, Manganese, Molybdenum, Nickel, Nitrate/Nitrite, Orthophosphate, Phosphorus, pH, Potassium, Praseodymium, Rubidium, Scandium, Selenium, Silicon, Sodium, Strontium, Sulfate, Sulfate by ICP, Sulfur, Temperature, Tin, Titanium, Uranium, Vanadium, Yttrium, Zinc, etc.).
  - For each analyte: DETERMINAND, FORM (mostly Dissolved), UNITS (ug/l, mg/l, mg/l-N, etc.), LQDC (limit of quantification), QUOTE TO, START/END dates, LOCATION OF ANALYSIS, ANALYTICAL METHOD QC DATA QUALIFIER, FILTRATION, PRESERVATION, METHOD, and DETECTION LIMIT NOTES.
  - Multiple analysis laboratories referenced (e.g., Wallingford, Lancaster, Staylittle, Bangor, Lancaster, etc.) with detailed method descriptions per analyte.

- Pre-concentration, preservation, and analytical methods
  - Pre-concentration approaches include evaporation of filtered samples (IR or hot plate) followed by dilution to form a concentrated solution (often 20-fold).
  - Preservation typically involves concentration in nitric acid to 1% and cooling; some elements preserved by specific solutions or storage conditions.
  - Filtration generally uses 0.45 μm membranes; field filtration details often specify rain and cloud conditions.
  - Analytical techniques span ICP-OES, ICP-MS, Ion Chromatography (IC), Automated Colorimetry, Atomic Absorption (AAS), and colorimetric/TOC methods for carbon species.
  - Some compounds measured in alternative ways (e.g., dissolved organic carbon via TOC analyzer, DON by calculation, total dissolved sulfur by ICP with re-expression as SO4).

- Data quality and QC framework
  - Analytical Method QC Codes (examples): 
    - 1–6 indicate instrument and method validation specifics, ISO/ILE accreditation status, and inter-laboratory proficiency context.
    - 7–9 provide time/date and site-related references.
  - Data Qualifier Codes (examples): 
    - 10: Raw instrument data, not yet rounded.
    - 11–17: Various data quality flags including detection-limit related flags, method changes, timing inconsistencies, and data corrections.
  - Some data are flagged to reflect ISO 17025 accreditation status, interlaboratory proficiency, or potential data issues (e.g., poor sensitivity during method changes, raw patterns needing caution).

- Sampling framework and time conventions
  - Sample types:
    - Stream and borehole: grab samples at recorded collection times.
    - Input samples (Rainfall, Throughfall, Stemflow, Cloud): time-integrated samples with sampling intervals defined by the period since the previous collection.
  - Volume-weighted sampling time
    - A volume-weighted approach is used to determine Year mean sampling and to align temporal interpretation when precipitation and runoff timing is critical.
    - Calculations take into account rainfall weighting from automatic weather stations (AWS) and interpolate when data gaps occur.
  - Time stamps
    - All samples are timestamped at collection time; in cases where time is missing, an assumption (often 10:00 am) is used per documentation.
  - Sampling period and data interpretation
    - For input samples, the sampling period is the interval between successive sample collection times; for stream samples, the sampling time is the interval used in ratio calculations.
    - The dataset notes potential overestimation in hourly rainfall flux due to averaging and correlation with rainfall intensity.

- Site and catchment context for runoff calculations
  - Site codes and catchment areas (approximate):
    - Lower Hore (A): 3.172 km²
    - Upper Hore (D): 1.62 km²
    - Tanllwyth (K): 0.916 km²
    - Lower Hafren (B): 3.58 km²
    - Upper Hafren (G): 1.22 km²
  - Conversion guidance:
    - From cumecs to mm/15 min: mm/15min = cumecs × 0.9 / catchment area (km²)
    - From mm/15min (flow) to cumecs: cumecs = (mm/15min) × catchment area / 0.9
  - Sampling times and data interpretation emphasize the use of volume-weighted time bases for precipitation-runoff correlations.

- Data organization and accessibility
  - Data are organized by analyte with detailed metadata per analyte (start/end dates, location of analysis, analytical method QC qualifiers, filtration, preservation, concentration technique, etc.).
  - The dataset provides explicit guidance on when sampling times should be used for calculating state variables like year mean sampling and area-weighted runoff, and how to interpret special samples (e.g., cloud catch, throughfall, hourly fluxes).

- Practical implications for analysts
  - The dataset supports robust trend analysis and correlation studies by providing:
    - Rich, multi-site, long-term time series of dissolved species.
    - Standardized pre-concentration and filtration protocols to harmonize detection limits.
    - Transparent QC and data-flagging framework to assess data reliability.
    - Explicit conversion rules to translate hydrological measurements (flow, rainfall) into area-weighted environmental flux metrics.

- Summary of key conventions to apply
  - Always consider volume-weighted sampling times for precipitation/runoff coupling.
  - Use documented start/end dates to determine the applicable analysis method and QC flags for each analyte.
  - Apply the specified filtration and preservation rules when preparing or interpreting data.
  - Use site catchment areas and the provided conversion equations to translate flow data into rainfall-runoff metrics.

- Note on data provenance and integrity
  - The metadata acknowledges multiple laboratories and varying analytical approaches over time.
  - QC codes reflect method accreditation status and known data caveats, guiding cautious interpretation where method changes or data gaps occurred.