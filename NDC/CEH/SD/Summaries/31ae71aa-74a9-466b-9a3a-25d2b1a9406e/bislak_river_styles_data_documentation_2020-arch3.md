# River Styles and stream power analysis reveal the diversity of fluvial morphology in a Philippine tropical catchment

## Overview
- Data support the Bislak River Styles Report and the paper "River Styles and stream power analysis reveal the diversity of fluvial morphology in a Philippine tropical catchment" by Tolentino et al. (2020).
- Analyses were conducted March–October 2020; authors identified river types (River Styles) and quantified stream power to understand fluvial morphology diversity.
- Methods combine remote sensing, GIS-based classification, and field verification to produce reproducible spatial data and metrics for monitoring river form and behavior.
- Outputs include shapefiles and spreadsheets that represent segment-level stream power, River Styles classifications, and supporting metadata.

## Data and Methods

- Segment-stream power shapefiles and spreadsheets
  - Use of TopoToolbox V2 to delineate the stream network and catchment areas with standard flow-routing algorithms.
  - Debris-flow–dominated channels vs. alluvial channels distinguished using a 1 km² upstream area threshold; analysis focused on alluvial channels (>1 km²).
  - Data cleaning via non-parametric quantile regression to remove artefacts in longitudinal profiles; quantile carving along the central tendency (τ = 0.5) to ensure downstream-decreasing elevations.
  - Segment-level slope averaged over 0.2 km segments; mean elevation, mean slope, and median catchment area extracted for each segment; validation of stream positions against recent Google Earth imagery.
  - For constant total stream power (Ω), Ω is related to unit weight of water, catchment area (A), and slope (S); Ω = 0.44 χ A S (as presented in the text). This enabled calculation of stream power attributes for 0.2 km river segments.
  - Resulting outputs: shapefiles of segments with stream power attributes and CSV spreadsheets detailing stream power broken down by River Style.

- River Style identification shapefiles
  - Stage One of the River Styles Framework used to identify river types across the Bislak Catchment, following a defined naming convention.
  - Classification criteria: confinement (channel position in valley), channel planform (continuity, number of channels, sinuosity), geomorphic unit assemblage, and bed material texture.
  - Identification aided by interpretation of Google Earth imagery at reach and unit scales; geomorphic attributes ground-truthed during field visits.
  - Outputs: shapefiles for landscape units (lowland, upland, hills, catchment), isohyet lines, and river styles; distribution mapped and major tributaries analyzed alongside catchment-wide analyses.
  - Note: Given the breadth of criteria, final River Style classification relied on expert judgment.

- Supporting documentation for spreadsheets
  - Numerous CSV sets corresponding to different River Style categories (e.g., Confined Floodplain Pockets, Confined Gorge, Confined Steep Headwater, Laterally Unconfined Braided, Laterally Unconfined Deltaic, Partly Confined Bedrock, Partly Confined Planform with Low Sinuosity, etc.).
  - File naming includes multiple variants to capture different data views and units. Examples include RS_Complete_Confined_Floodplain_Pockets.csv, RS_Complete_Laterally_Unconfined_Braided.csv, RS_Complete_Partly_Confined_Bed_rock.csv, and similar for 50 m and 200 m segment resolutions.
  - Column headers and details provided (e.g., FID, coordinates, Strahler/Shreve orders, upstream area, distance from outlet, slope, various chi indices with different concavity values, area_km2, distoutlet, segment identifiers, and coordinate fields x/y/z).

- Segment data and references
  - Segment data files include Bislak_200_m_segment.csv and Bislak_50_m_segment.csv with fields for stream power, spatial coordinates, stream order, area, distance to outlet, slope, Strahler/Shreve orders, and normalized channel steepness (ksn) under multiple concavity assumptions (0.45 and 0.79).
  - Additional segment metadata files (Segment_River_Styles_Figure_6a.cs_v, etc.) provide spatial and attribute details for figure-based segment analyses.

## Outputs, Metadata, and Reproducibility

- Spatial and tabular data products
  - Shapefiles of segment networks with stream power attributes.
  - River Styles polygon and polyline shapefiles (landscape units, isohyet, river styles).
  - Extensive CSV documentation mapping each River Style category to segment attributes and metrics.
- Metadata and documentation
  - Detailed supporting documentation lists and describes each CSV, including column headings and the type of data captured.
  - Clear naming conventions to facilitate reproducibility and cross-study comparability.
- Reproducibility considerations
  - Methodology leverages established tools (TopoToolbox), standardized thresholds, and transparent data processing steps (artefact removal, hydrological corrections, slope aggregation).
  - Field verification and imagery-based validation enhance reliability of River Styles classifications.
  - Expert judgment acknowledged as a component of River Style delineation, underscoring the importance of documentation and metadata for traceability.

## Data Quality and Governance Considerations

- Data quality addressed through:
  - Use of validated processing steps (quantile regression, central-tendency carving) to reduce artefacts.
  - Ground-truthing and satellite imagery validation to align classifications with real-world conditions.
- Governance and sharing
  - The work emphasizes transparent data sharing of underlying datasets and metadata, aligning with data governance principles essential for monitoring frameworks.
  - Comprehensive documentation supports governance, auditability, and potential replication or extension in other catchments.

## References
- Brierley GJ, Fryirs KA (2005) Geomorphology and river management: applications of the river styles framework. Blackwell, Malden
- Fryirs K, Brierley G (2018) What's in a name? A naming convention for geomorphic river types using the River Styles framework. PLoS ONE 13(9):e0201909
- Khan S, Fryirs KA (2020) Application of globally available, coarse-resolution digital elevation models for delineating valley bottom segments of varying length across a catchment. Earth Surf Process Landf 45(12):2788-2803
- Rhoads B (2020) River dynamics: geomorphology to support management. Cambridge University Press
- Schwanghart W, Scherler D (2014) TopoToolbox 2. Earth Surf Dyn
- Schwanghart W, Scherler D (2017) Bumps in river profiles: uncertainty assessment and smoothing using quantile regression techniques. Earth Surf Dyn
- Tadaki M, Brierley G, Cullum C (2014) River classification: theory, practice, politics. Wiley Interdiscip Rev Water