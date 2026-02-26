# riverfrome_waterquality_highres_2022

## Overview of data
- High-frequency water quality measurements from 12 Aug 2022 to 14 Sep 2022 in the River Frome catchment, Dorset, UK.
- 24 measurement sites spanning upstream to downstream reach between Dorchester and East Stoke flow gauging stations; includes river channels, major tributaries, boreholes, and STW effluents.
- Determinands cover nutrients and general water quality: ammonium, nitrate, nitrite, orthophosphate, soluble reactive phosphate, total phosphorus, alkalinity, conductivity, dissolved oxygen, DO%, pH, temperature, turbidity, BOD, COD, chloride, suspended solids.
- Additional 15-minute discharge readings at sewage treatment works (STW) effluents and Environment Agency flow gauging stations.
- Data gathered for a PhD project on high-resolution river water quality modelling; funded by GW4 FRESH CDT and NERC; data contributed by Wessex Water Services Ltd. and Environment Agency under Open Government Licence.
- File format: a single CSV riverfrome_waterquality_highres_2022 with 13 columns.

## Data structure
- Core file: riverfrome_waterquality_highres_2022.csv
- Key columns: Date, Time_GMT, Date_time, Site_name, Site_NGR, Site_type, Source, Freq, Determinand, Result, Sign, Censored, Unit
- Each row represents a measurement instance (continuous 30-min sensor readings or grab sample), with metadata about site, source, and measurement details.
- Site_NGR provided for locations; boreholes referenced to 1 km resolution.

## Experimental design and sampling regime
- Instruments: four YSI EXO2 and two EXO3 multi-parameter sondes deployed in situ; measured conductivity, dissolved oxygen, DO%, pH, temperature, turbidity (30-min resolution); Nitrate (NO3-N) via NitraLED UV sensors attached to EXO2; additional 15-min nitrate data from Nitratax sensors at selected sites; 15-min ammonium measurements at Dorchester STW effluent (ProAm monitor).
- Grab sampling: approximately three times per week; analyzed by Wessex Water Services Ltd.; DO and DO% measured in situ at grab time using YSI ProSolo ODO/T probe.
- Sampling regime: two periods to cover upstream vs downstream - upstream: 12 Aug–30 Aug 2022; downstream: 30 Aug–14 Sep 2022. Pallington monitored in both periods.
- Data sources per determinand include: EXO2/EXO3 sondes, Nitratax sensors, STW effluent measurements, and EA discharge data (15-min intervals).
- British National Grid References (NGRs) provided for all sites; data include discharge and river flow context.

## Sample analysis
- Grab samples analyzed at Wessex Water Scientific Centre using methods aligned with Kasprzyk-Hordern et al. (2022) and additional determinands.
- Determinant-specific methods, reporting limits, ranges, and uncertainty (UoM) differ for freshwater (FW) vs final effluent (FE):
  - Ammonia N, N total (TON), Nitrite, Nitrate, Orthophosphate, SRP, Chloride, Alkalinity, BOD, Suspended Solids (SS), pH, Conductivity, Turbidity, Total Phosphorus (TP)
- Analytical principles summarized (e.g., spectrophotometric methods for ammonia, nitrite, nitrate; alkaline reduction for TON; digestion for TP; ICP-OES for TP; turbidity by NTU).
- Reporting limits and ranges vary by determinand and sample type (FW vs FE).
- Quality control includes ISO-based uncertainty assessments and external quality checks.

## Quality control and error analysis
- Grab samples and continuous data quality checked visually and via target diagrams (bias and pattern agreement measures).
- Overall, good agreement between continuous high-frequency data and grab samples.
- Notable issues:
  - pH showed greater normalised bias, likely due to calibration sensitivity and measurement/logging quirks.
  - DO agreement poorer at some sites (South Winterbourne, Watery Lane south) due to local gradients and sampling proximity effects.
  - Nitrate disagreement at Lower Bocksouth likely due to downstream variable STW effluent, plus rounding effects.
- Conclusion: high confidence in continuous high-frequency measurements; potential local discrepancies explained by sampling/gradient factors.

## Data completeness and cleaning
- Data wrangling performed in R; outliers only removed if explainable and replaced with N/A.
- Cleaning steps included:
  - Removing negative concentrations.
  - Excluding Dorchester STW effluent data when flow too low to wet sensors.
  - Removing large turbidity spikes (> 6000 NTU) attributed to sensor fouling or bubble entrainment.

## Miscellaneous
- The sampling period coincided with an unusually low river discharge due to one of the hottest and driest summers on record (East Stoke at minimum flow 1.92 m3 s-1 on 31 Aug).
- Groundwater levels and discharge during the campaign largely exceeded historical norms (high percentile comparisons).

## References
- Halliday et al., 2014, 2015: high-frequency water quality monitoring studies
- Jolliff et al., 2009: target diagram method for model skill assessment
- Kasprzyk-Hordern et al., 2022: methods related to nutrient analyses and One Health implications