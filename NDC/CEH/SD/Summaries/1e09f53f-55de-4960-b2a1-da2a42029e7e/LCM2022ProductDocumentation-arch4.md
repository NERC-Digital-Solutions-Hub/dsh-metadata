# The UKCEH Land Cover Map for 2022

- LCM2022 provides annual UK land cover data across Great Britain and Northern Ireland, built from Sentinel-2 seasonal imagery and context layers.
- Product suite consists of seven datasets: three per region (GB and NI) plus a 1 km summary raster for both regions.
- Datasets include 10 m classified pixels, land parcels (both vector and rasterised), and a 1 km summary raster. Appendix 3 lists official dataset names; Table 5 provides DOIs for citation.

## Key datasets and structure

- 10 m Classified Pixel datasets (GB and NI)
  - Automatic classification from Classification Scenes; each pixel carries:
    - Band 1: most likely UKCEH Land Cover Class (21 classes)
    - Band 2: associated class probability/confidence
  - No generalisation by Land Parcel Spatial Framework to preserve fine features; used for detailed mapping and change detection.
- Land Parcel datasets
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterised from the 10 m classified pixels; three-band raster per parcel:
      - Dominant land cover (mode), confidence (conf), and purity (purity)
  - UKCEH Land Parcel Spatial Framework underpinning parcel structure; approx. 0.5 ha minimum parcel size (MMU)
  - Land Parcel Vector datasets (GB and NI) with additional parcel identifiers (DOIs available)
- 1 km raster products (GB and NI)
  - Summary products summarise 25 m rasters to 1 km cells
  - Dominant class per 1 km pixel and percentage cover per class (21 classes and 10 aggregates)
  - Rounding means sums may not equal exactly 100; coastal pixels may sum to less than 100
- Seasonal Composite Images and Context Rasters
  - Seasonal Composite Images derived from four seasonal windows using Sentinel-2 bands, resampled to 10 m
  - Context Rasters (GB: 10 rasters; NI: 9 rasters) include terrain (height, aspect, slope) and proximity/land-use masks (buildings, roads, coast, water, urban)
- Classification Scenes and methodology
  - GB classified in 32 Classification Scenes; NI uses a single Scene
  - Bootstrap Training data derived from previous LCM maps (2019–2021) plus additional crops data when needed
  - Random Forest classifier used; training balanced with replacement to ensure minority classes are learned
- UKCEH Land Parcel Spatial Framework
  - Framework to aggregate 10 m pixels into land parcels for consistent temporal comparisons
- Validation and quality
  - Formal validation with 33,107 reference points across 21 classes
  - Overall accuracy: 86.1% (full thematic detail)
  - Producer’s and user’s accuracy metrics provided by class in Appendix 4

## Production and data lineage

- Bootstrap Training
  - Uses historic LCM observations to sample current imagery for training; no new field data required
  - Large training sets help stabilize learning; some crops (arable vs. improved grassland) may require external data sources
- Random Forest classification
  - 10,000 samples per class used per iteration; balanced sampling ensures rare classes are learned
  - Implementation integrates Weka, PostGIS, and GDAL (open source tools)
- Data production cadence
  - Methods enable annual production to improve temporal consistency and enable change detection
  - Differences between years may reflect method changes as well as real change

## Data quality, limitations, and known issues

- Validation
  - 86.1% overall accuracy; detailed producer’s accuracy per class provided in Appendix 4
- Known issues
  - A small number of polygons missing from vector land parcel products; negligible effect on 1 km products
  - Some spectral/label confusion between related habitats (e.g., Saltwater vs Freshwater; various grassland and bog classes)
  - MMU (~0.5 ha) means many small patches and narrow features are not represented in parcel rasters
  - Seasonal and coastal areas may have edge-case misclassifications; coastal water regions prioritized for land cover mapping
- Interpretation caveats
  - Changes over time reflect both real land cover change and methodological updates; consider method notes when comparing across years

## Usage, access, and governance

- Access and citation
  - Each dataset has a DOI; DOIs and citations provided in Table 5
  - Marston et al. (2023/2024) provide production and validation context; see listed DOIs for data products
- Documentation and deliverables
  - Appendix 5/6 provide recommended colour palettes (and colour-blind friendly version) for display; accompanying QGIS symbology files are provided
  - Appendix 3 lists full datasets and metadata naming
- Data stewardship and updates
  - Annual updates aim for temporal consistency; users should differentiate real change from methodological shifts
  - The UKCEH Land Parcel Spatial Framework evolved over time, affecting cross-year parcel identifiers (gid)

## Technical specifications at a glance

- Coordinate systems
  - Great Britain: British National Grid, EPSG 27700
  - Northern Ireland: Irish Grid TM75, EPSG 29903
- Extents
  - GB extent: full national coverage
  - NI extent: truncated to landmass extent
- Resolutions
  - 10 m Classified Pixels (GB and NI)
  - 25 m Rasterised Land Parcels (GB and NI)
  - 1 km Summary rasters (GB and NI)
- Parcel counts
  - GB: ~6,741,294 parcels
  - NI: ~902,252 parcels

## Practical takeaways for Data Leaders

- Strategic value
  - Annual, high-detail land cover maps enable robust monitoring of state and change across the UK countryside
  - Rich time-series enables differentiation of random errors from real change; supports policy and environmental objectives
- Governance and interoperability
  - Clear provenance via DOIs; standardized spatial frameworks and coordinate systems facilitate cross-year and cross-region analyses
  - Detailed metadata, validation metrics, and explicit class mappings to BAP habitats aid in consistent reporting
- Data management and usage
  - Use 10 m pixel data for fine-scale analyses; aggregate to 1 km or parcel level for policy and performance reporting
  - Leverage context rasters and seasonal composites to improve classification robustness in challenging areas (coasts, urban, and mountainous regions)
- Implementation considerations
  - Plan for annual data refreshes; maintain versioning and audit trails
  - When comparing years, account for potential methodological differences and adjust change-detection workflows accordingly
- Dissemination and visualization
  - Utilize provided colour schemes and QGIS files to ensure consistent and accessible map outputs
  - Acknowledge DOIs when citing datasets in reports and dashboards