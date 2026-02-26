# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Pollinator abundance data

## Overview
- Provides pollinator abundance data collected as part of the Dorset Valuing Nature Project field component.
- Builds a baseline from Ronald Good’s 1931–1939 botanical survey to compare ecosystem services across habitat conditions.
- Archive is publicly available via the Dorset Environmental Records Centre (DERC).

## Experimental design
- Sites identified by Good (calcareous grassland, heathland, woodland) in the 1930s; used as a baseline for current site selection.
- Subsampling of Good-identified sites to form survey sites, using multiple data sources to determine current habitat types.
- Final survey included 13 calcareous grassland, 13 heathland, and 12 woodland sites.
- Sites selected to span a gradient of degradation from the original habitat.
- Habitat classifications integrate multiple sources: UK Land Cover Map 2007, Natural England Priority Habitat Inventory (2015), Sites of Special Scientific Interest (SSSIs), Horsfall (1981), Dorset Heathland survey (2000), and Higher Level Stewardship schemes.
- Gradient definitions map historical habitat (1940) to current habitat categories (2017), with specific mappings for each habitat type.

## Data collection methods
- Within each site, 50m x 50m plots (sample squares) were randomly assigned using ArcGIS prior to visits.
- Pollinator abundance assessed via two 50m transects per site; butterflies recorded to species level within a 5m box; bees, hoverflies, flies, and beetles recorded to species within a 2m box.
- Insects’ forage plant species also recorded.
- Surveys conducted on three dates per habitat type, with timing adjusted by habitat: calcareous grassland (June–August), heathland (May, August, September), woodland (May–July).
- Weather and timing data recorded: date, start/end times, weather conditions, cloud cover, temperature, and wind.
- Strict weather criteria for transects: dry, calm, min 13°C; cloud ≤ 40% (13–16°C window) or specified ranges; wind ≤ Beaufort 5; surveys between 10:00 and 16:00.

## Data quality control
- All surveys conducted by experienced field ecologists; same team conducted all surveys for consistency.
- Data checked for anomalies and recorded as fielded.
- Data stored with clearly defined column headings and units (pollinator data table structure detailed in document).

## Dataset structure and metadata highlights
- Core fields include: Site_no, Habitat (1940 and 2017 classifications via gradient mapping), Date_of_survey, Start_time, End_time, Transect_no, Grid_ref, %_Sunshine, %_Cloud_cover, Insect_seen_Y_N, Activity_when_seen, Flower_species_foraging_on, Insect_order, Insect_name, Caste_or_gender, Number_seen.
- A lookup table maps historical habitat (1940) to current habitat categories (2017), enabling gradient analyses across site histories (e.g., calcareous grassland → calcareous grassland (SSSI quality), improved grassland, restoring calcareous grassland, coniferous plantations on heathland, etc.).
- Data columns and units are standardized to support cross-site comparisons and reproducibility.
- Data are linked to multiple provenance sources, and the dataset is designed to enable assessment of pollinator abundance alongside habitat condition and change.

## Data provenance and sources
- Primary baseline: Good, R. 1937. An account of a botanical survey of Dorset.
- Supplemental historical/habitat context: Horsfall (1981); Rose et al. (2000) Dorset Heathland survey; Natural England datasets (SSSI, Priority Habitats Inventory 2014–2015); Higher Level Stewardship schemes.
- Archive and public access: Dorset Environmental Records Centre (DERC) project page and related Good project materials.

## Access and references
- Primary data source and project materials available via DERC: http://www.derc.org.uk/projects/good.htm
- References included for provenance and method justification:
  - Good, R. (1937) Proc Linn Soc
  - Horsfall, A. (1981) Dorset Proc
  - Natural England (2014) SSSI and historical monuments
  - Natural England (2015) Priority Habitats Inventory
  - Rose, R.J., et al. (2000) Biol Conserv