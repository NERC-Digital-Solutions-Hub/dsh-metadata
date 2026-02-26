# Dataset Documentation Bat activity and environmental data used to explore the merits of long-term passive acoustic monitoring of bats and associated drivers of bat activity in the Allt a'Mharcaidh

## Overview
- Provides nightly activity data for two Pipistrelle bat species (Pipistrellus pipistrellus and Pipistrellus pygmaeus) with associated weather and weekly potential food-resource data.
- Collected 30 April 2014 to 1 November 2014 (185 days) at three locations in an upland pine forest in the Cairngorms National Park, Scotland.
- Data collected with SM2BAT loggers, including automated identification of bat passes and subsequent human verification for several taxa.

## Data components
- Bat Activity Data: 
  - Two Wildlife Acoustic SM2BAT recorders with SMX-US microphones, running from sunset to sunrise at ~350 m asl, at three locations (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach).
  - Triggered recordings based on >12 dB above background noise at >16 kHz for >1 s; a single bat pass per recording.
  - Species identified automatically (Kaleidoscope Pro) and validated by human assessment for Plecotus auritus, Myotis, and unresolved Pipistrelles; P. pygmaeus vs P. pipistrellus inferred by peak frequency >50 kHz or <50 kHz; cross-checked against 1000 identifications with no mis-identifications found.
  - Output metric: PIPI Activity (passes per hour) and PIPY Activity (passes per hour), plus log-transformed versions.
- Environmental Data:
  - Hourly weather from UK Environmental Change Network (ECN AWS) and a Dundee University AWS (altitude-matched for site), plus forest-canopy wind data.
  - Cloud base height derived from a Met Office AWS to classify days into Fog, Low cloud, and High cloud categories.
- Food Resource Data:
  - Weekly total biomass of potential bat prey from a Mosquito Magnet Independence trap with octenol lure (22 weeks, 28 May 2014–29 Oct 2014), located 100 m from the nearest bat logger.

## Data file and metadata
- Acoustic_bat_data_(Cairngorms 2014).csv
  - Fields include: Logger (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach), Night, Hours in Night, PIPI Activity (pass/hr), PIPY Activity (pass/hr), PIPI Activity (log+1), PIPY Activity (log+1), Food Biomass (g), Forest Wind Speed (m/s), Forest Wind Direction (°), Prevailing Wind Direction (°), Wind Direction (Cardinal), Cloud Base Height (m), Cloud Base Height (Category), Mean Air Temp (°C), Total Precipitation (mm), etc.
- File format: CSV (70 KB).
- Location coordinates: site near Allt a’ Mharcaidh, Cairngorms National Park, Scotland (approx. 57.116544 N, -3.8487983 W).
- Data rights: © NERC - Centre for Ecology & Hydrology. Recommended contacting the data authors prior to reuse.

## Data collection and processing methods
- Data collection:
  - Three SM2BAT loggers with omnidirectional microphones; recordings from 30 minutes after sunset to 30 minutes before sunrise.
  - Loggers powered by solar arrays and large batteries; triggers set to detect bat activity with defined thresholds.
- Species identification and QA:
  - Auto-ID with Kaleidoscope Pro to distinguish P. pipistrellus and P. pygmaeus; human validation for Plecotus, Myotis, and unresolved Pipistrelles.
  - Ambiguities resolved using peak call frequency: >50 kHz -> P. pygmaeus; <50 kHz -> P. pipistrellus; 1,000 auto-IDs cross-validated with no mis-id detections; six calls could not be assigned with certainty.
- Data transformation and metrics:
  - Bat activity expressed as passes per hour; also log-transformed for analysis.
  - Environmental data integrated and altitude-adjusted using nearby AWS data to reflect conditions at bat-monitoring altitude.
  - Cloud base categories derived from meteorological data to relate cloud conditions to bat activity.

## Reuse guidance and governance
- Provenance and metadata are documented to support discoverability and reuse within data governance practices.
- Data should be reused with caution, and authors should be contacted prior to reuse to confirm any rights, caveats, and to clarify uncertainties.
- The documentation provides explicit methodological detail to support replication, auditing, and integration with other datasets.

## Limitations and considerations for data stewards
- Some bat identifications for certain genera (e.g., Myotis) are limited to genus level or unresolved Pipistrellus calls, which may affect species-specific analyses.
- Small number of uncertain recordings (six) where species could not be assigned with certainty.
- Temporal and spatial coverage is focused on three locations within a specific upland forest, which may limit generalizability to other habitats or years.
- Data format and field definitions are well-documented, but users should refer to the accompanying description for precise interpretation of fields and units.

## Version and citation
- Document Version: 1.0
- Primary study reference: Andrews, C., Dick, J., Black, A.R., Wadsworth, E., 2015. Differing responses of two sympatric bat species to environmental drivers may make them useful bioindicators of environmental change: Outcomes from 6 months of continuous recording at an upland pine wood, Scotland. Ecological Indicators. In Press.