# Dataset Documentation Bat activity and environmental data used to explore the merits of long-term passive acoustic monitoring of bats and associated drivers of bat activity in the Allt a'Mharcaidh.

- Purpose
  - Describes data used in Andrews et al. (2016) to evaluate long-term passive acoustic monitoring for bats and the environmental drivers of bat activity.
  - Supports consistent environmental monitoring and data reuse under defined QA processes.

- Scope and location
  - Location: upland pine forest in Cairngorms National Park, Scotland (Allt a' Mharcaidh catchment).
  - Period: 2014, 185 days (30/04/2014 to 01/11/2014; night-only sampling).

- Data components
  - Bat activity data
    - Species: Pipistrellus pipistrellus and Pipistrellus pygmaeus (with Plecotus/Myotis and unresolved Pipistrelles identified to genus or not assigned).
    - Method: three Wildlife Acoustic SM2BAT loggers with SMX-US microphones, recording from 30 min after sunset to 30 min before sunrise, at ~350 m a.s.l.
    - Trigger: sounds >12 dB above background at >16 kHz for >1 s; recording stops after 1 s of non-compliance or 30 s max.
    - Output: passes per hour for each species (PIPI, PIPY), plus log-transformed variants; spatially separated logs (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach).
    - Identification: automated Kaleidoscope Pro, with human validation for ambiguous calls; cross-validated 1,000 Pipistrellus identifications with no misclassifications found; six calls remained uncertain.
  - Environmental data
    - Weather: hourly mean air temperature, prevailing wind direction, total precipitation from UK ECN AWS; enhanced accuracy with Dundee University AWS data at similar altitude (~2.5 km east) to adjust temperature to logger altitude.
    - Local conditions: wind speed and direction inside forest canopy; cloud base height from Met Office AWS to categorize fog/low/high cloud relative to recording locations.
  - Food resource data
    - Weekly biomass of potential prey for Pipistrelles using a Mosquito Magnet trap with octenol lure (covering 22 weeks: 28/05/2014–29/10/2014).
    - Trap located 100 m from nearest bat logger to reduce local prey depletion effects.

- Data format and documentation
  - Data file: Acoustic_bat_data_(Cairngorms 2014).csv
  - Key fields (examples):
    - Logger location (Mharcaidh Downstream, Mharcaidh Upstream, Allt nan Cuilleach)
    - Night (Julien)
    - Hours in Night (decimal time)
    - PIPI Activity (passes per hour)
    - PIPY Activity (passes per hour)
    - PIPI Activity (log+1)
    - PIPY Activity (log+1)
    - Food Biomass (g)
    - Forest Wind Speed (m/s)
    - Forest Wind Direction (degrees and cardinal)
    - Prevailing Wind Direction (degrees and cardinal)
    - Mean Air Temp (°C)
    - Total Precipitation (mm)
    - Cloud Base Height (m and category: Fog/Low/High)
  - File size: 70 KB
  - Data quality: automated ID cross-checked against manual assessment; explicit QA steps documented for species assignment and parameter calculations.

- Data quality, processing, and QA
  - Verified auto-identification accuracy with independent human checks; 1000 records cross-checked with no misidentifications of target species.
  - Continuity rules: unresolved Pipistrelles assigned using 50 kHz delimiter when necessary.
  - Derived variables: translations of wind and cloud base into categorical factors; bat activity expressed as passes per hour (and back-calculated logs for analysis).
  - Documentation notes include explicit formulas used for wind direction and cloud-base categorization to support reproducibility.

- Temporal and analytical context
  - Data created to examine relationships between bat activity and environmental drivers (temperature, wind, cloud cover) and prey availability.
  - Aims to enable standardised analyses across time and sites for environmental monitoring and policy performance evaluation.

- Access and reuse
  - The dataset documentation recommends contacting the original data authors prior to reuse.
  - Data are suitable for integration into broader environmental monitoring datasets to enhance value beyond single studies and to support wider data sharing.

- Reference
  - Andrews, C., Dick, J., Black, A.R., Wadsworth, E., 2015. Differing responses of two sympatric bat species to environmental drivers may make them useful bioindicators of environmental change: Outcomes from 6 months of continuous recording at an upland pine wood, Scotland. Ecological Indicators. In Press.