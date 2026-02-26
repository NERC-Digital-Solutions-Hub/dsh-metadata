# Brief description of the dataset

## Overview
- High-frequency monitoring dataset for the River Enborne near Brimpton (National grid reference SU568648).
- Timeframe: November 2009 to February 2012.
- Parameters: total reactive phosphorus (TRP), nitrate (NO3), conductivity, temperature, dissolved oxygen, pH, chlorophyll.
- Includes hourly measurements and accompanying hourly averaged flow data from the nearby Environment Agency gauging station.
- Designed to support studies of phosphorus and nitrate inputs and river water quality in rural lowland systems.

## Monitoring setup and methods
- Instruments:
  - Micromac C automated nutrient analyser for TRP.
  - YSI 6600 sonde for DO, pH, temperature, conductivity, turbidity, chlorophyll.
  - Nitratax Plus probe for NO3.
- Deployment: instruments housed in a heated shed near the river; water pumped intermittently to minimize sediment disturbance and turbidity interference.
- Calibration and QC:
  - TRP checked daily with a standard; reagents changed fortnightly; TRP cross-checked with manual laboratory analyses (Seal AA3).
  - Nitrate checked against weekly laboratory ion chromatography.
  - YSI sensors calibrated every 2–3 weeks by trained staff.
  - Interference from turbidity accounted for in chlorophyll readings; turbidity readings temperature-compensated.
- Flow data: 15-minute measurements from the adjacent gauging station, averaged hourly for the dataset.
- Temperature control kept at 20°C to minimize reaction and sampling temperature effects.

## Data format and content
- Time format: day/month/year hour:minute.
- Flow: hourly average in cubic metres per second (m3/s).
- TRP: concentration in mg P L-1 (unfiltered, total reactive phosphorus; includes orthophosphate and readily hydrolysable P).
- Nitrate: concentration in mg NO3 per litre.
- Turbidity: nephelometric turbidity units (NTU), temperature-compensated.
- Chlorophyll: μg L-1 (total chlorophyll a, b, c) from fluorescence readings.
- Missing data: NaN indicates gaps.
- Notes: TRP represents an operational definition; 06:00:00 GMT TRP sample missing due to standard measurement timing.

## Data quality, validation, and caveats
- Cross-validation with laboratory analyses for TRP and nitrate enhances reliability.
- Frequent calibration and standard checks reduce measurement drift.
- Turbidity and sediment can affect chlorophyll readings; corrections/interpretations acknowledge this.
- Data gaps exist (e.g., specific TRP timestamp missing) due to standard procedures.

## Context, provenance, and references
- Related publications for context and methodology:
  - Bowes et al. 2015 (Science of The Total Environment): phosphorus and nitrate inputs to a rural river using high-frequency data.
  - Halliday et al. 2014 (Water): high-frequency observations of River Enborne water quality.
  - Wade et al. 2012 (Hydrology and Earth System Sciences): hydrochemical processes from in situ high-resolution monitoring.
- Location detail: River Enborne at Brimpton; site coordinates inferred from grid reference SU568648.