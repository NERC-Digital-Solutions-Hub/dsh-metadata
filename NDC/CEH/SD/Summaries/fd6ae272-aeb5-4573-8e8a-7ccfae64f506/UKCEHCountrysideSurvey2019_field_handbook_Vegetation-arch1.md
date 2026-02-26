# UK-SCAPE Field Survey Field Handbook 2019

- A field handbook detailing the UK-SCAPE vegetation plots survey protocol, emphasizing repeatability, data capture via ESRI Collector and Survey123, plot types and nesting, species recording, relocation procedures, and data submission.

## Purpose, scope, and data objectives

- Record plant species presence and abundance across two plot sizes to quantify vegetation change by habitat type and location.
- Maintain a valuable long-term dataset through repeatable relocation, header data, photos, and sketch maps.
- Structure data for analysis, reporting correlations, and monitoring habitat changes over time.

## Data model and structure

- Core entities:
  - Plot: header information (square, plot type, number, ID), location, surveyors, slope, aspect, and relocation status.
  - Nest: nested quadrats within a plot (Nest 0 to Nest 5 for 200 m² plots; 4 m² nest for soil plots).
  - Species observations: presence/absence and % cover (or present) per nest; includes vascular plants, bryophytes, and lichens as applicable.
- Plot types:
  - VEGETATION SQUARES: 200 m² areal plots with nested quadrats.
  - SOIL SQUARES: 4 m² nested in the same plots for soil flora.
- Nested sampling protocol:
  - 200 m² X plots (VEGETATION) use Nest 0 (innermost) through Nest 5 (outer), with cumulative species lists by nest.
  - 4 m² X plots (SOIL) record species within the 4 m² nest (Nest 1 includes Nest 0 data; total cover per species is recorded).
- Data capture fields include cover, presence/absence, and notes for late identifications or taxonomic aggregations.

## Plot location, relocation, and sampling design

- Repeated plots:
  - Use GPS, plot maps, photographs, and plot markers (metal plates or wooden stakes) to relocate exactly; if not found, mark as Not Found and consider a new plot or replacement.
  - Relocation accuracy is allowed within reasonable error margins; sometimes a change in habitat type means data cannot be treated as a repeat.
- New plots:
  - Randomly allocated X plots within squares, avoiding urban, inaccessible, or unsafe land; five-sector stratification guides new placements when limited land exists.
  - If land becomes accessible where previously refused, prioritize repeating old plots before adding new ones.
- Plot relocation rules:
  - Record land access permissions, broad/priority habitat assignments, and disease signs where relevant.
  - Provide slope, aspect, shade, plot map status, and notes on disturbances or non-recordable plots.

## Data entry tools and workflow

- ESRI Collector and Survey123:
  - Collector navigates to a plot; clicking a plot opens Survey123 data forms for entry.
  - Do not edit a plot via Collector if it already exists; edit via the Survey123 workflow.
  - After completing a form, data can be sent online (Send Now) or saved offline (Drafts/Outbox) and resubmitted later.
  - Auto-save features preserve work if a device crashes.
- Plot creation flow:
  - For new plots, launch forms from My Surveys in Survey123; begin with general header information, then move through plot-specific headers and vegetative data.
- Location accuracy and geopoint capture:
  - Geopoints can be captured via on-device GPS or full-screen map; Location Averaging can be used for reliability.
  - Distance and bearing measurements are recorded with reference features; GPS accuracy is shown in the app.
- Data submission and traceability:
  - Submissions are tied to a central database; resubmissions require copying to a new survey and including notes about the corrected version.
  - Offline work is preserved in Drafts/Outbox and can be synced when online.

## Plot types and layout details

- X plots (3 types):
  - VEGETATION SQUARES: 200 m² plot with five nested subplots for sequentially larger areas.
  - SOIL SQUARES: 4 m² nested within the 200 m² plot for soil vegetation sampling.
- 200 m² X plot layout:
  - Diagonals marked with survey poles; nests are color-coded along the diagonals.
  - Nest 0 is the innermost 1 m²; Nest 1 corresponds to the 2×2 m inner area; nests 2–5 expand to encompass the full 14.14 m square (200 m²).
  - Nest 0 data recorded first, then successive nests; total coverage targets ~100% per nest, with additional categories (litter, wood, rock, bare ground, water, bryophytes) included.
- 4 m² X plot layout:
  - Oriented along north–south or east–west axes; anchored from the south corner; in arable fields, sample within the crop away from edges to minimize disturbance.
- Plot center coordinates:
  - For 200 m² plots, GPS reading is taken at the south corner; 4 m² plots have no center post, and measurements are anchored to the south corner.

## Plot data content and protocols

- Plot header information (Page 1):
  - Square, Plot Type (X or XX), Plot Number, Plot ID, surveyors, and relocation status.
  - Location can be auto-filled via offline GPS; map-based accuracy is shown to guide placement.
- Plot relocation and notes:
  - Plot Recorded options include Found, Not Found, New Plot, Not appropriate, Access Denied, Too Dangerous.
  - Notes should capture reasons for relocation decisions, including disturbances or land-use changes.
- Plot photos protocol:
  - Two to three photos per plot to aid relocation; photos should depict the plot relative to a stable nearby feature and include plot number/type information on the back.
- Plot sketch map protocol:
  - Drawn with measured distances, compass bearings, and a north arrow; mark GPS reference point; maps should be transferrable or photographed.
  - If a map is edited/redrawn, indicate edits with pencil marks and initials/date or note redrawn status.
- Plot header page 2 (Plot-specific headers):
  - Additional fields relevant to X plots and soils are captured; soil sampling details are guided by separate handbooks.
- Entering species (Page 3):
  - Nested nest approach for X plots; species lists are accessible via dropdowns with full taxon lists; use "Other" for unidentified taxa and replace with correct names later.
  - Recording strategy emphasizes total vascular plant cover plus six extra categories (litter, wood, rock, bare ground, water, bryophytes); total cover should sum to ~100% or more if layered.
  - For soil plots, species presence is recorded within the 4 m² nest with similar cover estimation.
- Aggregations/Combinations (Section 4.1):
  - Record at species level when possible; use aggregated taxa only when species cannot be confidently separated (e.g., Cardamine hirsuta/flexuosa) to maintain consistency with prior surveys.
  - Avoid uprooting invasive species; use photos for subsequent identification rather than disturbance.

## Bryophytes, lichens, and Sphagna guidance

- Bryophyte and lichen data scope:
  - Record only bryophytes and lichens listed in section 7.2.1 (mosses) and in Vegplots lists; no other bryophytes/lichens are recorded.
- Sphagna (Sphagnum) categories:
  - Green/fat and green/thin; red/fat and red/thin forms are listed with specific species associations.
  - The protocol allows recording at the aggregated level for practical data collection, with taxonomic detail kept optional for efficiency.

- Mosses to record (4 m² nests where possible):
  - A prioritized list of common moss species is provided, with recommended comparisons to similar taxa; emphasis remains on vascular plants and total bryophyte cover, with mosses specifically targeted.

## Data quality, management, and accessibility

- Data quality:
  - Emphasis on repeatability, clear relocation evidence, accurate GPS/location, and robust plot maps/photos to minimize red herrings and ensure comparability across surveys.
  - QA steps include ensuring all plots are accounted for, with notes explaining any refusals or non-recordable plots.
- Data management and discoverability:
  - Datasets are tracked with metadata; plots and observations are designed to be discoverable and usable over time.
  - Appendices provide practical guidance on data collection tools, app usage, and data handling workflows.

## Tools, appendices, and resources

- Appendix 1 - COLLECTOR & SURVEY123:
  - Installation, navigation, map usage, data collection workflow, GPS accuracy notes, and FAQ (GPS timing, accuracy indicators, offline/online modes, map gallery, and survey management).
  - Detailed guidance on using the Collector map, My Surveys, and the Survey123 forms for data entry and submission.
- Appendix 2 - Random numbers:
  - Generated 0–1 random numbers used for sampling and plot placement workflows.
- General contacts and institutional context:
  - The handbook is produced by Lancaster Environment Centre, CEH Bangor/Edinburgh, and Environment Centre Wales, with addresses and contact details for further support.

## End notes

- The handbook provides a comprehensive, field-ready framework for collecting, organizing, validating, and submitting vegetation plot data, with a strong emphasis on repeatable relocation, nested sampling, standardized species recording, and digital data capture workflows to support robust ecological analyses.