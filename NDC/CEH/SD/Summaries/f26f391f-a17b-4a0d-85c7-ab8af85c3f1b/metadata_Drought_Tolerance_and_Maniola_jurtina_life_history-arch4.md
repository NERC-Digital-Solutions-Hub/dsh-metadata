# Life history data

## Overview
- Dataset of life-history data for newly hatched larvae from nine UK populations.
- Larvae reared on Poa trivialis plants under two conditions: control and drought-stressed.
- Outdoor insectary conditions with natural temperature, light, and photoperiod; cages shielded from rain and wind.
- Sample sizes: 108 larvae in control, 216 in drought stress; equal representation from each laboratory source population.

## Experimental design and collection method
- Larvae randomly selected from laboratory stock populations (nine UK populations) and placed on host plants (four larvae per plant) all from the same source population.
- Plants: Poa trivialis; treatments: control or drought-stressed.
- Rearing environment: netted outdoor insectary at UK Centre for Ecology & Hydrology, providing protection from rain/wind but natural temperatures and photoperiod.
- Monitoring: three growth checks at 49 days (pre-overwintering), 162 days (post-overwintering during growth), and 309 days (late growth and pupation).
- Measurements: larval mass recorded at the second check; number of larvae surviving to the third check recorded.

## Data structure and headers
- Population, Description: site in the UK from which the population was sourced.
- PlantID, Description: unique identifier for each host plant used for rearing.
- LarvalID, Description: larval identifier, numbered 1–4 per plant (four larvae per host plant).
- HostPlantTreatment, Description: drought stress vs. control treatment for the host plant.
- HatchDate, Description: date larvae hatched and assigned to the host plant treatment.
- CheckDate1, Description: date of the first growth monitoring point (49 days after hatching).
- CheckDate2, Description: date of the second growth monitoring point (162 days after hatching).
- NumLarvaeFound, Description: number of larvae found at the second growth monitoring point.
- LarvalMass, Description: mass of larva (in mg) at the second growth monitoring point.
- SurviveCheck, Description: survival status to the third growth monitoring point (1 = survived, 0 = not survived).
- Note: empty cells indicate missing data (e.g., due to larval death).

## Quality control and data management
- Data collected under standardized conditions using published methods.
- Data entry performed manually with quality assurance tools (input masks, input conditions) to ensure data coherence.