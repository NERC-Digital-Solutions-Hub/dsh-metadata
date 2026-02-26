# riverfrome_waterquality_highres_2022

## Overview
- High-frequency water quality dataset from the River Frome catchment, Dorset, UK, collected between 12 Aug 2022 and 14 Sep 2022.
- 24 sites spanning upstream to downstream reach, including river channels, major tributaries, boreholes, and STW effluents; site locations provided by British National Grid References (NGRs).
- Measurements include 30-minute sensor readings and frequent grab samples; 15-minute discharge readings at STW effluents and EA flow gauging stations.
- Determinands cover nutrients (ammonium, nitrate, nitrite, orthophosphate, soluble reactive phosphate, total phosphorus), alkalinity, conductivity, dissolved oxygen (DO), DO%, pH, temperature, turbidity, BOD, COD, chloride, suspended solids; plus discharge data.
- Data collected for a PhD project on high-resolution river water quality modelling; contributors include Wessex Water Services Ltd. and Environment Agency; licence under Open Government Licence.

## Data content and scope
- Purpose: support river water quality management through high-resolution data with potential for modelling and self-serve data exploration.
- Two monitoring phases: upstream sites (12/08/22–30/08/22) and downstream sites (30/08/22–14/09/22); Pallington sampled in both periods.
- Data types: continuous high-frequency sensor data, grab samples analysed inQuality Centre, borehole samples, and discharge data.
- Geographic coverage: 24 sites across the River Frome catchment between Dorchester and East Stoke flow gauging stations.

## Data structure and columns
- One CSV file named riverfrome_waterquality_highres_2022 with 13 columns:
  - Date, Time_GMT, Date_time, Site_name, Site_NGR, Site_type, Source, Freq, Determinand, Result, Sign, Censored, Unit
- Columns capture measurement time, site details, data source and frequency, the measured determinand, the value, any sign indicating below-detection values, censorship flag, and units.

## Experimental design and sampling regime
- High-frequency sampling campaign using six sondes (four EXO2, two EXO3) plus additional nitrate sensors; key measured parameters include conductivity, DO, DO%, pH, temperature, turbidity, with NO3-N from UV sensors at select sites and ammonium at Dorchester STW effluent.
- Calibration and maintenance: sensors calibrated before deployment; self-cleaning wipers; no mid-cycle recalibration required due to short deployment.
- Sampling schedule: continuous 30-minute measurements; grab samples approximately three times per week; additional 15-minute discharge data from STW effluents and EA stations.
- Data sources: EXO2/EXO3 sondes (Meteor Communications Ltd.; Wessex Water/University of Bath collaboration), grab samples analysed by Wessex Water Services Ltd., EA discharge data.

## Sample analysis
- Grab samples analysed at Wessex Water Scientific Centre following described methodologies; reporting limits and uncertainties provided for each determinand.
- Determinants include ammonia, TON (nitrate), nitrite, nitrate, orthophosphate, soluble reactive phosphorus, chloride, alkalinity, BOD, suspended solids, pH, conductivity, turbidity, and total phosphorus.
- Method details include spectrophotometric assays, digestion/oxidation procedures, and ICP-OES for total phosphorus, with specific reporting limits and uncertainties (varying by freshwater vs final effluent).

## Quality control and data quality
- Grab samples used to visually and quantitatively compare with continuous data; target diagram approach employed to assess bias and pattern agreement (normalised bias, normalised RMSD).
- General finding: good agreement between continuous high-frequency data and grab samples; notable biases for pH (sensitive calibration and log-scale effects) and some DO comparisons due to local gradients or sampling distance from sensors.
- Specific issues: poorer DO agreement at some sites, rounding differences near sensors; nitrate disagreement at a downstream site likely due to variable STW loading.
- Overall conclusion: high confidence in the continuous high-frequency measurements.

## Data completeness and cleaning
- Data wrangling and cleaning performed in R.
- Outliers addressed: replaced with N/A when explained (negative concentrations, sensor-wetness issues at low flow, turbidity spikes > 6000 NTU due to fouling or bubbles).
- Data completeness notes support reliable use of continuous time series for analysis and modelling.

## Access, licensing, and provenance
- Data contributed by Wessex Water Services Ltd. and partners; Environment Agency discharge data available under Open Government Licence.
- Clear documentation of data provenance, measurement methods, QA procedures, and data processing steps to enable reuse and replication.

## Context and miscellaneous
- Campaign occurred during an exceptionally dry summer; river discharge at East Stoke recorded at its lowest since 1976 drought (minimum 1.92 m3/s on 31 Aug).
- Groundwater levels and discharge during the period indicated typical extreme conditions relative to historical records.

## How Data Support can be used
- Fit-for-purpose for exploring hydrochemical dynamics and high-resolution river quality modelling.
- Data can be used to build dashboards or self-serve analyses enabling end users to inspect temporal patterns, site comparisons, and discharge interactions.
- Useful for cross-validation against other datasets or for One Health/hydrological impact studies.

## References
- Key methodological and QA references related to high-frequency water-quality monitoring and validation approaches cited in the document.