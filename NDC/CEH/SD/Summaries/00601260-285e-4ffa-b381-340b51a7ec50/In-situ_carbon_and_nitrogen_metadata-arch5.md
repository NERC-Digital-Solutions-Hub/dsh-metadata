# Fieldwork Protocol

- Documents field and laboratory methods for sampling surface water and porewater in streams, including deployment of diffusive equilibrium in thin-film (DET) gels and subsequent isotopic and concentration analyses.
- Focuses on data generation, instrument calibration, data structure, and quality control to support data governance, discoverability, and reuse.

## Field Sampling and Measurements

- Field sites: upstream and mid-stream sandy reaches; sampling conducted at 10 cm and 20 cm depth in stream environment.
- Immediate measurements: water temperature and dissolved oxygen (DO) recorded on-site using YSI ProODO or EcoSense ODO200.
- Sample processing: water samples filtered sequentially (0.45 μm then 0.22 μm) and frozen for later analysis.
- DET gels: deployed at least 72 hours prior to porewater sampling; sliced at 2.5 cm intervals within 25 minutes of sampling; stored cold until back-equilibration in the lab.
- Porewater gas sampling: headspace equilibrium method used in situ; 7 mL water with 14 mL ultrapure helium sealed in a syringe, shaken, and headspace collected in a pre-evacuated exetainer.
- Headspace to porewater: all headspace concentrations converted to porewater values using Henry’s constant.

## Laboratory Analyses and Isotopic Methods

- DET gel and water analyses: after elution, samples are prepared for chemical and isotopic analyses.
- Isotopic analyses:
  - δ15NNO3+NO2 and δ18O NO3+NO2 measured via denitrifier method (Casciotti et al.; Kaiser et al.; Sigman et al.) using a GEO 20:20 GC-IRMS.
  - δ13CCO2 measured at Centre for Ecology and Hydrology (Lancaster) using isotope ratio mass spectrometry (Isoprime/Isotrace setup).
- Organic and inorganic carbon/nutrients:
  - Ammonium (NH4+), nitrate (NO3−), nitrite (NO2−) measured by continuous-flow analyzer (Skalar San++) with colorimetric methods.
  - Dissolved organic carbon (DOC) measured with Shimadzu TOC-L CPH analyzer (non-purgable organic carbon quantified after sparging away inorganic/purgable carbon).
  - CO2 and CH4 measured by GC with TCD/FID detectors; N2O measured by GC with μECD.
- Instrument calibration and performance:
  - Daily and multi-point calibrations for GC-ECD, GC-FID, GC-TCD, and Skalar, with external standards and blanks to monitor drift.
  - QA references include standard materials (USGS, IAEA, NIST) and in-house references; reported accuracy, precision, and limits of detection (LOD) for each method.
  - Temperature and DO measured with factory-calibrated meters; a single-point 100% air saturation calibration used for field ODO.

## Calibration, Quality Assurance, and Uncertainty

- Gas chromatography and isotope ratio mass spectrometry calibration:
  - N2O: multi-point standards (0–100 ppm, depending on run) with drift-corrected measurements; typical accuracy and precision on the order of 0.1–1.75 ppm for N2O depending on run.
  - NO3−/NO2− isotopes: calibrated against international references (USGS 34/35, IAEA NO3−); in-house reference used for long-term precision checks.
  - 13C in CO2: calibrated against CO2-heavy standard (NIST 8562); precision reported as ±0.12‰ or better.
- Other analytes:
  - NH4+, NO3−, NO2−: calibration with multiple standards (0.02–5 mg N L−1; 0.58–1.00 mg L−1 references) with specified accuracy/precision and LODs; corrections for drift and baseline shifts.
  - TOC: calibration curves for low/medium/high methods; reported accuracy ~0.16 mg L−1, precision ~0.45 mg L−1 for a 15 mg L−1 standard; LOD ~0.5 mg L−1.
- Data quality indicators:
  - All measurements accompanied by individual error terms (e.g., NH4_Error, NO3_Error, NO2_Error, CO2_Error, CH4_Error, N2O_Error, DOC_Error, isotopic errors).
  - Some samples lack isotope data due to insufficient nitrate (NA entries).
  - Field sampling occasionally constrained by conditions (e.g., difficult piezometer sampling, negative pressure preventing gas sample collection).

## Data Structure and Files

- Two CSV files comprise the dataset:
  - In-situ_carbon_and_nitrogen_data (27 columns)
    - Key fields: Piezo_ID, Depth, Sediment_Type, Season, Reach, Dissolved_Oxygen, Temperature, CO2, CO2_Error, CH4, CH4_Error, N2O, N2O_Error, NH4, NH4_Error, NO3, NO3_Error, NO2, NO2_Error, DOC, DOC_Error, d15N_NO3+NO2-, d15N_NO3+NO2-_Error, d18O_NO3+NO2-, d18O_NO3+NO2-_Error, d13C_CO2, d13C_CO2_Error.
  - In-situ_DET_gel_data (11 columns)
    - Key fields: Gel_ID, Depth, Season, NH4, NH4_Error, NO3, NO3_Error, d15N_NO3+NO2-, d15N_NO3+NO2-_Error, d18O_NO3+NO2-, d18O_NO3+NO2-_Error.
- Data notes:
  - Units include mg L−1 for most dissolved species, μmol L−1 or mg N L−1 for nitrogen species, mg C L−1 for DOC, and per mil for isotopic ratios.
  - Some entries marked NA where isotope analysis was not possible due to insufficient nitrate.
  - Some field entries indicate sampling challenges (e.g., negative pressure preventing gas sample collection).

## Provenance, References, and Data Use

- References underpinning analytical methods and isotopic techniques:
  - Antweiler et al. 1996; Casciotti et al. 2002; Kaiser et al. 2007; Sigman et al. 2001; Wilhelm et al. 1977; Hudson 2004.
- Data provenance:
  - Field measurements linked to lab analyses with traceable instrument settings, calibration data, and reference materials to support reproducibility.
  - Detailed metadata on sampling depth, sediment type, season, and reach enhances data discoverability and interoperability.

## Data Governance Implications for Data Stewards

- Standards and interoperability:
  - Clearly defined field and laboratory methods, consistent units, and standardized metadata facilitate reuse and integration with other datasets.
- Metadata and documentation:
  - Comprehensive method descriptions, calibration protocols, QA metrics, and references support data lineage and trust.
- Quality assurance and uncertainty:
  - Per-measurement error fields, LODs, and accuracy/precision figures enable robust data quality assessment and uncertainty propagation.
- Data accessibility and structure:
  - Two well-documented CSV files with explicit column definitions and NA handling improve discoverability and downstream processing.
- Limitations and transparency:
  - Documented data gaps (e.g., NA isotope values, sampling constraints) provide essential context for researchers and data managers.
- Recommendations for stewardship:
  - Maintain versioning and changelogs for dataset updates; preserve instrument settings and calibration curves; ensure long-term storage of reference materials and in-house standards; provide machine-readable metadata alongside the CSVs for automated integration.