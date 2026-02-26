# Dataset documentation

- LCM2015 is a UK-wide land cover map produced from Landsat-8 (30 m) with supplementary AWIFS (60 m) data, classifying into 21 Broad Habitat-based classes.
- Outputs include a core vector dataset, a 25 m raster, and 1 km aggregated products (dominant and percentage cover) to support diverse user needs.
- The dataset is designed as a stable, archived resource with rich metadata, uncertainty information, and clear data provenance (including DOIs for all products).

## Purpose, scope and governance

- Purpose: provide a range of data products to support the LCM user community, with attention to governance, usability, and discoverability.
- Caveat for use: not recommended for change mapping in its current state; differences between LCM products reflect real change plus classification differences.
- Classification basis: 21 land cover classes derived from UK Broad Habitat definitions; per-polygon maps reflect real-world boundaries to aid interoperability with other geospatial datasets.
- Land cover vs land use: LCM2015 maps land cover, not necessarily land use; e.g., arable and horticulture are mapped as land cover rather than inferred use.

## Data products and structure

- Core vector dataset
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Attributes include: dominant class (BHAB), unique gid, pixels per class (pix_dist), uncertainty (unc), standard deviation (unc_stdev), number of pixels in polygon (npix), and modal_class (target class) with associated proportion (modal_prop), plus a composite image identifier.
- 25 m raster dataset
  - 2-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from Random Forest.
- 1 km raster products
  - Dominant class per 1 km grid (for both 21 classes and 10 aggregate classes).
  - Percentage cover per class per 1 km grid (21 bands for 21 classes; 10 bands for aggregates).
  - Sum across a 1 km cell may not equal exactly 100 due to rounding and coastal coverage considerations.
- Class details
  - 21 target classes, with some splits (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral subtypes).
  - Appendix notes provide mapping to JNCC Broad Habitat definitions for user interpretation.

## Differences in methodology and outputs (vs LCM2007)

- Classification algorithm
  - LCM2015 uses Random Forest; replaces Maximum Likelihood approach from LCM2007.
  - Eliminates the need for spectral sub-classes; handles multi-modal training data more robustly.
- Training data and ancillary data
  - Training areas are built from a stable dataset (areas consistently classified the same in 2000 and 2007) and supplemented for coastal areas and poorly mapped classes.
  - Ancillary data (e.g., slope, distance to rivers) are integrated as part of the input data rather than applied post-classification, enabling objective knowledge-based enhancements.
- Spatial framework and segmentation
  - No segmentation-based polygons in LCM2015’s spatial framework, aiming for per-pixel classification and easier cross-change analysis.
- Training targets and outputs
  - No spectral sub-class probabilities in vector outputs; probability is provided as a mean per-polygon value in the vector, and as band 2 in the 25 m raster.
  - Montane and Rough grassland classes were removed or redefined to align with current spectral-based mapping and Broad Habitat types.
- Woodland classification
  - Mixed woodland handling updated: training uses pure stands for Coniferous or Broadleaf woodland; final polygon labels reflect modal_class after per-pixel classification.

## Data quality, metadata and uncertainty

- Rich metadata
  - Each polygon contains a full set of attributes and a detailed description of dominant class, pixel-level composition, and processing lineage.
- Uncertainty
  - Random Forest provides per-pixel probability estimates, captured as mean polygon-level values (and in 25 m band 2); standard deviation is available (unc_stdev).
- DOIs and reproducibility
  - All LCM2015 products have DOIs; clear guidance on how to cite data in publications.
- Minimum mapping unit
  - Parcels smaller than 0.5 ha or linear features under 20 m are dissolved into the surrounding landscape during production.
- Data provenance
  - Products are produced with documented processing steps, training areas, and composite image usage where applicable.

## Data access, licensing and formats

- Access
  - 1 km raster products accessible via CEH Environmental Information Platform (EIP).
  - Full vector and 25 m raster products available on request under licence from CEH; licence fees may apply.
- Projections
  - Great Britain vector and GB 25 m raster: British National Grid.
  - Northern Ireland vector and NI 25 m raster: TM75 Irish Grid.
- Citing and DOIs
  - DOIs provided for GB and NI vector, 25 m raster, 1 km dominant and percentage products, and aggregate classes; use DOIs in citations to ensure reproducibility.

## Citing, reuse and governance guidance

- Data should be cited with the provided DOIs, including author list and date.
- Data users should refer to the accompanying documentation for methodological differences, class definitions, and interpretation guidelines.
- Guidance notes emphasise the differences from LCM2007 to support proper interpretation and avoid incorrect change inferences.

## Additional context and Appendix highlights

- Linkage to Broad Habitat definitions (JNCC Jackson, 2000) for class interpretation and consistency with national biodiversity frameworks.
- Appendix 1-3 provide detailed class definitions, colour mappings, and composite image metadata to support consistent visualization and communication of results.
- Appendix 4 lists composite images used in LCM2015 production, documenting imagery dates, sensors, and paths.

## Versioning and updates

- Version history included (1.0 original release; 1.1 corrections to dataset publication year; 1.2 updates to a vector attribute and minor corrections).
- Documentation emphasizes the evolving nature of LCM products and the rationale for methodological changes to support future change mapping and reproducibility.

## Contact and further information

- Contact: CEH Spatial Data team (spatialdata@ceh.ac.uk); telephone and website details provided.
- Additional information and data access portals:
  - CEH LCM2015 information pages
  - CEH Environmental Information Platform (for 1 km data)

- Data paper and references: citations to Jackson (2000) and Morton et al. (2011) for background on Broad Habitat classification and previous LCM methodology.