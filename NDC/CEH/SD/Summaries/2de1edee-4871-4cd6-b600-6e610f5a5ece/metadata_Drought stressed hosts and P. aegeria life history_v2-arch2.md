# Life history data

- Aim
  - Provide standardized data to monitor environmental health and policy performance over time by comparing life-history and morphological responses across landscape origins and drought-stress treatments.

- Study design and system
  - Four laboratory populations from Belgium: two from deciduous woodland (Lauzelle, St. Hubert) and two from agricultural landscapes (Lillois, Hoegaarden).
  - Newly hatched larvae randomly selected and assigned (three per plant; all from the same source population) to either control or drought-stressed P. trivialis host plants.
  - Larvae reared in climate-controlled common-garden conditions until eclosion as adults.
  - Sample sizes: 178 larvae in control; 390 in drought-stress treatment, with each source population contributing equally to both treatments.
  - On eclosion, adults weighed and sexed.

- Life history data collected
  - Date of eclosion; total development time from egg hatching to adult eclosion (days); square-root transformed development time for analyses.
  - Adult mass at eclosion (mg) and sex (m/f).

- Female reproductive output data
  - 100 females total (50 woodland-origin, 50 agricultural-origin) reared with a male and a plant for oviposition.
  - Measurements per female: total number of eggs laid, mean egg size, longevity, and timing metrics.
  - Reproductive metrics include: number of days until first egg after male introduction and the proportion of eggs hatched (with arcsine square-root transformation for analysis).

- Wing data and flight morphology
  - Post-mortem wing measurements: forewing surface area, hindwing surface area, forewing length; forewing melanization; wing loading (mg/mm^2); and forewing aspect ratio.

- Data format and headers (CSV)
  - Life_history_data.csv
    - Headers include: Description, Population, Landscape, Treatment, ID, Adult_mass, Total_development_time, Square_root_Total_devtime, sex
  - Female_reproductive_output_data.csv
    - Headers include: Population, Description, Landscape, Description (treatment), ID, Adult_mass, Mean_egg_size, Longevity, Number_days_until_First_egg_laid, Fecundity, Arcsine_square_root_%Eggs_hatched, %Eggs_hatched
  - Wing_data.csv
    - Headers include: Population, Description, Landscape, Treatment, ID, Adult_mass, Total_development_time, sex, Wing_loading, Mean_forewing_Melanin, Mean_FW_aspect_ratio, Total_Wing_area

- Data quality and accessibility
  - Empty cells denote missing data (e.g., death of the butterfly).
  - Data are verified, quality assured, cleaned, and transformed; stored in standardized formats and prepared for publication or portal upload.
  - Outputs are presented in clear formats (reports, maps, charts) to facilitate environmental monitoring and policy assessment.

- Context and notes
  - Host plant: Phytolacca trivialis (P. trivialis) used for larval rearing.
  - Experimental environment: climate room with common garden conditions.
  - The dataset enables cross-population and cross-landscape comparisons under drought stress, contributing to environmental monitoring efforts by providing multi-dimensional life-history and morphological data.