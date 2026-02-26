# GLASTIR MONITORING & EVALUATION PROGRAMME VEGETATION AND SOIL FIELD HANDBOOK

- Purpose and scope
  - Field handbook for recording vegetation and soil data to quantify Glastir scheme impacts on Welsh habitats over time.
  - Uses a fixed 1 km square grid with repeatable plots to enable landscape-scale change detection.
  - Emphasizes map-based data products, GIS integration, and time-series consistency.

- GIS, data models, and workflow
  - Core GIS tools: ArcMap-based VegPlots (VegPlotsWelsh.mxd) and VegPlots database (VegPlots.mdb) linked to a 1 km square plot layer.
  - Plot records are created in ArcMap (as points) and then populated in VegPlots through a Standard Recording form; each plot has Square, Plot Type, Plot Number, and Plot ID ( Square+Type+Number ).
  - Data capture includes header information, plot photos, sketch maps, and nested species entries; data validated before saving.
  - Mapping and plot locations are designed for repeatability: precise GPS stamping (Trimble differential GPS preferred), sketch maps, and photographs to aid re-finding.
  - Landscape photography protocol supports spatial analysis of enclosure, openness, texture, and visibility from rights of way.

- Plot types and allocation (GIS-driven sampling design)
  - Areal plots (A), Linear plots (B), Arable margins (A), Margin plots (M), Hedgerows and hedgerow diversity (H, D), Unenclosed plots (U), X/Y/U/B/H/D/S/W/P plotting framework.
  - Plot allocation is proportional and GIS-guided, using the Plot Calculator to determine numbers in-option vs out-of-option for Glastir groups based on habitat area and linear feature lengths.
  - Random placement within habitat types and along linear features to ensure representative sampling; X plots (random points) seed other plot types (B, A, S/W, H, D, P, etc.) as projections or adjustments.
  - Special handling for Countryside Survey squares in 2016 (repeat visits to extend the time series).
  - Five X plots per square (random points marking main plots) used to project other plots; pro rata distribution to fit available plot-able land.

- Data collection and integrity
  - VegPlots application workflow
    - After locating/creating a plot in ArcMap, the VegPlots app opens the Standard Recording screen for data entry.
    - Key fields: Select Plot ID, Nest (for nested plots), Square, Plot Type, Plot Number, and Plot ID; then proceed with Headers, Listed Species, Selected Species, and validation.
    - Collation of species data uses multiple groups (Common, Grasses, Sedges/Rushes, Ferns, Forbs/Woody, Mosses/Lichens) with capability to record unidentified species (A-C and D-Z).
    - Completion involves Save, Validate, and Exit; plots may be found, not found, replaced, or deemed Not Appropriate; relocation or new plot creation is tracked.
  - Plot relocation and repeat surveys
    - Plots are re-found using a combination of ArcMap maps, sketch maps, GPS stamps, and photos; if not found or land access changes, new plots may be created or the plot marked Not Found/Replacement.
    - For Counctryside Survey squares, repeat visits require careful documentation of previous positions and possible relocation errors.
  - Plot sketch maps and plot photos
    - Clear, accurate sketch maps with reference features and GPS coordinates are essential for re-finding.
    - Photos (2–3 per plot; orientation cues with marked back-of-photo labels) document plot context and aid relocation.
  - Data quality and QA
    - Validation highlights missing fields; red flags in headers and species entries trigger QA follow-up.
    - Mapping edits and redrawing are allowed to reflect landscape changes; GPS snapping can improve repeatability.

- GPS, equipment, and field logistics (GIS-enabled data capture)
  - GPS stamping
    - Use differential Trimble GPS where possible; stamp location from the south corner (X plots) or appropriate boundary corner (B, boundary plots) with correct offsets.
    - Snapping tools available to align plotted points precisely with GPS positions.
  - Coordinated data capture
    - Tables, nests, and plots are organized to support cross-survey comparability; landscape photography is aligned with X-plot centers for consistent viewpoints.
  - Centre and alignment
    - Centre map on the square when opening VegPlots for the first time; ensure consistent orientation and alignment across surveys.

- Vegetation sampling details (GIS-relevant capture)
  - Nested species recording by plot type
    - X plots in woodland use nested structure with multiple nests; non-woodland X plots use 4 m2 standard with total cover across nests.
    - Y plots focus on enclosed habitats and Priority Habitats (PH); U plots cover unenclosed habitats; A plots sample arable margins; M plots sample margins; H, D, S/W, P plots capture hedgerows, diversity, streamside, and perpendicular relationships.
  - Species data and cover
    - Selected Species tab lists species by nest; estimated total cover and nest-specific cover bands (1%, 5%, etc.) are recorded; avoid double counting and overestimation.
  - Bryophytes and lichens
    - Limited to specified lists; priority given to vascular plants, with bryophyte and lichen entries constrained to the recommended taxa.

- Soil sampling and ancillary data (X plots)
  - Soil cores and Gouge auger samples collected at specified offsets from the X plot center for chemistry, physics, biology (DNA), and fauna analyses.
  - Sample handling, labeling, storage, and mail-out protocols are specified to maintain sample integrity.

- Additional notes and guidance
  - Plot Calculator and allocation notes (Additional Note 4)
    - Focus on one option group at a time; enter % plot-able land and length estimates for linear features; use these to calculate required plots in and out of option land.
    - Handling mosaics, unenclosed vs enclosed habitats, and the interplay with X plots to minimize over-sampling.
  - Landscape photography methodology
    - Four quadrant-centre X plots selected for landscape photos; include cardinal bearings, orientation, and panoramic possibilities if available.

- Key considerations for GIS specialists
  - Maintain a linked data workflow between ArcMap (VegPlotsWelsh.mxd) and VegPlots.mdb; ensure plot IDs are consistent across systems.
  - Ensure repeatability by capturing precise GPS positions, thorough sketch maps, and robust photo documentation.
  - Use the Plot Calculator as the authoritative tool for determining plot numbers in each option group, reflecting habitat maps and linear feature analyses.
  - Manage data quality through regular validation, map edits/redraws, and clear relocation procedures for repeat surveys.
  - Integrate landscape photography and fixed-point imagery into GIS-based landscape analyses to describe enclosure, openness, and habitat texture over time.