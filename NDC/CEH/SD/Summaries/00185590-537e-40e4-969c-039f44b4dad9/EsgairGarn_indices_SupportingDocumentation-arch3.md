# Nant Esgair Garn catchment - 20 year derived statistics of rainfall, streamflow and acidity

- This dataset provides a 20-year record (April 1, 1982 to April 1, 2013) of monthly statistics for rainfall, streamflow, and stream acidity (pH) linked to a stream gauging station and nearby water quality station at Nant Esgair Garn, draining into Llyn Brianne reservoir, UK.
- Observations for 2013 were collected at 15-minute resolution by Lancaster University and used to develop a dynamic model of the data; the model-derived statistics were then used to derive the 20-year monthly statistics.
- The work was conducted under a NERC grant; modelling and statistics were implemented with the CAPTAIN Toolbox for Matlab, using the RIVC algorithm, and validated against observed data.
- Full site and data lineage details are provided in Supporting Documentation; the dataset was vetted for Intellectual Property Rights by the Environmental Information Data Centre (EIDC).

## Data provenance and lineage

- Data sources:
  - Rainfall: derived from multiple Welsh Water/National Rivers Authority/Environment Agency Wales archives; gaps filled via correlations with neighboring raingauges.
  - Streamflow and pH: observed at two stations (streamflow at a trapezoidal flume; pH from a digital sensor) during 2013.
  - NAO index: obtained from public data source (CRU).
- Modelling workflow:
  - Daily rainfall plus daily streamflow and daily pH modelled and then aggregated to monthly statistics for 2013.
  - Identified daily models used to simulate daily values for 1982–2013, from which monthly statistics were derived.
  - Tools: CAPTAIN Toolbox for Matlab, RIVC algorithm, LSIM in Matlab.
- Data and code:
  - Code for statistics is described as Matlab functions; data and modelling approach are documented in Supporting Documentation.
  - Data released through the Environmental Information Data Centre (IPR vetted).

## Site description and experimental design

- Location: Nant Esgair Garn catchment near Llyn Brianne reservoir, Powys, Wales, UK.
- Contributory catchment areas:
  - Streamflow gauging station: 0.573 km²
  - pH monitoring station: 0.690 km²
- Geology/soils: shales, mudstones, greywackes, grits; Podzols and Histosols; landscape includes moorland and improved pasture.
- Field context: The dataset is tied to a long-term monitoring setup; the 2013 data underpin the 20-year derived statistics.

## Instrumentation, fieldwork, and calibration

- Instruments:
  - Streamflow: Forth River Purification Board trapezoidal flume with a Sensortechnics CTWM82X5G4C3SUN pressure transmitter; data logged by Campbell Scientific CR1000.
  - pH: Hach Lange pHD sc digital differential pH sensor with SC200 controller; data logged by Campbell Scientific CR1000.
- Calibration and maintenance:
  - Salt-dilution gauging for stage-discharge calibration.
  - SC200 controller recalibrated every 2–3 months.
  - pH sensor recalibrated with pH 4.0 and 7.0 solutions as needed.

## Data processing, analytical methods, and statistical outputs

- Modelling approach:
  - Use of the RIVC algorithm (CAPTAIN Toolbox) to identify optimal rainfall–streamflow and rainfall–pH models from observed daily rainfall to daily streamflow/pH.
  - Daily models applied to simulate daily values for 1982–2013; monthly statistics derived from these simulated data.
- Software and implementation:
  - Matlab R2013-based analysis; code includes functions for mean, percentiles, moving-average statistics, pulses (high/low), durations, growth-season metrics, and rate calculations.
- Statistical outputs:
  - Monthly statistics derived for 1982–2013, with the 2013 data underpinning the back-calculation.
  - Variables include rainfall, temperature metrics, NAO index, streamflow metrics (means, percentiles, moving-average extrema, pulses, durations, rises/declines), and pH metrics (means, percentiles, moving-average extrema, range, CV).
  - Estimation windows vary by variable (e.g., 365 days for many precipitation/temperature metrics; 120 days for some rainfall/flow/pH metrics; December–March for NAO).

## Variables, units, and data structure

- The data are organized in a single CSV with 159 columns (columns 2–5 intentionally blank) and 32 rows.
- Each row corresponds to statistics for the first day of each month from April 1, 1982 to April 1, 2013; the first row is the header.
- Example of derived variables (with their estimation periods and references to columns):
  - Rainfall: mean, 10th percentile; estimation period typically 365 days prior to sampling.
  - Temperature: mean, max/min/range, coefficient of variation; several temperature-derived metrics with 365-day estimation periods.
  - NAO index: estimation period December–March.
  - Rainfall and Flow: multiple statistics (mean, percentiles, moving-average-based extrema, pulse counts, durations, rises/decays) with 120-day estimation periods for some variables.
  - pH: mean, percentiles, moving-average extrema, min/max, range, CV; 120-day estimation period.
- The dataset also documents the units and the exact structure of each statistic column in the accompanying metadata.

## Quality control and data structure details

- Quality control:
  - Data from CR1000 loggers checked for erroneous values (e.g., due to power issues); such values replaced with NaN using QA procedures.
- Data structure:
  - One CSV file containing 159 statistics columns; two to five empty; 32 rows (monthly snapshots across the 1982–2013 period).
  - Detailed definitions of each statistic are provided in the accompanying metadata section.

## Relevance to Monitoring Frameworks

- Demonstrates a framework for deriving long-term environmental health measures from a combination of observed and modelled data.
- Addresses common monitoring challenges highlighted in monitoring-framework literature:
  - Data gaps filled via robust modelling and cross-validated data sources.
  - Metadata and data provenance are explicitly documented, with open or sharable outputs (IPR vetted) and reproducible code practices.
  - Data governance considerations are visible (public sharing of underlying data, transparency of transformations, and quality assurance).
- Provides a concrete example of how to translate high-frequency observational data into stable, policy-relevant monthly indicators for environmental monitoring and biodiversity assessments.