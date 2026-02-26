Aluminum, FORM = Dissolved. Aluminum, DETERMINAND = Al.

## Overview
- A comprehensive, multi-parameter water quality and hydrological dataset spanning 6-Mar-2007 to 27-Jan-2009.
- Analytes cover a wide range of inorganic species (metals, metalloids, major ions) plus dissolved organic carbon (DOC), nitrogen species, sulfur species, pH, conductivity, and more.
- Samples analyzed at multiple laboratories (Lancaster predominantly; some entries indicate Wallingford, Bangor, and others) using standardized analytical methods and SOPs.
- Includes derived hydrological measures: area-weighted stream flow, area-weighted rainfall, hourly water fluxes, and field-derived time data.
- Time stamps and sampling methodologies are explicitly documented, including 7-hour precipitation intervals and volume-weighted sampling times.

## Data Content and Structure
- For each analyte, fields include:
  - FORM (e.g., Dissolved)
  - DETERMINAND (e.g., Al, NH4-N, Sb, As, etc.)
  - UNITS (e.g., ug/l, mg/l)
  - LQDC (lower quantification limit)
  - QUOTE TO (reported limit or value for quotation)
  - START and END dates
  - LOCATION OF ANALYSIS (Lancaster, Wallingford, Bangor, etc.)
  - ANALYTICAL METHOD QC DATA QUALIFIER (codes 1–5)
  - FILTRATION (PALL Lifesciences AcroCap with 0.45 µm membrane in lab)
  - PRESERVATION METHOD (e.g., acidification to 1% with concentrated nitric acid; stored at 4°C)
  - METHOD (instrumentation like ICP-MS, ICP-OES, IC, TOC, colorimetry, etc.)
  - COMMENT
- Key analytes include: Aluminum, Ammonium (NH4-N), Antimony, Arsenic, Barium, Beryllium, Boron, Bromide, Cadmium, Caesium, Calcium, Cerium, Chloride, Chromium, Cobalt, Conductivity, Copper, DOC, Iron, Fluoride, Gran alkalinity, Iodine, Lanthanum, Lead, Lithium, Magnesium, Manganese, Molybdenum, Nickel, Nitrate (NO3-N), Nitrite (NO2-N), pH, Potassium, Praseodymium, Rubidium, Scandium, Selenium, Silicon, Sodium, Strontium, Sulphate, SO4_by_ICP, Sulphur, Total Dissolved Nitrogen (TDN), Tin, Titanium, Tungsten, Uranium, Vanadium, Zinc, plus area-weighted hydrological metrics (stream flow, rainfall) and hourly water fluxes.
- Derived and auxiliary data:
  - Area weighted stream flow (mm/15min; derived from cumecs and catchment area)
  - Area weighted rainfall (mm)
  - Stream flow (cumecs)
  - Hourly water fluxes (mm/hr)
  - Time and date fields (Date; Time)
- Data qualifiers and quality codes:
  - ANALYTICAL METHOD QC CODES explain method accreditation and quality context (ISO 17025 vs non-accredited; proficiency testing)
  - DATA QUALIFIER CODES include 10 (raw data with no LQD), 11 (data at or below detection limit), 12 (raw data with anomalies)
- Field and sampling timing:
  - For stream samples: date/time stamp = sample collection time
  - For precipitation (CR) samples: start of the 7-hour interval
  - Volume-weighted mean sampling time is provided, with hour-weighting based on rainfall at Carreg Wen station
  - Autosampler changeovers noted (2007-05-01 moved to 12:00; earlier changeover may cause rain-containing samples at 7 PM)

## Data Quality and QC
- QC status is indicated via:
  - ANALYTICAL METHOD QC DATA QUALIFIER codes (1–5), reflecting accreditation and proficiency context
  - DATA QUALIFIER CODES 10, 11, 12 describing raw data, detection-limit cases, and unusual patterns
- Some method analyses are ISO 17025 accredited; others reference proficiency testing schemes
- LQDC values indicate detection limits or quantification thresholds for each analyte
- Some minor data formatting irregularities are present (e.g., Sodium LQDC field shows combined values), highlighting the need for data cleaning before integration

## Data Governance, Metadata, and Provenance
- Location-specific details:
  - Lancaster is the primary analysis location; some entries for Wallingford, Wallingford and Bangor/Lancaster combinations
- Analytical methods and SOPs:
  - ICP-MS (Perkin Elmer DRC 11; SOP 3504)
  - ICP-OES (Inductively Coupled Plasma Optical Emission Spectrometry; SOP 3104)
  - Ion chromatography (ICS-2000; SOP 3149)
  - Colorimetry (SOP 3115b; Berthelot reaction for ammonium)
  - TOC analysis (Shimadzu TOC- Vph Analyser; NPOC method)
- Filtration and preservation:
  - Filter: PALL Lifesciences AcroCap Filter, 0.45 µm
  - Preservation: acidification to 1% with high-purity nitric acid; cold storage where noted
- Data structure is designed for integration with hydrological data and field measurements, with explicit start/end dates for each measurement record

## Time, Sampling, and Data Integration Considerations
- Time stamps are in GMT; volume-weighted times should be used when timing between precipitation and runoff is critical
- First 8 weeks (2007-05-01 boundary) had autosampler unloading times that could bias 7 PM samples during rain; after 2007-05-01, boundary aligned to noon
- Conversions provided for relating stream flow to depth/precipitation measurements:
  - mm/15min = cumecs × 0.9 / catchment area (km^2)
  - cumecs = (mm/15min) × catchment area / 0.9
- Site catchment areas:
  - Lower Hafren (LHF) = 3.58 km^2
  - Upper Hafren (UHF) = 1.22 km^2

## Practical Implications for Data Leaders
- This dataset represents a rich, multi-constituent water quality and hydrological time series with extensive metadata, suitable for integrated environmental analytics, trend analysis, and policy-relevant reporting.
- To maximize governance and usability:
  - Maintain and enforce a comprehensive data dictionary capturing all fields, units, LQDC, QUOTE TO, QC codes, methods, and provenance
  - Implement data lineage tracking from field collection to laboratory analysis to final dataset
  - Align sampling times across analyte records using volume-weighted time bases for precipitation/runoff studies
  - Develop data quality filters that leverage DATA QUALIFIER CODES and ANALYTICAL METHOD QC CODES to flag suspect records
  - Establish data cleaning rules for anomal or inconsistent fields (e.g., mixed LQDC values in Sodium)
  - Document accreditation status and SOP references for traceability and audit readiness
- The dataset supports cross-domain use (chemistry, hydrology, environmental monitoring) but requires careful integration of time bases, units, and QC semantics to ensure reliable analyses.