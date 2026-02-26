# Life history data

- Overview
  - Newly hatched larvae were randomly selected from laboratory stock populations originating from nine UK populations.
  - Larvae were placed on potted Poa trivialis host plants, either control or drought-stressed.
  - Rearing occurred in netted outdoor insectary at UK Centre for Ecology & Hydrology under natural environmental conditions.
  - Four larvae per plant, all from the same laboratory source population for each plant.
  - Total larvae: 108 in control and 216 in drought-stress groups; each laboratory source contributed equally to both treatments.

- Experimental design and data collection
  - Monitored at three growth check points:
    - CheckDate1: 49 days after hatching (pre-overwintering)
    - CheckDate2: 162 days after hatching (post-overwintering during larval growth)
    - SurviveCheck (at 309 days after hatching): late larval growth and pupation phase
  - Measurements:
    - Larval mass (mg) recorded for individuals that survived to CheckDate2 using an Ohaus Explorer balance (accuracy 0.1 mg)
    - Number of larvae surviving to the third check (CheckDate3) recorded as NumLarvaeFound and SurviveCheck (1 = survived, 0 = not survived)
  - Experimental setup:
    - Outdoor insectary provides protection from rain and wind but exposes larvae to natural temperatures, light, and photoperiod.

- Data structure and headers
  - Population: site in the UK from which the population was sourced
  - PlantID: unique identifier for each host plant used
  - LarvalID: identifier for each larva (1–4 per plant)
  - HostPlantTreatment: drought stress vs. control treatment
  - HatchDate: date larvae hatched and assigned to plant treatment
  - CheckDate1: date of first growth monitoring (49 days)
  - CheckDate2: date of second growth monitoring (162 days)
  - NumLarvaeFound: number of larvae found at CheckDate2
  - LarvalMass: larval mass (mg) at CheckDate2
  - SurviveCheck: survival status to the third growth stage (1 = survived, 0 = not survived)
  - Note: empty cells indicate missing data (e.g., due to death)

- Quality control and data integrity
  - Data collected under standardised conditions using published methods
  - Manual data entry with quality assurance tools (input masks, input conditions) to ensure data coherence

- Notes on interpretation and potential analyses
  - The design anticipates higher mortality under drought stress, enabling comparisons of growth and survival between treatments across populations.
  - The dataset allows analyses of mass at 162 days, survival rates to 309 days, and survival patterns by population, plant, and treatment.
  - Data are suitable for creating self-serve products (e.g., summaries, dashboards) to explore growth and survival dynamics under drought vs. control conditions.