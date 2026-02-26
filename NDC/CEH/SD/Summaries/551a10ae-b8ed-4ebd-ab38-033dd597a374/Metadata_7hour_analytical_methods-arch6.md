Lancaster Water Chemistry Dataset: Analyte Details, Methods, and Hydrology (2007-2009)

Overview
- A comprehensive water quality dataset covering dissolved and total analytes, major anions/cations, and related metrics collected from Lancaster between 2007-03-06 and 2009-01-27.
- Includes extensive metadata on analytical methods, sample preservation, filtration, data quality indicators, and hydrological context (area-weighted streamflow and rainfall).

Data Coverage
- Location: Lancaster (water chemistry samples), with field data for hydrology at related sites.
- Temporal span: START and END dates for many analytes range from 2007-03-06 to 2009-01-27.
- Sample types: stream water and precipitation data; includes area-weighted hydrological calculations.
- Analytes: broad suite including metals (Al, Sb, As, Ba, Be, Cd, Cs, Cr, Co, Cu, Fe, Mn, Mo, Ni, Pb, Sb, Se, Sn, Ti, U, V, Zn, etc.), major ions (Cl–, NO3–, F–, SO4 2–, Na+, K+, Ca2+, Mg2+), nutrients (DOC, TDN, NH4-N, nitrate), conductivity, pH, alkalinity, chloride, and more.
- Data products: potential to create self-serve dashboards, trend analyses, and concentration-load calculations; includes area-weighted hydrology for load estimations.

Data Structure and Fields (key themes)
- Analyte records (example pattern):
  - ALUMINUM: FORM, DETERMINAND, UNITS, LQDC, QUOTE TO, START/END, LOCATION OF ANALYSIS, ANALYTICAL METHOD QC DATA QUALIFIER, FILTERATION, PRESERVATION METHOD, METHOD, COMMENT.
  - DETERMINANDS include Al, NH4-N, Sb, As, Ba, Be, B, Br, Cd, Cs, Ca, Ce, Cl, Cr, Co, Cu, DOC, Fe, F, Gran alkalinity, Iodine, La, Pb, Li, Mg, Mn, Mo, Ni, NO3-N, NO2-N, pH, K, Pr, Rb, Sc, Se, Si, Na, Sr, SO4, SO4_by_ICP, S, TDN, Sn, Ti, W, U, V, Zn, etc.
  - UNITS vary by analyte (ug/l, mg/l, uS/cm, mm, etc.).
  - LQDC represents the lower quantitation/quality control threshold; QUOTE TO gives reporting/rounding level.
  - START/END define measurement window; LOCATION OF ANALYSIS typically Lancaster; ANALYTICAL METHOD indicates instrument/method (ICP-OES, ICP-MS, IC, colorimetry, TOC, etc.).
  - FILTRATION indicates filtration protocol (PALL AcroCap 0.45 μm) in lab; PRESERVATION describes sample storage (e.g., acidification to 1% HNO3; 4°C storage).
  - METHOD specifies the analytical technique; QC DATA QUALIFIER codes describe data quality and accreditation context.
- Hydrology data:
  - Area weighted stream flow: DETERMINAND = Flow; UNITS = cumecs; Location = Field; METHOD = Dip flash measurement; PRESERVATION = Not applicable; QC = 6.
  - Area weighted rainfall: DETERMINAND = Rainfall; UNITS = mm; METHOD = Tipping bucket rain gauge; LOCATION = Field; QC = 6.
  - Area weighted runoff: derived from stream flow and catchment area; conversion between cumecs and mm/15min provided.
  - Area weighted rainfall/time: Volume-weighted mean sampling times described for precipitation data; includes weighting by hourly rainfall from Carreg Wen weather station.
- Temporal/sampling notes:
  - For stream samples (LHF/UHF): date/time indicates sampling time.
  - For precipitation samples (CR): beginning of the 7-hour interval during which sampling occurs.
  - Volume-weighted sampling times are recommended when timing between rainfall and runoff is critical.
  - Autosampler timing changes: before 2007-05-01 unloading/re-set in late afternoon; after 2007-05-01 change-over at 12:00 noon.

Analytical Methods and Quality Assurance
- Analytical methods include Inductively Coupled Plasma techniques (ICP-MS, ICP-OES), Ion Chromatography (IC), colorimetry, and TOC, with specifics per analyte (e.g., ICP-MS with PerkinElmer DRC 11 SOP 3504; IC methods SOP 3149/ICS-2000; TOC analysis SOP).
- Sample handling:
  - Filtration: PALL Lifesciences AcroCap Filter 0.45 μm in lab for most analytes.
  - Preservation: typically acidification to 1% with concentrated high-purity nitric acid; some samples stored at 4°C in dark.
  - Method-dependent QA: QC Data Qualifier values (e.g., 2, 4, 10) indicate various QA controls; some data flagged as raw (10) or problematic (11/12) per DATA QUALIFIER codes.
- QC and accreditation:
  - ANALYTICAL METHOD QC CODES indicate use of Aquacheck LGC proficiency testing; some methods ISO 17025 accredited; others not.
  - Data QUALIFIER codes (10, 11, 12) guide the treatment of data in analysis and reporting.

Hydrology Conversion and Temporal Reference
- Stream flow to area-weighted runoff conversions:
  - Lower Hafren catchment area: 3.58 km2; Upper Hafren catchment area: 1.22 km2.
  - mm/15min = cumecs × 0.9 / catchment area (km2)
  - cumecs = mm/15min × (catchment area) / 0.9
- Timing guidance:
  - For LHF/UHF streams: sample time stamps indicate collection time; precipitation samples indicate the interval start.
  - Volume-weighted mean times provide the proper basis for cross-matching rainfall and runoff.
  - Early period (first 8 weeks) autosampler timing may cause minor rain carryover; post-2007-05-01 timing aligned to boundary between intervals.

Data Use and Recommendations for Data Support
- Data integration opportunities:
  - Combine multi-analyte time series with hydrology (flow, rainfall) to compute mass loads via area-weighted flow.
  - Align data using volume-weighted sampling times to accurately relate rainfall to downstream concentrations and loads.
- Analytical transparency:
  - Leverage detailed method metadata to assess comparability across analytes and time periods.
  - Use QC codes and LQDC/QUOTE TO values to determine reporting limits and data suitability for trend analysis.
- Dashboards and self-serve products:
  - Build dashboards showing concentration trends by analyte, with flags for data quality (QC codes) and detection limits (DATA QUALIFIER 11).
  - Create load dashboards by integrating analyte concentrations with area-weighted flow data.
  - Include hydrology-derived metrics (area-weighted rainfall, runoff, hourly fluxes) to explore rainfall-runoff relationships.
- Data limitations and caveats:
  - Data coverage varies by analyte; some have longer reporting windows than others.
  - LQDC and QUOTE TO values indicate potential reporting limits; raw data may require processing for certain analyses (per DATA QUALIFIER 10).
  - Mixing of different analytical methods across analytes requires careful normalization when comparing across time or across analyte groups.

Notes for Data Support Practitioners
- Understand the ask: determine which analytes, time ranges, and data quality levels are needed for a given analysis (e.g., trend vs. load estimation).
- Validate data by checking QC qualifiers and ISO/ accreditation notes for each method.
- When building multi-analyte dashboards, ensure temporal alignment with hydrological data using the provided conversion formulas and volume-weighted times.
- Be mindful of data gaps and the potential need to flag or impute missing periods in time-series analyses.

End-of-Document Reference
- The document provides a cohesive framework for interpreting chemical and hydrological measurements within a 2007-2009 window, including comprehensive metadata for analytical methods, QA, and hydrological calculations to support data exploration, integration, and product creation.