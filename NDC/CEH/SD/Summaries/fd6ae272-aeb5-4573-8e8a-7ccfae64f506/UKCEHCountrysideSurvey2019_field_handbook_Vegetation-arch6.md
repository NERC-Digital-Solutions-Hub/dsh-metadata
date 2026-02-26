# UK-SCAPE Field Survey Field Handbook 2019

- A field data collection guide for recording vegetation presence, abundance, and related plot metadata across two plot sizes (200 m2 vegetation plots and 4 m2 soil plots) within the UK-SCAPE framework.
- Data collection is designed to be repeatable over time to quantify vegetation change by habitat type and landscape location.

## Purpose and scope (data support perspective)

- Enables standardized data gathering for broad-scale vegetation change analysis.
- Supports data integration from multiple plots and survey rounds to enable dashboards, reports, and self-serve analysis.
- Emphasizes accurate relocation, traceability, and documentation of why plots are repeated, relocated, or not recorded.

## Data collection workflow

- Use ESRI Collector to navigate to plot locations and initiate data entry.
- Launch Survey123 forms to capture:
  - Plot header information (location, plot type, square, plot number, GPS ID, surveyors).
  - Plot-level details (relocation status, accuracy, notes, slope, aspect, shade, plot maps).
  - Vegetation data (three pages: header, plot-specific headers, and vegetation/soil data).
  - Nested species recording for each nest size within 200 m2 plots; 4 m2 plots recorded similarly but focused on smaller quadrats.
- For repeated plots, rely on a combination of GPS geopoints, plot maps, and photographs to relocate; record whether plots are Found, Not Found, or New (replacement or new feature).
- Capture photos for relocation and visual context; ensure photos include plot number/type and a distinctive nearby feature.

## Plot types and data structure

- 200 m2 X plots (VEGETATION) and 200 m2 X plots (SOIL) are nested:
  - Nest 0 to Nest 5 capture progressively larger areas; Nest 0 is the inner 1x1 m (for 200 m2 plots) and nests expand outward up to 14.14 x 14.14 m.
  - Species presence and abundance are recorded per nest with covers as percentages (nearest 5%) or “present.”
- 4 m2 X plots (SOIL) record species presence and covers within a 2x2 m quadrat.
- Plot header includes site name, plot type, plot number, plot ID, surveyors, slope, aspect, shade, and whether a plot map was drawn.
- Plot relocation details:
  - Location accuracy, geopoint capture (offline GPS possible), and notes on any disturbance or reasons for relocation uncertainty.
  - Rules guide when to mark a plot as Found vs Not Found and when to create a new plot.
- Habitat data:
  - Broad habitat, Priority Habitat (at plot and wider polygon), and tree disease indicators if applicable.
- Vegetation height:
  - Modal height estimates for canopy, shrub, and ground layers.
- Plot photos:
  - Two to three photos per plot, with directions to aid future relocation and context.
- Plot sketch maps:
  - Clear, measurement-based sketches with GPS reference points, north arrow, and labelled square/plot numbers.

## Species recording and data standards

- Species entry uses dropdowns with auto-type options; “Other” allows free text for unidentified species (to be updated later if identified).
- Aggregations/combinations are used for difficult-to-distinguish taxa to maintain consistency with prior surveys.
- Bryophytes and lichens:
  - Recorded only from the approved mosses and liverworts/lichen lists; high priority on total bryophyte cover and designated Sphagnum categories.
- 200 m2 plot nesting:
  - Nest 0 records all species in the innermost 2x2 m, with cumulative species added in Nest 1 and so on through Nest 5.
- 4 m2 plot nesting:
  - Species are recorded in a single nested quadrat structure with cumulative/cover data.
- Uprooting restrictions:
  - Do not uproot plants to identify them; use photos or notes when necessary to avoid altering species richness.

## Data quality, validation, and QA

- Software enforces required fields and prompts for missing data prior to submission.
- Cautions about blank or duplicate entries; users should review entries to minimize errors.
- Emphasis on consistent relocation and documentation to maximize comparability across survey rounds.
- Documentation of reasons for inaccessible or refused plots is required.

## Data capture tools and offline workflow

- Collector and Survey123 apps are core tools:
  - Collector handles map-based navigation and offline GPS data collection.
  - Survey123 provides structured data entry forms for plot headers, nest data, and species lists.
- Offline-first workflow:
  - Surveys can be saved as drafts or outbox while offline and submitted when online.
  - Auto-save features help recover data after device crashes.
- Data submission and versioning:
  - “Send Now” for online submission; “Copy to new survey” for resubmission or edits.
  - Drafts, Outbox, and Sent sections track survey status; “Favourite answers” can be saved for reuse.

## Metadata and data products

- Output data layers include:
  - Plot-level metadata (location, surveying team, habitat context, disturbance notes).
  - Nested species presence and cover data per plot and nest.
  - Habitat classifications (Broad and Priority habitats) and tree disease indicators when relevant.
  - Photo and sketch map attachments for plot relocation and context.
- Data products can be used to build dashboards and pivot tables to analyze vegetation change by habitat, landscape location, and time.

## Appendices and guidance highlights

- Appendix 1: COLLECTOR & SURVEY123 setup and usage guidelines (installing apps, map interaction, GPS accuracy, and troubleshooting).
- Appendix 2: Random numbers section (illustrative; supports methods used in documentation).
- Practical field tips:
  - Importance of accurate plot relocation and maintaining clear sketch maps.
  - Handling of plots across land-use changes (e.g., housing development or inaccessible areas).
  - Methods for marking and re-finding plots in upland, lowland, and aquatic contexts.
- Species lists and bryophyte guidance:
  - Prioritized moss and bryophyte taxa lists with recommended recording practice.
  - Aggregated taxa rules when species-level identification is not feasible.

## End-to-end takeaway for data support

- This handbook standardizes field data collection for vegetation plots to enable robust, longitudinal analyses across sites and time.
- Data support should focus on ensuring accurate data capture, consistent relocation, and accessible metadata to support downstream analytics, dashboards, and public data sharing.
- The data pipeline emphasizes offline-to-online workflows, documentation of plot status, and structured nesting of species data to maximize re-use and comparability.