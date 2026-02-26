# Metadata for published database

- Purpose and scope
  - Metadata schema for a published drone survey dataset used to monitor environmental conditions and vegetation attributes.
  - Captures provenance, spatial context, plant information, and biomass/canopy measurements to enable reproducibility and reuse.

- What is included
  - Identifiers and provenance: survey_code, PlotID, email, Investigators.
  - Site and location: SiteName, Country, SiteLatitude, SiteLongitude, EPSG, UTM_zone.
  - Spatial geometry: Corner1 through Corner4 coordinates (X, Y, Z) representing harvest plot corners; plot_area_from_coordinates_m2.
  - Environmental context: MAT (mean annual temperature), MAP (mean annual precipitation), Wind_speed, sky_conditions.
  - Habitat and biology: CommunityDescription, plant_functional_type, life_cycle_strategy, PlotFamily, PlotGenus, PlotSpecies, PlotSubspecies, PlotOrder.
  - Biomass and structure: AGB (dry biomass in g), AGB_g_m2 (biomass density), HAG_plotmean_of_cellmax_m (mean canopy height).
  - Data governance and acknowledgments: Acknowledgements_Funding, Acknowledgements_Permission, Acknowledgements_Assistance.
  - Data collection specifics: drone_and_sensor, CameraShutterType, plot_area_from_coordinates_m2, NB note about using plot frame area when available.

- Data quality, provenance, and context
  - Emphasizes traceability with investigator details and contact (email) for dataset responsibility.
  - Documents measurement platform and sensor details (drone and camera), as well as shutter type.
  - Provides precise geospatial references (coordinates, EPSG, UTM zone) and plot geometry for reproducibility.
  - Includes environmental context (MAT, MAP, wind and sky conditions) to contextualize biomass and canopy measurements.

- How Analysts Monitoring the Environment would use it
  - Verify and clean data using standardized fields and units.
  - Transform data for analysis (e.g., biomass density calculations, canopy height summaries).
  - Present outputs in clear formats (maps, charts) linked to site and plot metadata.
  - Store and upload datasets to appropriate portals ensuring accessibility and traceability.

- Notable definitions and units
  - AGB: dry above-ground biomass in grams.
  - AGB_g_m2: biomass per square meter.
  - MAT: mean annual temperature in degrees Celsius.
  - MAP: mean annual precipitation in millimeters.
  - HAG_plotmean_of_cellmax_m: mean canopy height in meters.
  - Coordinates use UTM with specified EPSG and zone; corners define harvest plot geometry.