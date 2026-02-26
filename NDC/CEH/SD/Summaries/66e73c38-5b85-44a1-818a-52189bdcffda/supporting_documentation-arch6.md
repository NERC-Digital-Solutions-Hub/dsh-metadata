# Ozone exposure experiment on sweet potato: Methods, data files and quality control

## Overview
- Experimental study conducted at the UK Centre for Ecology & Hydrology’s air pollution facility in Abergwyngregyn, North Wales.
- Focus: effects of ozone (O3) exposure on sweet potato physiology and tuber yield.
- Plant material: three varieties (Erato orange, Beauregard, Murasaki) grown as potted plug plants.
- Design: randomized distribution of plants across three heated solardomes with Low, Medium, and High O3 treatments, plus episodic Low O3 days to simulate real-world exposure.
- Measurements collected across 2019–2021 seasons, ending with tuber harvest weights.

## Experimental design
- Environment: three solardomes (ambient + 6°C) with 3 m diameter, 2.1 m height; four replicates per treatment per variety.
- O3 treatments: daytime maximums of 30 ppb (Low), 80 ppb (Medium), and 110 ppb (High); two days per week all domes receive Low O3 to reflect episodic pollution.
- Plant setup: 25 L pots with John Innes No. 2 compost; plants watered manually as needed.
- Variants: Erato orange, Beauregard (orange), Murasaki (white flesh).

## Measurements and data collection
- Weekly measurements during 2019 and 2020 seasons:
  - Leaf stomatal conductance (gs)
  - Leaf temperature (TLeaf)
  - Light (photosynthetically active radiation)
  - Chlorophyll content index (Chl)
  - Soil moisture
  - Air temperature (Tair) and relative humidity (RH)
- Harvest: fresh weight of tubers recorded at end of each growing season.
- Time points: planting dates, O3 exposure start/end dates, and tuber harvest dates are provided per variety.

## Quality control
- O3 concentration monitored every 30 minutes using API 400A and Thermo 49i analyzers; calibration matched between instruments.
- Porometer (Delta-T AP4) calibrated prior to each session with ≤10% curve error.
- Data screening: removal of outliers (gs > 1500 mmol H2O m^-2 s^-1; light > 2100 µmol m^-2 s^-1). A small number of measurements removed.

## Data files and structure
There are four CSV data files, each with detailed column descriptions.

- Treatment_Data.csv
  - Content: Mean hourly O3 treatment concentrations
  - Key columns: Date, DayOfYear, Hour, Treatment (Low/Medium/High), O3_ppb

- SwtPot_gs_ci.csv
  - Content: Plant-level physiological and environmental measurements
  - Key columns: Date, Time, Treatment, PlantID, Leaf_side (B/T), gs, Light, TLeaf, Soil_moisture, Chl, Tair, RH
  - Notes: NA indicates missing measurement

- SwtPot_gs_ci_alongVine.csv
  - Content: Measurements along individual leaves on a vine
  - Key columns: Date, Time, Treatment, PlantID, Leaf_side, gs, Light, TLeaf, Soil_moisture, Chl, Leaf_No
  - Notes: Leaf_No identifies leaf position along the vine; includes similar metrics as SwtPot_gs_ci.csv

- SwtPot_yield.csv
  - Content: Tubers harvested per plant
  - Key columns: Date, Variety, Treatment, PlantID, Fresh_weight, No_tubers
  - Notes: Fresh_weight in grams; No_tubers counts harvested tubers

## How this data can be used (data support perspective)
- Create dashboards or self-serve reports to compare physiological responses (gs, Chl, TLeaf, Soil_moisture) across ozone regimes and varieties.
- Analyze relationships between ozone exposure and tuber yield, considering plant-level variability (PlantID) and along-vine measurements.
- Integrate time-series ozone data with physiological measurements to assess diurnal/episodic exposure effects.
- Promote reproducible analysis pipelines by leveraging the clearly defined QC steps and explicit NA handling.

## Considerations and limitations
- Experimental scope: three O3 treatments across three solardomes with four replicates per treatment; limited to three sweet potato varieties.
- Episodic Low O3 days introduce variability that should be accounted for in analyses.
- Data scope covers 2019–2021 growing seasons; year-to-year environmental variation may influence results.
- Some measurements have missing values (NA) per the data descriptions.