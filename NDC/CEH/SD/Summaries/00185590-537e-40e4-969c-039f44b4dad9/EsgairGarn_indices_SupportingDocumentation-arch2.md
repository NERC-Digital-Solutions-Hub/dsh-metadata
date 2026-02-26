# Nant Esgair Garn catchment - 20 year derived statistics of rainfall, streamflow and acidity

## Overview
- A 20-year record of monthly statistics for rainfall, streamflow, and stream acidity (pH) related to a Nant Esgair Garn stream gauging station and nearby water quality station.
- Observations were collected in 2013 at 15-minute resolution and used to develop a dynamic model to derive the 20-year monthly statistics (1982-04-01 to 2013-04-01).

## Purpose and use
- Statistics were produced to enhance understanding of the long-term controls on aquatic biodiversity observed in this stream.
- Outputs support standardised environmental monitoring and can be used to compare policy outcomes and ecosystem health over time.

## Site, data lineage, and governance
- Location: Nant Esgair Garn experimental catchment near Llyn Brianne reservoir, Powys, Wales. Contributory areas are 0.573 km2 (streamflow) and 0.690 km2 (pH).
- Geology/soils: Lower Paleozoic shales, mudstones, greywackes, and grits; Podzols and Histosols; historically moorland and improved pasture.
- Data provenance: Daily rainfall (from multiple Welsh Water/NR Authority sources; extended back to 1982) and temperature (Felindre station) with gaps infilled from nearby gauges; NAO index from public source.
- Data quality: All data vetted for Intellectual Property Rights by the NERC Environmental Information Data Centre (EIDC).

## Experimental design / data collection
- Field measurements: Streamflow and pH monitored in 2013 at two stations using a flume and sensors; data logged at 15-minute intervals; calibration every 2–3 months.
- Derived datasets: Daily rainfall, streamflow, and pH were modelled from 1 January–31 December 2013 and extrapolated back to 1 April 1982–1 April 2013 through modelling.

## Instrumentation and calibration
- Streamflow: Trapezoidal flume with Sensortechnics pressure transmitter and Campbell Scientific data-logger.
- pH: Hach Lange pH sensor with SC200 controller and Campbell Scientific data-logger.
- Calibration: Salt-dilution checks for stage-discharge; SC200 recalibrated every 2–3 months; pH sensor recalibrated to pH 4.0 and 7.0 as needed.

## Analytical methods and modelling
- Modelling framework: CAPTAIN Toolbox for Matlab; RIVC algorithm used to identify optimal rainfall–streamflow and rainfall–pH models; LSIM routine used for daily simulations.
- Data processing: Daily models based on 2013 observations; monthly statistics computed from simulated daily data.
- Software details: Matlab R2013; code snippets provided for statistical functions (mean, percentiles, moving averages, pulses, durations, rates, etc.).

## Variables, units, and data structure
- Derived variables with monthly statistics covering rainfall, temperature, flow, and pH (and related descriptive metrics such as percentiles, means, moving averages, variability, and pulse indicators).
- Time windows: Many metrics use 365 days prior to sampling; some use 120 days prior; NAO index pertained to December–March.
- Data file: One CSV with 159 columns (columns 2–5 intentionally blank) and 32 rows; first row is the header; rows 2–32 correspond to statistics for the first day of each month from 1 April 1982 to 1 April 2013.
- Note: Column naming and exact statistical definitions are detailed in the dataset documentation (Nature and Units of Recorded Values).

## Data quality and documentation
- Quality control: Observed data checked for erroneous values (e.g., due to power interruptions) and corrected to NaN where appropriate.
- Supporting documentation: Full site details and data lineage provided; references include Jones and Chappell (2014) and Jones, Chappell & Tych (2014).
- Associated identifiers: DOIs available for referenced works; dataset authorship acknowledged (Nick A. Chappell).

## Access, reuse, and governance
- Data released via the Environmental Information Data Centre (EIDC); IPR vetted.
- Dataset designed for reuse in environment monitoring, enabling cross-dataset analyses and data portal integration.