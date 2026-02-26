# Environmental_Selangor_perimeter_centre.csv

## Overview
- Data from five spatially reproducible transects within each study plantation in Banting, Peninsular Malaysia.
- Collected on the initial site visit; captures environmental variables, understory vegetation, and oil palm characteristics.
- Aimed at understanding spatial environmental context around oil palm plantations.

## Key Datasets and Content
- Environmental_Selangor_perimeter_centre.csv
  - Core fields include: PlantationCode, PlotWidth, PlotLength, TotalNumberOfPalms, ModalPalmAge, and various land-use and vegetation metrics.
  - Spatial and temporal details: WeatherDay1, DateDay1, SurveyStartTime, SurveyFinishTime.
  - Spatial targeting: PlantationZone (Central, PSide1-4), GPSCode (center of transect).
  - Habitat and land-use context: NeighbouringOPMono/NeighbouringOPPoly, NeighbouringHousing, NeighbouringRoad, NeighbouringGrassland, NeighbouringNonOPCrop, NeighbouringOtherSum, and related notes.
  - Vegetation and crop cover: TotalOtherCropCover, OtherCropCovers (e.g., Banana, Cassava, Coconut, Galangal, Yam, Jackfruit, Pineapple, Torch Ginger), DominantCoverSpecies, and various vegetation cover categories.
  - Palm and plantation structure: TotalNumberOfPalms, PlotWidth, PlotLength, ModalPalmAge, Plot location details.
  - Supplementary notes: NeighbouringHabitatTypesNotes.

- Environmental_Selangor_SamplePoints.csv
  - Data collected at four spatially reproducible sample points per plantation on a second visit (48 hours after the initial visit).
  - Variables cover soil moisture, pH, light, canopy openness (N, S, E, W), and fine-scale vegetation metrics in 5x5 m quadrats (bare ground, palm cover, other crops, leaf litter, frond cover, epiphytes, etc.).
  - Palm-centered measures: DistanceFromNearestPalm, PalmAge, PalmHeight, TotalEpiphyteCover, EpiphyteSpecies, PalmHerbivoryScore, PalmFungalScore, PalmRhinoBeetleScore, and Notes.
  - Additional context: presence of wildlife, herbivory, and free-text notes per palm point.

## Social Context and Management Data
- Social_Selangor.csv
  - A harmonised survey instrument used across three locations (SMARTRI in Riau, Indonesia; Wild Asia in Perak, Malaysia; Banting in Malaysia).
  - Topics include plantation characteristics, management inputs (fertiliser, herbicide, intercropping, harvesting), and socio-demographic factors of plantation managers, attitudes toward nature and the oil palm industry, and management motivators.
  - For Banting sites: detailed descriptors of plantation age and intercropping status (MM, MMIP, IP, etc.), plantation area, ownership, palm density, income, and management experience.
  - Extensive variables on education, employment, income, land use history, landowner status, management motivation, and perceived importance of nature values (economic, food, wildlife, beauty, culture, health, none).
  - Management and economic variables include herbicide and fertiliser usage (costs, volumes, per hectare metrics), intercropping practices, organic manure use, and vegetation control methods.
  - Wildlife and observer data encompass wildlife presence, animals seen daily, favorite/least favorite animals, and attitudes toward animal management and related impacts on farming decisions.
  - Rank-order metrics capture influence on management decisions from neighbours, scientific advice, cost, effort, consistency, and yields.

## Data Structure and Standards
- Common key: PlantationCode appears across Environmental and Social datasets, enabling cross-linking by plantation.
- Data types represented: Character, Integer, Numeric, Date, Time, and Boolean-like indicators (Yes/No through Character fields in many cases).
- Units and currencies vary: hectares, metres, percent cover, grams/kilograms, Malaysian ringgit and Indonesian rupiah, dates in YYYY-MM-DD format, times in HH:MM.
- Several fields include long descriptive text (e.g., free text weather notes, management motives, open-ended responses).

## Data Quality and Governance Considerations for Data Leaders
- Observed complexity and breadth: wide range of ecological and social variables collected at different spatial scales and visits.
- Metadata challenges: some fields include misalignments or ambiguous descriptions (e.g., inconsistent phrasing in crop cover fields), indicating potential data quality and documentation gaps.
- Standardization needs:
  - Harmonise variable naming and units across datasets to enable reliable integration.
  - Ensure complete and consistent data dictionaries and data dictionaries for field meanings, valid value ranges, and units.
  - Implement consistent handling of missingness and free-text fields (e.g., encoding, controlled vocabularies).
- Discoverability and lineage:
  - Maintain clear data lineage: when, where, by whom data were collected, and any transformations applied.
  - Establish a centralized metadata registry to support data discovery and reuse across the organisation and partner networks.
- Data access and ethics:
  - This collection spans environmental and social dimensions with sensitive demographic and livelihood information; ensure appropriate access controls, privacy protections, and consent provisions where applicable.
- Data maintenance:
  - Schedule updates or versioning of datasets, especially if continued data collection or re-surveys are planned.
  - Track data quality issues, corrections, and changes in a change log.

## Practical Uses for Data Leaders
- Cross-dataset analysis:
  - Link environmental transect data with sample-point measurements to study fine-scale ecological patterns and palm performance.
  - Integrate social and management data to examine how management decisions, economic factors, and attitudes influence environmental outcomes and agricultural practices.
- Data governance and strategy:
  - Use the datasets as a case study for establishing data standards, metadata practices, and cross-site data sharing within the organisation and with partners.
  - Foster co-ownership of data products by engaging policy colleagues and plantation managers in data interpretation and dissemination cycles.
- User-focused product development:
  - Develop dashboards and reports that reflect both ecological indicators (habitat quality, canopy openness, vegetation structure) and social indicators (management motivations, income, education) to support evidence-based decision-making.
- Community of practice:
  - Share methodologies for multi-disciplinary data collection and integration to reduce duplication of effort and strengthen sector-wide data standards.

## Context and Scope
- Geographic focus: Banting, Peninsular Malaysia, with broader cross-location application implied by the Social_Selangor.csv metadata noting three unique locations.
- Data purpose: to understand environmental conditions, vegetation structure, palm characteristics, and social management dynamics in oil palm plantations, enabling informed data-driven decisions at organizational and network levels.