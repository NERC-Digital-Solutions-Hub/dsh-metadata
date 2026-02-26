# Brief description of the dataset

- Location and period
  - River Enborne near Brimpton (National grid reference SU568648)
  - November 2009 to February 2012

- Parameters measured
  - Total reactive phosphorus (TRP), nitrate (NO3), conductivity, temperature, dissolved oxygen, pH, chlorophyll
  - Hourly data; accompanying hourly-averaged flow data from the Environment Agency (EA) gauging station at Brimpton (same site)

- Monitoring setup and instrumentation
  - Micromac C automated nutrient analyser for TRP (colorimetry; detection limit 0.025 mg P/L)
    - Intermittent pumping to avoid sediment resuspension; reference checks with manual samples (Bowes et al., 2015)
    - Daily check standard; fortnightly recalibration when reagents changed
    - No 06:00:00 GMT TRP sample due to standard measurement
  - Nitratax Plus probe for nitrate (UV absorption)
    - Detection limit 0.07 mg/L; field-tested with weekly laboratory IC checks (Bowes et al., 2015)
  - YSI 6600 sonde for DO, pH, temperature, conductivity, turbidity, chlorophyll
    - Turbidity: NTU; chlorophyll: μg/L
    - Calibration every 2–3 weeks; accounts for sediment interference in analysis
  - Environmental controls
    - Insulated shed heated to 20°C to minimise temperature-related errors and avoid frozen sampling pipes
  - Flow data
    - 15-minute EA flow data, averaged to hourly values; units: cubic metres per second (m³/s)

- Data quality assurance and validation
  - TRP cross-checks against manual lab analyses (Seal AA3) using the same colorimetric method
  - Cross-validation with Bowes et al. (2015) for high-frequency monitoring interpretation
  - Regular instrument calibration and standard checks; QA practices described with references

- Data format and units
  - Time format: day/month/year hour:minute
  - Flow: m³/s
  - TRP: mg P/L
  - Nitrate: mg/L
  - Turbidity: NTU
  - Chlorophyll: μg/L
  - NaN indicates missing data points

- Additional notes and references
  - Related publications for context and methods:
    - Bowes et al. 2015; Halliday et al. 2014; Wade et al. 2012
  - TRP is an operationally defined measurement comprising orthophosphate and readily hydrolysable P species