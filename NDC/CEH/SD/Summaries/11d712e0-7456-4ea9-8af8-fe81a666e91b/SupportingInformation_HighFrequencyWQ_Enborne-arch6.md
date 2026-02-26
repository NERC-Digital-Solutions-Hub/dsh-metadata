# Brief description of the dataset

## Overview
- Hourly physical and nutrient monitoring data from the River Enborne near Brimpton (National grid reference SU568648) from November 2009 to February 2012.
- Parameters: total reactive phosphorus (TRP), nitrate (NO3), conductivity, temperature, dissolved oxygen, pH, chlorophyll; accompanying hourly flow data from the EA gauging station at the same site.
- Purpose: high-frequency hydrochemical dataset to characterize nutrient inputs and river water quality.

## Data Collected
- TRP: unfiltered, molybdate-reactive phosphorus; operationally defined; detection limit 0.025 mg P/L; TRP mainly contains orthophosphate and readily hydrolysable P species.
- Nitrate: NO3 concentration per liter; measured with Nitratax Plus probe.
- Conductivity, temperature, dissolved oxygen, pH, turbidity, chlorophyll: measured by YSI 6600 sonde; chlorophyll reported as μg/L; turbidity in NTU.
- Flow: 15-minute flow data from the Environment Agency, averaged to hourly flow (m3/s).

## Instrumentation and Sampling Protocol
- TRP: Micromac C automated nutrient analyser (colorimetry); located in a heated shed 2 m from riverbank; intermittent pumping to minimize sediment resuspension; reagents changed fortnightly with daily check standard; TRP cross-validated against manual lab analyses (Murphy and Riley method) in Bowes et al. 2015.
- Nitrate: Nitratax Plus UV absorption probe; calibrated in the lab, periodically checked with standard solutions; cross-validated with weekly lab Ion Chromatography (Bowes et al. 2015).
- Chlorophyll, turbidity, DO, pH, conductance, temperature: measured in situ by YSI 6600 at hourly intervals; turbidity temperature-compensated; chlorophyll measured by fluorometer (470 nm); calibration and maintenance every 2–3 weeks by trained staff.
- Setup details: instrument shed heated to 20°C to reduce temperature-related errors and prevent sampling pipe freezing; intake ~1 m from riverbank; water pumped via intermittent pump to flow cells.

## Data Quality and Validation
- TRP: daily check standard; calibration when reagents changed; cross-checked with laboratory analyses (Bowes et al., 2015).
- Nitrate: validated against weekly laboratory analyses (Ion Chromatography) per Bowes et al., 2015.
- Chlorophyll and turbidity: accounted for potential optical interference from sediment by comparing with turbidity data.
- Data gaps: 06:00:00 GMT TRP sample missing due to the routine check standard measurement.

## Data Format and Units
- Date/time: day/month/year hour:minute.
- Flow: hourly average of 15-minute flows; units in cubic metres per second (m3/s).
- TRP: concentration in mg P/L.
- Nitrate: concentration in mg/L.
- Turbidity: nephelometric turbidity units (NTU).
- Chlorophyll: μg/L (total chlorophyll a, b, and c).
- Conductivity: (units not explicitly stated in summary; typically μS/cm in YSI outputs).
- NaN indicates missing data points.

## References and Related Publications
- Bowes MJ, et al. Characterising phosphorus and nitrate inputs to a rural river using high-frequency concentration-flow relationships. Science of The Total Environment, 2015.
- Halliday S, et al. The Water Quality of the River Enbourne, UK: Observations from High-Frequency Monitoring in a Rural, Lowland River System. Water, 2014.
- Wade AJ, et al. Hydrochemical processes in lowland rivers: insights from in situ, high-resolution monitoring. Hydrology and Earth System Sciences, 2012.

## Potential Uses
- Analyzing concentration–flow relationships to identify nutrient inputs and river catchment sources.
- Assessing temporal dynamics of phosphorus and nitrate in a rural lowland river.
- Developing data products for end users to explore high-frequency water quality and hydrological data.
- Supporting comparative studies of high-frequency river monitoring methods and quality assurance practices.