# CS Technical Report No.2/07: Vegetation Plots Handbook v1.0

- Aims and scope
  - Defines protocols for recording vegetation presence and cover in a range of plot types to support a long-term, globally unique dataset of vegetation change over time.
  - Combines field plotting with digital data capture (Vegplots) and GIS (ArcMap) for consistent, repeatable relocation and data entry.

- Data infrastructure and workflow
  - Spatial data core: ArcMap plot location maps and a Vegplots data capture system integrated with GIS.
  - Tablet-based data capture: Vegplots runs on tablets with digital plot photos downloaded to dedicated folders.
  - Data storage: Vegplots.mdb on tablets (named VegplotsA.mdb or VegplotsB.mdb when using two tablets); ArcMap-linked plot maps and photo repositories are stored under specified square folders (e.g., C:\CEH\<square>\Field_Data\VegPlots.mdb, New_Plot_Photos, 2007_plotmaps).
  - Plot maps and photos: Each plot location is supported by both map context and photographic evidence to aid relocation.

- Plot relocation, addition, and replacement
  - Relocation: Use ArcMap plot maps and photos to re-find previous plots; precise GPS positions may be uncertain, so relocation relies on landscape features and photos.
  - Not found and new plots: If relocation fails or land use changes, record as Not Found or New Plot (Replacement for unfound plot / New feature). New plots must be uniquely numbered within a square (e.g., Y6, U7).
  - ArcMap integration: New plots require saving in ArcMap (Stop Editing then Save) to register the plot for Vegplots entry.

- Plot types (purpose and layout)
  - X plots (Large, 200 m2; Wally plots): Random samples representing common vegetation; nested 4 m2 inner plots with additional nested 1 m2 and associated nests; 200 m2 square with 14.14 m sides.
  - Y plots (Small, 2 m x 2 m; targeted/habitat plots): Located in habitat patches or Priority Habitats not well represented by other plots.
  - U plots (Unenclosed, 2 m x 2 m): For unenclosed broad habitats; up to 10 per square; placed by proportion of unenclosed habitat within a square.
  - A plots (Arable field margins): 100 m x 1 m plots along arable field margins; up to 5 per square; used to monitor arable margin biodiversity.
  - M plots (Margins): 6 m wide margins beyond cross-compliance strips (often adjacent to hedges); up to 3 per field depending on margin width.
  - H plots (Hedgerow plots): Linear 10 m x 1 m plots along hedgerows; relocated to nearby hedgerows when necessary.
  - D plots (Hedgerow diversity): 30 m long plots on Woody Linear Features; assess woody diversity, gappiness, disturbance, and related features.
  - S/W plots (Streamside and Waterside): Linear plots along watercourses; S plots near water; W plots along watercourses; both 10 m x 1 m.
  - R/V plots (Roadside and Verge): Linear plots along roadsides and verges; 10 m x 1 m; roadside edge defined as the interface at the soil-tarmac boundary or edge of verge.
  - Other notes: Some plots combine features (e.g., R with boundary interactions) and have specific placement rules to avoid overlap.

- Plot marking and location conventions
  - Marker placement: Metal plates or wooden stakes used to mark plot centers or boundaries depending on land type; plates oriented to facilitate relocation.
  - Distances and alignment: Plots laid out along north/south and east/west axes when possible; specific rules exist for boundary features, hedgerows, and linear features.
  - Relocation ethics: If a feature is not accessible or changes, plots may be moved to the nearest permissible position with documentation.

- Data collection on Vegplots (field data entry)
  - Accessing a plot: Locate plot in ArcMap, then open VegPlots on the tablet to begin the Standard Recording screen for the relevant plot.
  - Header and metadata: Capture plot header information (plot type, square, plot number, GPS/location notes, photos, map status, slope, aspect, shade, etc.).
  - Plot relocation status: Record whether the plot is Found, Not Found, New Plot (replacement or new feature), Not Appropriate, etc.
  - Plate detection: Record whether a plate was detected; note if a plate is buried or absent.
  - Plot description: Record slope, aspect, shade, whether photos were taken, and whether the plot map was drawn/edited.
  - Vegetation height: Provide modal height estimates for canopy, shrub, and ground layers.
  - Admin and notes: Enter surveyor initials, plot completion status, and any explanatory notes (e.g., why a plot was lost).
  - Plot-specific header information: Data fields vary by plot type; only relevant fields are enabled per type.

- Species data collection and nesting (Nested plots)
  - Listed species: Tabs organized by species groups (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens, Crops, Unidentified).
  - Selection and identification: Mark present species; use A-C (common) and D-Z (unidentified) codes if needed for later identification; Mosses/Lichens limited to listed taxa.
  - Selected Species and nesting: Each species is recorded into nests corresponding to nested plots (e.g., nest 0, nest 1, etc.). Percent cover is entered in 5% increments, with total cover allowed to exceed 100% due to multiple layers; avoid double counting of overlapping parts.
  - Data validation: Use Save regularly; Validate to highlight missing fields; ensure cover estimates are consistent between partners.

- Plot photos and plot maps
  - Plot relocation photos: Take reference photos to aid relocation in subsequent surveys; include clear reference points; ensure plot number and type are visible.
  - Plot maps: Clear, precise maps drawn for each plot; if a map is edited or redrawn, indicate edits on the map with initials and date; keep a paper sketch when needed.
  - Photo workflow: Download photos to a central folder on the tablet after each survey period to avoid overloading memory; delete from camera as needed.

- Data quality, standards, and reporting
  - Consistency across surveys: Emphasis on repeatability and comparability of plots over time; careful handling of relocated or replaced plots to minimize bias.
  - Aggregations and combinations: Some taxa are recorded as combinations when separation is difficult; use validated species names when possible.
  - Bryophytes, Lichens, and Sphagna: Limited to listed taxa with specific, predefined categories; standardized classifications provided in the manual.
  - Documentation and training: Specific training material and protocols accompany the manual to ensure consistent application in the field and on devices.

- Practical considerations and governance
  - Data challenges acknowledged: Data distributed across multiple locations, varying resolutions, and evolving standards; emphasis on data cleaning, transformation, and provenance.
  - Roles and collaboration: GIS specialists collaborate with field surveyors to ensure accurate spatial data and robust, map-based data products.
  - Compliance and reuse: The handbook provides guidelines for data sharing and reuse within the Countryside Survey framework and associated organizations.

- Access, references, and contact
  - Publication and rights: NERC copyright with open reproduction for research and internal organizational use; attribution required.
  - Project context: Countryside Survey 2007, funded by NERC-led partnership with Defra and other agencies; emphasis on long-term data continuity.

- Summary takeaway for GIS specialists
  - The Vegetation Plots Handbook defines a GIS-centric workflow for capturing, storing, and updating a large, longitudinal vegetation dataset.
  - It integrates ArcMap plot maps with a tablet-based Vegplots data entry system, linking precise spatial locations, plot types, nesting schemes, and species data.
  - It provides explicit protocols for relocation, plot creation, and data quality control, ensuring consistent, repeatable map-based data products across years.