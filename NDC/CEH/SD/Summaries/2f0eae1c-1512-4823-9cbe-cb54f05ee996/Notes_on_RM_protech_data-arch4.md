# The PROTECH model

- Purpose and scope
  - PROTECH simulates responses of multiple phytoplankton populations in a one-dimensional vertical water column with daily time steps.
  - It also calculates key physical limnological parameters (thermocline development, stratification pattern, nutrient concentrations).
  - The model output supports analysis of phytoplankton dynamics under climate and nutrient scenarios.

- Calibration and baseline data
  - The 2016 Rostherne Mere observed data were used as the baseline.
  - An internal hypolimnetic SRP supply (7.8 µg SRP L-1 d-1) to the bottom 15 m for 90 days (June 1) was required to match observed hypolimnetic SRP during stratification.
  - Internal loading is assumed not to mix into surface water until stratification breaks down, appropriate for strongly stratified Rostherne Mere.

- Future climate scenarios
  - Baseline 2016 simulation re-run under future climate conditions for 10 years; analysis uses only the final year to ensure stabilization under new driving conditions.
  - Temperature scenarios drawn from UKCP09 with 11 model simulations, covering:
    - 2011–2020, 2051–2060, and 2091–2100 (25 km-2 Rostherne Mere grid).
  - Nutrient loads scaled relative to 2016:
    - Internal and external SRP loads multiplied by 100% (high), 60% (mid), or 20% (low).
  - Outputs include daily and yearly summaries to compare baseline and future conditions.

- Data outputs and structure
  - Two CSV files: RMPROTECHValidation and RMPROTECHFuture.
  - RMPROTECHValidation (24 columns) contains daily model outputs for a 360-day cycle:
    - Day, Description, TempWater, SRP, N, Si, GrazingRate, Flow, Cloud, Windspeed, Lakedepth, Mixeddepth (1 = fully mixed), Daylength, Energyin, Energyout, Totalchl, Species1–Species7, Cyanototal, Diatomtotal.
  - RMPROTECHFuture (31 columns) contains model-run summaries for future scenarios:
    - ModelNumber, TemperatureModel, FlowLoadRatio, InternalLoadRatio, ModelDate, TempWater, SRP, N, Si, GrazingRate, Flow, Cloud, Windspeed, Lakedepth, Mixeddepth, Daylength, Energyin, Energyout, Totalchl, Species1–Species7, Cyanototal, Diatomtotal, StratifiedLength, StratStart, StratEnd.
  - Data descriptions and units are provided alongside each field; notes indicate that RMPROTECHFuture presents year-average values per model run, while RMPROTECHValidation presents average daily values over the 360-day cycle.

- Data quality, metadata, and provenance
  - The dataset includes explicit metadata on variables, units, and the meaning of each column.
  - References accompany the modeling approach, including foundational works (e.g., Reynolds et al., 2001) and context for observed data and nutrient dynamics (e.g., Carvalho et al., 1995; Moss et al., 2005).
  - The data structure supports reproducibility and cross-scenario comparison, with clearly defined scenario parameters (TemperatureModel, FlowLoadRatio, InternalLoadRatio).

- References and context
  - Key scientific references underpinning the model and its application, including PROTECH development and lake nutrient dynamics studies.
  - The dataset provides traceable lineage to Rostherne Mere monitoring (2016–2017) and UK climate projection sources (UKCP09 HadRM3-PPE ensemble).