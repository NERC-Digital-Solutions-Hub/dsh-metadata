# Brief description of methods

- Location and purpose
  - Experimental work conducted at the UK Centre for Ecology & Hydrology's air pollution facility in Abergwyngregyn, North Wales.
  - Objective: assess effects of ozone (O3) exposure on sweet potato growth under standardized, replicated conditions using controlled solardomes.

- Experimental design
  - Plants: Sweet potato varieties Erato orange, Beauregard, and Murasaki (potted from plugs; 25 L pots with John Innes No. 2 compost).
  - Setup: Pots randomly distributed across three heated solardomes representing Low, Medium, and High O3 treatments (daytime target maximums of 30 ppb, 80 ppb, and 110 ppb, respectively).
  - Replication: Each solardome contained four replicates per treatment.
  - Timeline: Planting and O3 exposure varied by year (Erato orange in 2019, Beauregard in 2020 and 2021, Murasaki in 2021).

- Ozone treatment regime
  - Episodic exposure: For two days per week, all domes received Low O3 levels to reflect episodic pollution patterns.
  - Treatment labeling: Low, Medium, High O3 levels corresponding to the three domes.

- Measurements and data collection
  - Weekly measurements (during 2019–2021 seasons):
    - Leaf stomatal conductance (gs), leaf temperature (TLeaf), light levels.
    - Chlorophyll content index (Chl) and soil moisture status.
  - Additional metrics:
    - Harvest data: fresh weight of tubers at season end; tuber count.
  - Data captured per plant and, for some datasets, along-leaf-vine measurements.

- Quality control and data integrity
  - O3 concentrations monitored every 30 minutes with matched calibrations (API 400A and Thermo 49i analyzers).
  - Porometer calibrated before each session; concentration data checked for errors.
  - Outlier handling: gs values > 1500 mmol H2O m-2 s-1 and light values > 2100 µmol m-2 s-1 removed (total of two measurements edited).

- Data files and structure
  - Four CSV data files are provided:
    - Treatment_Data.csv: mean hourly O3 treatment concentrations with fields for Date, DayOfYear, Hour, Treatment (Low/Medium/High), and O3_ppb.
    - SwtPot_gs_ci.csv: per-plant measurements including stomatal conductance (gs), Light, TLeaf, Soil_moisture, Chlorophyll (Chl), Tair, RH; includes PlantID, Leaf_side, and temporal fields.
    - SwtPot_gs_ci_alongVine.csv: along-vine measurements (gs, Light, TLeaf, Soil_moisture, Chl) with Leaf_No indicating position along the vine.
    - SwtPot_yield.csv: harvest outcomes with Date, Variety, Treatment, PlantID, Fresh_weight, No_tubers.
  - Each file includes descriptions of column headings and missing-value indicators (NA).

- Relevance to environmental monitoring
  - Demonstrates a standardized, QA-bound workflow for collecting environmental exposure data (O3) and plant-response metrics suitable for time-series monitoring and policy assessment.
  - Data are stored in clearly structured datasets that can be combined with other environmental datasets to enhance the value of monitoring ecosystems and air quality impacts, aligning with aims of ensuring data accessibility and reusability.