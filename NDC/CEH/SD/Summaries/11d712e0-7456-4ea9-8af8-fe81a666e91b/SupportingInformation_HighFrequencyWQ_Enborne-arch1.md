# Brief description of the dataset

- Time period and location
  - Hourly physical and nutrient monitoring data from River Enborne near Brimpton (grid reference SU568648)
  - Span: November 2009 to February 2012
  - Accompanied by hourly flow data from the Environment Agency gauging station at the same site

- Parameters measured
  - Total reactive phosphorus (TRP), nitrate (NO3), conductivity, temperature, dissolved oxygen (DO), pH, chlorophyll
  - Flow data: hourly average flow (m3/s) derived from 15-minute measurements

- Monitoring and instrumentation
  - Micromac C automated nutrient analyser for TRP (colorimetry, molybdate-blue method)
    - Detection limit: 0.025 mg P L-1
    - TRP checked against manual samples (Seal AA3) and Bowes et al. (2015)
  - Nitratax Plus probe for nitrate (UV absorption)
    - Detection limit: 0.07 mg N L-1
    - Checked against weekly manual ion chromatography samples (Bowes et al. 2015)
  - YSI 6600 multi-parameter sonde for DO, pH, temperature, conductivity, turbidity, chlorophyll
    - Turbidity: NTU, temperature-compensated; chlorophyll: fluorometer (470 nm)
    - Calibration every 2–3 weeks
  - Site setup
    - Insulated shed 2 m from riverbank; intermittent pumping to minimize sediment resuspension and temperature errors
    - Flow-through cells and a separate sampling loop to reduce interference

- Data quality, checks, and processing
  - TRP standard measurement occurs at 06:00:00 GMT; no sample at that exact time
  - TRP and NO3 data cross-validated with laboratory analyses
  - Chlorophyll measurements account for turbidity interference using concurrent turbidity data
  - Heating kept at approximately 20°C to stabilize reaction conditions
  - Data quality assurance includes routine calibration and cross-validation with manual methods
  - NaN represents missing data points

- Data format and units
  - Date/time format: day/month/year hour:minute
  - Flow: cubic metres per second (m3/s); hourly average from 15-minute flows
  - TRP: mg P L-1 (total reactive phosphorus; includes dissolved and acid-extractable particulate P)
  - NO3: mg L-1
  - Turbidity: NTU
  - Chlorophyll: μg L-1
  - Other parameters (DO, pH, conductivity, temperature) as measured by respective instruments

- References and related works
  - Bowes MJ et al. Characterising phosphorus and nitrate inputs to a rural river using high-frequency concentration-flow relationships. Sci Total Environ. 2015
  - Halliday S et al. The Water Quality of the River Enborne, UK: Observations from High-Frequency Monitoring. Water. 2014
  - Wade AJ et al. Hydrochemical processes in lowland rivers: insights from in situ, high-resolution monitoring. HESS. 2012