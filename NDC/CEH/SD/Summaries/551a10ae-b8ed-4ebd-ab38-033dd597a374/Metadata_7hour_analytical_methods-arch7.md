# Aluminum, FORM = Dissolved.

- Scope and purpose
  - A comprehensive lab-processed dataset of dissolved chemical constituents in water, with extensive metadata on determinands, units, methods, quality controls, sampling times, and locations.
  - Designed for GIS-enabled analysis: supports map-based visualization of concentrations across sites and time, plus derived hydrological variables.

- Spatial and temporal coverage
  - Locations mentioned: Lancaster (primary analysis site), Wallingford, and Bangor/Lancaster as analysis points; field-derived data include area-weighted hydrological metrics.
  - Timeframe: samples collected between 6-Mar-2007 and 27-Jan-2009 (end dates vary by analyte).
  - Field data include area-weighted stream flow, area-weighted rainfall, hourly water fluxes, and time stamps all tied to field measurements.

- Analytes and data structure
  - Wide range of constituents (examples): Aluminum (Al), Ammonium (NH4-N), Antimony (Sb), Arsenic (As), Barium (Ba), Boron (B), Chloride (Cl), Chromium (Cr), Cobalt (Co), Calcium (Ca), Conductivity, Copper (Cu), DOC, Iron (Fe), Fluoride (F), Nitrate/Nitrate-N (NO3-N), Nitrite (NO2-N), pH, Potassium (K), Lead (Pb), Lithium (Li), Magnesium (Mg), Manganese (Mn), Molybdenum (Mo), Nickel (Ni), Phosphate (not listed; nitrate/nitrite present), Sulphate (SO4), Sulphur (S), Tin (Sn), Titanium (Ti), Tungsten (W), Uranium (U), Vanadium (V), Zinc (Zn), and several others.
  - Each analyte entry includes: FORM (often Dissolved), DETERMINAND, UNITS, LQDC (level/state of detection/qualification), QUOTE TO, START and END dates, LOCATION OF ANALYSIS, ANALYTICAL METHOD, QC DATA QUALIFIER, FILTRATION, PRESERVATION METHOD, METHOD, and COMMENT.
  - Some derived or related metrics included: Conductivity, Gran alkalinity, TDN (Total Dissolved Nitrogen), DOC (Dissolved Organic Carbon), area-weighted hydrological variables, and SO4_by_ICP (calculated from ICP data).

- Analytical methods and data quality
  - Primary analytical methods include:
    - Inductively Coupled Plasma Mass Spectrometry (ICP-MS) with Perkin Elmer DRC 11 (SOP 3504) for many metals.
    - Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES) (SOP 3104) for several elements.
    - Ion Chromatography (IC) for Cl, NO3-N, SO4, and related ions (SOP 3149/ICS-2000).
    - Automated colorimetry (for ammonium; Berthelot reaction; SOP 3115b).
    - TOC analyzer for DOC (NPOC via Shimadzu TOC- Vph).
    - pH by electrometric measurement; conductivity by lab meter with temperature correction.
  - Data quality codes and qualifiers:
    - ANALYTICAL METHOD QC CODES describe ISO 17025 alignment and interlaboratory proficiency (including specific notes on accreditation status).
    - DATA QUALIFIER codes include 10 (raw data), 11 (data at/below detection limit), 12 (data with anomalies to be treated with caution).
  - Filtration and preservation:
    - Filtration: PALL Lifesciences AcroCap Filter with 0.45 µm membrane (lab filtration is consistent across most analytes).
    - Preservation: acidification to 1% with high-purity nitric acid or cold storage as specified.
  - Units and detection limits:
    - Various units (ug/l, mg/l, uS/cm, mm, etc.) with defined LQDC values per analyte.
  - Data qualifiers indicate how to handle raw vs. processed values and data quality flags.

- Hydrological context and derived variables
  - Area-weighted stream flow: expressed in mm/15min, derived from measured cumecs and catchment area (Lower Hafren 3.58 km2; Upper Hafren 1.22 km2).
  - Conversion between stream flow and precipitation metrics:
    - mm/15min = cumecs × 0.9 / catchment_area_km2
    - cumecs = mm/15min × catchment_area_km2 / 0.9
  - Area-weighted rainfall: rainfall total in mm, based on tipping-bucket rain gauge at Carreg Wen station; rainfall attributed to the middle of each hour when rainfall occurred.
  - Derived hourly water fluxes: mm/hr, calculated from runoff and rainfall data.
  - Time alignment notes:
    - For stream samples (LHF/UHF): date/time stamps indicate sample collection time.
    - For precipitation (CR): stamps indicate the beginning of the 7-hour interval.
    - Volume-weighted sampling times: uses hourly rainfall-weighted averages for precipitation events; adjustments were made when autosampler times were changed (late 2007 from 7 PM–2 AM to 12 Noon boundary).
  - Time standardization: all times recorded in Greenwich Mean Time (GMT).

- GIS-relevant considerations and usage notes
  - Data are structured for spatial join with GIS features (site locations, catchment areas, flow paths) and temporal analysis (time-series maps, animated maps).
  - Useful for:
    - Visualizing spatial patterns of dissolved constituents across sites and across time.
    - Linking chemical data to hydrological variables (flow, rainfall, runoff) for watershed-scale analyses.
    - Filtering by QC codes or data qualifiers to balance data quality with spatial coverage.
  - Important caveats for mapping:
    - Temporal alignment between rainfall and runoff is critical; use volume-weighted time base for precise rainfall-runoff timing.
    - Be mindful of site-specific start/end validity windows per analyte when aggregating or comparing across sites.
    - GMT time stamps and autosampler changes may affect exact time alignment around early 2007; use the provided notes to adjust or document time references.

- Practical GIS tasks enabled by the dataset
  - Create point layers for sampling locations (Lancaster, Wallingford, Bangor) with time-stamped attribute values for each analyte.
  - Create derived raster surfaces or catchment-level summaries of dissolved metals and major ions using interpolation or areal-weighted approaches, incorporating area-weighted runoff and rainfall as covariates.
  - Build time-enabled maps or dashboards showing concentration trends and their relation to hydrological events (rainfall, discharge).
  - Apply QC filters to select high-quality data (e.g., QC codes aligned with ISO accreditation status) for policy or public-facing reports.