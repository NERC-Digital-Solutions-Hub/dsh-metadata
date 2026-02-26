# River Styles and stream power analysis reveal the diversity of fluvial morphology in a Philippine tropical catchment

## Purpose and scope
- Data supporting the Bislak River Styles Report and the paper on river styles and stream power in a Philippine tropical catchment.
- Analyses conducted March–October 2020; initial analyses by Tolentino, Perez, and Guardian; river style classification reviewed by remaining authors.
- Methods are described in Section 2 of the referenced document.

## Data products (segment-stream power and river style data)
- Segment-stream power shapefiles and spreadsheets
  - Derived with TopoToolbox V2 to extract stream networks and delineate catchment areas.
  - Debris-flow vs. alluvial channel distinction using an upstream area threshold (>1 km²).
  - Data cleaned with non-parametric quantile regression; longitudinal profile corrections to ensure plausible elevations.
  - Segment-level attributes include mean elevation, mean slope, median catchment area (for 0.2 km segments) and computed stream power (Ω).
  - Shapefiles include segment geometries with stream power attributes; accompanying CSVs break down stream power by River Style.
- River Style identification shapefiles
  - Uses Stage One of the River Styles Framework to classify river types by confinement, planform, geomorphic unit assemblage, and bed material texture.
  - Outputs include polygon shapefiles for landscape units (lowland, upland, hills, catchment) and polylines for isohyet and river styles.
  - Classification aided by Google Earth imagery, with ground-truthing during field visits; interpretation guided by expert judgement.
- Supporting documentation for spreadsheets
  - Extensive CSVs detailing River Style attributes, including:
    - RS_Complete_Confined_Floodplain_Pockets.csv, RS_Complete_Confined_Gorge.csv, RS_Complete_Confined_Steep_Headwater.csv, RS_Complete_Laterally_Unconfined_Braided.csv, RS_Complete_Laterally_Unconfined_Deltaic.csv, RS_Complete_Partly_Confined_Bedrock.csv, RS_Complete_Partly_Confined_Planform_Low_Sin.csv, etc.
  - Each dataset includes identifiers (FID), coordinate columns (x, y, z), river style names, and various descriptive/statistical fields.
  - Documentation also details field naming conventions such as x_<river style>, y_<river style>, z_<river style>, strahler_<river style>, area_km2_<river style>, dist_km_<river style>, slope_<river style>, chi_mn0.45, ksn_mn0.45, chi_mn0.79, ksn_mn0.79, Stream_Pow_<river style>, and related metrics.
- Segment data files
  - Bislak_200 m_segment.csv and Bislak_50 m_segment.csv
  - Fields include stream_pow (linking to River Style), coordinates (X, Y, Z), Strahler/Shreve stream order, flow accumulation, distance to outlet, slope, chi indices, and normalized steepness (ksn) values at two concavity indices (0.45 and 0.79).

## Data processing and methods
- Network extraction and analysis
  - TopoToolbox 2 used to extract the river network and calculate catchment areas.
  - Alluvial channels defined as those with catchment area >1 km².
  - Hydrological corrections via non-parametric quantile regression; quantile carving along central tendency to enforce downstream decreasing elevations.
  - Segment-level slope values averaged over 0.2 km lengths (n = 1,129).
- Stream power calculation
  - For constant total stream power (Ω), derived using unit weight of water and relationships between catchment area and slope.
  - Equation referenced: Ω = 0.44 × χ × A × S (details provided in the data documentation).
  - Output includes shapefiles of segments with stream power attributes and CSVs detailing stream power by River Style.

## River Styles framework and classification
- Stage One River Styles Framework applied to identify discrete river styles across the Bislak Catchment.
- Classification criteria include confinement, channel planform, geomorphic unit assemblage, and bed material texture.
- Expert interpretation supported by imagery at multiple scales and ground-truthing; results mapped to landscape units and river styles.

## File structure and key fields
- River Style output files
  - River styles shapefiles (polygons) and isohyet/river style polylines.
- Segment power and attribute files
  - Segment_River_Styles_Figure_6a.csv and related segment outputs containing multiple river-style-specific fields.
- Segment data
  - Bislak_200 m_segment.csv; Bislak_50 m_segment.csv with aligned stream_pow, coordinates, hydromorphological metrics, and derived indices (Strahler/Shreve, chi, ksn, distoutlet, area_km2, etc.).
- The supporting RS_Complete_* CSVs serve as the descriptive backbone for each River Style category and its spatial/unit context.

## Validation, quality assurance, and limitations
- Data validated against Google Earth imagery; river style boundaries and longitudinal profiles interpreted with cross-checks to regional analyses.
- Ground-truthing and field visits conducted where feasible.
- Acknowledgement that River Style classification involves expert judgement due to the integrative nature of multiple criteria.

## How this supports the Data Support archetype
- Provides ready-to-use data products (shapefiles and CSVs) that can be combined with other datasets for analysis and visualization.
- Enables self-service exploration via geospatial and tabular data (e.g., dashboards, pivot tables) for diverse topics and users.
- Data products are clearly organized by River Style and geographic attributes, with detailed metadata in accompanying CSVs.
- Clear data lineage, methods, and validation steps aid reuse, replication, and extension by others.

## References
- Brierley GJ, Fryirs KA (2005) Geomorphology and river management: applications of the river styles framework.
- Fryirs K, Brierley G (2018) What's in a name? River styles naming conventions.
- Khan S, Fryirs KA (2020) DEM-based delineation of valley bottom segments.
- Rhoads B (2020) River dynamics and management.
- Schwanghart W, Scherler D (2014, 2017) TopoToolbox and regression smoothing techniques.
- Tadaki M, Brierley G, Cullum C (2014) River classification theory, practice, politics.