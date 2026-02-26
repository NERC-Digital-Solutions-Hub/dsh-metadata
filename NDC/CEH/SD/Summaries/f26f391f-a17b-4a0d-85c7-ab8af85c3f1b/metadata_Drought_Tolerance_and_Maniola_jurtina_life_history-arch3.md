# Experimental design/collection method: Life history data

## Overview
- Study of life-history traits of newly hatched larvae from nine UK laboratory populations.
- Treatments: drought-stressed vs. control Poa trivialis host plants.
- Outdoor insectary rearing under natural conditions with protective enclosure.
- Three growth monitoring points to assess development: 49 days (pre-overwintering), 162 days (post-overwintering growth), and 309 days (late growth and pupation).
- Metrics: larval mass at the second check and survival to the third check; population-level representation ensured by equal contributions from each source population.

## Experimental design and collection methods
- Larvae: randomly selected from lab stock populations (nine populations), four larvae per plant.
- Allocation: larvae placed on host plants within netted cages, with equal numbers assigned to control and drought treatments across populations.
- Rearing environment: outdoor insectary at UK Centre for Ecology & Hydrology (UKCEH), enclosed with half solid walls and half wire mesh; protection from rain/wind but exposure to natural temperature, light, and photoperiod.
- Sample sizes: 108 larvae in control; 216 larvae in drought-stress group.
- Monitoring: three growth checks; data collected only for individuals surviving to the second check for mass measurements; survival data recorded up to the third check.

## Data structure and headers
- Population: site in the UK where the population was sourced.
- PlantID: unique identifier for each host plant used for rearing.
- LarvalID: labels 1–4 for larvae per plant.
- HostPlantTreatment: drought stress vs. control.
- HatchDate: date larvae hatched and assigned to the plant treatment.
- CheckDate1: date of first growth check (49 days).
- CheckDate2: date of second growth check (162 days).
- NumLarvaeFound: number of larvae found at the second check.
- LarvalMass: larva mass in mg at the second check.
- SurviveCheck: whether the larva survived to the third check (1 = survived, 0 = not survived).
- Notes: empty cells indicate missing data (e.g., due to larval death).

## Quality control and data management
- Standardised data collection: standardized conditions and published methods.
- Data entry: manual entry with quality assurance tools (input masks, input conditions) to ensure coherence.
- Instrument precision: mass measured with an Ohaus Explorer balance (accuracy 0.1 mg).
- Data transparency: missing data explicitly indicated; data structure designed to enable traceability from population to individual outcomes.