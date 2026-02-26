# Hourly physical and nutrient monitoring data for The Cut, Berkshire (2009-2012) - Supporting Information

## Overview
- Dataset of hourly physical and nutrient water quality data for The Cut at Bray Marina, Berkshire, UK (May 2010 – February 2012; Grid reference SU915786) with accompanying hourly flow data from the The Cut at Binfield gauging station (~10 km upstream; grid reference SU853713).
- Measured parameters: total phosphorus (TP), total reactive phosphorus (TRP), ammonium (NH4 as N), conductivity, temperature, dissolved oxygen, pH, chlorophyll, and turbidity (NTU).
- Flow data: fifteen-minute flow measurements aggregated to hourly averages.

## Monitoring setup and data collection
- Instruments:
  - Hach Lange Sigmatax and Phosphax Sigma for high-frequency TP and TRP analysis (in situ).
  - YSI 6600 sonde for in situ DO, pH, temperature, conductivity, turbidity, and chlorophyll.
- Deployment: instruments housed in a trailer 5 m from the riverbank; continuous water supply from river center to a flow cell in the trailer.
- Sample handling:
  - 10 mL sub-samples transferred to Phosphax Sigma for analysis.
  - TP measured colorimetrically after acid persulphate digestion (to 140°C, 359 kPa); TRP measured via phosphomolybdenum blue complexation.
  - No filtration step in analysis.
- Calibration and temperature control:
  - Phosphax Sigma calibration performed automatically each day.
  - Trailer temperature maintained at ~20°C to ensure reaction temperature stability.
- YSI measurements:
  - Turbidity measured with temperature-compensated light scattering (NTU) at 830–890 nm.
  - Chlorophyll measured by fluorometer (μg/L) at 470 nm; susceptible to sediment-related optical interference, mitigated by correlation with turbidity data.
  - YSI sensors calibrated every 2–3 weeks following standard procedures.

## Data format and measurements
- Time format: day/month/year hour:minute.
- Flow: hourly average derived from four 15-minute observations at Binfield gauging station (upstream ~10 km); units in cubic meters per second (m³/s).
- Concentrations and measurements:
  - TP and TRP: mg/L.
  - Ammonium (NH4 as N): mg/L.
  - Turbidity: NTU.
  - Chlorophyll: μg/L (total; includes types a, b, c).
- Missing data: NaN indicates missing observations.

## Data quality and considerations
- Chlorophyll readings may be affected by sediment-related optical interference; interpret alongside turbidity data.
- No filtration step used in chemical analyses; results depend on in situ digestion and colorimetric methods.
- Regular calibration of instruments; potential inter-instrument drift mitigated by automated daily calibration (Phosphax Sigma) and periodic YSI calibration every few weeks.

## Coverage and references
- Dataset linked to wider hydrological and nutrient‑dynamics research in lowland urban catchments.
- Related literature:
  - Wade et al. (2012) on hydrochemical processes in lowland rivers using in situ high-resolution monitoring.
  - Halliday et al. (2015) on high-frequency water quality monitoring, primary production, and implications for the Water Framework Directive.
  - Supporting Information: Hourly physical and nutrient monitoring data for The Cut, Berkshire (2009-2012) (April 2015).
- Location references:
  - Bray Marina site: SU915786.
  - Upstream flow gauging station: SU853713 (Binfield).

## Practical notes for use
- Suitable for self-service exploration and dashboards (time-series trends, correlations between nutrients and flow, or diel/seasonal patterns).
- Data can support analyses of hydrological and hydrochemical dynamics, and inform Water Framework Directive-related assessments.
- Be mindful of potential data gaps (NaN) and interferences in chlorophyll due to sediment; cross-check with turbidity where possible.