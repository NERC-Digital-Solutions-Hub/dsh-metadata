# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- Purpose: Documents pre-concentration steps used before analytical measurement to enhance detection limits across a wide suite of dissolved chemical constituents.
- Scope: Detailed metadata for numerous analytes (e.g., Aluminium, Ammonium, Arsenic, Barium, Beryllium, Boron, Bromide, Cadmium, Caesium, Calcium, Cerium, Chloride, Chromium, Cobalt, Conductivity, Copper, DOC, Fluoride, Gran acidity/alkalinity, Iodine, Iron, Lanthanum, Lead, Lithium, Magnesium, Manganese, Molybdenum, Nickel, Nitrate, Nitrite, Orthophosphate, pH, Potassium, Praseodymium, Rubidium, Scandium, Selenium, Silicon, Sodium, Strontium, Sulphate, Sulphur, Temperature, Tin, Titanium, Total Dissolved Nitrogen, Tungsten, Uranium, Vanadium, Yttrium, Zinc, Time, Stream flow, and rainfall-related inputs).
- Data model orientation: Each analyte entry includes field-level metadata describing sample form, determinand, units, lower quantification/detection limits (LQDC), appropriate quoted target ranges, start/end applicability, location of analysis, analytical method QC qualifier, filtration/preservation requirements, and the specific analytical method used (e.g., ICP-OES, ICP-MS, IC, colorimetry, etc.).

- Pre-concentration and analysis details:
  - Methods often involve concentration steps (e.g., evaporation, dilution to specific volumes) prior to measurement to reach detectable levels.
  - A variety of instrumentation is used, including Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES), Inductively Coupled Plasma Mass Spectrometry (ICP-MS), Ion Chromatography (IC), and colorimetric autoanalyzers.
  - Filtration and preservation protocols are specified (e.g., field filtration with 0.45 µm membranes, field rain/cloud handling, dark storage at 4°C, specialized preservatives).
  - Detection-limit notes and qualification qualifiers accompany many analyte entries, reflecting method changes and quality control over time.

Data structure notes:
- Location of Analysis: Multiple labs/sites referenced (e.g., Wallingford, Lancaster, Staylittle, Bangor, Lancaster; with several entries indicating location at time of analysis).
- Time frame: Entries include explicit Start and End dates for when data are valid, with some continuations (cont.) indicating ongoing data capture.
- Data qualifiers and QC: A dedicated Analytical Method QC Codes section and Data Qualifier Codes describe how results were validated, flagged, or flagged as suspect, with codes indicating ISO/16925-like proficiency testing and accreditation contexts.
- Provisions for data interpretation: Several analyte entries include notes on specific methodological caveats, sample handling, and concentration strategies that affect data interpretation (e.g., conversion steps, extraction/elution procedures, and correction factors).

- Data governance aspects relevant to stewardship:
  - Comprehensive metadata per analyte supports data discoverability and re-use.
  - explicit pre-concentration and preservation details enable reproducibility and proper data quality assessment.
  - QC and data-qualifier coding provide traceable data quality flags for end users.

- End sections and supplemental content:
  - The document closes with an Analytical Method QC Codes section and Data Qualifier Codes, clarifying how data quality was evaluated and flagged.
  - It also includes a separate conversion and sampling framework, describing how streamflow is converted to area-weighted runoff, and how sampling times are timestamped, including distinctions between grab samples and input samples (rainfall, throughfall, cloud, etc.).
  - Sampling-time conventions and time-weighted calculations are outlined to support temporal alignment of precipitation and runoff data.

Key implications for Data Stewards:
- The data model is highly granular, with per-analyte metadata governing comparability across time, sites, and laboratories.
- To ensure standardization, a controlled schema should be preserved when integrating new data (field forms, analyte metadata, QC qualifiers, and units).
- Data quality flags (LQDC, Quote To, QC qualifiers) must be consistently applied and documented to support robust uncertainty assessment.
- Data governance should track method changes over time (e.g., shifts in instrumentation or detection capabilities) that affect sensitivity and comparability.
- Timeliness and accessibility can be improved by centralizing the metadata dictionary, harmonizing units, and providing explicit lineage and data provenance.

Recommended actions for Data Stewards (aligned with the document):
- Maintain a centralized data dictionary mapping each analyte to its fields (Form, Determinand, Units, LQDC, Quote To, Start/End, Location of Analysis, Method QC qualifier, Filtration, Preservation, Method, Detection-limit notes, and Notes).
- Enforce consistent units and clearly document any historical method changes affecting detection limits or data comparability.
- Preserve and expose QC flags (e.g., data qualifier codes and analytical method QC codes) alongside primary results.
- Archive pre-concentration and preservation protocols with versioning to support reproducibility.
- Provide a discoverable portal or catalog entry for this dataset with explicit data lineage, sampling types, and temporal coverage.
- Implement guidance for users on interpreting time stamps, volume-weighted sampling times, and conversions between flow (cumecs) and area-weighted runoff (mm/15 min) for consistent downstream analyses.
- Encourage periodic data quality reviews and cross-lab interoperability checks to address potential interoperability issues arising from the use of multiple laboratories and evolving analytical methods.