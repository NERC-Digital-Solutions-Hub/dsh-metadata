# The PROTECH model

- Purpose: A one-dimensional, daily-time-step model (PROTECH) that simulates phytoplankton population responses and computes key physical limnological parameters (thermocline development, stratification pattern, nutrient concentrations) in Rostherne Mere. Full model description available in Reynolds et al. (2001) and Elliott et al. (2010); calibrated and evaluated against 2016 lake data.

- Calibration and internal nutrient loading: Initial run indicated a need for internal hypolimnetic soluble reactive phosphorus (SRP) supply. An internal load of 7.8 µg SRP L-1 d-1 added to the bottom 15 m for 90 days (1 June–90 days) matched depth-profile observations. Internal load is assumed not to mix into surface water until stratification breaks down (appropriate for Rostherne Mere’s strong stratification).

- Future climate scenarios: Baseline 2016 simulation re-run under combinations of progressive air temperature increases and nutrient load reductions using UKCP09 projections (11 temperature model simulations). Scenarios run for 10 years with daily steps; analysis uses the final year to capture new driving conditions after stabilization. Temperature changes combined with varying SRP loads: high (100% of 2016 baseline), mid (60%), and low (20%).

- Output data and structure:
  - Two CSV datasets: RMPROTECHValidation and RMPROTECHFuture.
  - Validation dataset (RMPROTECHValidation): 24 columns including Day, TempWater, SRP, N, Si, GrazingRate, Flow, Cloud, Windspeed, Lakedepth, Mixeddepth, Daylength, Energyin, Energyout, Totalchl, andSpecies1–Species7, Cyanototal, Diatomtotal.
  - Future dataset (RMPROTECHFuture): 31 columns including ModelNumber, TemperatureModel, FlowLoadRatio, InternalLoadRatio, ModelDate, plus the same physical/nutrient/ecological variables as in validation, plus StratifiedLength, StratStart, StratEnd.
  - Key variables and units: SRP and N in µg L-1; Totalchl in µg L-1; species abundances in cells mL-1; other environmental drivers (Flow, Cloud, Windspeed, Daylength, Energyin/Out) and stratification indicators (Lakedepth, Mixeddepth, StratifiedLength).

- Data structure notes:
  - RMPROTECHValidation provides daily outputs for a 360-day model cycle; RMPROTECHFuture provides year-average outputs per model run.
  - Table-like descriptions include explicit notes (e.g., “Note 1 means fully mixed”) and detailed column definitions.

- Data provenance and references:
  - Foundational references for PROTECH and related lake dynamics include Carvalho et al. (1995), Elliott (2010), Mackay et al. (2014), Moss et al. (2005), Murphy et al. (2009), Reynolds et al. (2001), Radbourne et al. (2017, 2018).
  - Data source contextualization: Rostherne Mere field data and prior monitoring underpin calibration and interpretation of model outputs.

- Relevance to monitoring and policy:
  - Demonstrates how a coupled physical-nutrient-ecological model can quantify potential responses of phytoplankton communities to climate and nutrient-management scenarios.
  - Provides structured, shareable datasets with metadata-like column descriptions to support transparency, reproducibility, and data governance in monitoring frameworks.