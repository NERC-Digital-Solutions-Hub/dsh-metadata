# UKCEH Countryside Survey: Field Handbook 2024-2029

- Purpose: Systematic vegetation plots to quantify countryside changes with high spatial precision, linking habitat type and landscape location to vegetation composition over time.
- Data focus: Presence/abundance of plant species across plot sizes, with repeat recordings to detect change. Emphasis on robust relocation data and metadata to enable near-perfect re-finding in future surveys.

## Key data collection workflow

- Tools: ESRI FieldMaps for plot navigation and Survey123 for data entry; offline syncing encouraged; paper plot maps provided as backups.
- Plot entry sequence: 
  - Open plot via FieldMaps, launch Survey123 for the plot data (header on page 1, plot-specific header on page 2, vegetation data on page 3).
  - For new plots, use My Surveys → Collect; for repeats, use existing plot context and decide if Found, Not Found, or New Plot (replacement/new feature).
- Relocation data: Each plot requires a square/plot ID, GPS coordinates, a sketch map, and photographs to aid re-finding; markers (where present) may be buried or moved and are used to confirm relocation.
- Data submission: Online submission possible via Send Now; offline drafting saved in Drafts/Outbox; auto-save supports recovery after crashes.

## Plot types and placement

- X plots (200 m2): Randomly allocated within squares; nested recording from Nest 0 (innermost) to Nest 5 (outermost) with increasing nest sizes; targeted for non-linear features; species are recorded cumulatively across nests.
- Linear plots (B, H, S, R):
  - B: Boundary plots along field boundaries (10 x 1 m), positioned 1 m from the dominant vertical feature.
  - H: Hedgerow plots (England: dominant species only; Wales/Scotland: full protocol); 10 x 1 m along hedge centerline with 1 m extension into adjacent land.
  - S: Streamside plots along watercourses; 10 x 1 m with attention to bank/water edge and flood status.
  - R: Roadside plots along roads/tracks; 10 x 1 m with roadside edge defined at soil/berm interface.
- Accessibility: If linear plots are inaccessible or disappeared, attempt approximate location; if not possible, proceed to next plot (no replacement plots across the square this year).

## Plot location, relocation, and verification

- X plot location: Use random points; if crossing a feature, relocate to vegetated land with minimum 12 m distance from edge; in arable fields, move to avoid trampling damage and crop disturbance.
- Re-finding: Precise GPS point, sketch map, and photos together determine re-finding accuracy; a degree of relocation error is allowed if vegetation is homogeneous and habitat type remains the same.
- Plot not found: Mark as Not Found and create a New Plot (Replacement) only if relocation evidence supports it; otherwise, treat as Not Appropriate (land use changed or access denied).
- Plot maps: If existing maps are inadequate or landscape changed, edit or redraw and document edits on the sketch map.

## Plot header and positioning data

- Plot identification: Square, Plot Type (X, B, R, H, S), Plot Number, Plot ID (auto-generated: Square + Plot Type + Plot Number).
- Positioning data: Geopoint captured automatically (offline GPS preferred); accuracy indicated via the Location button/map. Location averaging can be used for reliable coordinates.
- Land access and disturbance: Notes field to record disturbances (e.g., mowing, burning, access denial).

## Plot description and site characteristics

- Landform and habitat descriptors: 
  - Slope, Aspect, Shade
  - Plot Map drawn? (Yes/No/Edited/Redrawn)
  - Habitat details and disturbance notes
- Vegetation height (modal) estimates at three levels:
  - Canopy: None / 3-5 m / 5-10 m / >10 m
  - Shrub: None / 0-5 cm / 5-15 cm / 15-40 cm / 40 cm-1 m / 1-3 m / 3-5 m / >5 m
  - Ground: None / 0-7 cm / 7-15 cm / 15-40 cm / 40 cm-1 m / >1 m
- Photos: Two to three photos per plot, with direction noted on the sketch map; photos should reference a nearby, relatively stable feature.

## Nested vegetation recording for X plots

- Nest structure: Nested 1 m2, 2 m2, 4 m2, 7 m2, 14.14 m2, and ultimately 14.14 x 14.14 m (200 m2) outer nest; each nest records species presence and percent cover; overlap with higher nests builds cumulative data.
- Nest entries:
  - Nest 0: Inner 1 m2 area; list species and provide presence and total cover estimates, including additional components (litter, rock, bare ground, etc.) to total ~100%.
  - Nest 1–Nest 5: Add species not in previous nests; species from Nest 0 may appear in Nest 1; if not present, specify “Not present in nest 0 (nest 1 only).”
- Data integrity: Summaries of species listed and total covers are provided; monitoring for blank or duplicate entries is advised.

## Species data and taxonomic guidance

- Species lists: Comprehensive drop-down lists with autotype support for easier entry; avoid uprooting invasive species; if uncertain, use photo or “Other” with a free-text entry or unknown species entry.
- Taxonomic aggregations: Certain difficult-to-separate taxa should be aggregated to maintain consistency with past surveys; use listed combinations when true species ID is not unequivocal.
- Bryophytes and lichens: Recording limited to listed mosses and specified bryophyte/lichen groups; total bryophyte cover prioritized, with specific moss list provided for England/Scotland/Wales as applicable.
- Sphagnum categories: Green/fat, green/thin, red/fat, red/thin; can record at species level but aggregation is acceptable to expedite analysis.

## Data management, quality, and sharing

- Data provenance: Track data sources, maintain metadata, and upload created datasets to portals to ensure discoverability and reuse.
- Data quality considerations: 
  - Ensure full plot data entry (header, plot specifics, vegetation) before submission.
  - Record plots that are refused, inaccessible, or not appropriate, with reasons in notes.
  - Avoid removing invasive species to preserve ability to detect changes; photos are preferred for identification.
- Appendices and tools:
  - Appendix 1: FieldMaps & Survey123 generic notes (installation, app architecture, GPS accuracy, map navigation, data collection workflows, offline usage).
  - Appendix 2: Random numbers between 0 and 1 (likely used for plot randomization seeds or similar QA/stratification tasks).

## Practical considerations for analysts

- Data structure and lineage: Each plot has a clear ID, location, and nested vegetation data; X plots provide multi-scale vegetation detail; linear plots capture habitat-edge dynamics across years.
- Repeatability and replication: Emphasis on repeatable relocation (photos, GPS, sketch maps) to facilitate long time-series analysis.
- Handling gaps: Protocols exist for new plots, replacements, and when access is denied; documentation of reasons supports robust downstream analyses.
- Metadata richness: Header fields, soil sampling info for X plots, and detailed scoping for each plot type support robust modeling and correlation analyses across years and habitats.