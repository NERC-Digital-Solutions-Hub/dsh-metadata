# Continuous   measurements   of   conductivity,   dissolved   oxygen,   pH,   temperature and water level in rivers (20022007) [LOCAR] LOCAR BASELINE DATASETS LOCAR

## Overview
- LOCAR programme sensors collected continuous river data at 23 sites across the Frome, Piddle, Pang, Lambourn and Tern catchments from 2002 to 2007.
- Variables measured: conductivity, dissolved oxygen (DO), pH, water temperature, and water level.
- Data were captured every 15 minutes, with site-specific deployment durations.

## Measurements and instruments
- Water quality: YSI 6-Series multi-parameter sondes measuring
  - Temperature (units: °C)
  - pH (pH units)
  - Conductivity (units: µS/cm at 25°C)
  - Dissolved Oxygen (percentage of saturation, % sat)
- Water level: Druck pressure transducers (PDCR 1830) for water depth (units: mm; range 0.75 mH2O to 600 mH2O).
- Sondes calibrated and maintained per deployment cycle; data downloaded by Catchment Service Teams.

## Sites and data structure
- Co-located with Environment Agency monitoring sites; some correspond to NRFA registered stations.
- Site codes include FP01, FP02, FP06, FP11, FP12, FP15, FP21, FP22, FP23, FP26, FP31, PL09, PL15, PL17, PL18, PL19, PL20, TE03, TE05, TE09, TE16, TE20, TE22, with FP = Frome/Piddle, PL = Pang/Lambourn, TE = Tern catchments.
- Notable: Tern at Ternhill (TE05) and Bailey Brook at Ternhill (TE22) were at the same location.
- Normal ranges and site-specific context: Conductivity and water level are highly site-specific.

## Calibration, maintenance, and data handling
- Hardware and calibration
  - DO, conductivity, and pH calibration conducted using field routines; calibration steps documented for each parameter.
  - DO calibration involved saturated air exposure and barometric pressure input; conductivity calibrated with a standard solution; pH calibrated with buffer solutions (pH 7 and pH 10).
  - Post-field calibration checks performed upon return to the laboratory.
- Maintenance details
  - Routine cleaning and inspection of sondes and sensors prior to calibration.
  - DO membrane replacement and routine maintenance between deployments.
- Data handling
  - Data stored as raw measurements; no quality control or correction for instrument drift or failure applied in the dataset.
  - Box-and-whisker plots generated to depict range, central tendency, and variability; plots reviewed by senior water quality scientists.

## Data quality and caveats
- Observations from quality review:
  - Generally considerable scatter; some periods produce implausible values.
  - Battery level below 10 V indicates potentially unreliable data.
  - DO values above 200% are possible but unlikely; values near zero possible but uncommon.
  - pH should be within 0–14; values outside typical bounds (e.g., >11 or <4) are considered unreliable.
  - Temperature generally within 5–25°C; extreme values warrant investigation.
  - Conductivity and water level are highly site-specific; typical normal ranges noted (conductivity roughly 200–1200 µS/cm as a general guide).

## Personnel and responsibilities
- Data collection, maintenance, and data download were performed by Catchment Service Teams in each catchment.

## Supporting references and notes
- Normal ranges referenced to Chapman (1996): Water Quality Assessments overview for expected parameter ranges.
- Additional documentation and site layout referenced by Figure 1 and site codes; data context aligns with EA/NRFA site co-location.