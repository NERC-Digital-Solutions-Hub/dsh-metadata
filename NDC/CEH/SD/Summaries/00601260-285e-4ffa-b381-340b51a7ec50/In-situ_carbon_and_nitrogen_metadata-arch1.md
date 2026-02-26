# Fieldwork Protocol

## Overview
- Describes field sampling of surface water and multilevel piezometers to measure nutrients, greenhouse gases, and isotopic compositions.
- Aims to analyse carbon and nitrogen cycling processes (e.g., nitrification, denitrification) and relate porewater chemistry to streambed conditions.

## Field Sampling Design and Procedures
- Water samples collected manually from surface water and multilevel piezometers at depths of 10 cm and 20 cm using a syringe.
- In-situ measurements: dissolved oxygen (DO) and temperature recorded immediately after collection (YSI ProODO or EcoSense ODO200).
- Water samples filtered sequentially (0.45 µm then 0.22 µm Thames Resteck nylon) and frozen until analysis.
- Diffusive equilibrium in thin-film (DET) gels deployed upstream in the sandy reach and mid-stream in the sandy reach at least 72 hours before sampling; gels removed at sampling, sliced at 2.5 cm intervals within ~25 minutes, stored cold (4 °C) until lab back-equilibration.
- Porewater gas samples produced in situ via headspace equilibrium: 7 mL water + 14 mL ultrapure helium shaken for 2 minutes; headspace captured in a pre-evacuated 12 mL exetainer and stored in the dark at room temperature until analysis.

## Laboratory Analyses and Isotopic Methods
- Gel and water samples processed to determine dissolved and isotopic compositions.
- Isotopic analyses:
  - δ15NNO3+NO2 and δ18O NO3+NO2 via the denitrifier method (EA/IRMS setup described).
  - δ13CCO2 via isotope ratio mass spectrometry after preconcentration and drying steps.
- Instrumentation:
  - Nutrients and DOC: continuous flow analyzer (Skalar San++) and Shimadzu TOC-L CPH with ASI-L autosampler.
  - Gases: GC-GC detectors (ECD for N2O, FID for CH4, TCD for CO2) with headspace-derived concentrations converted to porewater using Henry’s constant.
  - Isotopes: GEO 20:20 IRMS for δ15N and δ18O; Isoprime IRMS for δ13C.
- Calibration and sample processing details cover multiple instruments and steps (see Calibration and Quality Control section).

## Calibration, Quality Control, and Performance
- Gas chromatography calibrations:
  - July N2O GC-ECD: four-point zero and external standard (0, 1.6, 3.1, 6.2 ppm) with drift corrections; accuracy ~0.1, precision ±0.2, LOD ~5.6e-3 ppm.
  - Other N2O analyses: four-point calibration with external standards (10, 50, 100 ppm); accuracy ~0.1, precision ±1.75 ppm; LOD ~5.6e-3 ppm.
  - CH4 GC-FID: three-point calibration (15,000, 30,000 ppm) with accuracy ~275 ppm, precision ~326 ppm; LOD ~0.5 µg/L.
  - CO2 GC-TCD: zero, 15,000, 30,000 ppm; LOD ~0.5 mg/L.
- NH4+, NO3-, NO2-: continuous flow analyzer calibration with 0.02–5 mg N/L standards; accuracy/precision ~0.03–0.06 mg N/L; LOD ~0.02–0.05 mg N/L per ion.
- TOC: daily calibration with low/medium/high curves; accuracy ~0.16 mg/L, precision ±0.45 mg/L for a 15 mg/L standard; LOD 0.5 mg/L.
- δ15NNO3- and δ18ONO3-: calibrated with international references (USGS 34/35, IAEA NO3-), in-house river-water nitrate standard; long-term precision ~±0.3 to ±0.4 ‰ (NO3), international references ~0.11–0.19 ‰ (NO3), etc.
- δ13CCO2: calibrated against CO2-heavy standard (NIST 8562); precision ≥ ±0.12 ‰.
- DO and temperature: YSI ProODO and EcoSense ODO200 with factory calibration; 100% air-saturation calibration for in-field reference.
- General notes: regular measurement checks, blanks, and standards to correct for drift and baseline shifts; multiple references used to ensure measurement reliability.

## Data Structure and Recorded Values
- Two CSV files included:
  - In-situ_carbon_and_nitrogen_data (27 columns)
    - Key fields: Piezo_ID (sampling location), Depth (cm), Sediment_Type, Season, Reach, Dissolved_Oxygen (mg/L), Temperature (°C), CO2 (mg/L), CO2_Error, CH4 (mg/L), CH4_Error, N2O (µg/L), N2O_Error, NH4 (mg N/L), NH4_Error, NO3 (mg N/L), NO3_Error, NO2 (mg N/L), NO2_Error, DOC (mg C/L), DOC_Error, d15N_NO3+NO2- (per mil), d15N_NO3+NO2-_Error, d18O_NO3+NO2- (per mil), d18O_NO3+NO2-_Error, d13C_CO2 (per mil), d13C_CO2_Error.
  - In-situ_DET_gel_data (11 columns)
    - Key fields: Gel_ID, Depth (cm), Season, NH4 (mg N/L), NH4_Error, NO3 (mg N/L), NO3_Error, d15N_NO3+NO2- (per mil), d18O_NO3+NO2- (per mil), (and associated errors for isotopes as provided in file).
- Notes on data quality:
  - Some samples lack isotope data when nitrate concentrations were insufficient (NA entries).
  - Field sampling can encounter difficulties (e.g., negative pressure preventing gas sampling) leading to missing gas data.

## Field and Laboratory Workflow Summary
- Deploy DET gels at strategic upstream and mid-stream locations; sample after 72 hours.
- Collect and process water and gel samples for nutrient, dissolved gas, and isotopic analyses.
- Use headspace gas sampling to infer porewater concentrations; convert to porewater values with Henry’s constant.
- Apply rigorous calibration and quality control across all instruments; document uncertainties and detection limits.
- Structure data into two comprehensive CSV files with detailed metadata and measurement errors to enable downstream statistical analyses and modeling.

## References
- Antweiler, R. C., Patton, C. J. and Taylor, H. E. 1996. Automated, colorimetric methods for determination of nitrate plus nitrite, nitrite, ammonium and orthophosphate ions in natural water samples. USGS Report. 93-638, 1-23.
- Casciotti, K. L., Sigman, M., Hastings, M. G., Böhlke, J. K. and Hilkert, A. 2002. Measurement of the oxygen isotopic composition of nitrate in seawater and freshwater using the dentirifier method. Anal. Chem. 74, 4905-4912.
- Hudson, F. 2004. Sample Preparation and Calculations for Dissolved Gas Analysis in Water Samples Using a GC Headspace Equilibration Technique. EPA Standard Operating Procedure (unapproved).
- Kaiser, J., Hastings, M. G., Houlton, B. Z., Röckmann, T. and Sigman, D. M. 2007. Triple Oxygen Isotope Analysis of Nitrate Using the Denitrifier Method and Thermal Decomposition of N2O. Anal. Chem. 79, 599-607.
- Sigman, D. M., Casciotti, K. L., Andreani, M., Barford, C., Galanter, M. and Böhlke, J. K. 2001. A Bacterial Method for the Nitrogen Isotopic Analysis of Nitrate in Seawater and Freshwater. Anal. Chem. 73, 4145-4153.
- Wilhelm, E., Battino, R. and Wilcock, R. J. 1977. Low-Pressure Solubility of Gases in Liquid Water. 77(2), 219-262.