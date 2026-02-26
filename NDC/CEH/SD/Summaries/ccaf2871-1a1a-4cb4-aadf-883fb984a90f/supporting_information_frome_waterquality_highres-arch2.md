# Overview of data

- Scope: high-frequency water quality measurements in the River Frome catchment, Dorset, UK, from 12/08/2022 to 14/09/2022.
- Sites: 24 monitoring locations across the catchment between Dorchester and East Stoke, including river channels, major tributaries, boreholes, and STW (sewage treatment works) effluents; each site has British national grid references (NGRs).
- Measurements: mixture of 30-minute sensor readings and frequent grab samples; includes 15-minute discharge readings at STW effluents and Environment Agency (EA) gauging stations.
- Determinands: ammonium, nitrate, nitrite, orthophosphate, soluble reactive phosphate, total phosphorus, alkalinity, conductivity, dissolved oxygen (DO), DO%, pH, temperature, turbidity, BOD, COD, chloride, suspended solids; additional discharge data.
- Study design: upstream and downstream halves of the river monitored separately (upstream first, then downstream); Pallington monitored in both periods.
- Data provenance: collected by PhD project “Supporting river waterquality management by high-resolution modelling” (GW4 FRESH CDT, NERC funding); Wessex Water Services Ltd. contributed high-frequency NH4-N and discharge data and borehole data; grab samples analysed by Wessex Water Services Ltd.; EA discharge data supplied under Open Government Licence.
- Licensing: EA data available under Open Government Licence v3.

## Data structure and file

- File: riverfrome_waterquality_highres_2022 (single CSV).
- Columns (13): Date, Time_GMT, Date_time, Site_name, Site_NGR, Site_type, Source, Freq, Determinand, Result, Sign, Censored, Unit.
- Additional details on units, measurement uncertainty, and reporting limits provided in sections 3.1 and 3.2 of the dataset documentation.

## Experimental design and sampling regime

- Deployment: four YSI EXO2 and two EXO3 multi-parameter sondes in-situ; measured conductivity, DO, DO% saturation, pH, temperature, turbidity (30-minute resolution); EXO2s included a NitraLED UV sensor for NO3-N.
- Supplemental data: Wessex Water supplied 30-minute NO3-N data from specific gauging stations; 30-minute NH4-N data from Dorchester STW effluent; grab samples analyzed at Saltford; 15-minute EA discharge data.
- Timeline: two monitoring periods—upstream (12/08/22–30/08/22) and downstream (30/08/22–14/09/22); Pallington sampled in both periods.
- Grab sampling: conducted mid-channel, stored on ice, analyzed the following day; DO/DO% measured in-situ with a YSI ProSolo probe; borehole grab samples for NH4-N, NO3-N, NO2-N, PO4-P.
- Frequency: continuous measurements every 30 minutes for sensors; grab samples approx. three times per week; additional 15-minute discharge data.

## Data sources and determinants

- Instrumentation and sources: EXO2 (Meteor Communications Ltd.), EXO3 (Wessex Water Services Ltd. & University of Bath), Nitratax NO3-N sensors (Wessex Water), grab samples (authors; analyzed by Wessex Water Services Ltd.).
- Determinands per data source: as listed in the experimental design; discharge data from STW and EA; borehole water quality measurements; various chemical determinands from grab samples.

## Sample analysis methods

- Grab samples analyzed at Wessex Water Scientific Centre; methodology aligned with Kasprzyk-Hordern et al. (2022) with determinand-specific protocols.
- Key determinand analysis summaries:
  - Ammonia N: colorimetric method with blue complex at 660 nm; reporting limits 0.4 mg/L (FE) and 0.02 mg/L (FW).
  - Total oxidised nitrogen (TON) and Nitrite: spectrophotometric methods at 540 nm.
  - Nitrate: calculated as TON minus Nitrite.
  - Orthophosphate and Soluble Reactive Phosphorus (SRP): colorimetric molybdenum blue method (SRP filtered for SRP).
  - Chloride: colorimetric iron thiocyanate reaction (480 nm).
  - Alkalinity: acid titration with methyl orange indicator (pH transition buffering).
  - BOD (with or without nitrification inhibitor ATU): five-day incubation at 20°C; reporting limits 8 mg/L (FE) and 2 mg/L (FW).
  - Suspended solids (SS): gravimetric method; reporting limit 5 mg/L.
  - pH, Conductivity, Turbidity: standard meters; reporting limits and ranges specified.
  - Total Phosphorus: digestion followed by ICP-OES measurement; reporting limit 0.05 mg/L.
- Uncertainty and reporting limits vary by freshwater (FW) vs. final effluent (FE) status.

## Quality control and error analysis

- QA approach: grab samples analyzed at a centralized lab; continuous data visually and statistically compared to grab data using target diagrams to assess bias and pattern agreement.
- Findings: generally good agreement between continuous and grab data; pH showed notable bias differences due to units and calibration/preservation artefacts; DO agreement lower at some sites due to local gradients and time-mismatch; nitrate discrepancies at downstream sites likely due to flushing from STW influence.
- Conclusion: strong confidence in the high-frequency continuous measurements despite some site-specific discrepancies.

## Data completeness and cleaning

- Data wrangling in R; outliers replaced with NA if explainable.
- Cleaning steps included:
  - Removing negative concentrations.
  - Excluding measurements at Dorchester STW effluent when flow too low to wet sensors.
  - Removing large turbidity spikes (> 6000 NTU) due to fouling or bubbles.
- Only outliers with plausible explanations were removed; the majority of data retained for analysis.

## Miscellaneous observations

- Period context: river discharge was unusually low due to one of the hottest and driest summers on record; East Stoke discharge at minimum since 1976 drought (1.92 m3 s-1 on 31 Aug).
- Groundwater levels and discharge values were at unusually low/high percentiles during the campaign.

## Access and references

- Data availability: collected under open data practices with licensing noted (Open Government Licence).
- References: Halliday et al. (2014, 2015) on high-frequency water quality monitoring; Jolliff et al. (2009) on target diagrams; Kasprzyk-Hordern et al. (2022) on analytical methods.