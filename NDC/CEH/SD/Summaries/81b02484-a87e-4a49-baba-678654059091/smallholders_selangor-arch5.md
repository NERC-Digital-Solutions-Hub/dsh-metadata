# Environmental_Selangor_perimeter_centre.csv

- Purpose and scope
  - Environmental data collected from five spatially reproducible transects within study plantations in Banting, Peninsular Malaysia.
  - Focus on environmental variables, understory vegetation, and oil palms; data collected on the initial site visit.
  - Intended to support understanding of plantation-scale environmental conditions and their relationship to oil palm management.

- Data structure and contents
  - Environment and plantation metadata
    - PlantationCode, Description, PlantationType (Immature Poly, Immature Mono, Mature Mono)
    - PlantationZone (Central, PSide1–PSide4), GPSCode, PlotWidth, PlotLength
    - TotalNumberOfPalms, ModalPalmAge, TotalOtherCropCover, various crop covers and neighboring land-use metrics
  - Site-level measurements
    - WeatherDay1, DateDay1, SurveyStartTime, SurveyFinishTime
    - Numerous neighboring land-use summaries (OPMono, OPPoly, Housing, Road, Grassland, NonOPCrop, OtherSum)
  - Perimeter-specific measurements
    - Complex set of fields capturing surrounding land-use context and notes
  - Data quality and format notes
    - Fields include data types (Character, Date, Time, Numeric, Integer) and units (e.g., Metres, %)
    - Some fields contain free text and free-form notes, potentially requiring standardization for downstream use

- Key variable themes (high-level)
  - Plantation and transect characteristics: plot dimensions, palm counts, age distributions, palm density
  - Vegetation and crop cover: percentages for oil palms and non-oil palm crops; surrounding habitat types
  - Environmental context: GPS location, weather descriptors, date/time stamps
  - Neighbouring land-use and habitat data: multiple PSide-based percentages and notes
  - Ancillary fields for notes and free-text descriptions to capture context not covered by structured fields

- Data collection context
  - Collected during the initial site visit across multiple transects; designed to capture baseline environmental conditions and spatial context around each plantation
  - Metadata supports linkage with other datasets (e.g., Environmental_Selangor_SamplePoints.csv and Social_Selangor.csv) for integrated analyses

- Data governance and stewardship considerations
  - Rich metadata with explicit variable descriptions, units, and data types supports discoverability and re-use
  - Presence of free-text fields and some potential inconsistencies in field labeling suggests a need for data cleaning and standardization prior to sharing
  - Sharing readiness depends on governance policies; consider documenting data sources, update cadence, and any embargoes or access restrictions
  - Documentation should include guidance for data upload to portals and the process for updating datasets to maintain currency

- Particular challenges relevant to Data Stewards
  - Incomplete or ambiguous mapping between some long field names and standardized schemas
  - Heterogeneous data formats across visible fields and free-text components
  - Large, multi-attribute spatial datasets with numerous surrounding-land-use variables that require careful versioning and provenance tracking

- Recommendations for Data Stewards
  - Validate variable definitions with data creators to ensure consistent interpretation (especially for complex neighbor-land-use fields)
  - Normalize field naming and units where possible; convert free-text notes into structured fields or controlled vocabularies where feasible
  - Establish a metadata standard for updates, data provenance, and data quality checks
  - Document data sharing terms, accessibility, and any limitations due to licensing or confidentiality
  - Provide a data dictionary and usage examples to facilitate discoverability and re-use

- Related datasets (context for integrated analyses)
  - Environmental_Selangor_SamplePoints.csv: second visit data (4 sample points per plantation) with soil moisture, light, canopy openness, vegetation cover, epiphyte metrics, palm characteristics, and notes
  - Social_Selangor.csv: cross-location survey data on plantation characteristics, management inputs, and socio-demographic factors, enabling integrated environmental-social analyses across locations (Indonesia and Malaysia)