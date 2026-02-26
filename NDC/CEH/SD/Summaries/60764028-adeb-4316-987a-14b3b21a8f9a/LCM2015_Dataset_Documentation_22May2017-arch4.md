# Dataset documentation

- LCM2015 is a parcel-based UK land cover map created by classifying satellite imagery into 21 Broad Habitat classes, mainly using Landsat-8 (30 m) with AWIFS (60 m) data as needed.
- The dataset provides a range of products (vector and raster) designed for diverse user needs and includes rich metadata and uncertainty information at multiple scales.
- It is explicitly cautioned that LCM2015 is not in its current state suitable for change mapping; differences between years reflect both real change and classification/processing differences.

## What LCM2015 is and why it matters for data governance

- Parcel-based land cover map for the UK, reflecting real-world boundaries and aligned with UK Biodiversity Action Plan Broad Habitat definitions.
- Produces 21 target land cover classes (with some subdivisions) and supports multiple data formats and spatial resolutions for varied applications (policy, planning, modelling, research).
- Output formats include:
  - Core vector data set (parcels with rich attributes)
  - 25 m raster (two-band: class and per-polygon probability)
  - 1 km raster products (dominant class, percentage cover for both 21 and aggregate classes)
- Each parcel (polygon) has unique labeling (gid) and extensive metadata, including the dominant class, pixel counts per class, and mean probability from classification.
- Data are archived with URIs/DOIs for citation; GB and Northern Ireland data are provided separately with appropriate coordinate systems.

## Key differences from earlier LCM products (LCM2007)

- Output data changes:
  - Montane class removed; upland areas reclassified to inland rock or other upland habitats based on spectral data.
  - Rough grassland removed; grassland types now align with JNCC Broad Habitats without soil-based refinements.
  - 25 m raster now two-band (classification first band; probability in band 2).
  - Probability information simplified to mean polygon probability; not provided for 1 km products.
  - Sub-class spectral groups removed; Random Forest handles multi-modal classes, reducing need for spectral sub-classes.
  - Spatial framework segmentation removed; per-pixel per-fragment segmentation is not used in LCM2015 to improve consistency for change mapping.
  - Mixed woodland classification defined by percentage cover rather than training-based blocks; training uses pure stands.
- Methodology changes:
  - Switch to Random Forest classifier (improves handling of multi-model training data and performance).
  - Stable training areas built from 2000 and 2007 classifications, supplemented by coastal, fen/marsh, swamp, and hard-to-map classes.
  - Ancillary data (e.g., slope, distance to rivers) are integrated into the input data rather than applied post-classification.

## Data products and structure

- Core vector data set:
  - ~6.7 million polygons in Great Britain; ~0.9 million in Northern Ireland.
  - Attributes include gid, dominant class (BHAB), pixel distributions (pix_dist), uncertainty (unc), number of pixels (npix), modal_class, modal_prop, and composite image reference.
- 25 m raster:
  - Two-band raster: band 1 = dominant LCM2015 class, band 2 = mean probability for the polygon’s dominant class.
- 1 km raster:
  - Dominant cover at 1 km (for both 21 classes and 10 aggregate classes).
  - Percentage cover at 1 km for both 21 classes and 10 aggregates (values are integers and may sum to slightly above/below 100 due to rounding).
- Spatial coverage and projections:
  - Great Britain: British National Grid (BNG, EPSG 27700)
  - Northern Ireland: TM75 Irish Grid (EPSG 29903)
- Resolution and extent:
  - 25 m and 1 km raster products; GB and NI datasets provided separately with corresponding metadata (grid size, pixel counts, extents).

## Classes and labeling

- 21 LCM2015 target classes, aligned with Broad Habitat definitions (JNCC Jackson, 2000).
- Some classes are subdivided in the dataset for enhanced detail (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral categories and coastal classes).
- Unique gid labeling for unambiguous data communication and traceability.

## Metadata and uncertainty

- Rich metadata available for vector polygons, including dominant class and pixel-level breakdown (pix_dist) with mean polygon probability.
- Uncertainty is provided as a per-polygon probability (scaled 0–255) and its standard deviation.
- DOIs are assigned to all LCM2015 products, enabling robust citation and reproducibility.

## Access, licensing, and citation

- Data access:
  - 1 km raster products available via the CEH Environmental Information Platform.
  - Full vector and 25 m raster products available on request under licence from CEH.
- Licensing: Some users/applications may incur licence fees; access is via CEH or licensed partners.
- Citations: Each LCM2015 product has a DOI; users should cite the appropriate DOI(s) in publications.
- Contact and information:
  - Data inquiries: spatialdata@ceh.ac.uk
  - Additional information and data paper forthcoming; resources at CEH websites and EIDC.

## Practical considerations for data leaders

- Data governance and stewardship:
  - Maintain gid and full metadata for traceability and interoperability.
  - Use DOIs to ensure reproducibility and proper attribution in analyses and reports.
- Data quality and suitability:
  - Be aware that changes between LCM2015 and prior maps reflect both real change and methodological shifts; exercise caution when using for change detection.
  - Leverage uncertainty information to assess confidence in classifications and prioritize review of ambiguous areas.
- Data integration and workflows:
  - Choose the product form that fits the workflow (vector for rich attributes, 25 m raster for detailed analysis with probability, 1 km for broad-scale modelling).
  - Align coordinate systems and projections (BNG for GB, Irish Grid for NI) when integrating with other datasets.
- Strategic use:
  - Use 1 km aggregated products for national-scale modelling with other datasets (e.g., climate, species distributions).
  - Use vector with gid and pixel distributions for detailed spatial analysis, reporting, and feature-level integrity checks.
- Community and reuse:
  - Note the stable, archived nature of LCM2015 with DOIs, facilitating reuse across networks and partners.
  - Reference the dataset via the provided DOIs to support reproducibility and traceability in organizational analytics.