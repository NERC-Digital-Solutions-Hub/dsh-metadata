# Collection and analysis of field data

- The document describes the PROTECH model and its application to Rostherne Mere, including calibration to 2016 field data and exploration of future climate and nutrient-load scenarios.

## PROTECH model and calibration

- PROTECH simulates multiple phytoplankton populations in a 1D vertical water column with daily time steps.
- It also calculates key physical limnological parameters: thermocline development, stratification pattern, and nutrient concentrations.
- The 2016 Rostherne Mere data were used to calibrate the model. An internal hypolimnetic SRP load was required to reproduce observed conditions.
  - Internal SRP: 7.8 µg SRP L-1 d-1 added to bottom 15 m from 1 June for 90 days.
  - Internal loading occurs only during stratification (anoxic conditions); the 90-day period is fixed across climate scenarios.
- A simplifying assumption: internally loaded SRP does not mix into surface water until stratification breaks down, appropriate for strongly stratified Rostherne Mere.

## Future climate scenarios

- The 2016 calibration serves as the baseline and is projected forward under changes to air temperature and nutrient load.
- Scenarios: daily, 10-year simulations using UKCP09 projections with 11 model simulations.
  - Temperature projections span 2011–2020, 2051–2060, and 2091–2100 for Rostherne Mere on a 25 km grid.
  - Temperature change combined with reducing SRP loads relative to 2016, via multiplying measured loads by:
    - 100% (high, i.e., no change from 2016),
    - 60% (mid),
    - 20% (low).
- For analysis, only the final year of each scenario is used to allow stabilization under new driving conditions.

## Nature and units of recorded values

- Model outputs include physical, nutrient, and ecological variables.
- RMPROTECHFuture provides collated year-average values per model run; RMPROTECHValidation provides average daily values over a 360-day cycle.

## Details of the data structure

- Two CSV files: RMPROTECHValidation and RMPROTECHFuture.

- RMPROTECHValidation (24 columns):
  - Day; TempWater (average water column temperature); SRP (µg L-1); N (µg L-1); Si (µg L-1); GrazingRate; Flow; Cloud (okta, 0–8); Windspeed (m s-1); Lakedepth; Mixeddepth (stratification depth; 1 = fully mixed); Daylength (hours); Energyin; Energyout; Totalchl (µg L-1); Species1–Species7 (phytoplankton cells mL-1); Cyanototal; Diatomtotal.

- RMPROTECHFuture (31 columns):
  - ModelNumber; TemperatureModel; FlowLoadRatio; InternalLoadRatio; ModelDate; TempWater; SRP (µg L-1); N (µg L-1); Si (µg L-1); GrazingRate; Flow; Cloud; Windspeed; Lakedepth; Mixeddepth (1 = fully mixed); Daylength; Energyin; Energyout; Totalchl (µg L-1); Species1–Species7; Cyanototal; Diatomtotal; StratifiedLength; StratStart; StratEnd.
- Note: StratifiedLength, StratStart, StratEnd pertain to the duration and timing of stratification.

## References and modeling basis

- Foundational works informing PROTECH and context:
  - Carvalho et al. 1995; Moss et al. 2005; Mackay et al. 2014; Reynolds et al. 2001; Elliott 2010; Murphy et al. 2009; Radbourne et al. 2017; Radbourne et al. 2018.
- Key methodological and data sources underpinning calibration, internal loading assumptions, and climate-projection inputs.