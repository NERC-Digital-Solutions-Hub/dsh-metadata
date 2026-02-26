# Dataset Documentation Bat activity and environmental data used to explore the merits of long-term passive acoustic monitoring of bats and associated drivers of bat activity in the Allt a'Mharcaidh.

## Overview
- Describes nightly bat activity data for two Pipistrellus species, with associated weather and weekly potential food resource data.
- Collected via continuous passive acoustic monitoring over 185 days in an upland pine forest in Cairngorms National Park, Scotland (late Apr to early Nov 2014).

## Data Collection and Bat Activity Data
- Equipment: two Wildlife Acoustic SM2BAT ultrasonic recorders with SMX-US microphones.
-Locations: three sites (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach) at ~350 m a.s.l.
-Recording window: 30 minutes after sunset to 30 minutes before sunrise.
-Triggering: sounds 12 dB above background at >16 kHz for >1 s; recordings stop after 1 s of non-qualifying sound or after 30 s.
-Each trigger is treated as a single bat pass.
-Identification: automated Kaleidoscope Pro assigns most passes to P. pipistrellus or P. pygmaeus; human assessment for Plecotus auritus, Myotis, and any unresolved Pipistrelles.
-Quality checks: 1000 Pipistrelle vocalizations cross-validated by humans; six recordings could not be assigned with certainty.
- Species distinction: P. pygmaeus vs. P. pipistrellus based on peak call frequencies (≥50 kHz for P. pygmaeus; <50 kHz for P. pipistrellus) when ambiguous.

## Environmental and Resource Data
- Temperature, wind direction, and precipitation: hourly data from UK Environmental Change Network (ECN) AWS; additional hourly temperature from Dundee University AWS to adjust for altitude; forest canopy wind data captured nearby.
- Cloud base height: derived from UK Met Office AWS to categorize days by fog/low/high cloud relative to site altitude.
- Potential food resources: weekly total biomass from a Mosquito Magnet Independence trap with octenol lure, located 100 m from the nearest bat logger; data cover 22 weeks (28/05/2014–29/10/2014).

## Data File and Variables
- Data file: Acoustic_bat_data_(Cairngorms 2014).csv (70 KB, CSV).
- Key variables include:
  - Logger, Night, Hours in Night
  - PIPI Activity (passes/hr), PIPY Activity (passes/hr)
  - PIPI Activity (log+1), PIPY Activity (log+1)
  - Food Biomass (g)
  - Forest Wind Speed (m/s), Forest Wind Direction (°), Prevailing Wind Direction (°), Forest Wind Direction (Cardinal), Prevailing Wind Direction (Cardinal)
  - Mean Air Temp (°C), Total Precipitation (mm)
  - Cloud Base Height (m), Cloud Base Height (Category: Fog, Low, High)

## Quality Control
- Strong emphasis on validation of automated identifications; 1000 records cross-checked with human assessment.
- Unresolved Pipistrelles assigned to species using a 50 kHz delimiter.
- Wind direction and cloud base categories generated via standard formulas (document provides explicit Excel-based methods).

## Usage Notes and Rights
- The document provides sufficient information to describe the data used in Andrews et al. (2016).
- Prior to data reuse, it is strongly recommended to contact the original data authors.

## References
- Andrews, C., Dick, J., Black, A.R., Wadsworth, E., 2015. Differing responses of two sympatric bat species to environmental drivers may make them useful bioindicators of environmental change: Outcomes from 6 months of continuous recording at an upland pine wood, Scotland. Ecological Indicators. In Press.