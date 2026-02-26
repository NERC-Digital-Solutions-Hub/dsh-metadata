# raw data sets on the behaviour and distribution of Lepidoptera (butterflies and day flying moths) at the Stonehenge Landscape in 2011

## Overview
- Provides raw datasets on Lepidoptera behaviour and distribution in the Stonehenge Landscape, Wiltshire, UK, sampled in 2011.
- Adapted from Grace Twiston-Davies’ PhD thesis (2014) on landscape connectivity and habitat restoration.
- Includes Lepidoptera flight-path observations, boundary and habitat context, and plant/nectar data; data quality checks described.

## Study area and sampling framework (geospatial context)
- Location: Stonehenge World Heritage Site, within four chalk grassland fragments on former arable land undergoing habitat restoration.
- Fragments: Full-moon Bank, Luxenborough Bank, Winterbourne Stoke Group, Fargo Barrow (all within the Stonehenge Landscape estate, National Trust).
- Boundary-based sampling design:
  - Four 20 m × 20 m survey boundaries per fragment, located at the fragment edge against adjacent land cover (arable or grassland restoration).
  - Some fragments have boundaries on different edges (e.g., western/eastern) or reduced sampling (e.g., Fargo Barrow).
  - 14 survey boundaries in total; corresponding control surveys in adjacent continuous habitat or within the fragment interior.
- Geospatial coordinates:
  - Each boundary and transect has grid references in two systems:
    - SU (Ordnance Survey grid) coordinates for transect start points.
    - British National Grid (BNG) coordinates for precise location references.
- Boundary vs control surveys provide context on Lepidoptera behaviour at habitat edges versus continuous habitat.

## Lepidoptera surveys (methods and timing)
- Survey window: May to July; conducted 10:00–16:00 (effort spread across day to minimise time-of-day effects).
- Methodology:
  - 20 m × 20 m survey areas centered on the boundary between chalk grassland and adjacent habitat.
  - Visual tracking of individual Lepidoptera flight paths within the survey area; three-minute observation per individual.
  - Termination of observation when the individual becomes stationary for >3 minutes or moves >20 m from the boundary edge.
  - Each boundary surveyed for a total of 20 minutes on three occasions (May, June, July).
- Flight-path categorisation:
  - Exited survey area behaviour categorized as Crossing, Following, or Avoiding boundary.
  - Staying assigned if the individual did not exit the survey area or flight path was too complex to assign.
  - Determinants based on which boundary edge the exit occurred (crossing vs following vs avoiding).
- Pseudoreplication controls:
  - To reduce pseudoreplication (same individual recorded multiple times), different species or sexes used for successive flight paths.
  - Approximately 15 days between replicates at each site.
- Weather and environmental context:
  - Weather criteria aligned with UK Butterfly Monitoring Scheme (Pollard & Yates, 1993).
  - Additional measures recorded for vegetation and nectar resources (see Plant data).

## Vegetation and nectar data (within-boundary plots)
- Vegetation characteristics and nectar availability recorded in eight 0.5 m × 0.5 m quadrats per boundary (four on each side: chalk grassland and adjacent land cover).
- Measured attributes:
  - Vegetation height and density (via drop disc method).
  - Percentage bare ground.
  - Nectar flower availability: number of flowering units, with counts by families (Asteraceae, Fabaceae, Dipsacaceae) selected from a nectar plant database.
- Botanical surveys:
  - Conducted on two occasions between May and August.
- Wind context:
  - Average wind speed and direction recorded from the Boscombe Down meteorological station (6.5 km SW) to approximate site conditions during surveys.

## Data schema and documentation (structure and codes)
- Data sheets and fields are described across several tables and sheets (referenced as DATA Lepidoptera Behaviour and related resources):
  - Key columns for Lepidoptera Behaviour data include:
    - DATE, TEMP, WIND SPEED, WIND DIRECTION, Cloud, REP, MATRIX TYPE, LOCATION, SURVEY, SURVEY TYPE, SIDE OF LOCATION, SHELTERED OR EXPOSED, START TIME, END TIME, SPECIES, SPECIES CODE, SEX, BEHAVIOUR, HABITAT TYPE START, HABITAT TYPE END, MOVEMENT DIRECTION, NOTES.
  - Location and transect coding:
    - Location codes for fragments (e.g., WSG, Fargo, Full, Lux, etc.)
    - Side of location (West, East, Centre for control/edge cases)
    - Sheltered (Sh) or Exposed (Ex) locations
    - START/END habitat types (chalk grassland fragment or adjacent habitat, including restoration or arable)
    - Transect grid references (SU) and British National Grid (BNG)
  - Data dictionaries for resource behaviour (DATA Resources Behaviour) and plant data (DATA Lepidoptera?) outline column definitions and units.
- Species and plant nomenclature:
  - Lepidoptera nomenclature follows standard field guides (Langmaid et al. 1989; Heath & Emmet 1985; etc.).
  - Plant nomenclature follows Stace (2010).
  - Tables list species surveyed, with scientific name, common name, and abbreviation codes (e.g., Ads.sta for Forester, Agl.urt for Small Tortoiseshell, etc.).
  - Flowering plant species are listed with scientific names, common names, and codes (e.g., Agr.eup for Agrimony, Cam.glo for Clustard Bellflower, etc.).
- Data quality assurance:
  - Outliers and anomalies checked via literature-informed expectations, pivot tables, and exploratory analyses (details not shown in text).
  - Efforts described to minimize pseudoreplication; sampling design aims to balance replicates and species/sex diversity across boundaries.

## Key geographic and data-structuring implications for GIS use
- Rich geospatial context:
  - Boundaries are precisely georeferenced, enabling boundary-edge analyses, edge effects, and habitat connectivity assessments.
  - Dual-coordinate references (SU and BNG) support integration with different GIS datasets and mapping standards.
- Rich attribute schema:
  - Detailed per-flight-path observations linked to boundary location, boundary type, habitat context, and environmental conditions.
  - Integrated vegetation and nectar resource metrics alongside Lepidoptera behaviours, enabling habitat suitability and resource-use analyses.
- Temporal layering:
  - Three replicate surveys across May–July, with time-of-day and weather variables enabling temporal comparisons.
- Data limitations and considerations:
  - Small fragment sizes and boundary-centric design may limit extrapolation to broader landscapes.
  - Pseudoreplication controls acknowledged; no capture/mark-recapture used, which impacts individual-tracking granularity.
  - Some data are described as not shown (QA analyses); users should consult accompanying metadata for details on data cleaning steps.

## References and data provenance
- Core references informing methods and nomenclature include:
  - Pollard & Yates (1993) UK Butterfly Monitoring Scheme
  - Ries & Debinski (2001) on butterfly responses to habitat edges
  - Stace (2010) plant nomenclature
  - Langmaid et al. (1989) and Heath & Emmet (1985) Lepidoptera references
  - Stewart et al. (2001) sward height measurement methods
- Data context derived from Grace Twiston-Davies’ PhD thesis on Landscape Connectivity (2014) and related project outputs.