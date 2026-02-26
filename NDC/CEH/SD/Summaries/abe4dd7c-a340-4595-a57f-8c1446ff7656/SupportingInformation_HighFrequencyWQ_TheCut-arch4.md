# Hourly physical and nutrient monitoring data for The Cut, Berkshire (2009-2012) - Supporting Information

- Overview
  - Provides hourly physical and nutrient monitoring data for The Cut at Bray Marina, Berkshire, UK.
  - Main dataset period: May 2010 to February 2012; accompanying supporting information covers 2009-2012.
  - Parameters: total reactive phosphorus (TRP), total phosphorus (TP), ammonium (NH4), conductivity, temperature, dissolved oxygen (DO), pH, chlorophyll; plus hourly averaged flow data.

- Monitoring site and data sources
  - Location: Bray Marina, The Cut, Berkshire; grid reference SU915786.
  - Flow data: 15-minute flow measurements from the Environment Agency gauging station on The Cut at Binfield (approximately 10 km upstream); hourly averages are provided and referenced as SU853713, in cubic metres per second.
  - Instruments: 
    - Hach Lange Sigmatax for sampling probe and automation.
    - Phosphax Sigma for in situ TP and TRP analysis.
    - YSI 6600 sonde for in situ measurements (DO, pH, temperature, conductivity, turbidity, chlorophyll).

- Monitoring setup and procedures
  - Instrument housing: trailer unit ~5 m from riverbank; continuous pumping from river center into a flow cell; probes placed in flow cell.
  - Sample handling: 10 mL sub-sample transferred to Phosphax Sigma after homogenisation by Sigmatax.
  - Analysis methods:
    - TP: acid persulphate digestion with colorimetric detection after heating to 140 C; TRP: phosphomolybdenum blue complexation.
    - Detection limits: 0.01 mg P L-1 for both TP and TRP.
  - YSI measurements: in situ readings every hour; turbidity via light scattering (NTU); chlorophyll via fluorometer (470 nm) reported as μg/L.
  - Calibration and quality control:
    - Phosphax Sigma: automated daily calibration; no filtration step.
    - YSI 6600: calibration every 2–3 weeks by Environment Agency staff following SOPs.
  - Environmental controls: trailer heated to 20 C to maintain reaction temperatures and prevent frozen pipes.

- Data format, units, and time stamps
  - Time format: day/month/year hour:minute.
  - Flow data: hourly average of the 4 observations within each hour from the Binfield gauging station; units in cubic metres per second.
  - Concentrations:
    - TP and TRP: mg/L as phosphorus.
    - NH4: mg/L as nitrogen.
    - Turbidity: NTU (temperature-compensated).
    - Chlorophyll: μg/L (total chlorophyll a, b, and c).

- Data quality, limitations, and notes
  - Interference: chlorophyll readings subject to optical interference from sediment; corrections applied via comparison with turbidity data.
  - Data gaps: missing data points represented as NaN.
  - Sensor interference and data interpretation: turbidity and fluorescence measurements may be affected by sediment; correlation with grab samples used to validate chlorophyll readings.
  - No filtration in analysis pipeline; automated daily calibration and standard solution validation employed.

- Metadata and references
  - Precise coordinates and references:
    - Bray dataset location: SU915786.
    - Upstream flow reference station: SU853713 (Binfield).
  - Related literature:
    - Wade et al., 2012: Hydrochemical processes in lowland rivers—insights from in situ high-resolution monitoring.
    - Halliday et al., 2015: High-frequency water quality monitoring in an urban catchment—hydrochemical dynamics and implications for Water Framework Directive.
    - Supporting Information: Hourly physical and nutrient monitoring data for The Cut, Berkshire (2009-2012), April 2015.