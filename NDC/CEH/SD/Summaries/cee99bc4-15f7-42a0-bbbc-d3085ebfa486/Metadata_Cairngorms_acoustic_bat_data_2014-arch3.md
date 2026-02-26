# Dataset Documentation

## Overview
- Describes data used in Andrews et al. (2016) on long-term passive acoustic monitoring of bats and related drivers of bat activity.
- Strong recommendation to contact the data authors directly before re-use.
- Context: dataset captures nightly bat activity, weather, and potential prey resource in upland pine forest in the Cairngorms National Park, Scotland, over 185 days in 2014.

## Data Content
- Nightly activity values for two bat species: Pipistrellus pipistrellus and Pipistrellus pygmaeus.
- Includes associated weather data and weekly potential food resource data.
- Location: three ultrasonic loggers (SM2BAT) at ~350 m above sea level, Allt a’ Mharcaidh catchment, Cairngorms NP.
- Period: 30/04/2014 to 01/11/2014 (185 days).
- File: Acoustic_bat_data_(Cairngorms 2014).csv with fields such as:
  - Logger location (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach)
  - Night (Julien)
  - Hours in Night
  - PIPI Activity (passes per hour)
  - PIPY Activity (passes per hour)
  - PIPI/PIPY Activity (log+1)
  - Food Biomass (g)
  - Forest Wind Speed/Direction
  - Prevailing Wind Direction
  - Mean Air Temp
  - Total Precipitation
  - Cloud Base Height (m) and Cloud Base Height (Category)
- Notes: Myotis can be identified only to genus; exact species identifications rely on automated software plus human verification.

## Data Collection Methods
- Bat activity data collected with two Wildlife Acoustic SM2BAT recorders and SMX-US microphones at three locations.
- Recording schedule: from ~30 minutes after sunset to ~30 minutes before sunrise.
- Trigger criteria: sounds 12 dB above background at >16 kHz for >1 s; recording stops if criteria not met for >1 s or after 30 s.
- Species identification:
  - Automated: Kaleidoscope Pro software differentiates P. pipistrellus and P. pygmaeus.
  - Manual: human assessment for Plecotus auritus, Myotis, and unsettled Pipistrellle calls; cross-check of 1,000 Pipistrellus vocalizations showed no mis-identifications; unresolved Pipistrellus calls assigned using 50 kHz delimiter.
- Data quality checks ensured high consistency in species calls; six recordings could not be confidently assigned.

## Environmental Data and Context
- Weather data: hourly temperature, wind direction, and precipitation from UK Environmental Change Network (ECN) AWS; supplementary hourly temperature from a Dundee University AWS at similar altitude (2.5 km away) to refine altitude-relevant conditions.
- Local wind and conditions: additional wind data from within the forest canopy; cloud base height derived from Met Office AWS to categorize fog or cloud regimes (base height thresholds).
  - Fog: cloud base < 350 m
  - Low cloud: base < 650 m (approximate treeline maxima)
  - High cloud: base > 650 m
- Food resource proxy: weekly total biomass from a Mosquito Magnet Independence trap with octenol lure (22 weeks), located 100 m from the nearest bat logger.

## Data Format and Metadata
- Data file: Acoustic_bat_data_(Cairngorms 2014).csv (70 KB).
- Columns include: Passes per hour for each species, log-transformed activity, weekly food biomass, forest wind metrics, prevailing wind metrics, mean temperature, precipitation, cloud base height, and cloud base category.
- Metadata details provided to facilitate interpretation and reuse, including camera-friendly identifiers for loggers and night timing.

## Data Access, Re-use, and Governance
- Original rights: Dataset Documentation © NERC - Centre for Ecology & Hydrology.
- Re-use guidance: Researchers should contact the data authors prior to data re-use; data sharing may require metadata additions and adherence to data governance and openness standards.
- Reproducibility: Clear description of data processing steps and quality control measures supports methodological replication.

## References
- Andrews, C., Dick, J., Black, A.R., Wadsworth, E., 2015. Differing responses of two sympatric bat species to environmental drivers may make them useful bioindicators of environmental change: Outcomes from 6 months of continuous recording at an upland pine wood, Scotland. Ecological Indicators. In Press.