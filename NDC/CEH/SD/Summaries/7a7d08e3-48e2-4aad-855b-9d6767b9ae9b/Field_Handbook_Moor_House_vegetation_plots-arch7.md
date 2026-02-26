# MOOR HOUSE VEGETATION RE-SURVEY 2008

- A field manual adapted from the Countryside Survey 2007 Vegetation Plots describing how to record plant species presence and abundance in 2x2 m plots, with data captured digitally via Vegplots and GIS-backed ArcMap mapping.

## Purpose and scope
- Capture plot-level vegetation data (presence, abundance, and cover) plus descriptive and locational metadata for each 2x2 m plot.
- Produce map-based outputs and datasets suitable for GIS analyses and sharing with policy colleagues, clients, or the public.
- Include plot photos, peat depth, vegetation height, and detailed species lists (with handling for unidentified taxa).

## GIS workflow and data model
- Spatial planning and localization:
  - Plot locations are mapped within the Troutbeck Catchment; a summary location map is accessible on tablets via an ArcMap document.
  - Precise plot positions derived from handheld GPS, tablet GPS, and relative distances (approx. 100 m between plots) with bearings when possible.
- Data capture platform and integration:
  - Vegplots software used on tablets, integrated with an ArcMap plot map; data entry tied to a selected ArcMap plot.
  - Data uploaded to network folders on a weekly basis; a dedicated workflow to distinguish data collected on different tablets (A or B) if multiple devices are used.
- Plot identifiers:
  - Transect, Plot Type (U = 2x2 m), Plot Number, and Plot ID (constructed from Transect + Plot Type + Plot Number).
- Plot types:
  - U plots (un-enclosed 2x2 m) with explicit layout orientation; standard data fields for most plots; U plots omit header-specific fields.

## Data capture structure and fields

- Header: Plot description
  - Slope (Flat, Slight, Moderate, Steep)
  - Aspect (None, N, NE, E, SE, S, SW, W, NW)
  - Location type (e.g., Open moorland, eroding area, sloping grassland, gully, valley bottom grassland, industrial/other)
  - Peat Depth (cm; measured after vegetation assessment)
  - Photos taken? (Yes/No; with protocol to ensure identifying plot location)
- Vegetation height
  - Height estimates at three points (e.g., North Corner, South Corner, Plot Centre), using defined height classes (e.g., 0–5 cm up to >1 m)
- Admin
  - Surveyors’ initials (with auto-fill from saved names)
  - Plot Completed? (Complete, Complete with validation errors, Incomplete)
- Notes
  - Free text notes (max 250 characters)
  - Date of Survey and altitude (GPS-derived)
- Listed species
  - Species lists across groups (Common species, Grasses, Sedges/Rushes, Ferns, Forbs/Woody species, Mosses/Lichens, Crops, Unidentified)
  - Up to 100 common species listed; other groups provide comprehensive lists
  - If immediate identification isn’t possible, record as species A–C (Common) and D–Z (Unidentified) for later identification
- Selected species
  - As species are selected, entries accumulate in a plot-specific species/nest list
  - Estimated total cover entered using 1% then 5% categories; redirection to the correct 5% category from a dropdown
  - All rows can be deleted via a Delete function; cross-check cover estimates between partners to avoid bias or double counting
  - Include trees/shrubs with overhanging canopies if they project over the plot
  - Bare ground excludes leaf litter and rock; all vascular plants plus restricted bryophytes/lichens (as listed)
- Aggregations/Combinations
  - Certain taxa are amalgamated when difficult to separate; use combination names (e.g., Cardamine hirsuta/flexuosa) per BRC list when separated IDs are not unequivocal
- Bryophytes and Lichens; Sphagna
  - Only taxa listed in the protocol recorded; others excluded
  - Sphagnum categories provided (Green/Thin and Red/Fat) with sub-classifications and representative species listed
- Data quality and validation
  - Regular saving; validation highlights missing fields (Header in red; Selected Species with exclamation in red)
  - Validation required before exiting or changing plots

## Plot completion, photos, and media

- Plot photo protocol
  - Take new photos for each plot to aid re-location; two photos recommended (one facing north, one south)
  - Use a weather writer label to indicate plot number/type; avoid glare and excessive sky
  - Photos reviewed immediately; retake if inadequate; download weekly to network folder
- Plot photo storage
  - Photos stored at a network path: S:\ECOPRO\Moorhouse Veg Resurvey 2008\Completed Data\Plot Photos
- U plots (un-enclosed)
  - Laying out 2x2 m plots with folding rules; poles oriented NS/EW
  - All species recorded from the 2 m2 quadrat; use standard species lists and 5% cover bands

## Data management, backups, and delivery

- Data backups and saves
  - Regular saving and backups via Vegplots; use Backup Current Data feature
  - Paper-recorded plots should be entered into the tablet as soon as possible
- Weekly data transfer
  - Move plot photos weekly to the designated network folder
  - Transfer field data weekly to the completed data server directory; create a dated folder (e.g., 150708)
  - Use Complete Square for Upload to Wiki to generate a zip file (sqcompleted_0001.zip) on the USB stick; copy to the dated folder
  - If two tablets were used, ensure data partitioning is distinguishable
- Outputs and references
  - Data are formatted for GIS integration (Vegplots outputs and ArcMap map layers) and uploaded to a wiki repository
  - Taxonomic references include BRC lists and select Sphagnum taxa classifications

## Equipment and field logistics (GIS-focused relevance)

- Field tools
  - Tablet with modified Vegplots software; GPS devices (handheld and tablet), digital cameras
  - 2 m quadrats and depth poles; folding rulers; diameters and measurement devices
  - Weatherwriter labels for plot photos; waterproof notes, gloves, protective gear
- Data infrastructure
  - Network storage paths for plot data and plot photos
  - Predefined folder structures for organized GIS-ready data delivery

## Appendix: Taxon lists and classification notes

- Detailed taxon groupings and combinations (e.g., Bryophytes, Lichens, Sphagnum species) provided for consistent, GIS-ready recording
- Emphasis on standardized abbreviations and nested species lists to support reproducible GIS datasets