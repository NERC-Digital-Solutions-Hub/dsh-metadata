# The PROTECH model

- PROTECH simulates the responses of multiple phytoplankton populations distributed in a 1-dimensional vertical water column at daily time steps and computes key physical limnological parameters (thermocline development, stratification patterns, nutrient concentrations).
- The model and its concepts are described in Reynolds et al. (2001) and Elliott et al. (2010); applied to Rostherne Mere with calibration to observed 2016 data.

- Calibration and internal loading:
  - Initial 2016 simulation revealed a need for an internal hypolimnetic SRP load.
  - Incremental daily SRP additions to the bottom 15 m from 1 June for 90 days; optimal rate found: 7.8 µg SRP L^-1 d^-1.
  - Internal load is not mixed into surface water until stratification breaks down, appropriate for Rostherne Mere during strong stratification.
  - The 90-day internal load period is fixed to occur only during anoxic stratification for all climate scenarios.

- Future climate scenarios:
  - The 2016-calibrated run serves as baseline and is re-run under projected changes to air temperature and nutrient load.
  - Simulations run daily for 10 years; final year analyzed to move away from baseline conditions.
  - Driving data come from UKCP09 projections (11 model simulations) for 25 km^-2 Rostherne Mere grid, with 360-day years (2011-2020, 2051-2060, 2091-2100).
  - Temperature changes are combined with reductions in SRP loads relative to 2016:
    - High: 100% of 2016 internal/external SRP loads
    - Mid: 60% of 2016 loads
    - Low: 20% of 2016 loads

- Nature and units of recorded values:
  - Model outputs include physical, nutrient, and ecological variables; RMPROTECHFuture presents year-average values for each scenario, while RMPROTECHValidation presents average daily values over the 360-day cycle.

- Data files and structure:
  - Two CSV files: RMPROTECHValidation and RMPROTECHFuture.

- RMPROTECHValidation (24 columns):
  - Day; Description = day of model run
  - TempWater = average water column temperature
  - SRP = average soluble reactive phosphorus (µg L^-1)
  - N = average dissolved inorganic nitrogen (µg L^-1)
  - Si = average biogenic silica (µg L^-1)
  - GrazingRate = simulated impact of phytoplankton grazers
  - Flow = inflow rate from catchment
  - Cloud = cloud cover in oktas (0–8)
  - Windspeed = wind speed (m s^-1)
  - Lakedepth = total lake depth
  - Mixeddepth = depth of stratification in Prot ech layer (10 cm from bottom); 1 = fully mixed
  - Daylength = hours of sunlight
  - Energyin = total thermal energy into the lake
  - Energyout = total thermal energy emitted from the lake
  - Totalchl = total chlorophyll in water column (µg L^-1)
  - Species1–Species7 = simulation of various phytoplankton species (cells mL^-1)
  - Cyanototal = cyanobacteria (cells mL^-1)
  - Diatomtotal = diatoms (cells mL^-1)

- RMPROTECHFuture (31 columns):
  - ModelNumber = simulation identifier
  - TemperatureModel = identification of 11 UKCP09 temperature models
  - FlowLoadRatio = ratio of inflow nutrient load from catchment
  - InternalLoadRatio = ratio of internal nutrient load from internal loading
  - ModelDate = date to which future temperature scenarios relate
  - TempWater, SRP, N, Si, GrazingRate, Flow, Cloud, Windspeed, Lakedepth, Mixeddepth, Daylength, Energyin, Energyout, Totalchl, Species1–Species7, Cyanototal, Diatomtotal
  - StratifiedLength = total days of stratification
  - StratStart = day stratification begins
  - StratEnd = day stratification ends

- References and context:
  - CARVALHO et al. 1995; ELLIOTT 2010; MACKAY et al. 2014; MOSS et al. 2005; MURPHY et al. 2009; REYNOLDS et al. 2001; RADBOURNE et al. 2017; RADBOURNE et al. 2018.