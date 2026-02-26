# The PROTECH model

- A modelling framework (PROTECH) that simulates responses of multiple phytoplankton populations in a 1-dimensional vertical water column at daily time steps and computes key limnological parameters (thermocline development, stratification, nutrients).
- Calibrated to Rostherne Mere data from 2016; required an internal hypolimnetic supply of soluble reactive phosphorus (SRP) to match observed depth profiles.
- Internal SRP is added to the bottom 15 m for 90 days starting 1 June, with a fixed period to ensure loading occurs only during anoxic stratification; SRP implementation is not mixed into surface water until stratification breaks down.

## Data products and purpose

- Data aim to support understanding of how phytoplankton, nutrients, and physical lake properties respond under future climate and nutrient loading scenarios.
- Two CSV data files are provided:
  - RMPROTECHValidation: daily model outputs for a 360-day cycle (baseline-like year), including physical, chemical, and biological variables.
  - RMPROTECHFuture: model outputs for future scenarios, including model identifiers and scenario parameters; provides year-average results for each run.
- Each file includes descriptive column metadata to aid interpretation and reuse.

## Data structure and key fields

- RMPROTECHValidation (24 columns) includes:
  - Day; TempWater (average water column temperature); SRP (µg L-1); N (µg L-1); Si (µg L-1); GrazingRate; Flow (inflow); Cloud (oktas); Windspeed (m s-1); Lakedepth; Mixeddepth (stratification depth; 1 = fully mixed); Daylength; Energyin; Energyout; Totalchl (µg L-1); Species1–Species7 (phytoplankton species in cells mL-1); Cyanototal; Diatomtotal.
- RMPROTECHFuture (31 columns) includes:
  - ModelNumber; TemperatureModel (11 UKCP09 temp models); FlowLoadRatio; InternalLoadRatio; ModelDate; TempWater; SRP; N; Si; GrazingRate; Flow; Cloud; Windspeed; Lakedepth; Mixeddepth (1 = fully mixed); Daylength; Energyin; Energyout; Totalchl; Species1–Species7; Cyanototal; Diatomtotal; StratifiedLength; StratStart; StratEnd.
- Output measures are presented as:
  - RMPROTECHValidation: average daily simulation over the 360-day model cycle.
  - RMPROTECHFuture: collated year-average values for each future model run.

## Modelling approach and scenarios

- Baseline: 2016 calibration simulation serving as the reference for future scenarios.
- Future scenarios: daily driving data from UK Climate Projections (UKCP09) using HadRM3-PPE ensemble (11 temperature models) for different periods (2011–2020, 2051–2060, 2091–2100) on Rostherne Mere’s grid.
- Climate change is tested in combination with reduced SRP loads relative to 2016 baseline, applied as:
  - High: 100% of 2016 internal/external SRP loads
  - Mid: 60% of 2016 loads
  - Low: 20% of 2016 loads
- Time handling: each future scenario run spans 10 years; only the final year is used for analysis to allow conditions to stabilise under new driving conditions.
- Internal loading period (90 days) and SRP dynamics are kept constant across climate scenarios to isolate effects of temperature and nutrient load changes.

## Data quality, provenance, and documentation

- Procelled calibration and scenario design are described with key references for model structure and lake dynamics:
  - PROTECH model foundations (Reynolds et al., 2001; Elliott et al., 2010)
  - Calibration and prior findings (Mackay et al., 2014; Carvalho et al., 1995; Moss et al., 2005)
  - UKCP09 climate projections and HadRM3-PPE ensemble (Murphy et al., 2009)
  - Related monitoring and data sources (Radbourne et al., 2017, 2018)
- The dataset provides explicit metadata for each field, including units where stated (e.g., SRP in µg L-1; Windspeed in m s-1; Daylength in hours).
- Notes clarify interpretation (e.g., 1 = fully mixed for Mixeddepth) and modelling assumptions (internal load not mixed into surface water until stratification ends).

## Governance, storage, and reuse considerations

- The dataset comprises model-derived outputs rather than field measurements; appropriate caveats should accompany analyses and interpretations.
- Clear separation between validation (daily, 360-day cycle) and future projections (year-average per run) supports reproducibility and versioning.
- Documentation includes explicit column descriptions to support discoverability, interoperability with other datasets, and reuse across studies examining lake responses to climate and nutrient changes.