# Fieldwork Protocol

## Overview
- Documents field sampling of surface water and multilevel piezometers to analyse chemical and isotopic composition.
- Samples collected and processed to enable laboratory analyses of nutrients, gases, and isotopic ratios.
- Two data products are produced: in-situ carbon/nitrogen measurements and DET gel porewater data.

## Field Sampling Methods
- Water samples collected manually from surface water and piezometers at 10 cm and 20 cm depths using syringes.
- Immediate measurements of dissolved oxygen (DO) and temperature in the field.
- Samples filtered sequentially (0.45 μm then 0.22 μm), then frozen for later analysis.
- Diffusive equilibrium in thin-film (DET) gels deployed at upstream and mid-stream sandy reaches at least 72 hours before sampling; gels removed at porewater sampling, sliced at 2.5 cm intervals within ~25 minutes, and stored cold until back-equilibration in the lab.
- In-situ gas sampling from porewater used a headspace equilibrium method: 7 mL water + 14 mL ultrapure helium drawn into a syringe, shaken, headspace collected into a pre-evacuated 12 mL exetainer, stored at room temperature in the dark until analysis.

## Laboratory Analyses (Preparation and Imaging)
- Gel slices weighed to determine water volume; gels eluted with 5 mL ultrapure water and shaken on ice for 24 hours; eluate frozen for analysis.
- Isotopic analysis of δ15NNO3+NO2 (nitrogen) and δ18ONO3+NO2 (oxygen) performed with the denitrifier method (Casciotti et al., 2002; Kaiser et al., 2007; Sigman et al., 2001) using a GEO 20:20 IRMS.
- δ13CCO2 analysis performed at the Centre for Ecology and Hydrology using Isoprime Isotope Ratio Mass Spectrometry; sample gas preconcentration, water removal, and cryogenic focusing prior to IRMS.

## Instrumentation and Analytical Techniques
- Nutrients and dissolved species: continuous flow analyser (Skalar San++); total organic carbon (TOC) analyzer (Shimadzu TOC-L CPH with ASI-L).
- Greenhouse gases: gas chromatography (GC) with micro-ECD for N2O, FID for CH4, TCD for CO2.
- Headspace concentrations converted to porewater concentrations via Henry’s constant.
- Isotopic analyses: GC-IRDMS (GEO 20:20) for nitrogen and oxygen isotopes; Isoprime IRMS for δ13C.
- Field DO and temperature measured with YSI ProODO and EcoSense ODO200 using factory calibration and a 100% air-saturation check.

## Calibration, Quality Assurance and Performance
- N2O GC-ECD calibrations:
  - July protocol used four-point calibration (0, 1.6, 3.1, 6.2 ppm) with drift corrections; accuracy 0.1, precision ±0.2, LOD 0.08 ppm.
  - Other samples used four-point external standards (0, 10, 50, 100 ppm); accuracy 0.1, precision ±1.75 ppm; LOD 5.6e-3 ppm.
- CO2 (TCD) calibration: daily three-point calibration (15,000 and 30,000 ppm) with reported accuracy 275 ppm, precision ±326 ppm; LOD 0.5 mg/L.
- CH4 (FID) calibration: daily four-point calibration (100, 1,000, 10,000, 100,000 ppm); accuracy 35 ppm, precision ±11 ppm; LOD 0.5 μg/L.
- Skalar San++ nutrient analyzer calibration: ten standards (0.02–5 mg N/L); external references for NH4+, NO3-, NO2-; typical accuracy ~0.03–0.06 mg N/L and precision ~0.02–0.05 mg N/L; LODs 0.02–0.05 mg N/L depending on ion.
- TOC calibrations: daily with low/medium/high method curves; accuracy ~0.16 mg/L, precision ±0.45 mg/L for 15 mg/L standard; LOD 0.5 mg/L.
- Isotope standards and performance: calibrated against USGS 34/35, IAEA NO3-; in-house river NO3- reference for long-term precision; typical in-house precision for δ15N_NO3- ≈ ±0.3‰ and δ18O_NO3- ≈ ±0.4‰; international references provide smaller uncertainties (0.11–0.19‰ for δ15N, 0.19–0.59‰ for δ18O) depending on standard.
- YSI/ODO calibration: factory calibration with one-point 100% air saturation in moist air.

## Data Structure and Variables
- Two CSV data files:
  - In-situ_carbon_and_nitrogen_data (27 columns):
    - Piezo_ID, Depth, Sediment_Type, Season, Reach
    - Dissolved_Oxygen (mg/L), Temperature (°C)
    - CO2 (mg/L) and CO2_Error, CH4 (mg/L) and CH4_Error
    - N2O (μg/L) and N2O_Error
    - NH4 (mg N/L) and NH4_Error
    - NO3 (mg N/L) and NO3_Error
    - NO2 (mg N/L) and NO2_Error
    - DOC (mg C/L) and DOC_Error
    - d15N_NO3+NO2 (per mil) and d15N_NO3+NO2_Error
    - d18O_NO3+NO2 (per mil) and d18O_NO3+NO2_Error
    - d13C_CO2 (per mil) and d13C_CO2_Error
  - In-situ_DET_gel_data (11 columns):
    - Gel_ID, Depth, Season
    - NH4 (mg N/L) and NH4_Error
    - NO3 (mg N/L) and NO3_Error
    - d15N_NO3+NO2 (per mil) and d15N_NO3+NO2_Error
    - d18O_NO3+NO2 (per mil) and d18O_NO3+NO2_Error
- Notes:
  - Some samples lack sufficient nitrate for isotope analysis (RNA: NA).
  - In some piezometers, negative pressure required to collect samples; gas samples may be missing.

## Data Processing and Interpretation
- Headspace gas data converted to porewater concentrations using Henry’s constant.
- Isotopic data calculated for nitrate/nitrite in both water and DET gels.
- DET gels provide depth-resolved porewater chemistry (2.5 cm intervals) to complement surface and piezometer data.
- Data are organized by Piezo_ID or Gel_ID with depth, season, and reach context to support spatial-temporal analyses.

## Data Use and Potential Limitations
- Outputs enable self-serve exploration of carbon and nitrogen dynamics and isotopic signatures in stream environments.
- Potential limitations include patchy data, missing gas samples due to sampling difficulties, and NA values for isotope analyses where nitrate is insufficient.
- Outputs rely on multiple calibration schemes and references; users should account for instrument-specific performance and detection limits when comparing across datasets.

## References
- Antweiler, R. C., Patton, C. J. and Taylor, H. E. 1996. Automated, colorimetric methods for determination of nitrate plus nitrite, nitrite, ammonium and orthophosphate ions in natural water samples. USGS Report. 93-638, 1-23.
- Casciotti, K. L., Sigman, M., Hastings, M. G., Böhlke, J. K. and Hilkert, A. 2002. Measurement of the oxygen isotopic composition of nitrate in seawater and freshwater using the dentirifier method. Anal. Chem. 74, 4905-4912.
- Hudson, F. 2004. Sample Preparation and Calculations for Dissolved Gas Analysis in Water Samples Using a GC Headspace Equilibration Technique. EPA Standard Operating Procedure (unapproved).
- Kaiser, J., Hastings, M. G., Houlton, B. Z., Röckmann, T. and Sigman, D. M. 2007. Triple Oxygen Isotope Analysis of Nitrate Using the Denitrifier Method and Thermal Decomposition of N2O. Anal. Chem. 79, 599-607.
- Sigman, D. M., Casciotti, K. L., Andreani, M., Barford, C., Galanter, M. and Böhlke, J. K. 2001. A Bacterial Method for the Nitrogen Isotopic Analysis of Nitrate in Seawater and Freshwater. Anal. Chem. 73, 4145-4153.
- Wilhelm, E., Battino, R. and Wilcock, R. J. 1977. Low-Pressure Solubility of Gases in Liquid Water. 77(2), 219-262.