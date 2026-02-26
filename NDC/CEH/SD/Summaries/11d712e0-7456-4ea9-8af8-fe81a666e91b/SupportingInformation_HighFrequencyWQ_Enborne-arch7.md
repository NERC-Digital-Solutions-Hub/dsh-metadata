# Brief description of the dataset

## Overview
- Hourly physical and nutrient monitoring data for the River Enborne near Brimpton (National grid reference SU568648), from November 2009 to February 2012.
- Measured parameters: total reactive phosphorus (TRP), nitrate (NO3), conductivity, temperature, dissolved oxygen (DO), pH, and chlorophyll.
- Includes accompanying hourly averaged flow data from the Environment Agency gauging station at the same site.

## Location and Coverage
- Site: River Enborne at Brimpton, near Brimpton.
- Grid reference: SU568648.
- Time period: November 2009 – February 2012.
- Data resolution: hourly measurements; flow data based on 15-minute intervals, averaged to hourly.

## Data Collection and Instruments
- TRP: Micromac C automated nutrient analyser; colorimetric method (phosphomolybdenum blue).
  - Detection limit: 0.025 mg P L^-1.
  - Daily check standard; fortnightly recalibration when reagents changed.
  - 06:00:00 GMT TRP sample not present.
  - cross-validated against laboratory analysis (Seal AA3).
- Nitrate (NO3): Nitratax Plus probe (UV absorption).
  - Detection limit: 0.07 mg L^-1.
  - Field checks with weekly lab Ion Chromatography.
- YSI 6600 multi-parameter sonde: measures DO, pH, temperature, conductivity, turbidity, and chlorophyll.
  - Turbidity: NTU, temperature-compensated, 830–890 nm scattering.
  - Chlorophyll: μg L^-1 (fluorometer at 470 nm).
  - Calibration: every 2–3 weeks.
- Housing and sampling: insulate in a shed 2 m from riverbank; water pumped from 1 m intake; intermittent pumping to reduce sediment resuspension and turbidity-related errors.
- Temperature control: shed heated to 20°C to stabilise reactions and prevent pipe freezing.
- Flow data: 15-minute flow from EA station; hourly average used in dataset; units: cubic metres per second (m^3/s).

## Parameters, Data Format and Quality
- Time format: day/month/year hour:minute.
- TRP: total reactive phosphorus (unfiltered sample; includes dissolved and acid-extractable particulate P); units: mg P L^-1.
- NO3: nitrate concentration; units: mg L^-1.
- Conductivity, temperature, DO, pH, turbidity, chlorophyll: as measured by respective instruments; units per parameter (e.g., NTU for turbidity; μg L^-1 for chlorophyll).
- Flow: hourly average of 15-minute flows; units: m^3/s.
- Missing data: NaN indicates missing values.
- Special notes: 06:00:00 GMT TRP sample missing; data quality supported by cross-checks with laboratory analyses and referenced studies (Bowes et al. 2015; Halliday et al. 2014; Wade et al. 2012).

## Data Quality and Validation
- TRP validated against manual samples analyzed by a Seal AA3 (same colorimetric method) and reported in Bowes et al. (2015).
- Nitrate validated against weekly lab Ion Chromatography analyses.
- Regular instrument calibration and cross-checks; environmental controls (temperature) to minimise measurement errors.

## Usage in GIS and Spatial-Temporal Analysis
- Georeferenced point data at a single site (River Enborne at Brimpton) suitable for time-series visualization and hydrochemical mapping when integrated with additional sites or catchment-scale layers.
- High-frequency (hourly) data enables temporal-spatial analyses of water quality in relation to flow, runoff events, and hydrological conditions.
- Data can support: concentration-hourly maps along the river network when combined with other sites; flow-normalized spatial analyses; trend and anomaly detection in nutrient and chlorophyll dynamics.

## References
- Bowes MJ, Jarvie HP, Halliday SJ, Skeffington RA, Wade AJ, Loewenthal M, et al. Characterising phosphorus and nitrate inputs to a rural river using high-frequency concentration-flow relationships. Science of The Total Environment 2015; 511: 608-620.
- Halliday S, Skeffington R, Bowes M, Gozzard E, Newman J, Loewenthal M, et al. The Water Quality of the River Enborne, UK: Observations from High-Frequency Monitoring in a Rural, Lowland River System. Water 2014; 6: 150-180.
- Wade AJ, Palmer-Felgate EJ, Halliday SJ, Skeffington RA, Loewenthal M, Jarvie HP, et al. Hydrochemical processes in lowland rivers: insights from in situ, high-resolution monitoring. Hydrology and Earth System Sciences 2012; 16: 4323-4342.