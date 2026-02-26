# Actuarial and phenotypic senescence in a wild field cricket ( Gryllus campestris ) population over ten years

## Overview
- Longitudinal field study conducted at WildCrickets site in Asturias, North Spain, monitoring Gryllus campestris over more than a decade.
- Population tracked within a defined meadow (~800 m2) on a larger ~20,000 m2 meadow area, with movement constrained by landscape features (railway, roads, shade).
- Monitoring period spans twelve consecutive years, focusing on lifecycle stages from nymphs to adults and including diapause in winter.

## Data assets and collection
- Individual-level data:
  - Weighing (±0.01 g), photographs, and unique PVC pronotum tags (1–2 character codes) for identification and re-identification.
  - Biological samples for individual pheromone and DNA profiling: cuticular hydrocarbons, haemolymph, and leg tissue.
- Behavioral and ecological data:
  - Infrared cameras (64 initially; up to 140 by 2017) installed at burrow entrances to record 24/7 activity around burrows (basking, moulting, singing, courtship, mating, spermatophore attachment/removal, fighting, feeding, oviposition, movement; predator interactions recorded).
  - Observations of burrow occupancy and adult emergence dates, including non-videoed burrows due to camera distribution.
  - Presence/absence data for singing behavior every 5 minutes per hour; mating success via spermatophore attachment.
- Environmental data:
  - Weather data from a central Davis Vantage Pro2 weather station (10-minute intervals) plus seven temperature sensors distributed around the meadow (surface and simulated burrows).
- Field and lab instrumentation:
  - Unique burrow identifiers; camera network managed to maximize data for individuals of interest; DVR storage of video data; ongoing maintenance and reallocation of cameras each year.
- Documentation and provenance:
  - All instruments factory calibrated; calibration steps recorded and maintained.
  - Data extraction and processing documented (two-stage video viewing, day-level data separation, event-level annotation, and spreadsheet-to-database import).

## Data collection methods and instrumentation
- Fieldwork:
  - Regular trapping and marking of individuals shortly after adult emergence; subsequent release into the same burrow.
  - Regular calibration and validation of measurement procedures; nymph-to-adult transitions tracked through direct observation and video.
- Data capture workflow:
  - Video recording initiated before adult emergence and continued until activity ceases for two consecutive days; continuous camera operation across the breeding season.
  - Weather and environmental sensors deployed at multiple meadow locations to capture microclimate variation.
- Documentation of field locations:
  - Each burrow flagged with a unique identifier; direct observation conducted for non-videoed burrows to maintain presence data.

## Data processing and analytics
- Data extraction:
  - Two-step per-day video processing: initial pass to separate burrows in use from empty burrows; detailed second pass for selected cameras to capture events.
  - Event-level logging in spreadsheets, followed by import into a relational database (MS Access) for downstream analysis.
- Data integration:
  - Linking of video-derived behavioral data with individual tagging, sampling results, and environmental measurements.
- Quality control:
  - Consistency checks via Access queries to detect contradictory records (e.g., a cricket recorded as using two burrows simultaneously); data finalized only after validation.

## Data management and governance implications
- Longitudinal identifiers:
  - Unique cricket IDs and burrow IDs support traceability across years and events.
- Metadata and standards:
  - Explicit documentation of collection timing (seasonal window), camera deployment schedule, and sampling methods to support reproducibility.
  - Calibration and instrument metadata maintained; factory calibration noted for all devices.
- Data lifecycle:
  - Annual updates with new cameras and continued data collection; data stored on DVRs and in a central MS Access database; video data archived and processed for the season.
- Data quality and provenance:
  - Emphasis on data integrity through multi-step validation and cross-referencing video with field observations.

## Storage, accessibility, and updates
- Storage:
  - Video data hosted on DVR systems across linked computers; environmental data stored via weather station outputs and sensors.
  - Processed data consolidated into MS Access databases to support analyses.
- Updates:
  - Yearly reinstallation of camera networks and ongoing data collection each breeding season; methodology and instrumentation maintained for consistency across years.
- Accessibility considerations:
  - Site-specific details (e.g., precise locale) available on request; data collection methods are thoroughly documented to enable future reuse and replication.

## Considerations for Data Stewards
- Interoperability and formats:
  - Multiple systems and formats (DVR, camera logs, MS Access, Excel) require ongoing data harmonization and careful metadata management.
- Handling large video datasets:
  - Substantial storage and archival requirements; strategies needed for scalable storage, retrieval, and long-term preservation.
- Standardization and provenance:
  - Maintain consistent event definitions (e.g., singing, mating, oviposition) and clear documentation of what constitutes an observable event to ensure comparability across years.
- Data quality assurance:
  - Regular verification workflows and automated checks to detect inconsistencies; maintain a transparent audit trail for data corrections and updates.
- Data sharing and reuse:
  - Rich, well-documented metadata enables reuse for related ecological and senescence studies; consider formalizing a metadata schema and data catalog entry to facilitate discovery.