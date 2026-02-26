# Continuous measurements of conductivity, dissolved oxygen, pH, temperature and water level in rivers (2002-2007) [LOCAR] LOCAR BASELINE DATASETS LOCAR

## Overview
- LOCAR baseline dataset recording continuous river water quality and level at 23 sites across the Frome/Piddle, Pang/Lambourn, and Tern catchments from 2002 to 2007.
- Measurements were taken at 15-minute intervals, with data collection length varying by site.
- Sited co-located with Environment Agency monitoring sites; some align with NRFA river flow stations.

## Measured parameters and units
- Conductivity at 25°C: microsiemens per centimetre (uS/cm)
- Dissolved oxygen: percent saturation (% sat)
- pH: pH units
- Temperature: degrees Celsius (°C)
- Water level: millimetres (mm)

## Site coverage and catchments
- 23 LOCAR water quality sampling (LCWQ) sites across three catchments:
  - Frome/Piddle (FP)
  - Pang/Lambourn (PL)
  - Tern (TE)
- Example sites include Bere Stream (FP01), Frome at East Stoke (FP11), Piddle at Baggs Mill (FP21), Tern at Ternhill (TE05), Bailey Brook at Ternhill (TE22); TE05 and TE22 share the same location.
- NRFA station references included for some sites (e.g., Frome at East Stoke Part of 44001; Pang at Bucklebury NRFA 39115).

## Instrumentation and deployment
- Water quality: YSI 6-Series multi-parameter sondes (Sensor: temperature, pH, conductivity, dissolved oxygen)
  - Temperature sensor: thermistor, -5 to 45°C, ±0.15°C, 0.01°C resolution
  - pH sensor: glass electrode, 0-14 pH, ±0.2 pH, 0.01 pH resolution
  - Conductivity sensor: 0–100 mS/cm, ±0.5% of reading + 0.001 mS/cm, 0.001 to 0.1 mS/cm resolution
  - DO sensor: Clark-type, 0–500% saturation, various accuracy depending on range, 0.1% resolution
- Water level: Druck PDCR 1830 pressure transducers (0.75 to 600 mH2O range; ±0.06% accuracy)
- Maintenance: Catchment Service Team installed, maintained, and downloaded data; data are raw, not quality controlled in this document.

## Calibration and maintenance procedures
- Pre-deployment and field calibration:
  - DO: saturate membrane in moist air, calibrate to 100% air saturation; record DO concentration and saturation
  - Conductivity: calibrate with standard conductivity solution (approx. 1413 µS)
  - pH: calibrate with pH buffers (pH 7.0 and pH 10.0)
- Cleaning and preparation:
  - Clean sonde body, guard, pH glass surface, and conductivity cell
  - Replace DO membrane, allow conditioning time (12 hours) before final calibration
- Post-field deployment checks:
  - Recalibrate DO, conductivity, and pH using standard procedures
- Calibration references and software:
  - YSI EcoWatch software used for data collection and calibration
  - Post-deployment calibration checks documented for data quality assessment

## Data quality and limitations
- Data are raw and not quality controlled or corrected for instrument failure or drift.
- General observed issues:
  - Substantial scatter in determinands; some periods where data are unreliable
  - Battery level below 10 V often indicates unreliable data for all determinands
  - DO readings above ~200% or near 0% saturation are unlikely/unreliable in practice
  - pH values outside 1–14; values above 11 or below 4 may be unreliable
  - Temperature generally sensible (0–30°C); very anomalous values warrant investigation
  - Conductivity and water level are site-specific; typical normal ranges noted for context
- Normal reference ranges (Chapman 1996) used as context:
  - Temperature: 0–30°C
  - pH: 6.0–8.5
  - Conductivity: 10–1000 µS/cm
  - Dissolved oxygen: 0–20 mg/L
- Visual quality checks via box-and-whisker plots highlighted:
  - Outliers and data gaps
  - Reliability indicators linked to battery status

## Additional notes for GIS and data users
- Site identifiers and NRFA connections provided, enabling spatial joins with other hydrological datasets.
- Two sites share identical locations (TE05 and TE22), which is relevant for mapping and avoiding duplicate point representations.
- The dataset provides a rich, high-resolution temporal view (15-minute intervals) suitable for spatially-aware analyses of water quality dynamics across multiple catchments.