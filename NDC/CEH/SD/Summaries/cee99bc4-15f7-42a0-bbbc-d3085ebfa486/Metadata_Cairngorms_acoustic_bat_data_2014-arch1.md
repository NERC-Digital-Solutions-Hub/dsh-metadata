# Dataset Documentation Bat activity and environmental data used to explore the merits of long-term passive acoustic monitoring of bats and associated drivers of bat activity in the Allt a'Mharcaidh.

## Purpose and scope
- Provides nightly activity data for two Pipistrelle species (Pipistrellus pipistrellus and Pipistrellus pygmaeus) plus weather and weekly potential food resource data.
- Collected to explore long-term passive acoustic monitoring and drivers of bat activity.
- Study period: 185 days, 30/04/2014 to 01/11/2014, in an upland pine forest in the Cairngorms National Park, Scotland.
- Location details: Allt a' Mharcaidh catchment, Cairngorms NP, Scotland; ~350 m above sea level; three logger locations.

## Data collected and structure
- Bat activity data
  - Equipment: Two Wildlife Acoustic SM2BAT recorders (with SMX-US microphones) recording from 30 minutes after sunset to 30 minutes before sunrise.
  - Spacing: Three locations (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach) with channel-specific recordings.
  - Recording trigger: >12 dB above background noise at >16 kHz for >1 s; recording stops after 1 s of non-compliance or after 30 s.
  - Output: Each triggered recording treated as a single bat pass.
  - Species identification: Automated identification (Kaleidoscope Pro) to two Pipistrelle species; human validation for Plecotus auritus, Myotis, and unresolved Pipistrelles.
  - Validation: Cross-check of 1,000 Pipistrellus identifications by human reviewer; no incorrect identifications found; six recordings unresolved to species.
  - Derived metrics: Passes per hour for each species; log-transformed versions (log+1) for analysis.
  - File: Acoustic_bat_data_(Cairngorms 2014).csv
- Environmental data
  - Temperature: Hourly mean air temperature from UK Environmental Change Network (ECN) AWS; additional hourly temperature data from a Dundee University AWS at similar altitude (2.5 km east) to adjust for altitude.
  - Wind: Hourly wind direction and wind speed within the forest canopy; prevailing wind direction from outside canopy.
  - Cloud: Cloud base height derived from a Met Office AWS 10 km north; categorized into Fog (<350 m), Low cloud (350–650 m), High cloud (>650 m).
  - Precipitation: Total hourly precipitation from ECN AWS.
  - Prey resource proxy: Weekly total prey biomass (g) from a Mosquito Magnet Independence trap with octenol lure, located 100 m from the nearest bat logger (week 28/05/2014–29/10/2014; 22 weeks).
- File schema and variables (in Acoustic_bat_data_(Cairngorms 2014).csv)
  - Logger: Location (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach)
  - Night: Julian night
  - Hours in Night: Decimal time between sunset and sunrise
  - PIPI Activity (pass/hr): Pipistrellus pipistrellus passes per hour
  - PIPY Activity (pass/hr): Pipistrellus pygmaeus passes per hour
  - PIPI Activity (log+1): Log10(PIPI Activity)
  - PIPY Activity (log+1): Log10(PIPY Activity)
  - Food Biomass (g): Weekly prey biomass
  - Forest Wind Speed (m/s): Forest canopy wind speed during night
  - Forest Wind Direction (°): Forest canopy wind direction during night
  - Prevailing Wind Direction (°): Outside canopy wind direction during night
  - Forest Wind Direction (Cardinal): Cardinal wind direction (forest)
  - Prevailing Wind Direction (Cardinal): Cardinal outside canopy wind
  - Mean Air Temp (°C): Mean air temperature during night
  - Total Precipitation (mm): Total precipitation during night
  - Cloud Base Height (m): Cloud base height during night
  - Cloud Base Height (Category): Fog/Low/High categories

## Data quality and processing
- Identification validation
  - Auto-ID cross-checked with human assessment: 1,000 records; no incorrect identifications found.
  - Unresolved Pipistrelles assigned using 50 kHz delimiter to separate species.
- Transformations and calculations
  - Activity metrics expressed as passes per hour; log-transformed values included for analysis.
  - Cloud base height categories derived from measured heights via established thresholds.
- Metadata and provenance
  - Data rights: Dataset documented by NERC - Centre for Ecology & Hydrology.
  - Original study: Andrews et al. (2015) Ecological Indicators; 2016 work referencing the data.
  - Documentation recommends contacting the authors prior to data reuse.

## Location, timing, and context
- Site: Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (57.116544 N, -3.8487983 W).
- Altitude: Approximately 350 m above sea level.
- Monitoring window: 30 Apr 2014 – 01 Nov 2014 (185 nights).
- Habitat context: Upland pine woodland; forest canopy structure relevant to bat activity and prey availability.

## Reuse considerations and potential analyses
- Analytical opportunities
  - Examine species-specific responses of P. pipistrellus and P. pygmaeus to environmental drivers (temperature, wind, cloud base, precipitation) and prey biomass.
  - Develop predictive models of bat activity using the multi-sensor time series (hourly environmental variables, nightly bat activity, weekly prey biomass).
  - Assess utility of long-term passive acoustic monitoring as a bioindicator of environmental change.
- Scale and data integration considerations
  - Local (site-level) and nightly-to-weekly scales; integration of three logger locations and environmental covariates.
  - Contentions around data scale gaps (185 nights) and potential biases due to species identification limits (especially for Myotis and unresolved Pipistrelles).
  Data coverage limited to 2014 and this specific locale; careful generalization needed.
- Usage cautions
  - Species identifications rely partly on automated tools with human validation; six calls could not be confidently assigned.
  - Location-specific factors (forest edges, proximity of prey trap) may influence generalizability to other settings.
- Access and attribution
  - Data reuse requires contacting original data authors; acknowledge CEH/NERC rights and the source study (Andrews et al., 2015; Ecological Indicators).

## References
- Andrews, C., Dick, J., Black, A.R., Wadsworth, E., 2015. Differing responses of two sympatric bat species to environmental drivers may make them useful bioindicators of environmental change: Outcomes from 6 months of continuous recording at an upland pine wood, Scotland. Ecological Indicators. In Press.