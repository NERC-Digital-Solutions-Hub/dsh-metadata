# COUNTRYSIDE SURVEY 1990

- Purpose and context
  - Large-scale monitoring of rural land use to update land-cover databases and support ecological/change analyses.
  - Combines ground-truth field surveys with remote-sensing data (satellite imagery) via a two-tier approach to link bottom-up field data with top-down imagery.
  - Aims to provide current datasets for scientific evaluation of ecological systems and track changes over time.

- Study design and scope
  - 512 survey squares planned for 1990, split among six ITE Research Stations; each square typically surveyed by a team of about 85 squares per station.
  - Each square expected to take about three days to survey; flexible scheduling to optimize travel time and minimize oversearching.
  - 128 new squares added to reach 512; 128 squares previously surveyed (1977/78 or 1984) relocated or re-sampled as applicable.
  - Standardized field handbook and rigorous quality control to minimise observer variation and ensure consistency across teams.

- Data capture and GIS integration
  - Data collection organized around three core elements: mapping, vegetation quadrats, and sampling (with a fourth emphasis on freshwater biota sampling under separate protocols).
  - Data coded on 1:10,000 scale maps using a controlled code set (primary and secondary codes) to capture land-use, vegetation, boundaries, and other landscape features.
  - Field Assessment Booklets (FABs) compile map annotations, quadrat data, ownership, and other contextual information for GIS-friendly records.
  - Permanent markers and standardized plotting enable accurate relocation for future surveys and longitudinal GIS analysis.

- Field methods and sampling design
  - Mapping component
    - Annotate enlarged 6" maps with structured data codes; use alpha-numeric combinations to capture complex features efficiently.
    - Boundaries clearly delineated; gaps or old features marked with specific codes (e.g., 999 for no longer present).
  - Vegetation sampling (6.2)
    - Large quadrats: five 200 m² plots per square (to characterize broad habitat mosaic).
    - Small quadrats: five 2 m × 2 m plots placed in natural/semi-natural habitats to capture finer-scale variation.
    - Nested quadrats: within each large 200 m² plot, nested smaller quadrats are used to derive species composition and cover.
    - Linear plots: up to five 1 m-wide plots for hedgerows, streamsides, roadsides, and boundary features to capture linear habitat structure.
    - Location/relocation rules provided for quadrats and linear plots, including handling squares recorded in earlier surveys.
  - Aerial photograph interpretation (API)
    - Optional API support to identify features not on OS maps (isolated trees, boundaries between semi-natural vegetation types, new buildings/roads).
    - Guidance on map alterations and interpretation conventions to ensure API-derived data remains ground-truthable.
  - Freshwater biota sampling
    - Two freshwater biota samples per square: flowing-water and standing-water habitats, collected under separate IFE/NELUP protocols.
    - Marked and documented locations on maps; samples preserved for laboratory processing.

- Data recording, coding standards, and quality
  - FAB completion rules emphasize neatness, legibility, and consistent coding to avoid data loss during later analysis.
  - Codes comprise primary and secondary categories; a composite alpha code can summarize multiple attributes (e.g., boundary type plus management attributes).
  - Rules ensure surveyors make decisions in the field; exceptions require notes or comments rather than deferring decisions to data processors.
  - Vegetation coding relies on a predefined list of common species (with allowances for combinations when species-level IDs are uncertain); bryophytes and lichens have a restricted, approved list.
  - Minimum mappable unit: 1/25 hectare; minimum mapping length: 20 m; non-vegetation areas and special cases require dedicated handling.
  - Time-series consistency: relocation markers, permanent metal plates, and standardized photography support longitudinal GIS analysis.

- Plot layout, permanent markers, and documentation
  - Permanent markers (metal plates) placed near quadrat corners to enable repeatable relocation; field sketches and measurements accompany FAB entries.
  - Photos of vegetation plots captured with a running plot number and location noted on a board at the plot edge.
  - Detailed guidance for placing quadrats in linear features (hedges, streams, roadsides) and for documenting distances, bearings, and surrounding landmarks.

- Boundaries, buildings, and land use
  - Boundaries coded to reflect actual and interpreted features (fences, walls, hedges, banks); “no longer present” boundaries flagged with code 999.
  - Building and curtilage coding covers urban-adjacent features, with a separate schema for garden/grounds, amenity spaces, car parks, and other built elements.
  - Special emphasis on differentiating land-use categories (e.g., unmanaged grass, ley, crops, moorland, wetlands) and on noting landscape mosaics.

- Species data, growth, and age coding
  - Species identifications targeted to species-level where feasible; combinations permitted when exact ID is uncertain but ecologically meaningful.
  - Codes include major crops, grasses, forbs, rushes, sedges, bryophytes, and lichens; covers a range of management states (cultivated, unimproved, abandoned, burnt, etc.).
  - Age and diameter classes for woodland and tree layers documented to support canopy composition and forest structure analyses.

- Photography and post-survey procedures
  - Systematic photography of vegetation plots; numbers displayed on a board visible in frame to link images to FAB entries.
  - End-of-day checks to ensure complete data capture; FABs and samples transported to ITE stations for processing.
  - Provisions for handling damaged maps or records, with recommendations to re-map only when necessary.

- Special notes for GIS specialists
  - A standardized, scalable field-to-GIS workflow designed to support integration with satellite-derived land-cover maps and downscaled landscape features.
  - A two-tier data framework (ground-truth plots and API-assisted boundaries) to enable robust spatial modeling and change detection.
  - Clear documentation of plot relocation rules and permanent markers to support reproducible GIS-derived analyses across survey years.
  - Comprehensive code sets for land cover, vegetation types, boundaries, and built features to maximize machine-readability and interoperability with GIS software.