# The PROTECH model

## Purpose and scope
- Simulates phytoplankton population responses in a 1-dimensional vertical water column at daily time steps.
- Calculates key physical limnological parameters (thermocline development, stratification patterns, nutrient concentrations).
- Calibrated against Rostherne Mere lake data (2016); includes an internal hypolimnetic SRP (soluble reactive phosphorus) load to match observed profiles during stratification.

## Calibration details
- Initial 2016 simulation indicated a need for internal SRP loading in the bottom 15 m from 1 June for 90 days.
- Optimal internal load: 7.8 µg SRP L^-1 d^-1.
- Internal SRP is assumed not to mix into surface water until stratification breaks down, appropriate for strongly stratifying Rostherne Mere.
- The 90-day internal load period is fixed to ensure load occurs only during anoxic stratification across all climate scenarios.

## Future climate scenarios
- Baseline (2016) run used as reference; future runs apply changes to air temperature and nutrient load.
- Simulations run daily for 10 years; analysis uses the final year to allow stabilization under new conditions.
- Temperature scenarios derived from UKCP09 projections (11 model simulations) using 360-day years for Rostherne Mere (HadRM3-PPE).
- Temperature changes combined with SRP load reductions relative to 2016: High (100%), Mid (60%), Low (20%).

## Data and outputs

- Datasets and files:
  - RMPROTECHValidation: 24 columns; daily model outputs for a 360-day cycle.
  - RMPROTECHFuture: 31 columns; year-average outputs per future scenario.

- Key columns in RMPROTECHValidation (examples):
  - Day, TempWater, SRP (µg L^-1), N (µg L^-1), Si (µg L^-1), Totalchl (µg L^-1)
  - GrazingRate, Flow, Cloud (oktas, 0–8), Windspeed (m s^-1)
  - Lakedepth, Mixeddepth (10 cm from bottom; 1 = fully mixed), Daylength (hours)
  - Energyin, Energyout, Species1–Species7 (cells mL^-1), Cyanototal (cells mL^-1), Diatomtotal (cells mL^-1)

- Key columns in RMPROTECHFuture (examples):
  - ModelNumber, TemperatureModel (UKCP09 models), FlowLoadRatio, InternalLoadRatio
  - ModelDate, TempWater, SRP, N, Si, Totalchl
  - GrazingRate, Flow, Cloud, Windspeed, Lakedepth, Mixeddepth
  - Daylength, Energyin, Energyout, Species1–Species7, Cyanototal, Diatomtotal
  - StratifiedLength, StratStart, StratEnd

- Output characteristics:
  - RMPROTECHValidation provides average daily values across the 360-day cycle.
  - RMPROTECHFuture provides year-average values for each future projection.

## Data structure and units
- Units (where specified):
  - SRP: µg L^-1; N: µg L^-1; Si: µg L^-1; Totalchl: µg L^-1
  - Flow: inflow from catchment (units not explicitly stated)
  - Windspeed: ms^-1; Cloud: okta scale (0–8); Daylength: hours
  - Species counts: cells mL^-1; Cyanototal and Diatomtotal: cells mL^-1
- Depth-related indicators:
  - Lakedepth: total lake depth
  - Mixeddepth: depth of stratification in PROTECH layer (10 cm from bottom); 1 indicates fully mixed
- Stratification timing:
  - StratifiedLength: total days of stratification
  - StratStart/StratEnd: day-of-model-year stratification begins/ends

## GIS-focused considerations

- What can be mapped or visualized:
  - Vertical profiles over time: temperature, SRP, chlorophyll, nutrients, and phytoplankton abundances as functions of depth and day.
  - Stratification dynamics: depth of mixing (Mixeddepth), duration of stratification (StratifiedLength), and stratification timing (StratStart/End).
  - Surface vs. bottom conditions: surface (TempWater, SRP, Totalchl) versus bottom layers (internal SRP load effects).
  - Model scenarios: compare future projections (High/Mid/Low SRP load) and temperature model impacts on ecological variables.

- GIS integration notes:
  - The PROTECH model is 1D (vertical) and configured for Rostherne Mere; to map spatially, couple outputs with a bathymetric lake polygon and derive representative depth layers or extract 1D profiles at multiple locations.
  - Build time-series or depth-sliced raster/3D visualizations from CSV data by linking Day and Depth (via derived layers) to map features.

- Data quality and limitations:
  - Data reflect a single-lraction lake system with 1D vertical structure; horizontal spatial variability is not captured.
  - Calibration hinges on 2016 observations and a fixed 90-day internal SRP loading period.
  - Future scenarios rely on UKCP09 projections and assumed loading scenarios; interpretation should consider uncertainties in climate and nutrient load estimates.

## References and data provenance
- Foundational and supporting works:
  - PROTECH modeling framework: Reynolds et al. 2001; Elliott et al. 2010.
  - Rostherne Mere phosphorus dynamics and stratification studies: Carvalho et al. 1995; Moss et al. 2005; Mackay et al. 2014; Radbourne et al. 2017, 2018.
  - UK climate projections: Murphy et al. 2009 (HadRM3-PPE; UKCP09).
  - Related data collection and lake monitoring: Radbourne et al. (2017, 2018) and associated databanks.