# Overview of data

- A high-frequency water quality dataset for the River Frome catchment, Dorset, UK, collected from 12 August 2022 to 14 September 2022.
- 24 monitoring sites spanning the river from Dorchester to East Stoke, including river channels, major tributaries, boreholes, and wastewater treatment works (STW) effluents.
- Data include 30-minute sensor readings and frequent grab samples; 15-minute discharge readings at STW effluents and EA flow gauging stations.
- Locations are provided with British National Grid references (NGRs); borehole sites are resolved to 1 km accuracy.
- The study period is split into upstream (12/08/22–30/08/22) and downstream (30/08/22–14/09/22) halves; Pallington monitored in both periods.
- Data were collected for a PhD project on high-resolution river water quality modelling, with contributions from Wessex Water Services Ltd. and the Environment Agency (EA); Open Government Licence applies to EA data.

## Data content and structure

- File: riverfrome_waterquality_highres_2022 (CSV) containing 13 columns:
  - Date, Time_GMT, Date_time: timestamps in GMT
  - Site_name, Site_NGR, Site_type: monitoring site details and location type (STW effluent, river, borehole)
  - Source, Freq: data source and measurement frequency (continuous or grab)
  - Determinand, Result, Sign, Censored, Unit: analyte name, measured value, qualifier (e.g., below reporting limit), censoring flag, and unit
- Determinands include ammonium, nitrate, nitrite, orthophosphate, soluble reactive phosphate (SRP), total phosphorus, alkalinity, conductivity, dissolved oxygen (DO), DO% saturation, pH, temperature, turbidity, biochemical oxygen demand (BOD), chemical oxygen demand (COD), chloride, and suspended solids.
- Additional 15-minute discharge data from STW effluents and EA gauges accompany the chemical measurements.

## Experimental design and sampling regime

- In-situ sensors: four YSI EXO2 and two EXO3 multi-parameter sondes measuring conductivity, DO, DO%, temperature, pH, turbidity; EXO2 units include a nitrate (NO3-N) sensor (NitraLED UV).
- Additional grab samples: collected ~three times per week; DO, DO% and temperature measured in situ with a YSI ProSolo ODO/T probe.
- 30-minute sampling cadence for most continuous sensor data; 15-minute discharge data for specific sources.
- Sampling locations and period distribution (upstream vs downstream) detailed in accompanying Table 2, including monitoring at Dorchester STW effluent and Pallington, Lewell Mill, Moreton, and other sites.
- Wessex Water provided 30-minute NO3-N data and ammonium data for certain sites; borehole samples collected by authors and analysed by Wessex Water Services Ltd.

## Laboratory analysis and determinand specifics

- Grab samples analysed at Wessex Water Scientific Centre following established methods; reporting limits and uncertainties differ by freshwater (FW) vs final effluent (FE) with ISO-based uncertainty estimates.
- Ammonia, TON (nitrate, via reduction and subsequent analyses), nitrite, orthophosphate, SRP, chloride, alkalinity, BOD, suspended solids, pH, conductivity, turbidity, and total phosphorus all measured using standard colorimetric, titrimetric, or ICP-OES techniques as described.
- For BOD, incubation at controlled temperature with inhibitors; for turbidity, nephelometric measurement; for conductivity, temperature-compensated readings.

## Quality control, data quality, and handling

- Grab samples compared with continuous data using time-series visualization and target diagrams to assess bias and pattern agreement.
- General finding: good agreement between continuous high-frequency data and grab samples; pH showed notable normalised bias due to measurement scale and calibration artefacts; DO differences at some sites reflect local gradients and grab-sensor timing.
- Data cleaning in R:
  - Outliers replaced with N/A only when explained
  - Negative concentrations removed
  - Concentrations at Dorchester STW effluent during low flow removed
  - Large turbidity spikes (> 6000 NTU) removed due to fouling or bubbles
- Continuous data deemed reliable after quality checks.

## Data completeness and limitations

- Grab samples are relatively limited in number; continuous data provide high temporal resolution but may still have site-specific discrepancies.
- River discharge was exceptionally low during the study due to drought conditions, with East Stoke discharge at a record-low for the period; groundwater levels and discharge reflect typical values for the period's context.

## Spatial coverage and coordinate details

- 24 sites across the River Frome catchment (upstream to downstream reach), with NGR coordinates provided for all sites; borehole locations resolved to 1 km accuracy.
- Spatial distribution supports mapping of water quality determinants along the reach, including proximity to STW effluents.

## Provenance, licensing, and references

- Data gathered under the PhD project funding and collaboration:
  - GW4 FRESH CDT; Natural Environment Research Council (Grant NE/R0115241)
  - Wessex Water Services Ltd. contributions (NO3-N, NH4-N, borehole data, and sample analysis)
  - Environment Agency data available under Open Government Licence
- References for data interpretation and methodology cited in the document (e.g., Halliday et al. 2014, 2015; Jolliff et al. 2009; Kasprzyk-Hordern et al. 2022).

## Practical takeaways for GIS use

- The dataset enables map-based visualization of high-resolution water quality dynamics along a river reach, suitable for policy briefing, client reporting, or public-facing GIS applications.
- Key integration points:
  - Join by Site_NGR or Site_name for spatial mapping; use Date_time for temporal animation or time-series mapping.
  - Distinguish data sources (EXO2/EXO3, NO3-N sensors, grab samples, STW/EA discharge) to create layer-specific symbology.
  - Be mindful of varying measurement types and units; refer to Unit and Determinand fields for accurate interpretation.
- Data quality notes should be attached to GIS products, especially regarding pH calibration nuances, DO measurement variability, and site-specific data gaps.