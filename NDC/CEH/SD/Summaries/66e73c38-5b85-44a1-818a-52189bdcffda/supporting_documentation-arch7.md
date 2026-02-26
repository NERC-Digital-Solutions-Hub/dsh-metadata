# Brief description of methods

- Location and setting
  - Experimental work conducted at the UK Centre for Ecology & Hydrology's air pollution facility, Abergwyngregyn, North Wales.
  - Site features: three heated solardomes (ambient + 6°C) used to create Low, Medium, and High ozone (O3) treatments.

- Plant material and experimental design
  - Sweet potato ( Ipomoea batatas ) plug plants from Thompson and Morgan.
  - Varieties: two orange fleshed ( Erato orange, Beauregard ) and one white fleshed ( Murasaki ).
  - Pots: 25 L tubs with John Innes No. 2 compost; randomly distributed across four replicates per treatment.
  - Treatments: O3 target maximums of 30 ppb (Low), 80 ppb (Medium), and 110 ppb (High).
  - Episodic exposure: two days per week all domes operated at Low O3 level to reflect episodic pollution.

- Measurements and data collection
  - Weekly measurements during 2019 and 2020 seasons:
    - Leaf stomatal conductance (gs), leaf temperature (TLeaf), and light.
    - Chlorophyll content index (Chl) and soil moisture status.
  - Additional environmental data:
    - Air temperature (Tair) and relative humidity (RH) recorded every 30 minutes.
  - Harvest data:
    - End-of-season fresh weight of tubers and counts (No_tubers).

- Quality control and data cleaning
  - O3 concentrations measured every 30 minutes with calibrated analyzers (API 400A and Thermo 49i).
  - Delta-T AP4 porometer calibration prior to measurements (curve error ≤ ~10%).
  - Outlier handling: remove gs > 1500 mmol H2O m^-2 s^-1 and Light > 2100 µmol m^-2 s^-1; total of two measurements removed.

- Data files and formats
  - Four CSV datasets:
    1) Treatment_Data.csv — mean hourly O3 treatment concentrations; fields include Date, DayOfYear, Hour, Treatment, O3_ppb.
    2) SwtPot_gs_ci.csv — gs, Light, TLeaf, Soil_moisture, Chl, Tair, RH; per measurement; includes Date, Time, Treatment, PlantID, Leaf_side, etc.
    3) SwtPot_gs_ci_alongVine.csv — same as above, plus Leaf_No indicating leaf position along the vine.
    4) SwtPot_yield.csv — harvest data; Date, Variety, Treatment, PlantID, Fresh_weight (g), No_tubers.
  - NA denotes missing measurements.
  - Descriptions provided for all columns to aid interpretation and reuse.

- Data integration and potential GIS applications
  - The dataset provides time-stamped, plant- and leaf-level physiological measurements across spatially distinct experimental units (domes, pots, vines).
  - GIS-ready opportunities:
    - Spatial mapping of treatment regimes across domes and replicates.
    - Spatial-temporal visualization of gs, Chl, TLeaf, and soil moisture under different O3 levels.
    - Linking stomatal and chlorophyll metrics to harvest yields by plot/replicate.
    - Incorporating environmental time-series (O3 concentrations, Tair, RH) for time-series mapping and analysis.
  - Considerations for GIS workflows:
    - Aligning measurements by Date/Time to create synchronized spatiotemporal layers.
    - Handling missing data and unit consistency across measurements.
    - Establishing metadata standards to describe domes, pots, and plant IDs for reproducibility.