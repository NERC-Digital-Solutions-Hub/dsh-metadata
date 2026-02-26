# Analytical data dictionary and sampling metadata for water quality at LHF/UHF (2007-2009)

## Overview
- A comprehensive metadata and parameter dictionary for dissolved chemical constituents and related hydrological metrics collected from water samples, precipitation, and derived stream/rainfall calculations.
- Covers numerous analytes (metals, anions, nutrients, DOC/TDN, alkalinity, pH, conductivity, etc.) and derived metrics (area-weighted flow, area-weighted rainfall, hourly water fluxes).
- Temporal scope: 6-Mar-2007 to 27-Jan-2009. Spatial scope includes Lower Hafren (LHF) and Upper Hafren (UHF) field sites, with analysis locations such as Lancaster, Wallingford, Bangor, and Wallingford/Lancaster.
- Includes both raw measurements (via multiple analytical methods) and computed quantities, along with detailed metadata about preservation, filtration, analytical SOPs, and data quality.

## Dataset content and structure
- For each analyte, a consistent set of metadata fields is recorded, including:
  - FORM (e.g., Dissolved), DETERMINAND (the species measured), UNITS, LQDC (limit of quantification data), QUOTE TO, START/END dates, LOCATION OF ANALYSIS, ANALYTICAL METHOD QC DATA QUALIFIER, FILTRATION, PRESERVATION METHOD, METHOD, and COMMENT.
- Analytes span a wide range (e.g., aluminum, ammonium, antimony, arsenic, barium, beryllium, boron, bromide, cadmium, caesium, calcium, cerium, chloride, chromium, cobalt, conductivity, copper, DOC, iron, fluoride, alkalinity, iodine, lanthanum, lead, lithium, magnesium, manganese, molybdenum, nickel, nitrate, nitrite, pH, potassium, praseodymium, rubidium, scandium, selenium, silicon, sodium, strontium, sulfate, total dissolved sulfur (TDN), tin, titanium, tungsten, uranium, vanadium, zinc, and more).
- Each analyte includes the determination method (e.g., ICP-MS, ICP-OES, ion chromatography, automated colorimetry, TOC), filtration (PALL AcroCap 0.45 µm), and preservation protocols (often acidification with high-purity nitric acid or storage at 4°C in the dark).
- Documentation of data qualifiers and QC frameworks (ANALYTICAL METHOD QC CODES) indicates calibration and proficiency testing context (ISO 17025 accreditation status for some methods).
- Derived and ancillary data include area-weighted stream flow (mm/15 min), area-weighted rainfall (mm), hourly water fluxes (mm/hr), stream flow (cumecs), and calendar date/time data formatting.

## Sampling times and time handling
- Sampling times are aligned with field data collection at LHF/UHF (streams) and precipitation collection (CR). 
- Precipitation samples have 7-hour collection windows with volume-weighted mean sampling times calculated from hourly rainfall data at the Carreg Wen station.
- For the first eight weeks, autosampler timing shifted; since 2007-05-01, changes were standardized to midday boundaries to align with sampling intervals.
- Time stamps are recorded in Greenwich Mean Time (GMT) and are used to anchor both raw samples and derived hourly flux calculations.

## Analytical methods and data quality
- Methods span:
  - Inductively Coupled Plasma techniques (MS and OES) using Perkin Elmer instruments and SOPs (e.g., SOP 3504, 3504; DRC 11).
  - Ion chromatography systems (ICS-2000) for chloride, nitrate, sulfate, etc. (SOPs 3149, 3149; ICS-2000).
  - Automated colorimetry (Berthelot reaction) for ammonium.
  - Total organic carbon (TOC) via thermal oxidation and conductivity detection (Shimadzu TOC-Vph).
  - pH via electrometric measurement with Metrohm equipment.
- Filtration and preservation practices are standardized (0.45 µm PALL AcroCap, 1% HNO3 for many metals, cold storage where appropriate).
- QC and accreditation notes:
  - Some methods are ISO 17025 accredited; several entries reference proficiency testing schemes (Aquacheck/LGC) for accuracy assessment.
  - Data qualifiers codes (10 Raw data, 11 Below detection, 12 Anomalous data) indicate data timing and processing levels.
  - ANNUAL QC codes provide context on method validity and inter-laboratory performance.

## Data governance and interoperability implications
- The dataset is large, multi-parameter, and spans multiple laboratories and information systems; governance should focus on:
  - Standardizing parameter naming conventions, units, and data qualifiers to improve interoperability.
  - Preserving full provenance: analyte, form, DETERMINAND, method SOP reference, QC qualifier, preservation, and location of analysis.
  - Maintaining alignment with ISO 17025 accreditation where applicable, and clearly documenting which methods are accredited and under what scope.
  - Documenting data transformation steps (e.g., conversions from cumecs to mm/15 min, and from mm/15 min to cumecs) and the use of volume-weighted sampling times for precipitation-derived metrics.
  - Providing clear handling rules for raw data vs. processed/derived values (LQDC, QUOTE TO, and Data Qualifier codes).

## Challenges and recommended actions for Data Stewards
- Challenges:
  - Incomplete picture of user needs and priorities for the dataset.
  - Timeliness and consistency of data delivery from multiple data creators.
  - Ensuring all data creators meet metadata and standardization requirements (metadata, units, formats, SOP references).
  - Managing data across many systems and formats, including non-interoperable legacy solutions.
  - Handling large datasets with many analytes and derived variables.
- Recommended actions:
  - Establish and enforce a unified metadata schema covering all analytes, units, LQDC, data qualifiers, methods, preservation, and QC status.
  - Implement controlled vocabularies for analyte names, forms (Dissolved), and DETERMINAND mappings; align with ISO 17025-accredited methods where applicable.
  - Create data validation and cleaning workflows to catch inconsistencies (e.g., irregular LQDC/QUOTE TO values, malformed START/END dates).
  - Preserve SOP references (e.g., SOP 3504, 3104, 3149, ICS-2000) and related QA documentation; store provenance with each dataset.
  - Document data processing steps for derived metrics (area-weighted values, rainfall/runoff conversions) and ensure transparent, repeatable calculations.
  - Communicate user needs and data use cases to guide dataset organization, discoverability, and sharing practices.