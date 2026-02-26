# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Pollinator abundance data.

## Overview
- Field component of the Dorset Valuing Nature Project focusing on pollinator abundance.
- Builds on a baseline from Prof. Ronald Good’s 1931–1939 Dorset botanical survey; archive public via Dorset Environmental Records Centre.
- Site selection and habitat gradient devised to compare ecosystem services across condition changes.
- Survey area includes calcareous grassland, heathland, and woodland sites with gradient categories reflecting degradation or restoration.

## Experimental design
- Baseline: Good’s 1930s survey used to identify target habitat types; public archive used for site selection and comparison.
- Site selection: Subsampled sites identified as calcareous grassland, heathland, or woodland in the 1930s; final survey set includes 13 calcareous grassland, 13 heathland, and 12 woodland sites.
- Gradient framework: Sites categorized along condition gradients (e.g., improving, restoring, maintaining) with specific mappings to current habitat classes.
  - Calcareous gradient examples include: improved grassland, restoring calcareous grassland, calcareous grassland (SSSI quality).
  - Heathland gradient examples include: coniferous plantation on heathland, gorse high heathland, heathland (SSSI quality).
  - Woodland gradient examples include: coniferous plantation, broadleaf woodland, ancient woodland (SSSI quality).
- Habitat and gradient data compiled to enable analyses of habitat condition vs. pollinator communities and ecosystem services.

## Collection methods
- Sampling design: 50m x 50m plots (sample squares) randomly allocated within Good survey area using ArcGIS.
- Field protocol: Multiple visits in 2017–2018; two 50m transects per site walked at a steady pace.
- Biodiversity recording:
  - Butterflies: recorded to species level within a 5m box along transect; in flight or nectaring noted.
  - Bees, hoverflies, flies, beetles: recorded to species within a 2m box along transect; plant species foraging on recorded.
  - Insects identified to species where possible; otherwise higher taxonomic levels used.
- Temporal sampling: Transects conducted on three dates per habitat type.
  - Calcareous grassland: June, July, August.
  - Heathland: May, August, September.
  - Woodland: May, June, July.
- Metadata: Date of survey, start/end times, and weather conditions recorded (cloud cover, temperature) with predefined weather criteria.
- Conditions for sampling: Dry, calm; minimum 13°C; 13–16°C preferred with ≤40% cloud cover; wind ≤ Beaufort 5; survey window 10:00–16:00.
- Spatial referencing: Grid reference of site stored to 10km resolution.

## Quality Control
- Field data collected exclusively by experienced ecologists; same team conducted all surveys for consistency.
- Data entry: Recorded directly into field spreadsheets; routine checks for anomalies.
- Documentation of data columns and units provided to ensure data usability and compatibility with GIS workflows.

## Data structure and variables
- Core pollinator dataset fields (examples):
  - Site_no (CEH allocated site number; 1–39)
  - Habitat (numeric code; 1940 original habitat category)
  - Habitat_1940 vs Habitat_2017 (mapping table provided)
  - Date_of_survey (DD.MM.YY) and Start_time / End_time (HHMM)
  - Survey_month (text) and Surveyor (initials)
  - Transect_no (1 or 2)
  - Grid_ref (site grid reference; 10km resolution)
  - %_Sunshine and %_Cloud_cover (environmental context)
  - Insect_seen_Y_N (Y/N)
  - Activity_when_seen (in flight, at rest, or foraging)
  - Flower_species_foraging_on (scientific name if known)
  - Insect_name (species level where possible)
  - Caste_or_gender (e.g., queen, worker; gender where known)
  - Number_seen (count)
- A dedicated habitat-1940 to habitat-2017 lookup table is included to define the proposed gradient category for each site.
  - 39 mappings pair original Good habitat with current habitat/SSSI-related classifications
  - Examples include: Calcareous 1940 → Calcareous grassland (SSSI quality); Heathland 1940 → Coniferous plantation on heathland; Woodland 1940 → Broadleaf woodland or Ancient woodland (SSSI quality)
- Data are structured to support GIS-ready analyses and cross-walk between historical habitat types and current conditions.

## Data sources and references
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125