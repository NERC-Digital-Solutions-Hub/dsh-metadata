# SUPPORTING DOCUMENTATION: Trade-off between reproduction and body maintenance in a wild field cricket ( Gryllus campestris ) population

## Overview
- Long-term field study (12 years) at WildCrickets site in Asturias, Spain, examining the trade-off between reproduction and body maintenance in Gryllus campestris.
- Multi-modal data collection combining behavioral observations, physiological samples, and environmental measurements.
- Data are managed with unique identifiers, structured workflows, and quality control to support reuse and discovery.

## Study site and population
- Location: meadow in Asturias, North Spain, near a river valley, with surrounding agricultural and tree cover.
- Meadow size and layout: ~20,000 m2 associated with a smaller population area of ~800 m2 for crickets.
- Population dynamics: flightless, univoltine crickets with synchronized adult emergence; monitoring from February to July each year.
- Environmental context: surrounding roads and a railway line partly confine movement; meadow mowing regime and sun exposure influence habitat use.

## Data collected and primary variables
- Individual identifiers: unique PVC tag codes glued to pronotum; weight, photos, and biological samples collected.
- Biological samples per individual: cuticular hydrocarbons, haemolymph, and a small leg tip for DNA/pheromone analyses.
- Core behavioral and life-history measures (per individual across days):
  - Emergence date: annual synchronization of adult emergence (mostly within ~14 days).
  - Calling activity: binary indicator of singing within the first 10 minutes of every hour; observed at burrow level.
  - Searching activity: duration of burrow visits converted to a binary metric (short ≤ 77 min = 1; long > 77 min = 0) when focal male is alone.
  - Dominance in fights: win/lose outcomes scored for each participant (1/0) aligned to male age.
  - Mating promptness: latency from first encounter to mating converted to binary (≤50 min = 1; >50 min = 0).
- Video and sensor data: infrared cameras (64 initially, up to 140 by 2017) recording around burrows; weather data via Davis Vantage Pro2 and additional sensors placed in simulated burrows.
- Video and event data capture: day-by-day processing with event-level coding; direct observations supplement camera coverage for non-videoed burrows.

## Data collection methods and instrumentation
- Embedding protocol: capture, weigh (±0.01 g), photograph, and tag each cricket; samples taken before release back into the same burrow.
- Video infrastructure: stationary infrared cameras covering burrows; continuous 24/7 recording during the active season; DVR-based storage with centralized computing for video management.
- Field instrumentation: weather station and multiple surface/underground temperature sensors for microclimate context.
- Direct field observations: used to cover burrows lacking video coverage; unique burrow IDs maintained for the season.

## Data management, formats, and workflow
- Data capture workflow:
  - Videos interpreted in two stages: broad daily screening across cameras, followed by detailed playback of selected cameras; events logged into spreadsheets.
  - Data imported into MS Access databases for subsequent processing and analysis.
- Data provenance and identifiers:
  - Burrow IDs: unique numbers for each burrow throughout the season.
  - Individual IDs: 1–2 character codes on PVC tags.
- Instrument calibration: all instruments factory-calibrated prior to use.
- Documentation and linkage:
  - Annotations and descriptive documents accompany attached datasets.
  - Methodological documentation describes each data section (emergence, calling, Searching, dominance, mating).

## Quality control and data integrity
- Consistency checks: database-level queries identify inconsistencies (e.g., same cricket recorded at two burrows simultaneously).
- Data validity: data are not used until quality control confirms internal consistency across events and timing.
- Calibration and standardization: use of standardized thresholds (e.g., 50-minute mating latency, 77-minute search threshold) based on observed distributions.

## Data governance, sharing, and reproducibility
- Data stewardship considerations:
  - Rich metadata and clear variable definitions enable reuse by other researchers.
  - Unique and stable identifiers for individuals and burrows support longitudinal analyses.
  - Data processing steps (video extraction, coding rules, binary transformations) are documented for reproducibility.
- Accessibility:
  - Data are described in attached datasets and descriptive documents; actual files include videos stored on DVR systems and analyses in MS Excel/Access, with potential for further distribution through accompanying metadata.
- Limitations and caveats:
  - Potential data gaps due to camera coverage limitations; movement of crickets between burrows may affect observation consistency.
  - Thresholds and binary classifications are simplified representations of continuous behaviors and may affect fine-scale analyses.

## Practical considerations for data stewards
- Maintain a clear data dictionary detailing all variables, units, coding schemes, and thresholds.
- Preserve linkage between individuals, burrows, cameras, and environmental sensors to enable integrated analyses.
- Ensure long-term storage plans for video data and associated datasets, including versioning of processing scripts and documentation.
- Provide guidance on updating datasets across years to maintain continuity (emergence timing, behavior measures, and metadata).
- Highlight potential data use constraints (e.g., non-public video footage) and ensure appropriate metadata describe access restrictions if applicable.