# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- Purpose: Metadata describing analytical data collected from multiple samples (primarily water chemistry) with pre-concentration steps to enhance detection limits.
- Scope: Includes numerous chemical species (metals, anions, nutrients, and related parameters) measured over extended time ranges, with detailed method, preservation, filtration, and pre-concentration information.

## Data content and structure

- Analytes and fields
  - For each chemical/species (e.g., Aluminium, Ammonium, Antimony, Arsenic, Barium, Beryllium, Boron, Bromide/Br, Cadmium, Cesium, Calcium, Cerium, Chloride, Chromium, Cobalt, Conductivity, Copper, Dissolved Organic Carbon, Don’t, etc.)
  - Each entry includes: FORM (e.g., Dissolved), DETERMINAND (element/ion), UNITS (e.g., ug/l, mg/l), LQDC (lower quantification/decision limit), QUOTE TO (target detection or reporting limit), START and END dates, ANALYSIS (laboratory), METHOD (analytical technique), QC QUALIFIER, FILTRATION details, PRESERVATION, and notes.
- Data sections
  - LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE: Primary data field definitions and attributes per analyte.
  - LOCATION OF ANALYTICAL DATA: Parallel metadata for analytical data without explicit pre-concentration context (structure mirrored for consistency).
- Temporal coverage
  - Records span from early 1980s to 2007 (dates indicate sampling periods, and some are ongoing/contiguous).
- Methods and QA
  - Analytical methods include optical emission spectroscopy (ICP-OES), mass spectrometry (ICP-MS), ion chromatography, automated colorimetry, etc.
  - Filtration: typically 10–47 mm membranes (GF/C, 0.45 µm), with field or lab processing notes.
  - Preservation: various, including acidification (usually to 1% nitric acid) and refrigeration; some samples undergo pre-concentration (evaporation and dilution) prior to analysis.
  - QC qualifiers: codes indicate instrument type (ICP-OES vs ICP-MS), interlaboratory checks, ISO/ISO17025 alignment, and data integrity notes.

## Data quality and QC

- Analytical Method QC Codes
  - Codes 1–9 describe how accuracy and proficiency checks were performed (e.g., interlaboratory schemes, ISO accreditation, instrument specifics).
- Data Qualifier Codes
  - Codes 10–17 flag data quality concerns, such as raw instrument data, detection-limit issues, method changes, time-sampling inconsistencies, and data treated with caution.
- Implications for use
  - Some data may be raw, have detection-limit-related uncertainties, or reflect method changes over time; consult qualifiers to assess suitability for trend analysis or comparisons.

## Sampling and timing

- Sampling types and timestamps
  - Samples labeled as “stream” or “borehole” are grab samples at the stated time.
  - “Input” samples (Rainfall, Throughfall, Stemflow, Cloud) are time-integrated, with periods defined by intervals between successive collections.
- Volume-weighted sampling time
  - A volume-weighted scheme is used to derive sampling times for precipitation-related inputs, using hourly rainfall data from local AWS stations; if data gaps exist, alternate stations are used, or the interval mean is assumed.
  - The “Year mean sampling” is calculated from this volume-weighted time base to reflect representative annual sampling.
- Time stamping recommendations
  - The dataset provides instructions to use volume-weighted times rather than raw timestamps when the timing of precipitation relative to runoff is critical.
  - For some entries, sampling times may be adjusted or averaged where gaps exist; guidelines are provided for handling missing times (e.g., default to 10:00 am when not recorded).

## Flow and runoff conversion

- Site and catchment information
  - Site names and catchment areas are specified (e.g., Lower Hore, Upper Hore, Tanllwyth, Lower Hafren, Upper Hafren) with corresponding catchment areas in square kilometers.
- Conversion formulas
  - Convert flow (cumecs) to area-weighted runoff (mm/15 min): mm/15min = cumecs × 0.9 / catchment area (km^2).
  - Convert area-weighted runoff (mm/15 min) to cumecs: cumecs = mm/15min × catchment area / 0.9.
- Purpose
  - Enables combining discharge/flow data with concentration data to derive area-weighted mass fluxes and related metrics.

## Key interpretation notes for data support

- Data organization
  - The dataset is designed for self-service exploration, enabling users to join concentration data with flow/runoff data, timing metadata, and QC flags.
- Units and reporting
  - Concentrations are expressed with specified units (ug/l, mg/l, etc.), and lower quantification limits (LQDC) guide interpretation near detection thresholds.
- Pre-concentration and preservation
  - Pre-concentration steps (e.g., evaporation and dilution) are explicitly documented per analyte, affecting detection limits and comparison across time periods.
- Documentation of sampling cadence
  - The document provides explicit guidance on how to treat input samples versus grab samples and how to handle time integration in analyses.
- Data provenance and reliability
  - The QC codes and notes emphasize traceability to proficiency schemes and ISO-accreditation status, aiding users in assessing data reliability for reporting or regulatory use.