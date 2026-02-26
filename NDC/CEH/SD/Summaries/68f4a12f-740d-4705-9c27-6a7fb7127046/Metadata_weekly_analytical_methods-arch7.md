# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- Overview
  - Comprehensive metadata for environmental chemical analyses, spanning numerous analytes (e.g., Aluminium, Ammonium, Chloride, Chromium, Iron, Lead, Nitrogen forms, Sulphate, Zinc, etc.) across water, rainfall, cloudwater, and related inputs.
  - Data traceable to sampling sites and times, with pre-concentration and analysis details (lab, method, preservation, filtration) to support GIS-based mapping and time-series visualizations.
  - Includes pre-concentration steps, preservation conditions, and domain-specific notes for many analytes and sampling types.

- Data Structure and Key Fields (relevant to map-based data products)
  - Analyte information per entry:
    - Form (e.g., Dissolved)
    - Determinand (e.g., Al, NO3-N, Cl)
    - Units (e.g., ug/l, mg/l)
    - LQDC (lower quantification data qualifier or detection limit concept)
    - Quote To (data rounding or reporting threshold)
    - Start/End dates of dataset coverage
    - Location of Analysis (laboratory)
    - Analyte Analysis Method (instrumentation)
    - Method QC Qualifier (QC code)
    - Filtration, Preservation, Pre-concentration details
    - Detection limit notes and any special notes
  - Data provenance and quality flags:
    - Analytical Method QC Codes (1–9) indicating accreditation, proficiency testing, and method reliability
    - Data Qualifier Codes (10–17) indicating raw data, detection-limit issues, or special cautions
  - Sample context:
    - Sampling type (stream, borehole grab samples; input samples like rainfall, throughfall, cloud catch)
    - Time stamping rules and “volume-weighted sampling time” for inputs
    - Year mean sampling and interval-weighted timing considerations

- Analytical Methods and QC
  - Multiple labs and methods across the dataset (e.g., Wallingford, Lancaster, Bangor, Staylittle, Staylittle; various ICP-OES, ICP-MS, IC, colorimetric, etc.)
  - QC codes address data accuracy, inter-laboratory proficiency, and ISO 17025 accreditation status
  - Data qualifiers indicate data quality state (raw data, detection-limit-related notes, and potential data caveats)

- Sampling Times and Temporal Context
  - Distinct sampling types:
    - Grab samples for stream and borehole
    - Time-integrated samples for rainfall, throughfall, stemflow, cloud
  - Volume-weighted sampling times computed to reflect timing of precipitation relative to runoff
  - Year mean sampling and interval-based timing used to harmonize long time series
  - Special notes explain how missing rainfall data are handled by using alternate weather stations

- Spatial and Hydrological Context for GIS
  - Site-level catchment data with specified catchment areas (e.g., Lower Hore, Upper Hore, Tanllwyth, Lower Hafren, Upper Hafren)
  - Area-weighted runoff calculations to convert flow (cumecs) to mm/15 min and vice versa, using site catchment areas
  - Sample site codes and associated lab/analysis location enable spatial joins and cross-referencing with GIS layers

- Data Quality Flags and Provenance
  - Analytical Method QC Codes (e.g., ISO accreditation status, proficiency testing)
  - Data Qualifier Codes (e.g., raw instrument data, data at detection limit, unusual patterns)
  - Explicit notes on data handling, potential corrections, and method changes over time

- Practical Guidance for GIS and Map-Based Data Products
  - Use site-level data with:
    - Analyte, concentration (units), and time stamp
    - QC flags to filter or annotate data points (e.g., raw vs validated, detected vs non-detected)
    - Lab location and analytical method for lineage and reproducibility mapping
  - Derive hydrological context for maps:
    - Convert stream flow to area-weighted runoff using given catchment areas
    - Include area-weighted rainfall inputs and related inputs (cloud catch, throughfall)
  - Distinguish sample types:
    - Grab samples (temporal precision) vs time-integrated inputs (seasonality and event-based visuals)
  - Leverage volume-weighted sampling times to synchronize precipitation and runoff signals in time-series visuals
  - Consider data quality notes and QC codes when labeling map features or selecting data subsets for policy or public-facing maps

- Key Hydrological and Sampling Details to Reference
  - Catchment areas used for conversions:
    - Lower Hore (3.172 sq km), Upper Hore (1.62), Tanllwyth (0.916), Lower Hafren (3.58), Upper Hafren (1.22)
  - Conversion formulas:
    - mm/15min (flow) = cumecs × 0.9 / catchment area
    - cumecs = mm/15min × catchment area / 0.9
  - Sampling times:
    - Time stamps indicate when the sample is collected
    - Volume-weighted sampling times account for rainfall-weighted timing and AWS data gaps
  - Temporal and sampling nuances:
    - Input samples are time-integrated; others are grab
    - Handling of AWS data gaps by using alternative stations or averages