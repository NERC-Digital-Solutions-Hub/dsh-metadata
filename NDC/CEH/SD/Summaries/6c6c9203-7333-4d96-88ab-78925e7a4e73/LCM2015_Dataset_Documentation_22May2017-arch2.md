# Dataset documentation

## Overview of LCM2015

- Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover map classifying satellite data into 21 land cover classes, based on UK Biodiversity Action Plan Broad Habitat definitions.
- Primary data sources: Landsat-8 (30 m) with AWIFS (60 m) as needed; created from two-date composites.
- Builds on the LCM2007 framework and uses GB Ordnance Survey and NI mapping boundaries; designed for interpretability and compatibility with other geospatial datasets.
- LCM2015 maps land cover (not necessarily land use); supports varied monitoring and modelling needs with multiple data products.

## Data products and formats

- Core vector data set: GB 6.7 million polygons; NI 0.9 million polygons; each polygon includes a rich set of attributes (e.g., dominant class, pixel breakdown, uncertainty, gid).
- 25 m raster: two-band product per polygon (band 1 = dominant class; band 2 = mean per-polygon probability).
- 1 km raster products: dominant class (21 target or 10 aggregate classes) and percentage cover (21 or 10 bands); used for large-area modelling.
- Attribute set and uncertainty: vector includes per-polygon probability; 1 km/25 m products provide aggregated uncertainty information.
- Metadata and labeling: each parcel has a unique gid; color mapping and class definitions aligned with Broad Habitats; detailed documentation in Appendices.
- Data projections: Great Britain in British National Grid; Northern Ireland in Irish National Grid; DOIs assigned for all products.

## Methodology and key differences from LCM2007

- Classifier: replaces Maximum Likelihood with Random Forest (better handling of multi-model data and avoids spectral sub-classes).
- Training data: uses a stable initial set of training areas (areas classified the same in 2000 and 2007) plus targeted additions for coastal areas and poorly mapped classes; ancillary data (where used) integrated into input data rather than post-classification rules.
- Output structure changes:
  - Montane class removed; mapped as Inland Rock or other upland habitats based on spectral data (use LCM2007 for Montane distributions if needed).
  - Rough grassland removed; aligns grassland types with JNCC Broad Habitats without soil data.
  - 25 m raster becomes a two-band image; probability data recorded as mean per-polygon probability (vector) and band 2 in the 25 m raster.
  - No spectral sub-classes as training subclassing is no longer needed with Random Forest.
  - Spatial framework: no segmentation-based polygons; per-pixel classification with improved consistency for change mapping.
- Mapping approach: 21 target classes with certain Broad Habitat subdivisions (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Broad Habitats split into related subclasses).
- Data as stable, archived products with DOIs; per-pixel analysis enabled through multiple resolutions.

## Class structure and mapping details

- 21 LCM2015 target classes (based on Broad Habitats); some are further subdivided for detailed outputs (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral categories).
- Aggregates: 1 km rasters also provide 10 aggregate classes for simpler analyses.
- Unique labeling: each parcel has a gid for unambiguous communication between users.
- Uncertainty: per-polygon probability from the Random Forest classifier included in vector (unc and unc_stdev attributes) and band 2 of the 25 m raster.

## Practical considerations for users

- LCM2015 is designed to support a broad range of applications but has complexities and uncertainties, especially for change mapping.
- Differences between LCM products across time can reflect real change plus classification differences; users should exercise caution when comparing LCM2007/LCM2015 outputs.
- Minimum mappable area: >0.5 ha; smaller parcels are dissolved into surrounding areas.
- Data access: 1 km rasters via CEH Environmental Information Platform; full vector and 25 m rasters available on request under license; fees may apply for some users.

## Data access, citations, and metadata

- Access points:
  - 1 km rasters: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25 m rasters: available under license on request from CEH.
- DOIs: Each product (GB NI vector, 25 m, and 1 km products) has its own DOI for proper citation.
- Citing: Include author(s) and date in text and full DOI in references; example format provided in the document.
- Projections and coverage: GB data in British National Grid; NI data in TM75 Irish Grid; consistent metadata and extensive polygon attributes.

## Important cautions and limitations

- The document explicitly states: LCM2015 is a complex dataset; users should familiarise themselves with the accompanying information to guard against inappropriate use.
- Do not rely on the LCM series for change mapping in its current state due to differences in methods, data sources, and spatial frameworks across time.
- Differences in output data and methodology across LCM generations require careful handling when performing temporal analyses.

## Appendices and additional context

- Appendix 1–3 provide detailed definitions of Broad Habitat classes, color mappings for visualization, and composite image information used in LCM2015.
- Appendix 4 lists the composite images used for the classification process.