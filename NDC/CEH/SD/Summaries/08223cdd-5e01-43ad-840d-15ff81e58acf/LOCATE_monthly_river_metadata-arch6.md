# Land Ocean Carbon Transfer (LOCATE)
Monthly river sampling dataset

- Multidisciplinary NERC project to understand carbon flow from land to ocean.
- Partners include National Oceanography Centre, British Geological Survey, Centre for Ecology and Hydrology, Plymouth Marine Laboratory, plus several universities and Environment Agency.
- Focuses on carbon flux from land to rivers; companion dataset covers estuaries.
- 2017: monthly sampling from 41 rivers across England, Scotland, and Wales (Jan–Dec); additional samples in Nov 2016; catchments chosen to reflect different land-use types.

## Data captured and scope
- Measured parameters (monthly, 2017): temperature; specific electrical conductivity (SEC); salinity; nutrients (NH4-N, NO3-N, PO4-P, TN, TP); non-particulate organic carbon (NPOC); total dissolved carbon (TDC); alkalinity; pH; dissolved organic matter fluorescence (fDOM) and absorbance; particulate organic carbon (POC); particulate organic nitrogen (PON); stable isotopes (δ13C, δ15N); and 13C/15N in particulates.
- Molecular analyses planned but reported elsewhere.
- Sampling sites were fixed per river; most within a 2–3 day window each month; exceptions noted (e.g., Dorset Stour DSTO paused until April 2017).
- Coordination led by Andy Tye (BGS); data integration moved toward HMS sites for easier integration with EA data.

## Sampling regime and field procedures
- Field protocol emphasizes on-site preparation, controlled conditions, and consistent sampling:
  - In-field filtering and separation into designated bottles (POC, PON, 13C/15N in POC, nutrients, DOM, alkalinity/pH, salinity).
  - Samples kept in the dark and cooled; field weather/river condition notes recorded.
  - Photos taken upstream and downstream at sampling sites.
  - Gloves worn; sampling depth ~0–30 cm at mid-channel; alternatives used if access was restricted.
  - Bottles and filters rinsed to prevent contamination; samples transported in cool boxes or freezers.
  - Samples returned to institute for lab processing and dispatch to laboratories handling specific analyses.
- Specific sample handling by type:
  - Particulates (POC, PON, 13C, 15N): two 1 L bottles for return to lab.
  - Nutrients and general chemistry: 60 mL syringe with filtration into 125 mL bottle; pH/alkalinity in raw water.
  - DOM (fluorescence/absorbance): 30 mL amber bottle after filtration.
- Field blanks used selectively to test batch quality; groups responsible for specific analyses performed blanks (BGS for fluorescence, CEH Lancaster for nutrients, NOC for POC).

## Analytical methods and quality control
- Nutrients, pH, alkalinity: documented instrumentation, methods, units, and detection limits (examples include NH4-N with SEAL_AQ2; NO3-N with DIONEX ICS2000; PO4-P with SEAL_AQ2; pH with SKALAR/SP10; alkalinity with METROHM).
- Isotopes and carbon/nitrogen: measurements via Flash EA 1112 + Conflo III connected to DeltaPlus XP IRMS; δ13C and δ15N normalized to USGS reference materials; ISO 17025-style procedures; analyses treated with quality considerations (not accredited in the formal sense due to repeatability constraints).
- Fluorescence and absorbance: fluorescence with Varian Cary Eclipse; absorbance with Varian Cary 60; blank and standard checks (Quinine sulfate) in each batch; PARAFAC modelling with Matlab DOMFluor toolbox.
- Calibration and QA:
  - δ13C and δ15N scales anchored to USGS standards.
  - Long-term precision metrics provided for QC standard (topsoil reference).
  - Blank and standard checks performed; instrument sensitivity monitored (daily Raman scans).
- River-related metadata:
  - Land cover and catchment variables derived from 2015 CEH Land Cover Map; additional descriptors include catchment area, peat soil presence, land-use fractions, BFI, carbonate rocks, mean altitude, and various habitat categories.
- Data reporting units:
  - Carbon/N concentrations: % w/w; δ13C/δ15N in per mil (‰); fluorescence results in Raman units; absorbance in cm^-1.

## Data structure and content
- Data file columns include:
  - Identification and timing: River_code, Date, Trip_number, Sampling_time_GMT, River_sample_ID.
  - Field measurements: Temperature_degC, Conductivity_uS/cm, Salinity_ppt, Weather, Sampler_comments, Flow_and_level.
  - Core chemical data: NH4-N_FILTERED_WATER_mg_per_L, NO3-N_FILTERED_WATER_mg_per_L, NPOC_FILTERED_WATER_ppm, PO4-P_FILTERED_WATER_mg_per_L, TN_RAW_WATER_ppm, TP_RAW_WATER_mg_per_L, pH_RAW_WATER, Alkalinity_RAW_WATER_mg_per_L.
  - DOM/absorbance: Absorbance_abs254, Absorbance_abs340; EEM-based features and PARAFAC component loadings (multiple components).
  - Isotopes and isotopically labeled measures: POC_delta_13C_parts_per_mil, POC_13C_Atom_percent, PON_delta_15N_parts_per_mil, PON_15N_Atom_percent.
  - Particulate data: POC_PON_Sample labels/status/comments.
  - Quality and data provenance: Nutrients_pH_alkalinity_comments, PARAFAC_comments, etc.
  - River/catchment context: Land cover and derived environmental variables (e.g., catchment_area, NRFA_code, peat_area, BFI, rock carbonate and altitudes).
- Data include both field-derived measurements and lab-derived analytics, with explicit notes on sample volumes and filtration status.

## Notable design and usage notes
- The dataset emphasizes self-contained river-to-river and month-to-month comparability through standardized sampling windows and consistent site selection.
- Some sampling deviations exist (e.g., trial run in Nov 2016; DSTO sampling begin April 2017; HMS site relocation) affecting temporal or spatial comparability.
- Outputs support exploration of carbon flux variability by geography and season, with rich ancillary data (land cover, hydrology, isotopes, fluorescence indices) enabling multi-parameter analyses and advanced modelling (e.g., PARAFAC for DOM characterization).
- Quality control is active but partial in some areas (select field blanks; Aquacheck participation for CEH Lancaster analyses; long-term QC standards for isotopes and carbon/nitrogen).