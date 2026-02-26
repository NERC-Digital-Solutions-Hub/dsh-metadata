# riverfrome_waterquality_highres_2022

## Overview
- High-frequency water quality dataset from the River Frome catchment (Dorset, UK), collected 12 Aug 2022 to 14 Sep 2022.
- 24 measurement sites across upstream to downstream reach (Dorchester to East Stoke), including river channels, major tributaries, boreholes, and STW effluents.
- Measurements include a mix of 30-minute sensor readings and frequent grab samples; 15-minute discharge readings at STW sites and EA gauges.
- Geographic references provided via British National Grid References (NGRs).
- Data collected for a PhD project on high-resolution river water quality modelling; funding and collaboration details provided; Open Government Licence governs EA discharge data.

## Data structure
- Single CSV file: riverfrome_waterquality_highres_2022 with 13 columns: Date, Time_GMT, Date_time, Site_name, Site_NGR, Site_type, Source, Freq, Determinand, Result, Sign, Censored, Unit.
- Column definitions and units summarized in Table 1; additional details on units, measurement uncertainty, and reporting limits in sections 3.1–3.2.
- Data provenance includes multiple sources (in-situ sensors, grab samples, and external labs) and a defined coding scheme for Source and Determinand.

## Experimental design and sampling regime
- High-frequency campaign using four YSI EXO2 and two EXO3 sondes, capturing:
  - Conductivity, DO (absolute and % saturation), pH, temperature, turbidity (30-min resolution).
  - Nitrate NO3-N via NitraLED UV sensor (pathlength 10 mm on EXO2).
  - Additional 30-minute NH4-N (ammonium) and discharge data from STW and EA sensors.
- Monitoring periods split into two halves:
  - Upstream sites: 12/08/22–30/08/22.
  - Downstream sites: 30/08/22–14/09/22.
- Pallington monitored in both halves.
- Grab samples collected mid-channel, stored on ice, and analyzed next day at Wessex Water Scientific Centre.
- In-situ DO, DO%, and temperature measured with YSI ProSolo ODO/T at time of grab sampling.
- Borehole water quality samples (NH4-N, NO3-N, NO2-N, PO4-P) collected by Wessex Water and analyzed centrally.
- 15-minute discharge data provided for STW effluent and EA gauges.

## Sample analysis and measurement methods
- Grab samples analyzed at Wessex Water Scientific Centre; methodologies described for each determinand, with reporting limits, ranges, and uncertainties.
- Key determinands: ammonia (NH4-N), total oxidised nitrogen (TON), nitrite (NO2-N), nitrate (NO3-N), orthophosphate (PO4-P), soluble reactive phosphorus (SRP), chloride, alkalinity, BOD, suspended solids (SS), pH, conductivity, turbidity, and total phosphorus (TP).
- Method details include spectrophotometric assays, digestion/oxidation steps, and ICP-OES for TP, with instrument models (e.g., Aquakem, ICP-OES) and specified reporting limits and uncertainties.
- Uncertainty and detection limits appear to differ between final effluent (FE) and freshwater (FW) samples.

## Quality control and data validation
- Grab samples analyzed in a quality-assured laboratory; continuous and grab data visually and via target diagrams to assess agreement.
- Target diagram approach used to compare normalised bias and normalised unbiased RMSE between continuous and grab data; overall good agreement, with some biases explained (e.g., pH scale sensitivity, DO gradients, and sampling time alignment).
- Confidence stated in the high-frequency measurements despite some minor discrepancies.

## Data completeness and cleaning
- Data wrangling and cleaning performed in R.
- Outliers replaced with NA when explainable (e.g., negative concentrations, sensor wetting issues at low flow, large turbidity spikes from fouling or bubbles).
- Data quality checks included exclusion of data from Dorchester STW effluent when flow was too low to wet sensors.

## Licensing, access, and provenance
- Discharge data from Environment Agency under Open Government Licence v3.0.
- Overall provenance includes collaboration between authors, Wessex Water Services Ltd., Meteor Communications Ltd. (WQaaS), and the University of Bath.
- Data are documented with a clear data dictionary, sampling regime, analytical methods, and QA/QC procedures to support reuse and governance.

## Miscellaneous context
- During the sampling period, River Frome discharge was exceptionally low due to an unusually hot and dry summer, with groundwater levels and mean daily discharge noted for context.

## References
- Key methodological and context references related to high-frequency water-quality monitoring and analytical methods are listed for further reading.