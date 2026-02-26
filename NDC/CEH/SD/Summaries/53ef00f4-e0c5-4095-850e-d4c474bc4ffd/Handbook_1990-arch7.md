# COUNTRYSIDE SURVEY 1990

- Overview
  - A national, map-based field survey to monitor land use, land cover and landscape changes in Britain, linking ground-truth data with remote sensing.
  - Two-tier approach: ground-truth field data (ITE Land Classification System) and satellite imagery to construct a Britain-wide land cover map; ground data used for validation and modelling.
  - Re-survey planned for 1990 to update datasets and assess changes; includes increased sample size and enhanced data collection (more detailed attributes and collaboration).

- Aims and GIS relevance
  - Produce current, standardised spatial data products that enable exploration and visualization of rural environments.
  - Standardised field recording to reduce observer variation; critical for reliable change detection and trend analysis.
  - Provides a framework for integrating datasets at different resolutions (field observations, map codes, aerial interpretations, and remote sensing).

- Planning and data governance
  - The sample is divided into six teams, each handling a set of squares; flexible working arrangements to maximise coverage and minimize travel.
  - Permissions are essential for full-square access; procedures defined for handling refusals and partial access.
  - All data collection follows a Field Handbook with clear definitions, ownership and farmer information, and quality control mechanisms.

- Data collection framework (FAB)
  - Data Recording: Field Assessment Booklets (FAB) combine square metadata, ownership, farmer information, physiography, land use, boundaries, buildings, and contact points.
  - Mapping: annotate 1:10,000 scale (6") maps with uniform data codes; use alpha-numeric coding to compress complex attributes while preserving detail.
  - Aerial photography interpretation (API): supplementary guidance to identify features not visible on OS maps; dashed lines for identified boundaries; crosses for isolated features; diamonds for no longer present boundaries.
  - Permanent markers: metal plates placeable for accurate relocation of plots in future surveys.

- Plot design and sampling (6.2 Method)
  - Large quadrats: five 200 m2 quadrats per square, with nested sub-quadrats to capture fine-scale vegetation; grid-based, systematically placed to cover habitat diversity.
  - Small quadrats: five 2 m × 2 m quadrats per square in natural/semi-natural land cover types to sample finer mosaics.
  - Vegetation sampling: nested quadrats record species presence and cover (5% increment categories) with a standard species list; unlisted species recorded as needed; include bryophytes and lichens.
  - Plot relocation: predefined rules for relocating plots if land use changes or access issues arise; aim to maintain comparability with earlier survey rounds when possible.

- Vegetation data, coding and interpretation
  - Codes: two-tier coding system (primary and secondary) to describe land cover, vegetation types, boundaries, and features; use dominant primary code when mosaics occur.
  - Boundaries: clearly delineated on maps; note if boundary no longer exists (code 999); provide end-point definitions and perpendicular markers to clarify boundaries.
  - Species and cover: record dominant ground cover types and up to three cover codes per mosaic; provide species-level data only where cover exceeds 25% (with a 5% reporting precision).
  - Data consistency: maintain same species-combination allowances used in prior surveys for comparability; standardized abbreviations and lists (e.g., crops, grasses, forbs, bryophytes).

- Vegetation sampling types and layout (6.2.3 and 6.2.4)
  - Quadrats: large 200 m2 (with inner nested plots) and small 2 m × 2 m quadrats; precise relocation using metal plates and fixed reference lines.
  - Linear plots: up to five 1 m width × 10 m length plots along hedgerows, streamsides, and roadsides to capture linear habitat variation; includes rules to prevent overlap and ensure coverage.
  - Boundary relocation: linear plots positioned at hedges, walls, fences, ditches, or corresponding boundaries; when necessary, relocate to nearest permissible boundary while preserving grid integrity.
  - 1978 rules: legacy locations for linear plots in older squares updated per 1990 methodology; maintain traceability of previous placements.

- Sampling of freshwater biota (7)
  - Freshwater samples: collected from flowing waters (IFE) and standing waters (NELUP) to capture two characteristic habitats per square.
  - Protocols include sieving, preservation, labeling, and rapid transport of samples for analysis; documentation on squares and surveyors.

- Photography and documentation
  - Photograph vegetation plots to document appearance and landscape context; plot and marker plate clearly identified on each image.
  - All FAB pages, maps, and photographs are prepared for efficient data transcription and GIS integration.

- Procedures after fieldwork
  - End-of-day review to ensure no features are missing; transport of FABs and samples to ITE stations promptly.
  - Data management emphasizes timely return to central repositories and traceable relocation markers for future surveys.

- Practical GIS considerations
  - Data standards: use uniform field codes, map annotations and standardized palettes; ensure geographic alignment across FAB, maps, and API outputs.
  - Relocation and time-series analysis: permanent markers and documented relocation rules enable robust time-series GIS analyses of land-cover change.
  - Data integration: FAB metadata (ownership, physiography, land use) supports contextual GIS layers, while vegetation and boundary codes enable rich thematic mapping and multivariate analyses.
  - Output potential: generate land-cover maps, change-detection layers, habitat typologies, and landscape features for policy, client, and public-facing GIS products.

- Key takeaways for GIS specialists
  - Build a comprehensive geospatial dataset by harmonising FAB attributes, plot locations, and coding schemes with map-based outputs.
  - Maintain rigorous documentation of plot locations, ownership, and permissions to support reproducibility and longitudinal studies.
  - Leverage API and high-resolution field data to enrich boundary delineations and vegetation classifications beyond OS map content.
  - Plan for data quality control and observer calibration to ensure reliable change detection over the survey cycle.