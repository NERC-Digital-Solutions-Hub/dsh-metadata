# Brief description of methods

- Experimental context and location
  - Conducted at the UK Centre for Ecology & Hydrology's air pollution facility, Abergwyngregyn, North Wales.
  - Focus on sweet potato (Ipomoea batatas) varieties: Erato orange, Beauregard (orange flesh), and Murasaki (white flesh).
  - Plants grown in 25 L pots with John Innes No. 2 compost; manual watering.

- Experimental design
  - Three heated solardomes (ambient +6 °C) used to impose ozone (O3) treatments.
  - Treatments: Low, Medium, High daytime max O3 targets of 30, 80, and 110 ppb, respectively.
  - Episodic exposure: for two days per week, all domes operated at Low O3 to mimic episodic pollution.
  - Randomized distribution with four replicates per treatment within each dome.
  - Trials conducted across 2019 and 2020 seasons; tuber harvests recorded at season end.

- Measurements and data collected
  - Weekly measurements: leaf stomatal conductance (gs), leaf temperature, light; plus simultaneous readings of leaf chlorophyll content index and soil moisture.
  - End-of-season harvest: fresh weight of tubers.
  - Planting/treatment timeline per variety provided (dates of planting, O3 exposure, and harvest).
  - Additional notes: multiple varieties and life stages included, with harvests occurring in 2019, 2020, and 2021 for Beauregard and Murasaki.

- Quality control and data integrity
  - O3 concentrations inside domes monitored every 30 minutes with matched calibration between two analyzers (API 400A and Thermo 49i).
  - Porometer (Delta-T AP4) calibrated before each session; curve error kept ≤ ~10%.
  - Outlier handling: gs values > 1500 mmol H2O m^-2 s^-1 and light values > 2100 µmol m^-2 s^-1 removed.
  - Graphical screening for outliers and unusual values; two measurements removed in total.

- Data files and schema
  - Four CSV files provided:
    1) Treatment_Data.csv: mean hourly O3 treatment concentrations with fields Date, DayOfYear, Hour, Treatment (Low/Medium/High), O3_ppb.
    2) SwtPot_gs_ci.csv: plant-level measurements including gs, Light, TLeaf, Soil_moisture, Chlorophyll, Tair, RH; with Date, Time, PlantID, Leaf_side, and treatment.
    3) SwtPot_gs_ci_alongVine.csv: along-vine leaf measurements with additional Leaf_No indicating leaf position along the vine.
    4) SwtPot_yield.csv: harvest data including Fresh_weight and No_tubers per PlantID, by Variety and Treatment.
  - Descriptions for each column are included within the files; missing data indicated as NA.
  - Units and measurement methods are documented alongside variables (e.g., gs in mmol H2O m^-2 s^-1; Light in µmol m^-2 s^-1; Tair in °C).

- Data governance and use considerations for stewardship
  - Rich, well-documented metadata for each file and column supports discoverability and reuse.
  - Per-plant identifiers, treatment groups, and time-stamped measurements enable traceability and provenance.
  - Explicit data cleaning steps and QC criteria enhance dataset reliability and interoperability.
  - The structured format supports integration into portals or catalogues to aid sharing, while preserving the ability to assess data limitations (e.g., incomplete timing in weekly measurements, potential variability across varieties and years).