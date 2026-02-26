# SUPPORTING DOCUMENTATION: Actuarial and phenotypic senescence in a wild field cricket ( Gryllus campestris ) population over ten years

## Overview
- Long-term, multi-modal data collection on Gryllus campestris at the WildCrickets field site in Asturias, North Spain, aiming to study actuarial and phenotypic senescence.
- Data span individual identities, demography, behavior, and environmental context, gathered via physical sampling, video surveillance, and environmental sensors.
- Dataset designed to support discovery and reuse, with explicit records of methods, instruments, and data processing steps.

## Study site and sampling regime
- Location: meadow on the northwest slope of a meadow bordered by railway and roads; surrounds include meadows, orchards, eucalyptus, chestnut, and oak patches.
- Population details: cricket population concentrated in a ~800 m2 area within a ~20,000 m2 meadow; crickets avoid shaded areas.
- Temporal scope: monitored for twelve consecutive years with consistent management (mowing in mid-March and July–August; seasonal mowing elsewhere as needed; weekly burrow searches Feb–July).
- Sampling focus: identification and tracking of individuals and burrows to capture emergence, movement, reproduction, and mortality signals.

## Data collection methods (Collection methods)
- Individual data: weigh each cricket (±0.01 g), photograph, and mark with a unique PVC tag glued to the pronotum; tag encodes a 1–2 character code for identification on video.
- Biological samples per individual: cuticular hydrocarbons, a small haemolymph sample, and a hind leg tissue fragment for pheromone and DNA analyses.
- Behavioral and ecological data: installation of infrared day/night cameras (initially 64, later up to 140) around burrows to record activity 24/7; behaviors documented include basking, moulting, singing, courtship, mating success (spermatophore presence), fights, oviposition, and predator encounters; additional observations of other wildlife using burrows.
- Data alignment with burrows: each burrow has a unique number; occupancy monitored through cameras and direct observation to cover burrows without video.
- Seasonal workflow: camera network deployed before adult emergence; continuous recording during the breeding season; cameras moved between burrows to maximize information; recording ceases when activity remains absent for two consecutive days.
- Population and environment context: predator and non-cricket activity recorded; singing activity quantified as a presence/absence indicator per 5-minute sample within hourly intervals.

## Field instrumentation
- Video, storage, and surveillance: network of motion-activated DVR systems; cameras connected to multiple computers; video stored on site (house adjacent to meadow) and managed with video software (historically Diginet, then i-Catcher).
- Weather and microclimate: weather station (Davis Vantage Pro2) logging data at 10-minute intervals plus seven additional sensors in simulated burrows around the meadow.
- Calibration: all instrumentation is factory calibrated.

## Calibration steps and values
- Instruments are factory calibrated to ensure measurement consistency; no site-specific calibration updates detailed beyond standard factory calibration.

## Analytical methods
- Data extraction process:
  - Step 1: per-day pass to separate burrows in use from empty burrows using multiple cameras simultaneously.
  - Step 2: detailed review of selected cameras (typically four, sometimes up to nine or sixteen) with events timestamped into a spreadsheet.
  - Data consolidation: event data imported into a MS Access database for subsequent processing and analysis.
- Data integration: video-derived behavioral data linked to individual IDs, burrow IDs, and sampling events (biological samples, morphometrics, and DNA/pheromone profiling).

## Quality control
- Data consistency checks via Access queries to detect anomalies (e.g., a cricket recorded as using two burrows at the same time).
- Data are not used until internal consistency checks pass, ensuring dataset integrity for downstream analyses.

## Data governance and sharing considerations for Data Stewards
- Data architecture relies on multiple systems (unique IDs for crickets and burrows; camera-based video; MS Access databases; MS Excel spreadsheets; DVR storage; weather sensor data).
- Documentation of methods, instruments, and data processing steps supports reproducibility and data discovery.
- Long-term storage requirements include centralizing unique identifiers, maintaining links between biological samples, video events, and environmental data, and managing large video data volumes.
- Interoperability considerations: heterogeneous data formats and software (video formats, Excel, Access) necessitate clear metadata and potential data standardization for sharing.
- Data provenance and lineage: explicit recording of collection methods, sampling times, and processing steps helps future users understand data origin and transformations.

## Key takeaways for data stewardship
- Maintain robust unique identifiers for individuals and burrows to enable longitudinal tracking across years and datasets.
- Document all data collection methods, instruments, calibrations, and processing workflows to support reproducibility and reuse.
- Ensure consistent data quality checks and clear error-detection rules to preserve dataset integrity.
- Plan for storage and interoperability of multi-format data (video, spreadsheets, databases, environmental sensors) with thorough metadata to facilitate data discovery and reuse.