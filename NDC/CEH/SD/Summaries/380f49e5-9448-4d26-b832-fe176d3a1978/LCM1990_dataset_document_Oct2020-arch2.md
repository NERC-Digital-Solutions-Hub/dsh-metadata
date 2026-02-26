# Dataset documentation

## Overview and purpose
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map created from Landsat-5 data (30 m) with 21 classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Built to support diverse LCM user needs and to enable compatibility with later products (LCM2007 framework; LCM2015) for long-term change analyses (e.g., a 25-year land cover change product).
- Vector (core) and raster (25 m and 1 km) data products provided; DOIs assigned for transparent citation and long-term accessibility.

## Data design and outputs
- Spatial framework and boundaries: constructed from generalised cartography (OSMM for GB; Northern Ireland equivalents), refined with rural boundary data to reflect real-world parcels; designed for easy interpretation and cross-dataset compatibility.
- Class structure: 21 LCM1990 classes mapped from 21 Broad Habitat types; some Broad Habitats split into finer LCM classes (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland).
- Data products:
  - Vector data: polygons with rich attributes per parcel, including dominant class, per-polygon class breakdown, uncertainty, and an unique geometry identifier (gid). GB vector contains ~6.7 million polygons; NI vector ~0.9 million polygons.
  - 25 m raster: three-band GeoTIFF per area (band 1 = dominant class, band 2 = per-polygon mean confidence, band 3 = percentage of polygon covered by modal class).
  - 1 km rasters: dominant cover (target and aggregate classes) and percentage cover (21 target bands and 10 aggregate bands). Rounding may cause sums to deviate from 100%; coastal areas may sum to less than 100 due to mapping boundaries.
- Minimum mapping unit: 0.5 ha (parcels <0.5 ha and linear features <20 m dissolved into surrounding landscape).

## Data content and formats
- Classes and mapping:
  - 21 target LCM1990 classes aligned with Broad Habitats; some splits allow finer distinctions (e.g., urban vs suburban, heather vs heather grassland, littoral/supralittoral divisions).
  - Detailed class descriptions and mapping rationale provided in appendices, with guidance on potential misclassifications (notably for grasslands and peat-related habitats).
- Metadata and uncertainty:
  - Vector: attributes include dominant class, hist (class composition within polygon), purity, conf (mean confidence), stdev, n (pixel count), and cmp (composite image reference).
  - Uncertainty quantified via Random Forest per-pixel probability; included in both vector and 25 m raster outputs.
- Documentation and DOIs:
  - Each product (GB NI vector, GB 25 m, GB 1 km targets/dominants, NI equivalents) has a DOI for citation.
  - Projections: GB vector and raster in British National Grid; NI vector and raster in Irish National Grid.

## Quality assurance and validation
- QA checks cover projections, spatial completeness, modal class presence, data range (0–100 for rasters), and pixel size integrity.
- Validation against other datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be reported in a separate publication.
- Full dataset lineage and processing information retained to enable traceability and repeatability.

## Access, licensing, and citation
- Access:
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request under licence from CEH (licensing may apply).
- Citation:
  - DOIs provided for each product; cite with authors, date, and DOI in references.
  - Example citation formats and data-citation guidance are included in the documentation.

## Use for environmental monitoring and analysis
- Standardised, high-resolution land cover data across the UK provide a consistent basis for monitoring environmental health and policy performance over time.
- Outputs in multiple formats support diverse analytical workflows:
  - Vector data with rich metadata for detailed site- or parcel-level analyses.
  - 25 m rasters for analyses requiring metadata-light surface data and efficient processing.
  - 1 km rasters for regional or national-scale modelling with other datasets (e.g., meteorology, species distributions).
- DOIs and metadata facilitate reproducibility, data provenance, and integration with other environmental datasets.

## Limitations and considerations
- LCM1990 maps land cover rather than definitive land use; some classifications may not directly indicate land use (e.g., recreation grass vs grazed pasture).
- Some habitat classes (e.g., Fen, Marsh and Swamp; Bog) are spectrally challenging; underestimation is possible in certain mosaics and small patches due to MMU and remote-sensing limitations.
- Water bodies and coastal features have mapping constraints near shorelines; rounding and area outside the MMU can affect exact area shares in 1 km products.

## Appendix highlights (context for analysts)
- Broad Habitat definitions provide the mapping rationale and guidance on potential misclassifications, particularly for grasslands, woodlands, and coastal habitats.
- The standard colour-mapping recipe is included for visualization consistency (not essential for data use but helpful for presentation).

## Summary for environmental analysts
- LCM1990 offers a robust, well-documented basis for monitoring UK land cover in 1990 with rich metadata, per-polygon uncertainty, and multiple output formats (vector, 25 m, 1 km) suitable for long-term environmental health assessments and policy performance analyses.
- The dataset supports data integration and cross-time comparisons, with clear DOIs and access pathways to encourage reproducibility and data sharing within monitoring frameworks.