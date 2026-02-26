# Fieldwork Protocol

- Field procedures encompass sampling of surface water and multilevel piezometers, deployment and retrieval of DET gels, in-situ gas sampling, and laboratory analyses of nutrients, carbon, nitrogen species, and isotopes.
- Two complementary datasets are produced: in-situ carbon and nitrogen concentrations with isotopic data, and in-situ DET gel measurements with accompanying isotopic data.

## Field Sampling and In-situ Measurements

- Water samples collected manually from surface water and at 10 and 20 cm depths in multilevel piezometers using syringes.
- Immediate in-situ measurements:
  - Dissolved oxygen (mg/L) and temperature (°C) using YSI ProODO or EcoSense ODO200.
- Sample handling:
  - Water samples filtered sequentially (0.45 μm then 0.22 μm Thames Resteck nylon) and frozen until analysis.
- DET gel deployment:
  - DET gels placed with multilevel piezometers in upstream and mid-stream sandy reaches at least 72 hours before sampling.
  - Gels removed at sampling, sliced at 2.5 cm intervals within ~25 minutes, stored cold (4 °C) until laboratory back-equilibration.
- Porewater gas sampling in-situ:
  - Headspace equilibration method: 7 mL water + 14 mL ultrapure He drawn into a syringe, shaken 2 minutes, headspace captured in a pre-evacuated 12 mL exetainer, stored in dark at room temperature until analysis.

## DET Gels and Porewater Sampling Details

- Gel slice volume determination by weighing each DET gel slice and assuming 95% water content (saturated gel).
- Elution of solutes from gel slices:
  - Add 5 mL ultrapure water, shake for 24 hours on ice, collect eluate and freeze for analysis.
- In-lab isotopic analyses:
  - δ15NNO3+NO2 and δ18ONNO3+NO2 via the denitrifier method.
  - δ13CCO2 via isotope ratio mass spectrometry after preconcentration and CO2 purification steps.
- Sample preparation for nitrate/nitrite isotopes:
  - Adjust aqueous sample to ~2 μM NO3 (plus NO2 if present) before denitrifier processing.

## Laboratory Instrumentation and Analyses

- Nutrients and carbon in surface water, porewater, and DET gels:
  - Continuous flow analyser (Skalar San++) for NH4+, NO3−, NO2−.
  - TOC analyzer (Shimadzu TOC-L CPH with ASI-L) for DOC.
  - Gas chromatography (GC) with detectors:
    - Micro Electron Capture Detector (μECD) for N2O.
    - Flame Ionisation Detector (FID) for CH4.
    - Thermal Conductivity Detector (TCD) for CO2.
  - Headspace concentrations converted to porewater using Henry’s law.
- Isotopic analyses:
  - δ15NNO3+NO2− and δ18ONNO3+NO2− via GC-IRMS (GEO 20:20).
  - δ13CCO2 via IRMS (Isoprime).
- Analytical specifics:
  - Instruments calibrated with appropriate standards prior to analyses; different concentration ranges and gas volumes handled by each method.

## Calibration, QA/QC, and Performance

- N2O analyses (GC-μECD):
  - July samples: four-point calibration with zero and 1.6, 3.1, 6.2 ppm standards; drift checks with external standard; LOD and performance metrics documented.
  - Other samples: four-point calibration with zero and 10, 50, 100 ppm; drift corrections applied; LOD and accuracy reported.
- CO2 (TCD) calibrations:
  - Three-point calibration with 15,000 and 30,000 ppm standards; periodic checks; LOD and accuracy reported.
- CH4 (FID) calibrations:
  - Four-point calibration with 100, 1,000, 10,000, 100,000 ppm; periodic checks; LOD and accuracy reported.
- Nutrients (Skalar San++):
  - Daily calibration with ten standards (0.02–5 mg N/L) and external references for NH4+, NO3−, NO2−; reported accuracy and precision.
  - LODs for NH4+, NO3−, NO2− provided.
- TOC (Shimadzu TOC-L CPH with ASI-L):
  - Daily calibration with multiple curves across low/medium/high ranges; accuracy and precision specified; LOD 0.5 mg/L.
- Isotope measurements:
  - GEO 20:20 calibrated with USGS and IAEA standards; in-house references used for long-term precision; reported precision values for both 15N and 18O in NO3−.
  - 500 ppm CO2 standard calibrated against CO2-heavy reference (NIST 8562); precision reported.
- Temperature and oxygen sensors:
  - YSI ProODO and EcoSense ODO200 calibrated per factory guidance; 100% air-saturation calibration used for field conditions.

## Data Structure and Recorded Values

- Two CSV files:
  - In-situ_carbon_and_nitrogen_data:
    - Piezo_ID (surface water indicated by SW), Depth (cm), Sediment_Type, Season, Reach.
    - Dissolved_Oxygen (mg/L), Temperature (°C), CO2 (mg/L), CO2_Error, CH4 (mg/L), CH4_Error, N2O (μg/L), N2O_Error.
    - NH4 (mg N/L), NH4_Error, NO3 (mg N/L), NO3_Error, NO2 (mg N/L), NO2_Error.
    - DOC (mg C/L), DOC_Error, d15N_NO3+NO2 (‰), d15N_NO3+NO2_Error, d18O_NO3+NO2 (‰), d18O_NO3+NO2_Error, d13C_CO2 (‰), d13C_CO2_Error.
  - In-situ_DET_gel_data:
    - Gel_ID, Depth (cm), Season.
    - NH4 (mg N/L), NH4_Error, NO3 (mg N/L), NO3_Error.
    - d15N_NO3+NO2 (‰), d15N_NO3+NO2_Error, d18O_NO3+NO2 (‰), d18O_NO3+NO2_Error.
- Notes:
  - Some samples lack sufficient nitrate for isotope analysis (NA recorded).
  - Occasional sampling difficulties required negative pressure in piezometers; no gas samples collected in those cases.

## Practical Considerations and Data Governance

- Data quality and transparency are supported by:
  - Comprehensive calibration records, method references, and instrument performance metrics.
  - Public sharing of underlying datasets where feasible, with detailed metadata and unit definitions.
  - Clear documentation of data structure, measurement depths, seasonal contexts, and sampling reaches to enable comparability across time and sites.
- The methodology integrates surface water and porewater signals (via DET gels and headspace equilibration) to inform environmental health monitoring and policy-relevant decisions.
- References provide established protocols for isotopic analyses and nitrate/nitrite/nitrogen cycling measurements, ensuring methodological rigor and reproducibility.

## References

- Antweiler, R. C., Patton, C. J. and Taylor, H. E. 1996. Automated, colorimetric methods for determination of nitrate plus nitrite, nitrite, ammonium and orthophosphate ions in natural water samples. USGS Report. 93-638, 1-23.
- Casciotti, K. L., Sigman, M., Hastings, M. G., Böhlke, J. K. and Hilkert, A. 2002. Measurement of the oxygen isotopic composition of nitrate in seawater and freshwater using the denitrifier method. Anal. Chem. 74, 4905-4912.
- Hudson, F. 2004. Sample Preparation and Calculations for Dissolved Gas Analysis in Water Samples Using a GC Headspace Equilibration Technique. EPA Standard Operating Procedure (unapproved).
- Kaiser, J., Hastings, M. G., Houlton, B. Z., Röckmann, T. and Sigman, D. M. 2007. Triple Oxygen Isotope Analysis of Nitrate Using the Denitrifier Method and Thermal Decomposition of N2O. Anal. Chem. 79, 599-607.
- Sigman, D. M., Casciotti, K. L., Andreani, M., Barford, C., Galanter, M. and Böhlke, J. K. 2001. A Bacterial Method for the Nitrogen Isotopic Analysis of Nitrate in Seawater and Freshwater. Anal. Chem. 73, 4145-4153.
- Wilhelm, E., Battino, R. and Wilcock, R. J. 1977. Low-Pressure Solubility of Gases in Liquid Water. 77(2), 219-262.