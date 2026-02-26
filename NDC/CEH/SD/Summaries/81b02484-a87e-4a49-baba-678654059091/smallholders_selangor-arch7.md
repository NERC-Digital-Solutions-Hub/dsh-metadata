# Environmental_Selangor_perimeter_centre.csv

- Overview
  - Spatially explicit environmental dataset collected from five transects within study plantations in Banting, Peninsular Malaysia.
  - Captures environmental variables, understory vegetation, and oil palm metrics from the initial site visit.
  - Data designed for map-based analyses and GIS visualisations of plantation structure and surrounding land use.

- Datasets included (within the same document)
  - Environmental_Selangor_perimeter_centre.csv: transect-level environmental and vegetation measurements.
  - Environmental_Selangor_SamplePoints.csv: four spatially reproducible sample points per plantation with detailed point-level environmental and vegetation measurements.
  - Social_Selangor.csv: socio-economic and management survey data linked to plantation locations (shared across multiple sites).

- Spatial design and sampling
  - Transects: five spatially reproducible transects per plantation; assesses perimeter context and interior conditions.
  - Survey zones: PlantationZone categories include Central and PSide1–PSide4, enabling boundary-to-interior spatial comparisons.
  - Sample points: four reproducible sample points per plantation for point-level measurements.
  - GPS: GPSCode fields provide coordinates for transect centres and PSide corners; enables precise mapping and integration with plantation boundaries.

- Key variables (highlights)
  - Plantation attributes: PlantationCode, Description, Type (Immature Poly, Immature Mono, Mature Mono), PlotWidth, PlotLength, TotalNumberOfPalms, ModalPalmAge.
  - Vegetation and land cover: TotalOtherCropCover and multiple crops (Banana, Cassava, Coconut, Galangal, Yam, Jackfruit, Pineapple, TorchGinger), Neighbouring land-use metrics (OPMono, OPPoly, Housing, Road, UnusedLand, Grassland, NonOPCrop, OtherSum), NeighbouringHabitatTypesNotes.
  - Environmental and site context: WeatherDay1, DateDay1, Canopy openness metrics (CanopyOpennessN/S/E/W), SoilType, SoilType-related notes.
  - Plot-level measurements: Distances and dimensions, Palm counts, Palm age, and various understory/vegetation indicators.
  - Data quality/QA-ready fields: Descriptions, Units, and Type metadata aligned for GIS consumption.

- Data quality and preparation considerations
  - Complex, multi-table schema with extensive field definitions; careful harmonisation needed for cross-dataset integration.
  - Potential data quality challenges include inconsistent field descriptions across crops and land-use categories, missing values, and resolution differences between perimeter transects and center plots.
  - Requires data cleaning and standardisation before GIS analysis to ensure consistent units and coding across transects and PSides.

- GIS relevance and potential visualisations
  - Map-based representation of plantation extents, transect paths, and PSide boundaries.
  - Spatial layers for environmental conditions, understory vegetation, and crop/land-use cover surrounding each plantation.
  - Point-based analyses using Environmental_Selangor_SamplePoints.csv for canopy openness, soil characteristics, vegetation cover, and palm-nearest metrics.
  - Integration with Social_Selangor.csv enables spatially informed socio-economic mapping (e.g., where management motivations and demographics cluster).

- Usage notes for GIS specialists
  - Leverage GPSCode and Plot/Transect coordinates to create accurate shapefiles or geodatabases for plantation footprints and transect lines.
  - Use canopy openness, vegetation cover, and neighboring land-use variables to explore spatial relationships with palm health, yield potential, and habitat features.
  - Combine with Social_Selangor.csv data to contextualize spatial patterns with management practices and socio-demographic factors.

- Considerations and challenges for deployment
  - Data standardisation: align crop naming, land-use categories, and measurement units across datasets.
  - Data discovery and integration: data reside in multiple files with extensive metadata; plan for metadata curation and dataset linking.
  - Resolution and scope: ensure spatial alignment between transect-level perimeter data and point-level measurements; handle differing resolutions in analysis.
  - Skills and tooling: robust data wrangling and GIS proficiency required to create coherent map products and analytical layers.

- End-use applications
  - Spatial analysis of oil palm plantations with respect to neighbouring land uses and peri-plantation habitats.
  - GIS-based decision support for landscape-level planning, intercropping decisions, and management interventions.
  - Visualization of environmental gradients, understory structure, and palm plantation metrics for policy briefs, stakeholder engagement, and research.

- Summary of the Social_Selangor component
  - Shared survey instrument across Banting (Malaysia) and additional sites (SMARTRI, Indonesia; Wild Asia, Malaysia).
  - Captures plantation characteristics, management inputs, and socio-demographic factors of smallholder respondents.
  - Enables GIS-enabled mapping of management motivations, income, intercropping, land tenure, education, wildlife interactions, and yield-related variables.
  - Supports cross-site comparisons and spatially informed interpretations of social drivers of plantation management.