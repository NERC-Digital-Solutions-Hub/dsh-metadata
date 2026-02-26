# WINTER AND SUMMER SPECKLED WOOD SURVIVAL AND PERFORMANCE

- A field and laboratory study of the F1 larval offspring of wild-caught adult Speckled Wood butterflies (P. aegeria) to examine survival, growth, and development in different habitats (woodland vs. grassland) across winter and summer, with supporting microclimate, host-plant quality, and cold-tolerance data.
- Objectives include identifying how habitat, microclimate, host-plant quality, and cold exposure affect larval survival, development time, pupal mass, and growth rates; and enabling subsequent analyses and modelling of landscape- or climate-driven impacts on survival and performance.

## Study design and data collection

- Winter experiment (2008–2009)
  - Sites: 1 woodland (Bishop Wood) and 1 grassland (Wistow) in England.
  - Setup: Pots containing larvae placed in field in Sep; 40 pots per site; 5–15 larvae per pot; split brood design (larvae from one female contributed to one pot at each site).
  - Duration: Overwintered until June; plants replaced as eaten; pots buried to be flush with soil surface and netted to prevent grazing, predation, and larval movement.
- Summer experiment (2009)
  - Sites: 3 woodlands (The Grange, Bishop Wood, Skipwith Common) and 3 grasslands (University of York Campus, Wistow, Skipwith Common).
  - Setup: Pots (7 per site) with 5 larvae per pot; larvae from each female split evenly among treatments; randomly assigned to pots within treatments.
  - Duration: Aug to end of Sep; desiccation in the field.
- Adult origin and rearing
  - Adult P. aegeria captured at Bishop Wood (northern England) in Aug 2008 and July 2009.
  - Females laid eggs on potted Poa pratensis in greenhouses; fresh host plants used for larval rearing and field planting.
  - Acknowledges potential variability due to uneven pot counts from site disturbances.

## Datasets and key variables

- Winter_survival_and_performance.csv
  - Habitat (W = woodland, G = grassland)
  - Female (codes for contributing maternal lineage)
  - Alive (number pupated)
  - Dead (number died)
  - Development time (weeks for winter; from field placement to pupation)
  - Pupal mass (mg) at pupation
  - Growth rate (mg/week)
  - Notes: NA values where no individuals pupated; uneven pot counts noted.

- Summer_survival_and_performance.csv
  - Habitat (W/G)
  - Site (woodland: 1 The Grange, 2 Bishop Wood, 3 Skipwith Common; grassland: 1 University of York Campus, 2 Wistow, 3 Skipwith Common)
  - Pot (pot code; uneven counts due to loss)
  - Alive as larvae
  - Alive as pupae
  - Dead
  - Development time (days; from field placement to pupation)
  - Pupal mass (mg)
  - Growth rate (mg/day)
  - Notes: NA values where no pupation occurred.

- Winter_microclimate.csv
  - Date and time (hourly)
  - Temperature readings (°C) from four loggers placed at 30 cm above ground, within netting around each pot
  - Habitat and logger identifiers encoded in column headers
  - Notes: Foil-wrapped loggers to reduce direct solar insolation; some loggers failed, leading to uneven counts.

- Summer_microclimate.csv
  - Date and time (hourly)
  - Temperature readings (°C) from loggers, with site and logger codes
  - Habitat and site-specific coding included; logger failures noted

- SUMMER HOST PLANT QUALITY
  - Potted grass samples (3 cm diameter) taken from each pot at experiment end
  - Nearby wild grass samples collected at 2 m and 4 m perpendicular to transects
  - Water content measured after drying (60 °C, 24 h)
- Potted grass water content
  - Habitat (W/G)
  - Site
  - Pot
  - Percentage water content
  - NA where pot lost
- Wild grass water content
  - Habitat (W/G)
  - Site
  - Sample (within site)
  - Percentage water content
  - NA where no grass found near pot

- SPECKLED WOOD COLD TOLERANCE
  - Controlled laboratory experiment on larval cold exposure
  - Treatments: -5 °C or -10 °C for varying durations; rate of cooling 1 °C per minute
  - Post-exposure: 5 °C for 2 days; larvae moved to host plants; max n = 10 per plant
  - Measurements: immediate survival, survival to pupation, survival to eclosion, development time post-treatment, pupal mass, growth rate
  - Control: 5 °C for 8 days (longest cold exposure) without sub-zero treatment
- Cold_tolerance.csv
  - Exposure temperature (°C) (-5 or -10)
  - Duration of exposure (days)
  - Sample (group of 10 larvae)
  - Immediate survival (%)
  - Successful pupation (%)
  - Successful eclosion (%)
  - Development time (days)
  - Pupal mass (mg)
  - Growth rate (mg/day)

## Measurements and unit details

- Development time
  - Winter: weeks
  - Summer: days
  - Cold tolerance: days (from removal to pupation)
- Mass
  - Pupal mass measured in mg; instrument accuracy: 0.1 mg
- Growth rate
  - Winter: mg/week
  - Summer: mg/day
  - Cold tolerance: mg/day (from removal to pupation)

## Data quality, limitations, and considerations

- Uneven sampling
  - Uneven number of pots per site due to disturbances; some pots lost or failed
  - Uneven numbers of loggers or logger failures leading to incomplete microclimate data
- Missing data
  - NA values in development time or mass where no pupation occurred
  - NA for water content when pots or grass samples were lost
- Experimental scope
  - Uses F1 offspring from wild-caught adults; host plant limited to Poa pratensis
  - Netting and field conditions may influence predation, grazing, and larval movement
- Metadata granularity
  - Site codes and habitat designations provided; OS grid references given for some sites
  - Clear documentation of treatment structure (winter vs. summer; brood design)

## How analysts can use the data

- Compare survival, development time, mass, and growth across habitats (woodland vs. grassland) and seasons (winter vs. summer).
- Link larval performance to microclimate data to assess climate or microhabitat effects.
- Assess the influence of host-plant quality (water content) on larval growth and survival.
- Evaluate cold-tolerance thresholds and the sublethal effects of cold exposure on development and growth.
- Develop predictive models of survival and growth under varying habitat, microclimate, and temperature-stress scenarios.
- Explore potential interactions between habitat type, site-specific microclimate, and plant quality on overall performance.

## Summary of potential analyses and comparisons

- Habitat effect: woodland vs. grassland on survival, development time, pupal mass, and growth rate (winter and summer separately).
- Seasonal effect: compare winter vs. summer performance metrics within the same habitat types.
- Microclimate associations: relate hourly temperature profiles to survival and development outcomes.
- Plant quality associations: correlate water content of pot and wild grass with larval performance.
- Cold tolerance outcomes: quantify how duration and severity of cold exposure influence immediate survival, pupation, and eclosion, plus post-treatment growth.