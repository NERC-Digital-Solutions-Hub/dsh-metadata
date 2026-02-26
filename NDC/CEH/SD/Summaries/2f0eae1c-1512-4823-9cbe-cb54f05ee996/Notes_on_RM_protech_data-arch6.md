# The PROTECH model

- Purpose: The PROTECH model simulates responses of multiple phytoplankton populations in a 1-D vertical water column at daily time steps and computes key physical limnological parameters (e.g., thermocline development, stratification patterns, nutrient concentrations). It was calibrated against 2016 Rostherne Mere field data and used to explore responses under future climate and nutrient scenarios.

- Calibration and internal load: Calibration showed a need for an internal hypolimnetic SRP supply during stratification. An internal load of 7.8 µg SRP L-1 d-1 was optimally added to the bottom 15 m for 90 days (starting 1 June) to match observed hypolimnetic SRP concentrations. The model assumes this internal load is not mixed into surface water until stratification ends, reflecting strongly stratifying conditions at Rostherne Mere. The 90-day internal loading period is fixed across all climate scenarios to confine loading to anoxic stratification.

- Future climate scenarios: The 2016 calibration run serves as baseline and is re-run under combinations of air temperature changes and nutrient loads. Each scenario is run daily for 10 years; analysis uses the final year to allow stabilization under new forcing. Temperature changes are based on UKCP09 projections (11 model simulations) for Rostherne Mere on a 25 km-2 grid. Temperature changes are paired with decreasing SRP loads relative to 2016 using three load scenarios: high (100%), mid (60%), and low (20%).

- Nature and units of recorded values: Outputs include physical, nutrient, and ecological variables. RMPROTECHFuture provides year-average values per model run, while RMPROTECHValidation provides average daily values over the 360-day model cycle.

- Data structure and files: The dataset comprises two CSV files:
  - RMPROTECHValidation: 24 columns (e.g., Day, TempWater, SRP, N, Si, GrazingRate, Flow, Cloud, Windspeed, Lakedepth, Mixeddepth, Daylength, Energyin, Energyout, Totalchl, Species1–Species7, Cyanototal, Diatomtotal). Notes indicate 1 = fully mixed for Mixeddepth.
  - RMPROTECHFuture: 31 columns (e.g., ModelNumber, TemperatureModel, FlowLoadRatio, InternalLoadRatio, ModelDate, TempWater, SRP, N, Si, GrazingRate, Flow, Cloud, Windspeed, Lakedepth, Mixeddepth, Daylength, Energyin, Energyout, Totalchl, Species1–Species7, Cyanototal, Diatomtotal, StratifiedLength, StratStart, StratEnd). A Description field explains each column; notes clarify that 1 means fully mixed for Mixeddepth.

- Additional context and references: The model and data are part of Rostherne Mere ecosystem studies (2016-2017) with field data and analyses described in Radbourne et al. (2018). Foundational references include:
  - CARVALHO et al. (1995) on phosphorus dynamics and restoration strategies
  - ELLIOTT (2010) and MACKAY et al. (2014) on stratification and phosphorus supply
  - MOSS et al. (2005) on nutrient loading consequences
  - MURPHY et al. (2009) on UK Climate Projections (HadRM3-PPE)
  - REYNOLDS et al. (2001) on the ecological basis of PROTECH
  - RADBOURNE et al. (2017, 2018) on Rostherne Mere monitoring and nutrient-ecology-hydrology data
  - Data are located in the NERC Environmental Information Data Centre (Radbourne et al., 2018).