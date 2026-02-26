# Hourly physical and nutrient monitoring data for The Cut, Berkshire (2009-2012) - Supporting Information

## Overview
- Dataset of hourly physical and nutrient measurements from The Cut at Bray Marina, Berkshire, UK (grid reference SU915786), covering May 2010 to February 2012; accompanying hourly averaged flow data from the Environment Agency gauge at The Cut at Binfield (about 10 km upstream).
- Supporting information accompanying related publications; additional context notes reference data spanning 2009–2012.

## Data content
- Measured parameters (hourly): 
  - Total reactive phosphorus (TRP)
  - Total phosphorus (TP)
  - Ammonium (NH4) expressed as N, mg/L
  - Conductivity
  - Temperature
  - Dissolved oxygen (DO)
  - pH
  - Chlorophyll (in μg/L; total of types a, b, and c)
- Flow data: hourly averages of 15-minute flow measurements from the Binfield gauging station (upstream), in m³/s.
- Data format: time given as day/month/year hour:minute; missing data indicated as NaN.

## Monitoring methods and instrumentation
- Instruments:
  - Hach Lange Sigmatax and Phosphax Sigma for high-frequency TP and TRP analysis.
  - YSI 6600 sonde for in situ DO, pH, temperature, conductivity, turbidity, and chlorophyll.
- Setup:
  - Instruments housed in a trailer 5 m from the riverbank; sampling flow cell fed by submersible pump from the river center.
  - Sigmatax homogenizes sample; 10 mL sub-sample sent to Phosphax Sigma for TP/TRP analysis.
  - TP: acid persulphate digestion (140 °C, 359 kPa) with colorimetric detection.
  - TRP: phosphomolybdenum blue method.
  - No sample filtration.
  - Automated daily calibration of Phosphax Sigma.
  - Trailer temperature maintained at 20 °C with three tubular heaters to ensure consistent reactions.
- YSI 6600 measurements:
  - In situ measurements of DO, pH, temperature, conductivity, turbidity (NTU), and chlorophyll (fluorometer at 470 nm).
  - Turbidity is temperature-compensated; chlorophyll data may be impacted by sediment fluorescence but correlated with grab-sample chlorophyll; interference accounted for in analysis via comparison with turbidity.
  - YSI sensors calibrated every 2–3 weeks following standard procedures.

## Data formats and units
- Time reference: day/month/year hour:minute.
- Flow: hourly average of 15-minute flows, units in cubic metres per second (m³/s).
- TP and TRP: mg/L (concentration of phosphorus).
- Ammonium (NH4): mg/L as nitrogen.
- Turbidity: NTU (nephelometric turbidity units), temperature-compensated.
- Chlorophyll: μg/L (total chlorophyll a, b, c).

## Temporal coverage and location
- Main dataset: May 2010 – February 2012 (The Cut at Bray Marina, SU915786).
- Upstream flow reference: The Cut at Binfield gauge (approx. 10 km upstream), grid reference SU853713.
- Supporting information notes broader 2009–2012 context for hourly physical and nutrient monitoring data of The Cut, Berkshire.

## Data quality, calibration, and caveats
- Daily automated calibration of the Phosphax Sigma; no filtration step applied.
- Chlorophyll measurements subject to possible optical interference from sediment; mitigated by cross-checking with turbidity data.
- 15-minute flow data used to produce hourly flow values; accuracy depends on upstream measurement and averaging procedure.
- Data may contain NaN values representing missing observations.

## Related literature and usage
- References for hydrochemical processes and high-frequency water quality monitoring in urban catchments:
  - Wade et al. (2012) on hydrochemical processes in lowland rivers using high-resolution in situ monitoring.
  - Halliday et al. (2015) on high-frequency water quality monitoring and its implications for the Water Framework Directive.
- Supporting Information published April 2015.