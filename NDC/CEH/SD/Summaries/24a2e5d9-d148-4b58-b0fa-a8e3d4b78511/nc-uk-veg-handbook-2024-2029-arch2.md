# Vegetation plots

- Purpose: Use standardized data to monitor environmental condition over time by recording vegetation presence, abundance, and plot-level characteristics across a 1 km2 survey square. Data are designed for scrutiny of environmental health and policy performance, enabling long-term trend analysis.

- Data framework and tools:
  - Data are collected and managed using ESRI FieldMaps and Survey123 apps, with offline syncing and central database submission when online.
  - Plot data include header information, plot-specific headers, and vegetation species data, plus plot photos and sketch maps to aid relocation.

- Plot location and relaying concepts:
  - Repeated plots: Many plots have been surveyed previously (since 1978); relocation relies on GPS, sketch maps, and photos. If relocation fails, plots can be marked Not Found and replaced.
  - Plot markers (where present) include metal plates or wooden stakes to aid relocation; metal detectors are provided, but plates may have moved or buried over time.
  - Accuracy and decision-making: Some relocation error is acceptable in homogeneous habitats; otherwise, plots may be treated as not comparable if relocation is unreliable.

- Plot types and layout:
  - X plots (200 m2): Nested 14.14 x 14.14 m square with nests 0–5 for progressively larger sampling areas; focus on ground flora with nested, cumulative species recording. GPS is taken at the south corner. Randomly allocated within survey squares; new plots avoided in urban, unsafe, or restricted areas.
  - Linear plots: B (boundary), H (hedgerow), S (streamside), R (roadside); 10 x 1 m plots located near linear features, recorded in half of the squares (those first surveyed in 1978). Hedgerow plots have region-specific rules (dominant species in England; full rules in Scotland).
  - Placement rules consider dominant features, proximity to edges, and safety; linear plots align with previous X plots to maintain time-series continuity.

- Plot data capture: header and species data
  - Plot header (page 1): Square number, Plot Type (X, B, R, H, S), Plot Number, Plot ID (auto-generated), surveyors, slope, aspect, shade, plot map status, and notes.
  - Geopoints: Location captured via offline GPS if available; online maps provide visual accuracy checks; Location Averaging and multiple basemaps enhance precision.
  - Plot description: Recording whether a plot map exists, and notes on disturbances or loss, with photos linked to the plot.
  - Vegetation height: Estimates or measurements for canopy, shrub, and ground layers, plus photos.
  - Plot photo protocol: Two to three photos per plot showing the plot relative to a stable nearby feature to ease relocation; photos must include plot number/type automatically when taken in Survey123.
  - Plot sketch map protocol: Clear, measured sketches with a north arrow, reference features, and GPS coordinate marks; photos of maps when redrawn or edited.

- Recording X plots (Nest system)
  - Nest 0 (innermost 1x1 m area within the 4x4 m nest) through Nest 5 (outermost 14.14 m^2) are recorded sequentially with cumulative species lists.
  - For each nest, record presence/absence of species; for species appearing only in a nest beyond Nest 0, indicate “Not present in nest 0 (nest 1 only)” in nest 0’s cover field.
  - Total cover across all categories (vascular plants, bryophytes, litter, etc.) should approach 100%, with overstory layers allowed to push totals above 100% due to layering.
  - Species lists include autocompletion; unknowns can be entered as “Other” with a free-text note or photographed for later identification.
  - Bryophytes and lichens: recording is limited to a predefined list (mosses, lichens, liverworts) with guidance to avoid excessive taxonomic detail; Sphagnum categories are provided and can be recorded at a coarse level.
  - Aggregations/combinations: certain taxa may be recorded as combinations when species-level ID is uncertain; do not uproot plants for identification; photos are preferred for unknowns.

- Soil sampling and special headers
  - X plots and some linear plots include soil sampling with date, barcode scanning, and depth guidance; peat depth is recorded per protocol.

- Data submission and QA
  - Data can be submitted online via the central database; offline work is saved as Drafts or Outbox and can be re-edited and resubmitted; auto-save protects against data loss.
  - If a plot cannot be re-recorded in the same location, mark as Not Found or Not Appropriate; preferentially reuse oldest location to maximize the time between surveys.
  - Ensure all plots in a square are attempted, including those refused or inaccessible; provide reasons in notes to support downstream QA and analysis.

- Plot types in practice and adjustments
  - If a linear plot is inaccessible or has changed, record a near-location plot or move on to the next plot; the aim is to document environmental change, even when some plots are lost or heavily altered.
  - When X plots cross crop edges or water, adjust placement to minimize damage and maintain sampling integrity (e.g., keep 12 m from crop edge, follow tramlines when necessary).

- Appendices and tools
  - Appendix 1: FieldMaps & Survey123 setup, GPS usage, offline syncing, and common navigation tips.
  - Appendix 2: Random numbers between 0 and 1 (used for plot placement/randomization).
  - Contact information for UK Centre for Ecology & Hydrology (CEH) across Bangor, Edinburgh, Lancaster, and Wallingford headquarters.