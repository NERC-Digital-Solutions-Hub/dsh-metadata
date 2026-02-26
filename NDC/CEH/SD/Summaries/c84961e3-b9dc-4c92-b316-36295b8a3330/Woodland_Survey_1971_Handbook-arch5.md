# NAIIONAL WOODLANDS CLASSIFICAIIDN 1971 HANDBOOK OF FIELD METHODS

- A detailed field manual outlining standardized methods for surveying British woodlands, including ground flora, trees, saplings, shrubs, plot and site descriptions, soil data, herbarium collection, and data recording.
- Designed to support large-scale woodland surveys (e.g., 1648 plots) with formal data collection, documentation, and basic soil interpretation to enable later numerical analysis.

## Purpose and Scope
- Establishes a publishable, repeatable workflow for surveying woodlands, ensuring data are discoverable, comparable, and fit for analysis.
- Covers permissions, site and plot setup, data recording, herbarium practices, soil sampling and interpretation, and data packaging for transmission.

## Data Collection Process and Permissions
- Before survey: prepare an outline plan to minimize travel and coordinate with regional staff; obtain site access permission from owners/occupants; maintain good public relations.
- Access points: determine optimal entry to minimize disruption; avoid trespass or damage; use marked tracks and boundaries where possible.
- Documentation of access: keep a clear trail of permissions and any back-up sites if access is refused.

## Sampling Design and Location
- Sites mapped using road maps and site maps; 16 sampling points per site on a 22" map, with precise ground location using control points and bearings.
- Location accuracy target: within a 20 m radius of the true point; procedures emphasize minimizing subjective bias in point selection.
- Randomized orientation and consistent plotting layout: centre point with right-angle gauge; nested plots from 2x2 m up to 14.14x14.14 m; clear marking of plot corners.

## Data Capture and Forms
- Two main forms per site: Site Description and Habitats Form; Plot Description and Habitats Form (reduced, but aligned with site form).
- Data capture areas include:
  - Ground Flora: presence/absence in increasing quadrat sizes and percent cover estimates.
  - Trees, Saplings, and Shrubs: diameters (DBH) and heights; location within plot quarters; dead or multi-stemmed indicators.
  - Plot Description and Habitats: slope, aspect, topographic features, and a detailed habitat description using defined attributes.
  - Soil Data: small pit (top 25–30 cm) and auger borings; composite soil sample from top 10–15 cm; field interpretation of horizons Ao, Al, A2, B1/B2, C; limited set of measurements due to scale (pH, loss on ignition, mechanical analysis).
- Recording rules to reduce disturbance and bias:
  - Ground flora documented first to limit trampling bias; other observations follow.
  - Complete, consistent notation of species using field codes; herbarium specimen collection for uncertain identifications.
  - Office-use code column for data punching; standardized dating, plotting, and recorder initials.

## Herbarium and Taxonomic Documentation
- Appendices provide instructions for collecting herbarium specimens with emphasis on obtaining type or diagnostic specimens (flowering/fruiting material when possible).
- Specimens are labeled, stored, and linked to field codes to ensure data traceability and taxonomic accuracy.
- Encourages collecting specimens when uncertain identifications arise to prevent data misclassification.

## Site and Plot Descriptions; Habitat and Margin Data
- Site Description and Habitats Form collects site-wide attributes; Plot Description and Habitats Form collects plot-level attributes (slope, aspect, vegetation structure, presence of specific habitat features).
- Attributes include a coded hierarchy for habitats (rock, aquatic, open habitats, hedges, boundary types, human influences) and marginal land use (e.g., orchard, arable, railway, road).
- Data integration strategy: site and plot forms use parallel attribute codes to enable cross-checks and consistent data merging.

## Soil Data Methodology
- Rationale: limited resources for 1648 plots; combine limited physical/chemical measurements with a descriptive, horizon-based soil description.
- Measured parameters: pH, loss on ignition, and a simplified mechanical analysis (sand/silt/clay fractions); preserved sub-samples for potential future analyses.
- Soil profile interpretation: horizon-by-horizon recording (Ao, Al, A2, Bl/B2, C) with emphasis on horizon presence, color, texture, structure, moisture, and deposition.
- Underlying material is recorded when discernible; depth notes and auger limits are documented; guidance provided for difficult or ambiguous profiles.
- Detailed procedural guidance for horizon identification and coding, including how to treat gleyed horizons, peat layers, and podzolic features.

## Data Packaging, Archiving, and Transmission
- Completed data consist of four site forms and two plot forms per site, with corresponding soil reports and bryophyte/ herbarium samples.
- Samples and forms are organized into labeled boxes for shipment; three boxes for soil samples and one for bryophytes; pre-paid postage and labeling provided.
- Emphasis on completeness and correctness, even if it requires extra time, to ensure long-term data utility.

## Equipment and Field Logistics
- Comprehensive field equipment list (plot markers, compasses, tapes, hand tools, labels, herbarium supplies, bags, boxes, maps).
- Clear instructions about handling, labeling, and transporting materials to preserve data integrity.

## Data Governance Takeaways for Data Stewards
- Data model and lineage:
  - Core entities: Site, Plot, SamplingPoint, GroundFloraObservation, Tree/Sapling/ShrubObservation, SoilSample, HerbariumSpecimen, HabitatAttribute, BoundaryType, MarginalLandUse, Equipment, Recorder.
  - Relationships defined by site, plot, and sampling point; multi-form linkage (site vs plot data) with consistent coding schemes.
- Standardization and metadata:
  - Use of standardized forms with explicit attribute codes, units, and observation rules; need for a comprehensive data dictionary and codebooks (species, habitat, boundary, marginal land use).
  - Office-use codes and field codes require careful mapping to ensure data integrity during punching and later analysis.
- Data quality and validation:
  - Emphasis on note- and specimen-based validation (herbarium) to mitigate misidentification; planning for data checks, cross-field consistency, and logical integrity between site and plot forms.
  - Written procedures to minimize observer bias (randomized plot orientation, control-point-based location, fixed pacing rules).
- Data capture and digitization:
  - Primary data are collected on paper forms; data punching and digitization are implied steps, underscoring the need for audit trails, versioning, and standardized digitization workflows.
- Data accessibility and preservation:
  - Physical archival workflow (boxes, packing lists, postage) highlights governance considerations for long-term preservation; digital counterparts should ensure durable identifiers, locality, and provenance metadata.
- Taxonomy and provenance:
  - Explicit herbarium work and specimen handling to anchor species data; ensure linkage between field codes and taxonomic names in the digital dataset.

- Practical guidance for implementing governance in similar field programs:
  - Build a formal data dictionary including all codes used on forms (species codes, habitat codes, boundary types, marginal land uses).
  - Define data provenance: who collected, when, where (site/plot), and how (equipment and methods); preserve raw field sheets alongside digitized records.
  - Establish clear data quality checks and review steps, including specimen verification for taxonomy.
  - Plan for data sharing and archiving: specify data formats, version control, and access policies; ensure traceability from field to analysis.
  - Consider geospatial linkage: integrate site/plot data with GIS coordinates and map references for discoverability and interoperability.

- Overall: The handbook provides a comprehensive, codified framework for conducting large-scale woodland field surveys. For Data Stewards, it highlights the importance of structured data models, rigorous metadata, standardized coding, quality control through physical validation (herbarium), and robust archival workflows to ensure datasets are reliable, reproducible, and usable for future discovery and analysis.