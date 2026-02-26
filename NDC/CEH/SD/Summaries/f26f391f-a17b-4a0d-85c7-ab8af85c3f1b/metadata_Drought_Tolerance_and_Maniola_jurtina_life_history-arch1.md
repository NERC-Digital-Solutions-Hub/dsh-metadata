# Life history data

## Overview
- Study of life history traits using newly hatched larvae from nine UK populations.
- Larvae reared on Poa trivialis host plants under two conditions: control and drought-stressed.
- Outdoor insectary at UK Centre for Ecology & Hydrology (UKCEH) with protective netting, exposing larvae to natural temperature, light, and photoperiod.
- Sample sizes: 108 larvae in control; 216 larvae in drought-stress, with equal representation from each laboratory source population across treatments.
- Experimental design ensures four larvae per plant, all from the same laboratory source population per plant.

## Experimental design and data collection
- Larvae placed on potted Poa trivialis plants and housed in cages within the outdoor insectary.
- Drought stress expected to elevate mortality relative to control.
- Growth monitored at three time points:
  - 49 days after hatching (pre-overwintering)
  - 162 days after hatching (post-overwintering during larval growth)
  - 309 days after hatching (late larval growth and pupation)
- At the second check (162 days), larval mass recorded for all surviving individuals.
- At the third check (309 days), record whether each larva survived to this stage.

## Data structure and headers
- Population: Site in the UK where the population originated.
- PlantID: Unique identifier for the host plant used for rearing.
- LarvalID: Identifier for each larva (1–4 per plant).
- HostPlantTreatment: Drought-stress vs. control.
- HatchDate: Hatch date for the larvae.
- CheckDate1: Date of the first growth monitoring (49 days).
- CheckDate2: Date of the second growth monitoring (162 days).
- NumLarvaeFound: Number of larvae found at the second monitoring point.
- LarvalMass: Mass of each larva (mg) at the second monitoring point.
- SurviveCheck: Survival status to the third point (1 = survived, 0 = did not survive).
- Note: Empty cells indicate missing data (e.g., due to larval death).

## Quality control and data handling
- Data collected under standardized methods using published procedures.
- Manual data entry with quality assurance tools (input masks, input conditions) to ensure data coherence.
- Data management practices include tracking data sources and enabling discoverability with metadata.

## Potential analyses and interpretation
- Assess effects of host plant drought stress on larval growth (mass) and survival, controlling for population origin and plant identity.
- Explore interactions between population source, plant treatment, and larval performance.
- Consider time-point data to examine growth trajectories and overwintering outcomes.
- Data facilitate correlations between early growth (mass at 162 days) and late-stage survival (to 309 days), with treatment and source population as factors.