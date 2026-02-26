# Comprehensive Water Quality Analytical Data Report (Lower Hafren / Upper Hafren)

- Purpose and scope
  - A detailed dataset documenting a wide range of dissolved chemical constituents and field hydrology data from water samples collected at Lower Hafren (LHF) and Upper Hafren (UHF), with associated sampling times, analytical methods, and quality indicators.
  - Includes both chemical analyte measurements and hydrological metrics (area-weighted flow, rainfall, stream flow, hourly fluxes, and time data).

- Analyte and parameter metadata (representative examples)
  - Chemical species covered: Aluminum, Ammonium, Antimony, Arsenic, Barium, Beryllium, Boron, Bromide, Cadmium, Cesium, Calcium, Cerium, Chloride, Chromium, Cobalt, Conductivity, Copper, DOC, Iron, Fluoride, Gran alkalinity, Iodine, Lanthanum, Lead, Lithium, Magnesium, Manganese, Molybdenum, Nickel, Nitrate (NO3-N), Nitrite (NO2-N), pH, Potassium, Praseodymium, Rubidium, Scandium, Selenium, Silicon, Sodium, Strontium, Sulphate, Sulphur, TDN, Tin, Titanium, Tungsten, Uranium, Vanadium, Zinc, and related form/determination details.
  - Form and determinations: Predominantly dissolved forms; specific determinations (e.g., Al, NH4-N, Sb, As, Cl, NO3-N, NO2-N, Fe, Cu, Pb, etc.).
  - Units and detection qualifiers: Various units (ug/l, mg/l, uS/cm, mm/15min, etc.); LQDC values provided for many analytes; data qualifiers indicate data quality state (e.g., 10 raw data, 11 near detection limit, 12 anomalous patterns).
  - Start/end dates and locations: Measurements conducted 6-Mar-07 to 27-Jan-09; primary location of analysis is Lancaster; some hydrological measurements recorded in the field.

- Analytical methods and sample handling
  - Analytical methods used: Inductively Coupled Plasma Mass Spectrometry (ICP-MS), Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES), Ion Chromatography (IC), automated colorimetry, and other standard procedures (SOPs noted).
  - Filtration and preservation: Filtration via PALL Lifesciences AcroCap Filter (0.45 μm); preservation generally acidification to 1% with high-purity nitric acid; samples stored in dark at 4°C when appropriate.
  - Data qualifiers and QC: Analytical Method QC codes describe accreditation and proficiency testing context (ISO 17025, Aquacheck LGC PT schemes); some results flagged under different QC categories.

- Data quality and QC codes
  - ANALYTICAL METHOD QC CODES: Range from ISO 17025-accredited methods to non-accredited/competition-based assessments; notes on accreditation status and proficiency testing usage.
  - DATA QUALIFIER CODES: 10 Raw data with no lower-quantitation (LQD) adjustments, 11 Data at or below detection, 12 Data patterns requiring caution; codes inform interpretation and processing.

- Hydrological and time-based data
  - Area weighted stream flow: Calculated flows in mm per 15 minutes (mm/15min) from cumecs using site catchment areas (Lower Hafren 3.58 km^2; Upper Hafren 1.22 km^2).
  - Conversion to cumecs and vice versa: Formulas provided to convert between mm/15min and cumecs.
  - Rainfall and rainfall-based metrics: Area weighted rainfall (mm) and rainfall sampling times; 7-hour sampling intervals with calibration based on Carreg Wen automated weather station data.
  - Sampling times and time stamping: 
    - For stream samples (LHF/UHF), date/time stamps indicate sample collection time.
    - For precipitation samples (CR), stamps indicate the beginning of the 7-hour sampling interval.
    - Volume-weighted sampling times are used when timing is critical; rainfall within hours is allocated to the middle of the hour; autosampler changeovers explained (notably from 2007-05-01 onward at 12:00).
    - All times recorded in Greenwich Mean Time (GMT).

- Location and data management notes
  - Primary analysis location: Lancaster, with some field data in Bangor/Lancaster contexts.
  - Data integration and accessibility: The datasets appear to be structured for discoverability via portals with metadata; multiple datasets and analyte records are linked through consistent metadata fields (dates, methodologies, units, qualifiers, and QC notes).

- Temporal scope and sequencing
  - Sampling window spans 6-Mar-2007 to 27-Jan-2009, covering a broad suite of chemical analyses and hydrological measurements.
  - Detailed timing rules supplied to ensure correct alignment of rainfall, runoff, and sample collection times, especially around initial weeks and autosampler adjustments.

- Notable structural features
  - Comprehensive, analyte-by-analyte metadata schema including form, determinand, units, LQDC, start/end dates, location, analytical method QC qualifier, filtration, preservation, and method notes.
  - Explicit conversion rules and sampling-time guidance intended for analysts performing hydrological time-series interpretation and event-based correlation studies.

- Practical takeaway for analyses
  - The dataset provides a robust framework to investigate correlations between dissolved chemical concentrations and hydrological variables (flow, rainfall) across LHF and UHF catchments.
  - When using the data, reference the QC codes and LQDC values to determine data usability and apply time-base (volume-weighted) adjustments for precipitation-runoff analyses as described.
  - Ensure alignment of sample times (GMT) with their corresponding rainfall/runoff intervals and apply the specified stream-to-mm/h conversions when aggregating or modeling the hydrological component.