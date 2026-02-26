# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

## Overview
- Describes metadata for a large, multi-analyte dissolved water chemistry dataset with pre-concentration prior to analysis.
- For each analyte, records include: form, determinate (determinand), units, lower quantification/data quality concentration (LQDC), quote-to value, start and end dates, location of analysis, analytical method QC qualifiers, filtration, preservation, analytical method, detection limit notes, and any notes.
- Data cover numerous elements/ions (e.g., Aluminium, Ammonium, Arsenic, Barium, Bromide, Chloride, Chromium, Iron, Lead, Manganese, Nitrate, Phosphate, Sulphate, Uranium, Zinc, etc.) across multiple sites and laboratories.
- Laboratories involved include Wallingford, Lancaster, Staylittle, Bangor, Tanllwyth, Staylittle, and others; methods include ICP-OES, ICP-MS, IC, Autoanalyzer, and various pre-concentration/dilution steps.
- Emphasizes pre-concentration steps (e.g., evaporation, acidification, dilution) and field/lab filtration and preservation protocols.

## Data Model and Field Definitions
- Analyte-level metadata schema per entry:
  - Form: e.g., Dissolved
  - DETERMINAND/DETERMINAND: e.g., Al, NH4-N, Cl, Fe, NO3-N, PO4, S, U, Zn
  - UNITS: e.g., ug/l, mg/l, mS/cm, mm
  - LQDC: Lower Quantification/Data Concentration thresholds
  - QUOTE TO: Target reporting concentration or rounding guidance
  - START/END: Temporal coverage for each analyte (start/end dates; can be “cont.”)
  - ANALYSIS: Laboratory or method family (e.g., Wallingford, Lancaster)
  - METHOD QC QUALIFIER: Quality control data qualifier codes
  - FILTRATION: Filtration details (e.g., 0.45 µm membrane, GF/C, field vs lab)
  - PRESERVATION: Sample preservation conditions (e.g., storage at 4°C, dark, refrigeration)
  - METHOD: Analytical approach (e.g., ICP-OES, ICP-MS, IC, Autoanalyzer)
  - DETECTION LIMIT NOTES: Notes on detection limits or reporting conventions
  - NOTES: Additional contextual notes
- Data relationships:
  - LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION: Indicates where data were generated or pre-concentrated before analysis
  - LOCATION OF ANALYSIS: Indicates the specific lab (e.g., Wallingford, Lancaster)
  - PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE DETECTION LIMIT: Explicitly tracked
- Temporal and site context:
  - START/END capture timeframes; some data are continuous (“cont.”)
  - Multiple sites and catchments with site codes (e.g., Tanllwyth K, Lower Hore A, Hafren B, etc.)

## Data Quality, QC, and Provenance
- Data Quality Codes (ANALYTICAL METHOD QC CODES) reference external proficiency testing and ISO 17025 accreditation status:
  - Examples include materials from Aquacheck LGC and SRMs; notes on ISO accreditation status
  - Codes indicate whether determinations were externally validated, instrumentally validated, or require caution
- Data Qualifier Codes (DATA QUALITY CODES) provide:
  - 10 Raw data from instrument (uncorrected)
  - 11 Below detection limit
  - 12 Periods of reduced sensitivity due to method changes
  - 13–17 various data caveats (pattern anomalies, sampling time issues, corrections)
- The dataset supports traceability to proficiency testing, method validation, and accreditation status, aiding data stewardship and user trust.

## Laboratories, Methods, and Pre-Concentration
- Labs and methods:
  - Wallingford, Lancaster, Staylittle, Bangor, Tanllwyth, and others
  - Techniques include Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES), Inductively Coupled Plasma Mass Spectrometry (ICP-MS), Ion Chromatography (IC), Technicon Autoanalyzer systems, and manual/colorimetric assays
- Pre-concentration and sample handling:
  - Evaporation steps (e.g., 400 mL samples evaporated to concentrate analytes)
  - Acidification to 1% nitric acid or other acids for preservation
  - Dilution to prepare concentration ranges (e.g., 20-fold)
  - Filtration practices in field and lab to isolate dissolved fraction
  - Preservation in dark, at 4°C, and other lab-specific protocols
- Data integration aspects:
  - Different time periods use different laboratories and methods; cross-site harmonization notes are implied via QC codes and LQDC

## Analyte Coverage (Representative)
- Major categories include:
  - Metals and metalloids: Aluminium, Antimony, Arsenic, Barium, Beryllium, Boron, Cadmium, Cesium, Chromium, Cobalt, Copper, Iron, Lanthanum, Lead, Lithium, Magnesium, Manganese, Molybdenum, Nickel, Niobium (not listed), Rhenium (not listed), Selenium, Silver (not listed), Tin, Titanium, Tungsten, Uranium, Vanadium, Yttrium, Zinc
  - Metalloids and non-metals: Chloride, Fluoride, Nitrate, Nitrite, Orthophosphate, Phosphorus, Sulphate, Sulphur (total dissolved S vs sulfate), Total dissolved nitrogen (TDN), Dissolved organic carbon (DOC), Dissolved organic nitrogen (DON)
  - Nutrients and related: Ammonium (NH4-N), Nitrate-N, Nitrite-N, Orthophosphate, Total Dissolved Nitrogen, Dissolved Organic Nitrogen
  - Physical/chemical properties: Conductivity, pH, Temperature
  - Flow and rainfall context: Stream flow, Area-weighted runoff, Area-weighted rainfall, Rainfall inputs (input samples), Cloud catch, Throughfall, Hourly water fluxes
- Temporal coverage varies by analyte, with some starting in the 1980s and continuing through 2007, and some ongoing or cont.

## Flow, Runoff, and Sampling Time Conversions
- Conversion formulas:
  - From cumecs to mm/15 min: mm/15min = cumecs × 0.9 / catchment area (km^2)
  - From mm/15min to cumecs: cumecs = (mm/15min) × catchment area / 0.9
- Site catchment areas provided for flow-to-runoff conversions (Lower Hore, Upper Hore, Tanllwyth, Lower Hafren, Upper Hafren)
- Sampling times and data interpretation:
  - Sampling times indicate actual collection times for grab samples; input samples (rainfall, throughfall, rainfall-derived chloride) are time-integrated
  - Volume-weighted sampling time is calculated differently for stream/rain inputs and other inputs
  - Year mean sampling is derived from volume-weighted sampling
  - Emphasis on using volume-weighted time base for critical timing analyses of precipitation and runoff
- Flux calculations:
  - Hourly water fluxes derived from runoff and rainfall intervals; notes warn that averaging can overestimate true rainfall flux due to interval timing

## Governance and Stewardship Implications for Data Stewards
- Data discoverability and interoperability:
  - Rich, analyte-level metadata supports dataset discoverability and reuse across projects
  - Clear lab provenance, method details, QC qualifiers, and pre-concentration steps enable reproducibility
- Data integrity and lifecycle:
  - Maintain provenance by preserving raw data alongside QC-flagged data
  - Track changes in analytical methods and accreditation status; document method transitions affecting comparability
  - Preserve preservation conditions and filtration details to contextualize concentrations
- Standards and compliance:
  - Align with ISO 17025 accreditation and inter-laboratory proficiency testing references
  - Maintain standardized units and reporting conventions across analytes and labs
- Data management recommendations:
  - Store analyte-level metadata, site metadata, and temporal extents with clear relationships (analyte ↔ lab ↔ method ↔ QC)
  - Ensure explicit pre-concentration details are captured for reproducibility
  - Provide documented data quality flags and their meanings to end users
  - Include conversion formulas and site catchment data to support downstream hydrological analyses

## Endnotes and Supporting Context
- The document includes detailed data qualifiers, method QC codes, and a mapping of sampling times to analytical contexts.
- Provides explicit guidance for converting flow to area-weighted runoff and for interpreting sampling times in relation to precipitation and runoff events.
- Serves as a comprehensive data governance artifact for a long-running hydrochemical monitoring program, enabling robust data sharing, quality assessment, and re-use by data stewards and researchers.