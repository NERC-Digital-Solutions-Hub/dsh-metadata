# River Styles and stream power analysis reveal the diversity of fluvial morphology in a Philippine tropical catchment

## Purpose and scope
- Data submitted for the Bislak River Styles Report and the paper conducting river styles and stream power analysis in a Philippine tropical catchment.
- Analyses cover March–October 2020; aims include identifying river types, computing stream power, and supporting environmental monitoring and policy performance assessment over time.

## Data processing workflow
- TopoToolbox V2 used to extract the river network and delineate catchment areas with standard flow-routing algorithms.
- Debris flow–dominated channels thresholded at 1 km² to exclude them; only alluvial channels (>1 km²) considered for analysis.
- Data cleaned with non-parametric quantile regression to remove artefacts; quantile carving along the central tendency (τ = 0.5) to enforce downstream-decreasing elevations.
- Segment-level slope averaged over 0.2 km lengths (n = 1129); mean elevation, mean slope, and median catchment area computed for each segment and exported.
- Validation of stream network position against recent Google Earth imagery.
- Total stream power (Ω) relation used: Ω = 0.44 × χ × A × S, with unit weight considerations described in the text.

## River Style identification and outputs
- Stage One of the River Styles Framework applied to classify segments into River Styles based on confinement, channel planform, geomorphic unit assemblage, and bed texture.
- Identification aided by expert judgment, interpretation of Google Earth imagery, and field ground-truthing during site visits.
- Outputs include:
  - Shapefiles of river styles (polygons for landscape units: lowland, upland, hills, catchment; polylines for isohyet and river styles).
  - Shapefiles with segment-level stream power attributes.
  - Spreadsheets (.csv) containing stream power data disaggregated by River Style.

## Supporting documentation and data schemas
- Numerous CSVs listed for different River Style environments (e.g., Confined Floodplain Pockets, Confined Gorges, Confined Steep Headwaters, Laterally Unconfined Braided, Deltaic, Bedrock-confined, Planform-Low Sin, etc.).
- Metadata fields and column headers cover:
  - Identification IDs, coordinates (X, Y, Z), Strahler and Shreve stream orders, upstream area, distance from outlet, slope, area, and various stream power metrics.
  - Multiple river style naming conventions and segment identifiers (e.g., RS_Name_<river style>, FID_<insert river style>).
  - Additional derived metrics for comparison and mapping (e.g., chi indices with different concavity values, ksn values, area_km2, dist_km, slope_FID, stream_pow cross-references).

## Data quality, validation, and limitations
- Geomorphic attributes validated through field visits and cross-checked with Google Earth imagery.
- River Style classification relies on expert judgement due to the integration of multiple criteria (confinement, planform, geomorphic units, bed texture), acknowledging potential subjectivity.

## Data management, sharing, and references
- Outputs designed for archival, sharing, and portal uploading with standardized naming conventions to facilitate reuse.
- Key references underpinning methods include foundational River Styles framework (Brierley & Fryirs) and related methodological works on TopoToolbox, quantile regression smoothing, and river morphology classification.