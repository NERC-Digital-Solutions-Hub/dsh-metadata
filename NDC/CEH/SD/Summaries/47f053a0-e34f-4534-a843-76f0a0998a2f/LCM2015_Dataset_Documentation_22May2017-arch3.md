# Dataset documentation

- UK Land Cover Map 2015 (LCM2015) is a parcel-based land cover map for the UK, delivering 21 classes based on UK Biodiversity Action Plan Broad Habitats; produced from two-date composite satellite imagery (Landsat-8 30m, AWIFS 60m where needed).
- Purpose: support monitoring frameworks by providing environmental health measures to scrutinise policies, evaluate decisions, and inform future actions.
- Data origins and framework: built to update LCM2007; spatial framework uses generalised cartography (GB OSMM, NI Land & Property Services) refined with rural boundary data; parcels reflect real-world boundaries for easier interpretation and compatibility with other geospatial data.

## Data products and structure

- Core data: vector dataset (dominant class per parcel) plus rich metadata; 25m raster and 1km raster products derived from the vector.
- Vector data: ~6.7 million polygons for Great Britain and ~0.9 million for Northern Ireland; nine core attributes including dominant class, source image, uncertainty, pixel counts per class, and modal class; each parcel has a unique gid.
- 25m raster: two-band raster; band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from the classifier.
- 1km raster: aggregate products – dominant class and percent cover per class (21 target classes or 10 aggregated classes); percent values are integer and may not sum to exactly 100 due to rounding.
- Spatial coverage and scale: GB and NI provided separately with respective projections; GB uses British National Grid (EPSG 27700), NI uses TM75 Irish Grid (EPSG 29903).
- Minimum mapping unit: >0.5 ha; parcels <0.5 ha and linear features <20 m dissolved into surrounding landscape.
- Access: 1km raster via CEH Environmental Information Platform; full vector and 25m raster on request (licensing may apply).

## Methodology

- Classification: Random Forest (RF) used for per-pixel classification; replaces previous maximum-likelihood approach.
- Training data: stable areas defined from classifications that agreed in 2000 and 2007; augmented with coastal zones and hard-to-map classes; ancillary data are integrated as inputs rather than post-classification rules.
- Spatial framework: no segmentation in LCM2015; per-pixel approach improves consistency for change detection and avoids segmentation-driven misalignment.
- Ancillary data and enhancements: data such as altitude and soil type are incorporated directly into the input features; knowledge-based enhancements are now objective parts of the input rather than post-hoc rules.
- Output emphasis: maps land cover (not land use); some classes are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).

## Classes and mapping

- LCM2015 uses 21 target classes aligned with Broad Habitats; some classes have sub-categories or aggregations:
  - Built-up Areas and Gardens split into Urban and Suburban.
  - Dwarf Shrub Heath split into Heather and Heather grassland.
  - Littoral Sediment split into Saltmarsh and Littoral sediment (together forming Littoral Sediment Broad Habitat).
  - Mixed woodland handling differs; training uses pure stands for woodland categories with modal_class assigned to polygons.
- Appendix references: detailed JNCC Broad Habitat definitions and crosswalks between LCM2015 classes and Broad Habitat types.

## Metadata, uncertainty and quality

- Rich metadata: each polygon includes dominant class, per-polygon pixel counts for all classes (pix_dist), number of pixels (npix), mean probability (unc), and standard deviation (unc_stdev); Modal_class and Modal_prop indicate the recommended display class and its share.
- Uncertainty: RF provides per-pixel probability; represented as mean per-polygon probability (unc) and stdev; available in the vector and 25m raster (but not in 1km products).
- Composite information: a composite image number (composite) indicates which inputs contributed to the classification; 99 indicates infill from LCM2007.
- Documentation and citations: each product has its own DOI to support repeatability and transparency; detailed metadata accompanies the vector product.

## Data access and citation

- DOIs exist for all products (GB vector, GB 25m raster, GB 1km products, NI equivalents); recommended citation includes authors and date in-text and full DOI in references.
- Data access points:
  - 1km raster: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25m raster: available on request under licence from CEH.
- Projections and coordinates: GB data in British National Grid; NI data in TM75 Irish Grid; documentation provides pixel, extents, and origin details.
- Additional information: project pages and contact details available; data paper in preparation.

## Practical considerations for monitoring frameworks

- Temporal comparability: LCM2015 introduces methodological changes relative to LCM2007 (e.g., montane class removal, rough grassland removal, segmentation removal, RF classifier, integrated ancillary data). When evaluating policy changes over time, ensure crosswalks and compatibility with earlier LCM maps.
- Data quality and accessibility: potential data gaps and access barriers may affect timely monitoring; plan for metadata verification and data governance.
- Uncertainty as a policy tool: per-polygon RF probability enables assessment of confidence in habitat classifications; use dominant class with uncertainty measures for reporting or to weight results.
- Aggregation and reporting: 1km aggregated products (percent cover, dominant/aggregate classes) can support large-area modelling and integration with other datasets (e.g., meteorology, species distributions); when exact totals matter, account for rounding in 1km percent products.
- Data governance: maintain gid (geometry id) for traceability; ensure appropriate sharing of underlying data and document DOIs for reproducibility.

## Appendices and references (highlights)

- Appendix 1-3 provide detailed class definitions, crosswalks to Broad Habitat types, and standard LCM2015 color mappings.
- Key references: Jackson (2000) Broad Habitat definitions; Morton et al. (2011) LCM2007 technical report.
- Composite and metadata details documented to support reproducibility and traceability across monitoring efforts.