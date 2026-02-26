# Life history data

- Purpose: Document experimental life-history data for newly hatched larvae collected from nine UK populations, reared on Poa trivialis under control or drought-stressed conditions, in an outdoor netted insectary under natural conditions.

- Experimental design and rearing setup:
  - Nine UK populations represented; larvae sourced from laboratory stock populations.
  - Four larvae per plant, all from the same lab source per plant.
  - Host plants: Poa trivialis, with two treatments—control and drought stress.
  - Rearing environment: outdoor netted cages in UKCEH, protected from rain/wind but exposed to natural temperatures, light, and photoperiod.
  - Replication: total of 108 larvae in control and 216 larvae in drought-stress groups, with equivalent numbers from each laboratory source contributing to each treatment.

- Monitoring and measurements:
  - Three growth checks: 49 days (pre-overwintering), 162 days (post-overwintering growth), 309 days (late growth and pupation).
  - Mass measurements: larval masses recorded at the second check (162 days) for all survivors.
  - Survival tracking: number of larvae surviving to the third check (309 days) recorded.

- Data structure and headers (key fields and meanings):
  - Population: site in the UK where the population was sourced.
  - PlantID: unique identifier for each host plant used for larval rearing.
  - LarvalID: larva identifier (1–4 per plant).
  - HostPlantTreatment: drought stress vs. control treatment applied to the host plant.
  - HatchDate: hatch date and assignment date to the host plant treatment.
  - CheckDate1: date of first growth monitoring (49 days).
  - CheckDate2: date of second growth monitoring (162 days).
  - NumLarvaeFound: number of larvae found at the second growth monitoring point.
  - LarvalMass: larval mass (mg) at the second growth monitoring point.
  - SurviveCheck: survival status to the third growth point (1 = survived, 0 = not survived).
  - Missing data: empty cells indicate missing data (e.g., death of a larva).

- Quality control:
  - Data collected under standardized conditions using published methods.
  - Manual data entry enforced with quality assurance tools (input masks, input conditions) to ensure data coherence.

- GIS-relevant implications:
  - Spatial mapping potential using Population (site) as a geographic dimension, with attributes per PlantID/LarvalID.
  - Comparative analysis across treatments (HostPlantTreatment) and outcomes (SurviveCheck, NumLarvaeFound, LarvalMass).
  - Integration with environmental layers (e.g., drought conditions, temperature) to explore spatial-temporal patterns in larval development and survival.

- Limitations and considerations for GIS use:
  - Missing data due to mortality; some fields may be incomplete.
  - Data tied to specific host plants and laboratory-source populations, which may affect generalizability.
  - Temporal checks are fixed points, reflecting specific time frames since hatching.