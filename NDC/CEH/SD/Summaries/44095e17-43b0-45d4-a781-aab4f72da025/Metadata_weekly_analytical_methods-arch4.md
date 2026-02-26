# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- Overview
  - A comprehensive metadata/document describing analytical data collected for numerous chemical species, with pre-concentration steps prior to analysis aimed at improving detection limits.
  - Covers many analytes (metals, metalloids, major ions, nutrients, dissolved organic carbon, total dissolved nitrogen, etc.) across multiple sites and time periods.
  - Includes detailed parameter-by-parameter data definitions, pre-concentration methods, preservation, filtration, analysis methods, detection limits, and QC information.

- Data Structure and Coverage
  - Entities: Individual analytes (e.g., Aluminium, Ammonium, Antimony, Arsenic, Barium, etc.) each with a full set of metadata.
  - Core fields per analyte include:
    - FORM, DETERMINAND, UNITS, LQDC (lower quantification/detection), QUOTE TO, START, END.
    - ANALYSIS (laboratory), METHOD (pre-concentration or analytical approach), LOCATION OF ANALYSIS, PRESERVATION, FILTRATION, DETERMINATION, and QC-related qualifiers.
    - Special notes on detection limits, and any method-specific details (e.g., evaporation, acidification, ICP-AES/MS, IC, colorimetry).
  - Temporal and spatial breadth:
    - Many analytes span 1983–2007 (with some continuations indicated by “cont..”).
    - Analyses conducted at multiple laboratories (Wallingford, Lancaster, Staylittle, Bangor, Lancaster, etc.).
  - Sample handling:
    - Pre-concentration steps (e.g., evaporation of filtered samples under IR, dilution to targeted volumes, field/rain/cloud filtration considerations).
    - Preservation strategies (acidification, refrigeration, dark storage) and filtration specifics (types and pore sizes).

- Analytical Methods and QC
  - Methods include Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES), Inductively Coupled Plasma Mass Spectrometry (ICP-MS), Ion Chromatography (IC), various colorimetric assays, and autoloaders (Technicon Autoanalyzer systems).
  - QC and data quality indicators:
    - Data Qualifier Codes (10, 11, 12, 13, 14, 15, 16, 17) with defined meanings (e.g., raw data, values around detection limits, patterns requiring caution, corrections, sampling-time inconsistencies).
    - Analytical Method QC Codes (1–9) describing accreditation status and interlaboratory proficiency testing.
    - Notes on ISO 17025 accreditation and proficiency testing usage for method accuracy.

- Pre-Concentration and Handling Details
  - Documented pre-concentration workflows (e.g., evaporation of 400 mL filtered sample under infrared light, subsequent dilution to 20 mL to achieve ~20x concentration).
  - Field vs. lab processes, including filtration schemes (e.g., 0.45 μm membranes, GF/C filters), field vs. lab filtration, and acidification norms (typically 1% nitric acid or higher purity acids).
  - Preservation practices (e.g., storage conditions, darkness, refrigeration) and post-concentration handling specifics.

- Data Provenance and Location
  - Data provenance includes the origin of analytical data (which lab performed the analysis) and the associated QA/QC qualifiers.
  - Analyses are attributed to several labs/locations (Wallingford, Lancaster, Staylittle, Bangor, etc.), enabling cross-site comparability but requiring harmonization.

- Data Calculations and Conversions
  - The document provides explicit instructions for converting streamflow to area-weighted runoff for select sites (site catchment areas listed: Lower Hore, Upper Hore, Tanllwyth, Lower Hafren, Upper Hafren).
  - Conversion formulas between cumecs and mm/15 min, and vice versa, using catchment area for area-weighted computations.
  - Sampling time conventions explained:
    - Grab samples for stream and borehole types.
    - Time-integrated sampling for rainfall, throughfall, stemflow, and cloud samples.
    - Volume-weighted sampling times and year means are computed to reflect sampling timing relative to precipitation/runoff events.
  - Sampling times should be used as the basis for temporal analyses and any flux/rate calculations.

- Practical Considerations for Data Leaders
  - Data completeness and harmonization:
    - Large, multi-site, multi-decade dataset with many analytes and varying methods; governance needed to ensure consistent metadata standards, units, and QC tagging.
  - Data quality and comparability:
    - Varied detection limits, pre-concentration methods, and QC qualifiers across time and sites; careful interpretation required when comparing across periods or locations.
  - Provenance and lineage:
    - Clear traceability of where data were produced (laboratories, methods, pre-concentration steps) is essential for trust and reproducibility.
  - Metadata governance:
    - Rich metadata granularity (METHOD, PRESERVATION, FILTRATION, LQDC, START/END, QC qualifiers) supports reproducibility but requires robust data management to maintain consistency and readability.
  - Operational insights:
    - The explicit conversion rules for hydrological contexts enable integrated environmental analyses (e.g., linking hydrology with chemistry data), but demand accurate catchment data and timing alignment.

- Key Takeaways for Strategy and Implementation
  - Establish a metadata-focused data governance framework that standardizes analyte definitions, units, QC codes, and method descriptors across sites and time.
  - Maintain a provenance-aware data store that captures pre-concentration protocols, filtration, preservation, and analysis methods to enable reliable cross-site comparisons.
  - Ensure data systems support interpretation of QC qualifiers and detection-limit handling (including special codes and notes) to prevent misinterpretation.
  - Implement reproducible data processing pipelines that can apply the documented conversion rules (streamflow to area-weighted runoff) and time-weighted sampling considerations when producing site-level summaries.
  - Prioritize data quality improvements and standardization efforts to reduce gaps and inconsistencies, aligning with ISO 17025-like accreditation practices where applicable.