# Fieldwork Protocol

## Overview
- Describes field and laboratory procedures to quantify carbon and nitrogen species in surface water, porewater, and DET (diffusive equilibrium in thin-film) gels.
- Data are produced as two CSV datasets:
  - In-situ_carbon_and_nitrogen_data (27 columns)
  - In-situ_DET_gel_data (11 columns)

## Field Sampling Methods
- Water samples collected manually from surface water and multilevel piezometers at depths of 10 cm and 20 cm using a syringe.
- Dissolved oxygen (DO) and temperature measured immediately after collection using YSI ProODO or EcoSense ODO200.
- Samples filtered sequentially (0.45 μm then 0.22 μm) and frozen for analysis.
- DET gels deployed upstream and mid-stream in sandy reaches at least 72 hours before sampling.
- DET gels removed at porewater sampling, sliced at 2.5 cm intervals within 25 minutes, and stored cold (4 °C) until back-equilibration.

## DET Gel Deployment and Porewater Sampling
- Headspace equilibrium approach used to obtain in-situ gas samples from porewater:
  - 7 mL water + 14 mL ultrapure helium injected into syringe, shaken, headspace collected into a pre-evacuated 12 mL exetainer.
  - Samples stored at room temperature, dark, until analysis.

## In-Situ Measurements and Gas Sampling
- Headspace gas concentrations converted to porewater concentrations using Henry’s constant.
- Gases analyzed include CO2, CH4, and N2O; isotopic analyses performed for nitrate/nitrite and CO2.
- Temperature and DO measured in the field; field samples used for further lab analyses.

## Laboratory Analyses
- Nutrients and related species:
  - Ammonium (NH4), nitrate (NO3), nitrite (NO2) via continuous flow analyser (colorimetry).
  - Dissolved organic carbon (DOC) via Shimadzu TOC analyser (non-purgable OC method).
  - CO2 and CH4 analysed by gas chromatography with FID/TCD detectors.
  - N2O analysed by GC with micro electron capture detector (ECD).
- Isotopic analyses:
  - δ15N of NO3+NO2 and δ18O of NO3+NO2: using the denitrifier method (GC-IRMS).
  - δ13C of CO2: analysed on an isotope ratio mass spectrometer (IRMS).
- Instrumentation:
  - GC-ECD for N2O; GC-FID for CH4; GC-TCD for CO2.
  - Continuous flow analyser for NH4+, NO3−, NO2−.
  - TOC analyser for DOC.
  - IRMS and GC-IRMS for isotopes.

## Calibration and Quality Control
- Daily calibrations with multi-point standards for each instrument; blanks included.
- Specific accuracy, precision, and detection limits reported for each measurement:
  - N2O: GC-ECD calibration with zero and external standards; typical LOD around 5.6e-3 ppm; accuracy and precision specified.
  - CH4: GC-FID calibration with known standards; LOD around 0.5 μg L−1.
  - CO2: GC-TCD calibration with high-ppm standards; LOD ~0.5 mg L−1.
  - NH4+, NO3−, NO2−: San++ analyser with standards; accuracies and precisions in the cited ranges; LODs specified.
  - TOC: calibration with low/medium/high curves; accuracy ~0.16 mg L−1, precision ~0.45 mg L−1; LOD ~0.5 mg L−1.
  - Isotopes: calibration with USGS/IAEA references; long-term precision reported (e.g., ±0.3 to ±0.4‰ for NO3− isotopes).
- Henry’s constant used to convert headspace to porewater concentrations.
- Use of in-house references and international standards to monitor instrument performance.

## Data Produced and File Structure
- Two CSV files:
  - In-situ_carbon_and_nitrogen_data
    - 27 columns including: Piezo_ID, Depth, Sediment_Type, Season, Reach, Dissolved_Oxygen, Temperature, CO2, CO2_Error, CH4, CH4_Error, N2O, N2O_Error, NH4, NH4_Error, NO3, NO3_Error, NO2, NO2_Error, DOC, DOC_Error, d15N_NO3+NO2, d15N_NO3+NO2_Error, d18O_NO3+NO2, d18O_NO3+NO2_Error, d13C_CO2, d13C_CO2_Error.
  - In-situ_DET_gel_data
    - 11 columns including: Gel_ID, Depth, Season, NH4, NH4_Error, NO3, NO3_Error, d15N_NO3+NO2, d15N_NO3+NO2_Error, d18O_NO3+NO2, d18O_NO3+NO2_Error, (and related DET gel isotope fields).
- Data fields cover:
  - Field measurements (temperature, DO), inorganic and organic carbon and nitrogen species, and isotopic ratios.
  - DET gel measurements of NH4, NO3 and their isotopes from 2.5 cm depth intervals.
- Some samples may be NA where insufficient nitrate for isotope analysis was available.
- Notes on data collection challenges:
  - Difficulties sampling piezometers requiring negative pressure; some gas samples not collected.

## Data Fields and Units (Key Examples)
- Temperature: degrees Celsius
- Dissolved Oxygen: mg L−1
- CO2, CH4: mg L−1
- N2O: μg L−1
- NH4, NO3, NO2: mg N L−1
- DOC: mg C L−1
- Isotopes: δ15N_NO3+NO2, δ18O_NO3+NO2, δ13C_CO2 expressed in per mil (‰)
- Errors: corresponding measurement uncertainties (as listed in each column)

## Data Limitations and Considerations for GIS
- Not all samples produced isotope data due to nitrate quantity limitations.
- Some field sampling difficulties can lead to missing gas samples.
- Data originate from multiple sample types (surface water, porewater, DET gels) and may require harmonization for GIS workflows.
- Units and calibration status are instrument-specific; harmonize units across datasets before GIS integration.
- Spatial context is provided by Piezo_ID, Depth, Reach, Sediment_Type, and Season; no explicit geographic coordinates are included, so GIS integration would rely on linking to network/reach geometry.

## GIS-Relevant Applications
- Create map-based representations of carbon and nitrogen dynamics across stream reaches.
- Link water chemistry and isotopic data to sediment types, depths, and seasons to analyze spatial patterns.
- Integrate with continuous surface water data and groundwater exchange models to assess biogeochemical processes in streams.

## References
- Methodological references for isotopic analyses and denitrifier method (e.g., Antweiler et al., Casciotti et al., Kaiser et al., Sigman et al., Wilhelm et al.)