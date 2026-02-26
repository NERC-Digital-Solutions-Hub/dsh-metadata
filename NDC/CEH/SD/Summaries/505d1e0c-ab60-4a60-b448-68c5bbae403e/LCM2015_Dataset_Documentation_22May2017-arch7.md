# Dataset documentation

- LCM2015 (Land Cover Map 2015) is a parcel-based UK land cover map derived from satellite data (primarily Landsat-8 at 30 m, supplemented with AWIFS at 60 m) and classified into 21 Broad Habitat-based classes.
- Data products include a core vector dataset, a 25 m raster, and 1 km aggregated products (dominant and/or percentage cover) suitable for a range of GIS applications.
- The dataset is designed to support map-based data visualisation and analysis for policy, planning, conservation, and public-facing audiences, with emphasis on spatial clarity and traceable metadata.

## Data products and formats

- Vector data set
  - 6.7 million polygons for Great Britain (GB) and 0.9 million for Northern Ireland (NI).
  - Each polygon includes attributes such as unique gid, dominant land cover class (Modal_class), breakdown of pixel counts per class (Pix_dist), uncertainty (unc), standard deviation (unc_stdev), number of pixels (npix), and the proportion of the polygon classified as the dominant class (Modal_prop), plus a composite image indicator.
  - 21 target LCM2015 classes; gid enables unambiguous cross-user communication.
- 25 m raster
  - Two-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from the Random Forest classifier.
- 1 km raster
  - Aggregated products derived from the 25 m raster:
    - Dominant cover at 1 km (for both 21 classes and 10 aggregate classes).
    - Percentage cover at 1 km for 21 classes and for 10 aggregate classes (values are integer; sums may not exactly equal 100 due to rounding and coastal area handling).
- Spatial resolution and coverage
  - Separate GB and NI datasets with appropriate coordinate systems (GB: British National Grid; NI: Irish Grid equivalents).
  - Minimum mappable unit: parcels >0.5 ha; linear features <20 m dissolved into surrounding landscape.

## Methodology and classification

- Purpose and approach
  - LCM2015 maps land cover (not land use) and is designed as a stable, archived dataset with rich metadata and uncertainty information.
- Classification algorithm
  - Random Forest classifier (replacing the previous Maximum Likelihood approach).
  - Ancillary data (e.g., elevation, slope, proximity to rivers) are integrated as input features in the classification process.
- Training data and stability
  - Initial training areas draw from areas consistently classified in 2000 and 2007, then supplemented with coastal areas and classes historically difficult to map (Fen, Marsh, Swamp, etc.).
  - Per-pixel classification summaries are used to determine polygon labels; mixed woodland training uses pure stands for GB NI training.
- Spatial framework
  - LCM2015 moves away from segmentation-based segmentation in the spatial framework to per-pixel classification, reducing segmentation-related errors, particularly in uplands.
- Output considerations
  - Montane and Rough grassland classes removed to better support change mapping and consistency with spectral data.
  - Spectral sub-classes removed; probabilities are summarized as mean polygon probability (vector) and band 2 of the 25 m raster.
- Class definitions
  - 21 target Broad Habitat classes aligned with JNCC Broad Habitat definitions; several classes are subdivided for enhanced detail (e.g., Urban vs Suburban; Heather vs Heather Grassland; Littoral/Nearshore categories).

## Differences from LCM2007 (highlights)

- Montane class removed; mapped as Inland Rock or other upland habitats in LCM2015.
- Rough grassland removed; grassland types re-aligned with Broad Habitat definitions; no soil data used in LCM2015.
- 25 m raster redesigned as two-band product; probability data moved to band 2.
- Probability representation streamlined: vector uses mean polygon probability; 25 m raster band 2 carries the same information.
- Subclass spectral groupings removed; Random Forest handles multi-modal outputs without spectral sub-classes.
- Spatial framework segmentation removed; per-pixel classification aids change detection and reduces frame-to-frame segmentation misfits.
- Training data and ancillary data integration moved from post-classification rules to integrated inputs, improving objectivity and reproducibility.

## Metadata, uncertainty, and data lineage

- Rich metadata: polygon-level attributes including dominant class, per-class pixel counts, and probabilities.
- Uncertainty information: Random Forest provides per-pixel probability; reported as a mean per polygon in vector and as band 2 in the 25 m raster; not provided for 1 km products.
- Composite information: a composite image index indicates the source image(s) used to derive the classification.
- Documentation: each product has DOIs for citation; data citation encouraged for reproducibility.

## Data access and licensing

- GB 1 km and NI 1 km products
  - Accessible via the CEH Environmental Information Platform (EIP) at https://eip.ceh.ac.uk/
- Full vector and 25 m raster products
  - Available under licence on request from CEH; licence fees may apply.
  - Application via CEH website or contact spatialdata@ceh.ac.uk.
- Projections and codes
  - GB data in British National Grid (EPSG 27700); NI data in the Irish Grid (TM75 Irish Grid, EPSG 29903).
- DOIs
  - All LCM2015 products have individual DOIs for proper citation (GB vector, GB 25 m raster, GB1 km products, NI vector, NI 25 m raster, NI 1 km products).

## Use cases, cautions, and best practices for GIS work

- Intended use
  - Primarily for map-based data visualisation and spatial analysis; supports diverse GIS applications and policy/public-facing outputs.
- Change mapping caution
  - The LCM series is not recommended for change mapping in its current state; observed differences reflect both real changes and classification/classification-error components.
- Data handling tips
  - Retain the gid attribute in vector products for unambiguous data communication.
  - Choose product type to suit application: vector offers rich per-polygon metadata; 25 m raster provides a lighter-weight representation; 1 km products facilitate regional-scale modelling with meteorological or species-distribution data.
- Documentation and reproducibility
  - Cite DOIs when using products; reference methodology (Random Forest, stable training areas) in analyses and publications.

## Appendix highlights (conceptual)

- Class mapping and color conventions are defined (see Appendix 3 for standard LCM2015 color mapping; 21 target classes with corresponding RGB values).
- Detailed broad habitat definitions (JNCC Broad Habitats) provided to aid interpretation and class aggregation decisions.
- Composite images and data provenance are documented to support reproducibility and lineage tracing of classifications.

- Queries and further information
  - For more details, see the CEH LCM2015 information pages and the CEH data access portal; contact spatialdata@ceh.ac.uk for data-specific questions or licensing inquiries.