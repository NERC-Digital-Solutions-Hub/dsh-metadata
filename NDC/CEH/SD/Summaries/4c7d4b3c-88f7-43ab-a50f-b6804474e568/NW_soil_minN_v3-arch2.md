# NW_soil_minN.csv

- Purpose and context
  - Supplement to supporting documentation for data series; contains soil inorganic nitrogen (NH4-N and NO3-N + NO2-N) concentrations and soil moisture.
  - Data from a grassland fertiliser trial conducted in 2016 at North Wyke Research Station (Rothamsted Research).
  - Aimed at enabling consistent environmental monitoring and assessment of nitrogen dynamics under different fertiliser treatments.

- Dataset characteristics
  - 9 columns, 512 rows.
  - Variables include sampling date, experimental design factors, treatment types, and soil chemical/physical measurements.

- Columns and meanings (with units)
  - Date: Date of sampling
  - N_app: fertiliser application event (1, 2, or 3); 1st/2nd applications 90 kg ha-1, 3rd application 60 kg ha-1
  - Block: blocking factor in a randomized block design (1–4)
  - Plot: plot identifier (1–16)
  - Treatment: fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0N control)
  - Soil_NH4_mgNkg: ammonium concentration; mg NH4-N per kg soil (dry weight basis)
  - Soil_NO3_NO2_mgNkg: nitrate + nitrite concentration; mg NO3-N per kg soil (dry weight basis)
  - moisture_dry: soil moisture on a dry weight basis (g H2O per g dry soil)
  - moisture_wet: soil moisture on a wet weight basis (g H2O per g wet soil)

- Sampling design and laboratory methods
  - Soil sampled from 0–10 cm depth using a 25 mm diameter corer.
  - For each plot, 6–8 subsamples were combined (bulk sampled).
  - Extraction: 2 M KCl (50 g fresh soil : 100 ml KCl); shaken for 60 minutes at 150 rpm.
  - NH4-N analysis: discrete photometric analysis.
  - NO3-N + NO2-N analysis: discrete photometric analysis.
  - Soil moisture: determined after drying at 105°C for at least 24 hours.

- Data provenance and use
  - Part of a structured monitoring dataset for environmental nitrogen dynamics under different fertiliser regimes.
  - Designed for storage and upload to monitoring portals; aligns with standardized data handling and quality assurance practices.