# Dataset Documentation Bat activity and environmental data used to explore the merits of long-term passive acoustic monitoring of bats and associated drivers of bat activity in the Allt a'Mharcaidh.

## Overview
- Provides nightly activity values for two Pipistrelle bat species (Pipistrellus pipistrellus and Pipistrellus pygmaeus) plus weather and weekly potential food resource data.
- Collected from three ultrasonic loggers over 185 days (31/04 to 01/11/2014) in an upland pine forest, Cairngorms National Park, Scotland.
- Data intended to support analysis of long-term passive acoustic monitoring and drivers of bat activity.

## Data Collection and Coverage
- Instrumentation: two Wildlife Acoustic SM2BAT recorders with SMX-US microphones.
- Recording window: 30 minutes after sunset to 30 minutes before sunrise, at ~350 m above sea level.
- Locations: downstream and upstream logger sites along two channels, plus a third site in a confluence area within pine/woodland.
- Recording trigger: sounds 12 dB above background, >1 s, within frequencies above 16 kHz; recordings stop after conditions lapse for 1 s or after 30 s.
- Pass definition: each triggered recording constitutes a single bat pass.
- Species identification:
  - Automatic: Kaleidoscope Pro software for P. pipistrellus vs P. pygmaeus.
  - Manual: Plecotus auritus, Myotis, and unresolved Pipistrelles; doubt cases resolved by manual review.
  - Validation: 1000 Pipistrelle vocalizations cross-checked; no incorrect identifications found; six recordings could not be assigned with certainty.
  - Note: Myotis identified only to genus; some unresolved Pipistrelles used as delimiter (50 kHz).
- Environmental data sources:
  - Hourly weather: UK Environmental Change Network (ECN) AWS; augmented with Dundee University AWS temp data for altitude adjustment; forest canopy wind data; cloud base height from Met Office AWS.
  - Derived environmental context: cloud base height categorized into Fog, Low cloud, and High cloud based on altitude thresholds.
  - Food resource proxy: weekly biomass from a Mosquito Magnet trap with octenol lure, located 100 m from the nearest bat logger (weeks 22, 2014).
- Data file: Acoustic_bat_data_(Cairngorms 2014).csv (70 KB, CSV format).
  - Key fields include: Logger (site), Night, Hours in Night, PIPI Activity, PIPY Activity, PIPI/PIPY (log+1) transforms, Food Biomass, Forest Wind Speed/Direction, Prevailing Wind Direction, Cloud Base Height (and Category), Mean Air Temp, Total Precipitation.

## Data Quality, Provenance, and Quality Control
- Quality control: cross-checking of auto-identifications against a sample of 1000 records; no mis-identifications found.
- Continuity rules: unresolved Pipistrelles handled using 50 kHz delimiter; wind direction and cloud base category codes provided through explicit formulas.
- Data provenance: dataset documented to describe data used in Andrews et al. (2016); authors are recommended as a contact for reuse.

## Metadata, Access, and Reuse
- Copyright: Dataset documented under Dataset Right/Copyright © NERC - Centre for Ecology & Hydrology.
- Reuse guidance: Authors strongly recommended to be contacted prior to data reuse.
- Version: Document Version 1.0.

## Considerations for Data Leaders
- Scope: Longitudinal, site-specific acoustic bat activity with associated meteorological and prey-resource data; high value for understanding data system design, metadata standards, and cross-domain data integration.
- Data gaps and limitations:
  - Species identifications primarily cover Pipistrellus spp; Myotis identified only to genus; potential uncertainty in unresolved Pipistrelles.
  - Spatial and temporal specificity limited to a single upland pine forest site over part of 2014; may affect generalizability.
  - Data governance: clear attribution and reuse restrictions; direct author contact required for reuse.
- Potential uses:
  - Evaluating the effectiveness of long-term passive acoustic monitoring for bat activity and environmental drivers.
  - Integrating acoustic, weather, and prey-resource data to explore co-ownership of data products and end-user needs (policy colleagues, researchers).
  - Assessing data quality practices, metadata detail (cloud base, wind, temperature altitude adjustments), and cross-validation of automated identification in a real-world dataset.

## References
- Andrews, C., Dick, J., Black, A.R., Wadsworth, E., 2015. Differing responses of two sympatric bat species to environmental drivers may make them useful bioindicators of environmental change: Outcomes from 6 months of continuous recording at an upland pine wood, Scotland. Ecological Indicators. In Press.