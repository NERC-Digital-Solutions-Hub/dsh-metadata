# Experimental study of ozone exposure on sweet potato (Ipomoea batatas) in solardomes at CEH

## Overview
- Experimental work conducted at the UK Centre for Ecology & Hydrology’s air pollution facility in North Wales.
- Plant material: sweet potato varieties Erato orange, Beauregard, and Murasaki grown from plugs in 25 L pots with John Innes No. 2 compost.
- Setup: randomised distribution across three heated solardomes (ambient + 6°C) with three ozone treatments (Low, Medium, High) and replication (four per treatment per dome).

## Study design and setting
- Ozone exposure treatments:
  - Daytime maximums: Low = 30 ppb, Medium = 80 ppb, High = 110 ppb.
  - Episodic pattern: on two days per week, all domes operated at Low O3 to reflect episodic pollution.
- Planting and harvest timelines varied by variety (dates provided in accompanying table).
- Measurements included physiological and environmental parameters collected weekly or at harvest.

## Treatments and timing
- Treatments administered across three seasons (2019–2021) with start and end dates per variety:
  - Erato orange: planting 11/06/2019; O3 treatment 13/06/2019 to 10/10/2019; harvest 19/11/2019.
  - Beauregard: planting 26/06/2020; O3 treatment 08/08/2020 to 18/10/2020; harvest 04/11/2020.
  - Beauregard: planting 17/05/2021; O3 treatment 03/06/2021 to 25/10/2021; harvest 23/11/2021.
  - Murasaki: planting 17/05/2021; O3 treatment 03/06/2021 to 25/10/2021; harvest 23/11/2021.

## Measurements and outcomes
- Weekly measurements:
  - Stomatal conductance (gs), leaf temperature (TLeaf), light levels.
  - Chlorophyll content index (Chl) and soil moisture status.
  - Air temperature (Tair) and relative humidity (RH) from monitored probes.
- End-of-season harvest:
  - Fresh weight of tubers (yield) and number of tubers per plant.

## Quality control and data handling
- O3 concentrations monitored every 30 minutes using two calibrated analyzers (API 400A and Thermo 49i).
- Porometer calibrated prior to measurements; data cleaned by removing outliers:
  - gs values > 1500 mmol H2O m^-2 s^-1 and light > 2100 µmol m^-2 s^-1 removed.
- Data visually checked for outliers and unusual values.

## Datasets and metadata
- Four CSV data files:
  - Treatment_Data.csv: Date, DayOfYear, Hour, Treatment (Low/Medium/High), O3_ppb (mean hourly).
  - SwtPot_gs_ci.csv: Plant-level measurements including gs, Light, TLeaf, Soil_moisture, Chl, Tair, RH; fields include Date, Time, Treatment, PlantID, Leaf_side.
  - SwtPot_gs_ci_alongVine.csv: Measurements along a vine; includes Leaf_No, along with gs, Light, TLeaf, Soil_moisture, Chl.
  - SwtPot_yield.csv: Harvest data with Date, Variety, Treatment, PlantID, Fresh_weight, No_tubers.
- NA indicates missing measurements.
- Column descriptions provided for each file to support data discovery and reuse.

## Data management and reuse considerations for Data Leaders
- Comprehensive metadata and multiple related data files enable integrated analyses of ozone effects on physiological parameters and tuber yield.
- Clear measurement protocols and quality control steps support data reliability and reproducibility.
- The dataset structure supports cross-variety and cross-season comparisons, with explicit treatment and environmental context.
- Potential considerations:
  - Episodic low-ozone periods introduce design complexity when aggregating treatment effects.
  - Seasonal and varietal differences may affect generalizability; consider stratified analyses.
  - Missing data (NA) in measurements; plan for imputation or exclusion depending on analysis.