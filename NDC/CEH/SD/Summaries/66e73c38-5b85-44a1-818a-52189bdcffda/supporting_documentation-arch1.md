# Brief description of methods

- Experimental setting and plant material
  - Location: UK Centre for Ecology & Hydrology air pollution facility, Abergwyngregyn, North Wales (53.2°N, 4.0°W)
  - Plant material: Sweet potato plug plants (Ipomoea batatas) in 25 L tubs with John Innes No. 2 compost; manual watering
  - Varieties: Erato orange, Beauregard, and Murasaki (two orange, one white-fleshed)
  - Growth structure: Three heated solardomes (3 m diameter, 2.1 m height); pots randomly distributed across domes; four replicates per dome

- O3 treatments and experimental design
  - Treatments: Low, Medium, High ozone with daytime max targets of 30, 80, and 110 ppb, respectively
  - Episodic exposure pattern: For two days each week, all domes receive the Low O3 level
  - Design: Each solardome corresponds to a treatment level; replicates are plants within each dome
  - Timeline: Planting and O3 exposure periods and tuber harvest dates are detailed in Table 1 for each variety

- Measurements and data collection
  - Weekly measurements (during 2019 and 2020 seasons): leaf stomatal conductance (gs), leaf temperature (TLeaf), light (photosynthetically active radiation)
  - Ancillary measurements: leaf chlorophyll content index (Chl) and soil moisture status
  - End-of-season harvest: fresh weight of tubers (yield)
  - Instruments: porometer for gs and light; Opti-Sciences CCM200 for chlorophyll; Delta-T ML2 probe for soil moisture; automatic probes (Skye Instrument) for air temperature and relative humidity
  - Additional data: Time-stamped records (Date, Time/Hour, DayOfYear) and PlantID; leaf side (top/bottom) and along-vine leaf position in extended data

- Quality control and data cleaning
  - O3 validation: ozone concentrations measured every 30 minutes using API 400A and Thermo 49i analyzers with matched calibration
  - Instrument calibration: Delta-T AP4 porometer calibrated to curve error ≤ ~10%
  - Data cleaning: remove outliers such as gs > 1500 mmol H2O m-2 s-1 and light > 2100 µmol m-2 s-1 (two measurements removed total)
  - Data verification: graphical checks for outliers and unusual values

- Datasets available (four CSV files)
  - Treatment_Data.csv: Mean hourly O3 treatment concentrations
    - Columns include Date, DayOfYear, Hour, Treatment (Low/Medium/High), O3_ppb
  - SwtPot_gs_ci.csv: Plant-level measurements
    - Columns: gs (stomatal conductance), Light, TLeaf (leaf temperature), Soil_moisture, Chl (chlorophyll index), Tair, RH, plus Date, Time, Treatment, PlantID, Leaf_side
  - SwtPot_gs_ci_alongVine.csv: Along-vine measurements (per leaf)
    - Similar columns to SwtPot_gs_ci.csv plus Leaf_No and repeated measurements along the vine
  - SwtPot_yield.csv: Harvest data
    - Columns: Date, Variety, Treatment, PlantID, Fresh_weight (g), No_tubers

- Key considerations for analysis
  - Mixed-effects modeling with PlantID as a random effect to account for repeated measures
  - Fixed effect of ozone Treatment (Low/Medium/High) on physiological responses and yield
  - Longitudinal data structure: weekly measurements enable temporal trend analysis
  - Multiple data granularities: per-plant, per-leaf (along vine), and end-of-season yield data
  - Data gaps and potential scale issues: cross-year differences (2019 vs 2020), missing values indicated as NA
  - Data provenance: explicit documentation of data sources and measurement conditions to support reproducibility and cross-dataset integration