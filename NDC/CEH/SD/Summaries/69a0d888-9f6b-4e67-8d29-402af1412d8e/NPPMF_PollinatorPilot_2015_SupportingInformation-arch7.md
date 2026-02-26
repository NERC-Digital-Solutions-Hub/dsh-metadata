# NPPMF_PollinatorPilot_2015

## Overview
- A pollinator monitoring pilot from 2015 collecting data on pollinating insects, floral resources, and environmental conditions.
- 14 sites across the UK, sampled in four rounds from April to August 2015 ( rounds attempt to match specific dates but often extended due to weather).
- Half the sites in agricultural habitats, half in semi-natural habitats.
- Aimed to: compare sampling methods, assess different recorder groups’ capabilities, gather method feedback, and evaluate implementation costs and support needs.

## Study design and sampling framework
- Site definition: each site is a 1 km2 Ordnance Survey grid square; five pan trap stations and transects placed diagonally through the square.
- Sampling rounds and timing: Round One (27 April–10 May), Round Two (1–14 June), Round Three (6–19 July), Round Four (17–30 August).
- Recorder types and data resolution:
  - Researcher protocol: paid staff with training; species-level identification for bees and hoverflies.
  - Consultant protocol: professional experts; species-level for bees and hoverflies; includes expert inputs.
  - Volunteer protocol: citizen scientists; broad taxonomic groups (not species-level for most taxa).
- Data scope across methods: insects recorded or collected categorized into broad groups; Core groups include Bumblebee, Honeybee, Solitary bee, Hoverfly, Beetle, Butterfly, Fly, Moth, Other/Unknown; researchers and consultants capture species-level data for certain groups; volunteers use broad groups.
- Interaction with existing schemes: habitat coding aligns with BeeWalk (BeeWalk habitat codes) to facilitate cross-scheme analyses.

## Methods and data collection
- Pan trapping
  - Five stations per site; three pans per station (painted blue, white, yellow; UV reflective); samples collected per visit.
  - Used by researchers; volunteers may trial under researcher supervision.
- Fixed transects
  - Five transects per site, each 200 m long, 1 m wide.
  - All recorder types walk the same transect routes; insects visiting flowers within 1 m width recorded.
- Timed focal flower observations (FFOs)
  - Standardised 10-minute observations on focal plants within 0.5 x 0.5 m quadrats; two observations per site visit.
  - All recorder types capable of performing FFOs.
- Standardised free search in good habitats
  - Two fixed areas per 1 km2 site; 30 minutes per search; some methods used only by consultants; researchers may be involved in other protocols.
- Floral surveys of transects
  - Quadrat-based plant counts (1 m2) around transects to estimate floral abundance; 3–6 quadrats per transect; plus overall transect flower abundance estimates by all researchers.
- Floral transects and quadrats
  - Floral quadrats located around pan traps and along transects to assess floral abundance and composition.

## Protocol and logistics
- One-day site protocols tailored to each recorder type; site defined as a 1 km2 grid square.
- Deployment: five pan trap stations and five 200 m transects per grid; transects can follow linear features or run straight, with some flexibility for safety and habitat constraints.
- Floral resource surveys conducted after transect insect sampling on each transect.
- Data collection windows include between-transect periods for FFOs and free searches; timing coordinated across recorder types.

## Data files and schemas
- Data files included (CSV format) and their focus:
  - SiteVisitConditions.csv: date, recorder, environmental conditions (temp, wind, cloud), site, round, protocol, transect details, habitat codes, notes.
  - FreeSearchConditions.csv: environmental conditions and effort for consultant-led free searches, including habitat codes, expertise levels, and counts.
  - FFOBConditions.csv: timings, environmental conditions, and floral resources for focal floral observations.
  - AllInsects.csv: records for all insects by site and visit, including protocol, method, taxonomic group, genus, species (where available), date ID, and quantity.
  - FloralTranssects.csv: floral abundance data on transects by plant species, with abundance scores and derived median abundance.
  - FloralQuadrats.csv: flower abundance data from 1 m2 quadrats around transects and pan traps, with plant species and unit counts.
- Metadata and taxonomic detail:
  - Habitat codes reference BeeWalk taxonomy.
  - Species-level data available for bees and hoverflies for researchers and consultants; volunteers primarily provide broad groups.
- Quality control note: No formal quality control applied across datasets.

## Data quality, limitations, and GIS considerations
- Limitations:
  - No explicit quality control applied to data; potential inconsistencies across recorder types and data resolutions.
  - Data are distributed across multiple files with different scopes and taxonomic resolutions; integration requires careful harmonisation (e.g., aligning species-level data with broad-group data).
  - Some methods (e.g., pan trapping) limited to researchers, with volunteer participation contingent on supervision.
- GIS relevance and integration:
  - Spatial framework anchored to 1 km2 OS grid squares; suitable for spatial joins with other national monitoring schemes (WCBS, NPMS) and for creating grid-based pollinator resources and habitat maps.
  - Rich environmental and habitat metadata support spatial analyses of pollinator–resources relationships (temperature, wind, cloud cover, habitat types).
  - Data can be used to map pollinator abundance, floral resource availability, and survey effort across the landscape; allows linking insect data with floral and environmental layers.

## Practical takeaways for GIS workflows
- Prepare data by harmonising taxonomic resolution across recorder types; create consistent GIS-ready fields for site, round, protocol, and recorder.
- Build spatial layers from 1 km2 grid references and overlay with habitat and environmental rasters.
- Generate map-ready summaries:
  - Insect richness and abundance by 1 km2 grid and recorder type.
  - Floral resource density maps derived from transect quadrats and FFOs.
  - Temporal comparisons across rounds for pollinator activity and floral resources.
- Ensure robust metadata and lineage tracking to support reproducibility and cross-scheme compatibility (e.g., alignment with BeeWalk codes and NPMS/WCBS references).
- Recognize data quality limitations in analyses and communicate where data are species-level versus broad-group level.