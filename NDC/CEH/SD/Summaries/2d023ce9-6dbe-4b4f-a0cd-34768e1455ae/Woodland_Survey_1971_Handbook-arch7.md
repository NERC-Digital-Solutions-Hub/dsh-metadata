# NATIONAL WOODLANDS CLASSIFICATION 1971 HANDBOOK OF FIELD METHODS

- A detailed field manual for standardized woodland classification and data collection, focusing on map-based data products and spatially-referenced survey methods.

## What the document is for (GIS-relevant purpose)

- Defines procedures to generate geospatially usable data on woodlands, including:
  - Ground flora, tree saplings and shrubs, plot habitats, soil characteristics
  - Site description and habitat contexts for mapping and analysis
- Emphasizes consistent data collection, quality assurance, and repeatable methods suitable for GIS datasets.

## Survey planning and permissions (spatial data context)

- Prepare an outline survey plan to minimize travel and optimize base locations.
- Obtain access permissions for each site; follow tactful, public-relations-oriented engagement with landowners.
- If permission cannot be obtained, use backup sites with maps and sampling details supplied by Merlewood.
- Identify best entry points to minimize walking distances and avoid disturbing owners or fences.

## Spatial sampling framework

- Sites are located using 22" Ordnance Survey maps with pre-marked sampling points.
- Each site has 16 sampling points to be located on the ground; aim for an accuracy of within ~20 meters of the true point.
- A control point on the ground is used to orient the map; bearings are taken from control points to each sampling point, correcting for magnetic variation.
- Distance to sample points is measured from the control point using the map scale on the compass; then the point is paced out on the ground.
- The method prioritizes minimizing subjective bias in point location; strict adherence to predetermined paces and directions is required.

## Plot layout and quadrat system (data structure for GIS)

- Each sampling point becomes the centre of a nested plot system:
  - A central 2 x 2 m plot (4 m²) and progressively larger plots up to a 14.14 x 14.14 m plot (about 200 m²).
  - The four corner posts and distance strings delineate the plots; short pegs mark corners of each successive larger plot.
- Ground flora is recorded first to minimize disturbance; subsequent data (trees, saplings, shrubs, soil) follow.
- The sampling framework yields multi-scale presence/absence data and abundance estimates suitable for GIS layering.

## Data collection at each plot (data types and structure)

- For each sampling point, four data streams are collected (one per data sheet) plus soil samples:
  - Ground flora: presence/absence in five quadrat sizes and percent cover/abundance estimates for the largest plot; comprehensive bryophyte collection is optional for the full vascular plant survey.
  - Trees, saplings, and shrubs: species, diameter at breast height (DBH) for trees >5 cm; saplings and shrubs recorded in diagonally opposite quarters; tallest tree height measured.
  - Plot description and habitats: attribute presence/absence for defined habitat/landscape features; includes slope and aspect.
  - Soil data: small pit and auger sampling at plot centre; composite soil sample (top 10–15 cm) plus horizons interpretation (A, B, C) using a standardized form.
- Specimens:
  - Collect herbarium specimens for identified species (and type specimens where possible) and label with field codes for later verification.

## Site-wide data collection (GIS-ready site descriptors)

- Site Description and Habitats form: a separate, comprehensive form for each site capturing overall habitat context, management history, and landscape features.
- Data are organized to align with the plot-level forms, enabling GIS-based aggregation across the site.

## Soil data methodology (data model implications)

- Limited set of physical/chemical measurements chosen for large-scale data management:
  - pH, loss on ignition, mechanical analysis (sand/silt/clay distribution)
  - Optional future analyses on retained sub-samples
- Soil profiles are described using horizon-based interpretation (Ao, Al, A2, B1/B2, C); horizons are recorded with depth, color, texture, structure, moisture, and other attributes.
- Ground-truthing includes horizon boundaries, presence of organic layers, gleying, and underlying materials, with guidance for questionable profiles (diagrams recommended).

## Data standards, coding, and data quality

- Data are entered on standardized forms with defined attribute codes; “Code No” fields are reserved for office use to support data punching and consistency checks.
- The documentation emphasizes:
  - Consistency between plot-level and site-level forms
  - Logical consistency checks (e.g., if an attribute is present on a plot, it should appear on the site form)
  - Complete site coverage to avoid missing attributes
- Herbarium and specimen data linked to field forms to support later verification and data integrity.

## Data packaging, transport, and workflow (GIS data integration)

- At the end of fieldwork, forms and samples are gathered and packed:
  - Four site data sheets (plot and site) plus herbarium and soil samples organized into separate boxes
  - Pre-paid, pre-addressed shipment labels included; parcels sent promptly
  - Emphasis on thoroughness and completeness, even if it takes a bit longer in the field
- Equipment and forms are documented for reproducibility and auditability.

## Equipment and field administration

- Includes a full equipment set for marking plots, measuring, soil sampling, and specimen handling.
- Appendix items provide:
  - Instructions for herbarium specimen collection
  - Examples of completed forms
  - Checklists and forms for site and plot descriptions
  - Plant identification coding aids and storage guidelines

## Practical GIS outcomes and applications

- The methodology yields rich, multi-scale spatial data suitable for GIS:
  - Species presence/absence and abundance across nested quadrats
  - Tree/sapling/shrub measurements with spatially explicit plotting
  - Detailed site and habitat classifications mapped to plot locations
  - Soil horizon types and associated attributes mapped to plots
  - Site-level descriptions and marginal land/boundary features that enhance landscape-scale analysis
- The standardized protocol supports data sharing, archiving, and future re-analysis with consistent coding and documentation.

## Appendices and supplementary elements

- Appendices cover:
  - Herbarium collection procedures
  - Examples of completed plots and site forms
  - Soil data collection instructions and interpretation
  - Equipment checklists and data sheets
- The document provides concrete templates and codes to facilitate GIS-ready data capture and integrate with larger woodland classification datasets.