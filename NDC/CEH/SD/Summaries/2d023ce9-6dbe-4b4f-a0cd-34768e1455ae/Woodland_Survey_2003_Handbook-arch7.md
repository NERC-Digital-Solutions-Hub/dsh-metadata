# Woodland Indicators: analysis of field survey

- Purpose and scope
  - National Woodland Survey 2002 Field Handbook; methods for collecting standardized woodland field data to support map-based data products.
  - Focus on vegetation, trees, soils, habitats, and site descriptions for GIS-enabled analysis and visualization.

- Spatial design and data collection framework
  - Each site includes 16 randomly located plots; plot locations supplied on multiple maps (1:50,000 OS map, original 2½" map, and enlarged versions).
  - Ground relocation relies on map-derived distances/angles; GPS is discouraged to avoid bias from map-ground mismatches.
  - No permanent plot markers; relocation aims for accuracy with minimal subjectivity; avoid bias by not preferentially selecting “typical” spots.

- Plot layout and sampling points
  - Main vegetation plot: 14.14 x 14.14 m (200 m²) with four corner posts and diagonal distance strings.
  - Inner 2 x 2 m plot and three successive larger quadrats (to 14.14 x 14.14 m) used to record ground flora presence/absence and, for the full plot, % cover.
  - 16 sampling points per site correspond to 16 plots; planned re-recording locations mapped from 1:50k and 2½" maps.

- Data collection components (per plot)
  - Vegetation plot: ground flora presence/absence in five quadrats (2 x 2 m to full plot), with % cover estimates for the full plot; common bryophytes recorded (Appendix I).
  - Trees, saplings and shrubs: species, DBH (cm), and height data collected for stems >5 cm DBH (trees); saplings and shrubs recorded in diagonally opposite quarters 1 (NE) and 3 (SW); dead trees flagged; height measured via clinometer or hypsometer.
  - Plot description and habitats: presence/absence of defined attributes to generate habitat/frequency data; some habitats recorded based on partial plot presence.
  - Soil sampling: one composite soil sample per plot collected from top 15 cm; careful labeling and storage; samples returned to CEH Merlewood.

- Data forms and data flow
  - Four recording forms per plot:
    - Vegetation plot (ground flora): presence/absence across quadrats, % cover, bryophytes.
    - Site description and habitats: site-wide attributes and habitats.
    - Trees, saplings and shrubs: species, DBH, height by plot quadrant; dead/live status.
    - Plot description and habitats: attributes and comments.
  - Per-site site description sheet accompanies all plots; per-site workflow ensures consistency between site and plot data.
  - Appendix IV provides detailed definitions for attributes; Appendix II and III illustrate form layouts and data entries.

- Data quality, relocation, and GIS considerations
  - Emphasis on accuracy and avoidance of subjective bias in plot relocation and habitat recording.
  - Relocation method uses compass bearing and map-derived distances/angles; conversion to metric scales may be needed.
  - Avoid GPS to prevent bias; coordinate data relies on map-based localization and field notes.
  - Cross-checking between site and plot forms to ensure consistency and complete coverage; field sketches recommended for rapid GIS-ready metadata capture.

- Soil handling and per-site logistics
  - 16 soil samples per site, stored in labeled self-sealing bags; bags placed in site-specific plastic boxes for shipment.
  - Samples shipped to CEH Merlewood within about a week when feasible; avoid weekend delays; cool storage recommended if delay is anticipated.

- Appendices, equipment, and protocols (supporting GIS data preparation)
  - Appendix I–II: bryophyte species lists and presence data (for ecological context in GIS outputs).
  - Appendix III: Tree, sapling and shrub data forms (structure for DBH and height attributes).
  - Appendix IV: Site Description and Habitats definitions (coding scheme and attribute mappings).
  - Appendix V: Field equipment lists (data collection and GIS fieldwork logistics).
  - Appendix VI: Soil analysis protocols (pH, moisture loss on ignition) for linking soil properties to spatial datasets.

- Practical notes for GIS implementation
  - Data outputs are structured to support per-site and per-plot spatial layers, with site-level habitat attributes and plot-level vegetation, trees, and soil attributes.
  - Expect a mix of qualitative presence/absence, quantitative percent cover, DBH/height measurements, and soil chemistry/physical properties for integration into GIS projects.
  - Metadata should capture: site number, plot number, date, recorder initials, slope and aspect, map sources, relocation method, permission status, and any ground-change notes.
  - Ensure alignment of plot-to-site relationships and maintain data provenance from field forms to GIS databases; maintain appendices and equipment logs for traceability.