# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- Purpose and content
  - Comprehensive metadata describing how analytical data were collected, prepared, and analyzed before concentration to improve detection limits.
  - Covers a wide range of elements (e.g., aluminium, ammonium, antimony, arsenic, barium, beryllium, boron, bromide/ bromine, cadmium, caesium, calcium, cerium, chloride, chromium, cobalt, conductivity, copper, dissolved organic carbon, nitrate, nitrite, phosphate, pH, potassium, magnesium, manganese, molybdenum, nickel, phosphorus, sulfur, silicon, sodium, strontium, sulfate, tin, titanium, uranium, vanadium, yttrium, zinc, and more) with detailed parameterization for each.

- Data structure and fields (typical per parameter)
  - Form and DETERMINAND (e.g., dissolved; Al, NH4-N, Cl, etc.)
  - Units (e.g., ug/l, mg/l, mg/l-N, uS/cm)
  - LQDC (low quantitation decision/limit) and QUOTE TO values
  - START and END dates (time span of data record)
  - LOCATION OF ANALYSIS or ANALYSIS LAB (e.g., Wallingford, Lancaster, Staylittle, Bangor)
  - ANALYTICAL METHOD and METHOD QC QUALIFIER (e.g., ICP-OES, ICP-MS, AAS, IC, TOC)
  - FILTRATION and PRESERVATION (field filtration details, storage conditions)
  - PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE DETECTION LIMIT (describes pre-concentration schemes)
  - DETECTION LIMIT NOTES (notes on detection capabilities or transformations)
  - NOTES (any special considerations)

- Analytical methods and laboratories
  - Multiple laboratories and instruments used over time, including Wallingford, Lancaster, Staylittle, Bangor, and other sites.
  - Common analytical approaches include:
    - Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES)
    - Inductively Coupled Plasma Mass Spectrometry (ICP-MS)
    - Atomic Absorption Spectrometry (AAS)
    - Ion chromatography (IC)
    - Colorimetric methods (e.g., autoanalyzers, Berthelot reaction for ammonium)
    - Total Organic Carbon (TOC) analyses
  - Pre-concentration steps and acidification practices vary by element and time period (e.g., evaporation of sample aliquots, concentration to 20-fold, field filtration, specific preservation solvents).

- Quality control and data validation
  - Explicit Analytical Method QC Codes (1–9) describing how accuracy was assessed (interlab schemes, ISO/EN accreditation, instrument specifications).
  - Data Qualifier Codes (10–17, and additional notes) indicating data quality status, detection-limit issues, time-period method changes, and data corrections.
  - Data qualifiers cover raw data, low-detection scenarios, interlaboratory comparisons, methodological changes, and sampling-time consistency notes.

- Sampling and data timing
  - Distinguishes between sample types:
    - Stream and borehole samples (grab samples at specified times)
    - Input samples (rainfall, throughfall, stemflow, cloud) that are time-integrated over intervals
  - Volume-weighted sampling time computation is used for precipitation-related inputs to reflect the timing of rainfall relative to runoff.
  - Time stamps are used to determine year-mean sampling and inform analyses that require synchronized precipitation-runoff timing.

- Calculations and conversions for hydrology
  - Conversions between streamflow (cumecs) and area-weighted runoff (mm/15 min) for four sites (Lower Hore, Upper Hore, Tanllwyth, Lower Hafren, and Upper Hafren) with provided catchment areas.
  - Formulas:
    - mm/15min = cumecs * 0.9 / catchment_area_km2
    - cumecs = mm/15min * catchment_area_km2 / 0.9
  - Site codes and catchment areas are specified for accurate conversion.

- Data integration guidance for end users (Data Support perspective)
  - The metadata enables cross-lab data integration by standardizing units, forms, pre-concentration procedures, and QC coding.
  - Facilitates the creation of self-serve data products (dashboards, pivot tables, reports) that summarize elemental concentrations, detection-limit handling, and QA/QC status across sites and time.
  - Supports transparent data provenance, ensuring end users understand where each data point originated (lab, method, pre-concentration, preservation, sampling type, and time stamp).

- Practical notes and caveats for data handlers
  - Data span multiple decades with changes in labs, instrumentation, and pre-concentration practices; this should be accounted for in trend analyses.
  - Missing or inconsistent time stamps are addressed by standard assumptions (e.g., sampling times set to 10:00 am when not recorded) and volume-weighting considerations.
  - Some data involve recalculations or corrections (e.g., DON from DON and related species, or conversions from other units) and are flagged via data qualifier codes.
  - Handling of non-detects and data below detection limits is guided by LQDC, QUOTE TO, and qualifier codes.

- Quick reference for data users
  - Analytical Method QC Codes explain accuracy validation (interlaboratory proficiency testing, ISO accreditation status).
  - Data Qualifier Codes indicate data reliability and special cases (raw data, method changes, potential data artefacts).
  - Pre-concentration and preservation details vary by element and period; these explain detection-limit improvements and potential biases.
  - Sampling types and volume-weighted timing are critical when aligning precipitation inputs with hydrological responses.

- Scope of the dataset
  - An extensive, historically rich set of analytical data with detailed metadata for pre-concentration and analysis across a wide suite of chemical constituents, designed to support robust data exploration, integration, and product development for end users.