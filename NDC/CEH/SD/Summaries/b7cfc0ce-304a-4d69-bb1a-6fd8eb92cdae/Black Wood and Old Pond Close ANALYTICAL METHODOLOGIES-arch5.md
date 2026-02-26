# Rainfall catch

## Overview
- Measurements span Rainfall catch, Throughfall catch, and Stemflow catch from 23 May 1990 to 06 Apr 1992.
- Field samples collected at Wallingford lab; analyses conducted there with clear field and laboratory workflows.
- Strong data governance signals: per-analyte metadata (start/end dates, laboratory, filtration, preservation, method, units) support dataset discovery and reuse, aligning with publishable, interoperable structures typical of large dataset networks.

## Data contents and structure
- Sample types
  - Rainfall catch
  - Throughfall catch
  - Stemflow catch
- Analyte groups (examples)
  - Dissolved elements and compounds (e.g., Al, B, Ca, Cu, Fe, Mn, Na, Sr, Zn, K, Mg, Cl, F, NO3, NH4, SO4, Si, P, etc.)
  - Nutrients and ancillary parameters (pH, SRP, NO3, NH4)
  - Major ions and trace metals with consistent labeling across analytes
- Metadata per analyte (typical fields)
  - START and END dates
  - LAB (laboratory)
  - FILTRATION method and specifics
  - PRESERVATION (e.g., acidification to 1% with nitric acid; dark storage at 4°C)
  - METHOD (instrumentation/technique, e.g., ICP-OES, ion chromatography, automated colorimetry, radiometer pH)
  - UNITS (e.g., mg/l, µg/l-equivalents, pH)
  - LQDC (detection/limit quality control value)
  - QUOTE TO (uncertainty or reporting threshold)
- Data gaps
  - Numerous placeholders (= .) indicate incomplete metadata in parts of the record, signaling areas for metadata completion.

## Data collection and processing
- Sampling and handling
  - Field filtration with specified filters; notes indicate exceptions for rain/cloud events and subsequent lab handling.
  - Preservation practices documented (acidification, dark storage, temperature control).
- Laboratory analyses
  - Multiple techniques across analytes (ICP-OES, ion chromatography, automated colorimetry, radiometer pH).
  - Wallingford frequently listed as the laboratory; field/lab distinctions implied by filtration/preservation notes.
- Data management and updates
  - Metadata supports discovery and potential updates via portals/catalogues; START/END windows enable longitudinal analyses across sample types and time.

## Metadata quality and governance considerations
- Strengths
  - Uniform structure across analytes facilitates cross-parameter data integration.
  - Rich per-analyte metadata supports reproducibility and provenance (START/END, LAB, FILTRATION, PRESERVATION, METHOD, UNITS, LQDC).
- Gaps and risks
  - Widespread placeholders (= .) indicate incomplete metadata in parts of the record, which can hinder interoperability and automated validation.
  - While several analytes share metadata patterns, field-level values are not always complete, impacting data quality assessment.

## Data availability and sharing implications
- Discoverability and reuse
  - Detailed, analyte-specific metadata supports interpretation and reuse by data users and downstream systems.
  - Time-bounded data enable longitudinal analyses across Rainfall, Throughfall, and Stemflow types.
- Governance and stewardship needs
  - Need to ensure consistent completion of missing metadata fields to improve interoperability.
  - Maintain versioning and update procedures for time-series data and metadata to support ongoing sharing via portals.

## Challenges and considerations for Data Stewards
- Aligning user needs with data provision
  - Incomplete user-needs picture could affect prioritization and depth of documentation.
- Timely data access and standardization
  - Consistent collection protocols across analytes, but incomplete fields and varying units/methods can impede interoperability.
- Interoperability across systems and formats
  - A uniform schema exists, yet missing fields and legacy methods pose interoperability challenges.
- Handling large, multi-parameter time-series
  - Comprehensive data governance, curation, and update workflows are required for the broad analyte set over the time span.
- Outdated or bespoke components
  - Filtration/preservation and some analytical methods reflect older practices; map to current standards for long-term interoperability.

## Recommendations for Data Stewards
- metadata completeness
  - Fill in missing fields where possible and document known gaps with provenance notes.
- data dictionary and standards
  - Develop or align with a data dictionary that standardizes analyte naming, units, detection limits, and methods across all parameters.
- versioning and updates
  - Implement a clear versioning scheme for both data and metadata; record updates to START/END windows or methods.
- accessibility and publishing
  - Upload datasets to relevant data portals with machine-readable metadata and cross-references to related sample types (Rainfall, Throughfall, Stemflow).
- user-centered enhancements
  - Capture a concise summary of user needs and intended use cases to reduce the “incomplete picture” risk and guide metadata enrichment.