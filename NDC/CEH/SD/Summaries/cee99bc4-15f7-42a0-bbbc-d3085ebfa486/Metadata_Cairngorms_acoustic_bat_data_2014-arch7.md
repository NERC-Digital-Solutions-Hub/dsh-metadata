# Dataset Documentation Bat activity and environmental data used to explore the merits of long-term passive acoustic monitoring of bats and associated drivers of bat activity in the Allt a'Mharcaidh.

- Purpose: Describes the data used in Andrews et al. (2016) to investigate long-term passive acoustic monitoring of bats and drivers of bat activity in an upland pine forest, Cairngorms National Park, Scotland; authors recommended contacting data authors prior to reuse.
- Scope: Nightly bat activity data for two Pipistrelle species plus associated weather and weekly potential food resource data, collected over 185 days (31/04 to 01/11/2014).

## Data components

- Bat Activity Data
  - Recording setup: Two Wildlife Acoustic SM2BAT loggers with SMX-US omnidirectional microphones, at three locations in Allt a' Mharcaidh catchment, ~350 m a.s.l.
  - Locations: downstream logger along pine plantation edge, upstream logger in mixed woodland, and a channel-specific setup separated by ~50 m cable extensions.
  - Recording window: ~30 minutes after sunset to ~30 minutes before sunrise.
  - Timing: Nightly data from 30/04/2014 to 01/11/2014.
  - Metrics: Pipi Activity (passes per hour for P. pipistrellus) and Pipy Activity (passes per hour for P. pygmaeus); additional transformed metrics (log of passes per hour).
  - Identification: Species identified with automated Kaleidoscope Pro; human review for Plecotus auritus, Myotis, and uncertain Pipistrelle calls; cross-checks performed (1000 calls) with no mis-identifications; unresolved Pipistrellus calls assigned by 50 kHz threshold when needed.

- Environmental Data
  - Temperature: Hourly mean temperature data from UK Environmental Change Network; supplemented by Dundee University AWS data near the site and altitude-adjustment.
  - Wind: Hourly wind direction and speed from within forest canopy; additional wind data near the monitoring location.
  - Precipitation: Total hourly/ nightly precipitation data.
  - Cloud: Cloud base height from Met Office AWS, used to infer fog and cloud conditions (categories: Fog < 350 m, Low cloud 350–650 m, High cloud > 650 m).
  - Location-based context: Data tied to the bat monitoring site with spatial relevance to forest canopy and river channels.

- Food Resource Data
  - Biomass proxy: Weekly total biomass of potential prey captured by a Mosquito Magnet Independence trap with octenol lure (22 weeks: 28/05/2014–29/10/2014).
  - Location: Trap placed ~100 m from the nearest bat logger in similar woodland edge habitat to avoid local prey depletion.

## Data format and fields

- Acoustic_bat_data_(Cairngorms 2014).csv
  - Columns include: Logger location (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach), Night, Hours in Night, PIPI Activity (pass/hr), PIPY Activity (pass/hr), PIPI Activity (log+1), PIPY Activity (log+1), Food Biomass (g), Forest Wind Speed (m/s), Forest Wind Direction (°), Prevailing Wind Direction (°), Forest Wind Direction (Cardinal), Prevailing Wind Direction (Cardinal), Mean Air Temp (°C), Total Precipitation (mm), Cloud Base Height (m), Cloud Base Height (Category).

- Quality control notes
  - Automated identifications validated by human review; 1000 records cross-check showed no mis-identifications.
  - Continuity rules: unresolved Pipistrellus calls assigned using a 50 kHz delimiter; wind and cloud base categories derived via predefined Excel formulas.
  - Bat activity expressed as passes per hour (normalized by night length).

## Spatial and temporal context

- Location: Cairngorms National Park, Scotland; Allt a' Mharcaidh catchment.
- Specific coordinates: 57.116544 N, -3.8487983 W for the monitoring site.
- Elevation: Approximately 350 m above sea level.
- Timeframe: Data collection during 2014 (April to November); 185 days of bat activity with concurrent environmental and prey data.

## How GIS Specialists can use this dataset

- Create map-based visualisations of bat activity by logger location, night, and species.
- Overlay bat activity with environmental drivers (temperature, wind, precipitation) and cloud base to explore spatial-temporal relationships.
- Integrate prey biomass data to assess ecological drivers of bat activity across space and time.
- Combine with other GIS layers (habitat type, forest structure, proximity to water) to identify spatial patterns and potential indicators of environmental change.
- Use the CSV to derive derived metrics (e.g., activity density, nocturnal activity proxy) for GIS analyses.

## Access, rights, and provenance

- Rights: Dataset Right/Copyright © NERC - Centre for Ecology & Hydrology.
- Usage note: Strongly recommended to contact data authors prior to reuse.

## References

- Andrews, C., Dick, J., Black, A.R., Wadsworth, E., 2015. Differing responses of two sympatric bat species to environmental drivers may make them useful bioindicators of environmental change: Outcomes from 6 months of continuous recording at an upland pine wood, Scotland. Ecological Indicators. In Press.