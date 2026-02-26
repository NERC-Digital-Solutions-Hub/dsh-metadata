# CS Technical Report No.2/07 Vegetation Plots Handbook

## Overview
- Long-term, globally unique vegetation dataset documenting presence and abundance of plant species across varied plot types over time.
- Data are collected using forms-based VegPlots software, ArcMap GIS maps, and tablet-based data entry, with photos and paper maps as backups.
- Emphasizes repeatability (relocation of plots) and standardized data capture to enable trend analysis.

## Data collection and formats
- For each plot: header information (plot number, type, height, location), plot photos, and plot maps (paper and digital).
- Data are entered in VegPlots via a map-selected plot ID, with a nested structure of data entry (Headers, Listed Species, Selected Species, Admin, Notes).
- Data are stored on tablets; two tablets per team may be used (A and B) to avoid overwriting, with datasets named accordingly (e.g., VegetationPlotsA.mdb).

## Plot relocation and new plots
- Relocation relies on ArcMap plot maps and photos; precise GPS may be used as an aid but not for core relocation.
- If a plot cannot be relocated satisfactorily, it is recorded as Not Found or New Plot (Replacement or New feature/Land cover).
- New plots are added based on changes in land use, habitat, or newly surveyed squares; new plot numbers follow existing conventions (e.g., Y6 if prior Y plots existed).

## Plot types and layout (high-level)
- X plots: Large 200 m2 random samples with nested 1 m2 and 4 m2 subplots; several nests per plot.
- Y plots: Small 2 m x 2 m plots in habitats not well represented by other plots; may target Priority Habitats.
- U plots: Unenclosed Broad Habitats, 2 m x 2 m; up to 10 per square, allocated to habitat types by area proportion.
- A plots: Arable field margins along B plots; 100 x 1 m, up to 5 per square; record central 4x1 m and presence in nest 0/1.
- M plots: Margins associated with arable fields; 2 m x 2 m; measure margins beyond cross-compliance strips.
- H plots: Hedgerow plots; 10 x 1 m along hedges; relocated if hedge changes.
- D plots: Hedgerow diversity; 30 m long, 1 m width; detailed structural and ecological metrics.
- S/W plots: Streamside/waterside plots; 10 x 1 m along watercourses; record stream/river conditions and width.
- R/V plots: Roadside and verge plots; 10 x 1 m along roadsides/verges.
- A note: Each plot type has specific header fields and species recording rules; overall goal is consistent, comparable data across years.

## Data capture workflow
- Locate the plot position in ArcMap, then open VegPlots on the tablet to record the plot.
- Headers tab includes relocation status, plate presence, plot ID, and descriptive fields (slope, aspect, shade, photos, maps).
- Listed Species: capture presence and, where applicable, nested plots; use group tabs (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens) and identify up to 100 common species with options for unidentified specimens.
- Selected Species: accumulate identified species with estimated total cover percentages in 5% bands; avoid double counting when multiple layers exist.
- Admin: recorder initials, plot completion status, and validation state.
- Notes: free text for reasons plots were lost or not appropriate.
- Completing plots: regular saves, validation of missing fields, and exit only after validation.

## GPS logging and relocation
- Tablet GPS used as an aid for relocation; non-differential GPS is available but not relied upon for exact positioning.
- Surveyors stamp GPS coordinates on the ArcMap plot map during recording; plot labels show square, type, number, and ID.
- Prior locations (GPS or marker plates) guide relocation; for difficult sites, move decisions rely on map/photo evidence and expert judgment.

## Data validation and quality assurance
- VegPlots includes a Validate step highlighting missing fields (Header red, Missing Selected Species data circled).
- Regular saving and post-collection validation help ensure completeness before moving to the next plot or exiting.

## Photos and plot maps
- Take new photos of each plot location to aid relocation and illustrate vegetation changes over time.
- Photos should reference the plot number and type; back-of-photo aids are provided (weather writers) to label photos clearly.
- Plot maps must be clear and precise; if maps are edited or redrawn, edits must be clearly indicated on a sketch map with initials and date.

## Plot maps and map protocol
- Plot maps accompany data entry and must be either retained as printed maps or redrawn/edited with clear measurements and reference features.
- For new plots or re-positioned plots, sketch maps should define location with measured distances and bearings to nearby features; multiple plots can appear on a single map when co-located.

## Species and taxonomic considerations
- Aggregations/Combinations: certain taxa are combined when separation is difficult; use the most accurate designation available and the combination name otherwise.
- Bryophytes and Lichens: only listed bryophytes/lichens with individual covers are recorded; other bryophytes/lichens are not.
- Sphagna: detailed subcategories for various Sphagnum species included.
- Data options support self-consistency across partners; ensure cover estimates are cross-checked between int/ext teams.

## Administrative and end-of-survey notes
- The handbook emphasizes operational details (e.g., five-sector X plot placement, constraints on A plots near B plots, no plots within 10 m of Y plots, etc.).
- Aggregations ensure data compatibility with historical surveys while allowing new plot allocations and habitat representations.
- The document is released with permissions and disclaimers; usage rights and attribution to NERC are noted.

## Practical implications for Data Support
- Central role in enabling consistent data capture, storage, and retrieval across multiple plot types and years.
- Requires careful coordination between GIS mapping (ArcMap), field data collection (VegPlots), and tablet-based data management (A/B datasets).
- Strong emphasis on data quality, traceability (photos, maps, GPS), and explicit protocols for handling missing, moved, or new plots.
- Provides a structured framework for scalable data products (dashboards, reports) derived from standardized plot-level data and nested species data.