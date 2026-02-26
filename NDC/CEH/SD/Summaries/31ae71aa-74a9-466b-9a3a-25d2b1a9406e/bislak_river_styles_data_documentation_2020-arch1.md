# The data submitted here are used in the Bislak River Styles Report and paper, 'River Styles and stream power analysis reveal the diversity of fluvial morphology in a Philippine tropical catchment'

## Overview
- Data were submitted to support the Bislak River Styles Report and the associated paper.
- Initial analyses occurred March–October 2020; methods are described in Section 2.
- Analyses and data gathering were led by Tolentino, Perez, and Guardian; River Style classification reviewed by all authors.

## Data products and how they were produced

- Segment-stream power shapefiles and spreadsheets
  - Tooling: TopoToolbox V2 used to extract the stream network and calculate catchment areas via standard flow-routing algorithms.
  - Channel selection: debris-flow–dominated to alluvial transition identified with a 1 km² upstream-area threshold; only alluvial channels (>1 km²) used for analysis.
  - Data cleaning: non-parametric quantile regression to remove artefacts; quantile carving along the central tendency (τ = 0.5) to enforce downstream-decreasing elevations.
  - Segment definition: slope values averaged over 0.2 km segments (n = 1129).
  - Outputs: for each segment, mean elevation, mean slope, and median catchment area; results exported to a stream network shapefile with stream power attributes and CSVs of stream power by River Style.
  - Power formulation: Ω (unit total stream power) calculated using the relationship Ω = 0.44 χ A S, where χ is a dimensionless coefficient, A is catchment area, and S is slope.

- River Style identification shapefiles
  - Framework: Stage One of the River Styles Framework used to identify river types across the Bislak Catchment.
  - Criteria: confinement (channel position in valley bottom), channel planform, geomorphic unit assemblage, and bed material texture.
  - Process: imagery interpretation (Google Earth) at reach scales, ground-truthing in the field, and expert judgement for final River Style delineation.
  - Outputs: shapefiles polygon for landscape units (lowland, upland, hills, catchment) and polylines for isohyet and river styles.

- Supporting documentation for spreadsheets
  - A comprehensive set of CSV files corresponding to various River Styles (e.g., Confined Floodplain Pockets, Confined Gorges, Confined Steep Headwaters, Laterally Unconfined Braided, Laterally Unconfined Deltaic, Partly Confined Bedrock, Partly Confined Planform with different Sin values, etc.).
  - Descriptions indicate detailed metadata per river style, with headers and identifiers (e.g., FID, X/Y coordinates, Strahler/Shreve orders, area, upstream area, distance to outlet, slope, chi values, ksn, flow accumulation, and Stream Power).
  - Additional files provide segment-level attributes and references to River Style name, coordinates, and segment identifiers.

- Additional segment and format details
  - Form_Wandering.csv and Segment_River_Styles_Figure_6a.cs v files capture dataset structure and column headers for mapping River Styles to segment-level attributes.
  - Bislak_200 m_segment.csv and Bislak_50 m_segment.csv include stream power, coordinates, order metrics, area, distance from outlet, slope, concavity-adjusted indices (chi with 0.45 and 0.79), Stream Power metrics, and area metrics at different segmentation scales.
  - The datasets include both Strahler and Shreve stream orders, various flow-accumulation metrics, and multiple representations of river style identifiers.

- References to file naming conventions
  - File naming encodes river style type, measurement scale (e.g., 200 m, 50 m), and segment-level attributes (e.g., x, y, z, chi, ksn, stream_pow).

## Methods and validation

- Computational workflow
  - TopoToolbox v2 for network extraction and catchment delineation.
  - Threshold-based segmentation to focus on alluvial channels.
  - Data cleaning and smoothing via quantile regression to mitigate data artefacts.
  - Validation of river-network location against Google Earth imagery.
  - River Style classification relies on expert judgement grounded in established River Styles framework procedures.

- Key considerations
  - The River Styles classification depends on expert interpretation due to the multitude of criteria considered.
  - Data are structured to support cross-comparison of river styles and associated morphodynamic metrics across the catchment.

## References
- Brierley GJ, Fryirs KA (2005) Geomorphology and river management: applications of the river styles framework.
- Fryirs K, Brierley G (2018) What's in a name? River Styles naming conventions.
- Khan S, Fryirs KA (2020) Delineation of valley-bottom segments using coarse-resolution DEMs.
- Rhoads B (2020) River dynamics for management.
- Schwanghart W, Scherler D (2014, 2017) TopoToolbox and smoothing/uncertainty methods.
- Tadaki M, Brierley G, Cullum C (2014) River classification: theory, practice, politics.

## Access, provenance, and intended use

- Timeframe: Analyses and data gathering conducted March–October 2020; results and methods described in Section 2.
- Data types: shapefiles for stream power and River Styles; CSV spreadsheets with extensive attribute data by River Style; metadata to enable discovery and reuse.
- Provenance: data produced by a collaboration of multiple authors, with field verification and image-based interpretation, intended to support the Bislak River Styles Report and related publication.
- Data usability: designed to be discoverable and usable with clear metadata, supporting analysis of correlations and predictions about fluvial morphology and stream power across a tropical catchment.