# Dataset documentation

- LCM2015 is a parcel-based UK land cover map with 21 classes aligned to UK Biodiversity Action Plan Broad Habitats, produced from two-date Landsat-8 (30 m) imagery (supplemented by AWIFS as needed) to update LCM2007 and match a per-pixel, repeatable mapping approach.
- The dataset supports diverse user needs with multiple data products and formats, including detailed vector data, a 25 m raster, and 1 km aggregated rasters.

## Data products and formats

- Core vector data set (GB and NI) with polygons and rich attributes; 25 m raster derived from the vector; 1 km percentage and dominant cover products (21 target classes and 10 aggregates).
- Vector, 25 m raster: 6.7 million polygons (GB) and 0.9 million polygons (NI). 1 km products are created by aggregating the 25 m data.
- 0.5 ha minimum mappable unit; parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape.
- The 25 m raster is two-band: band 1 = dominant class per polygon; band 2 = mean per-polygon probability from the classifier.
- The 1 km rasters provide dominant and percentage cover for both 21 target classes and 10 aggregates.
- Data are provided in Great Britain (British National Grid) and Northern Ireland (TM75 Irish Grid) projections.

## Classification method and workflow

- Random Forest classifier used (instead of Maximum Likelihood), enabling multi-modal training data and often improved performance.
- Training data: an initial stable set from 2000 and 2007, expanded for coastal areas and historically problematic classes; ancillary data (e.g., slope, distance to water) incorporated as inputs.
- No use of spectral sub-classes; no segmentation in the spatial framework for LCM2015 to improve change-mapping compatibility.
- Ancillary data are integral to classification (objective, not post-classification editing).
- Outputs include per-polygon probability (uncertainty) and a modal_class for display.

## Differences from LCM2007 (output, methodology, and framework)

- Output data: Montane class removed and reclassified based on spectral data; Rough grassland removed; 25 m raster now two-band; probability information simplified (vector shows mean polygon probability; 25 m band 2 has the mean per-polygon probability; 1 km products do not include probability).
- Methodology: New Random Forest classifier; stable training areas built from 2000/2007, with additional coastal and poorly mapped areas; ancillary datasets used as inputs; knowledge-based enhancements embedded in the input data rather than post-classification rules.
- Spatial framework: No segmentation in the LCM2015 framework; per-pixel classification instead of segmentation-based polygons (affects GB vector and 25 m raster; NI unchanged in this respect).

## Land cover classes and mapping

- LCM2015 maps 21 target classes based on Broad Habitats; several classes are split into sub-classes (e.g., Urban vs Suburban, Heather vs Heather grassland, Littoral categories).
- Appendix 1–3 provide detailed class definitions, mappings to Broad Habitat categories, and standard colour mapping (for visualization).
- The vector’s gid attribute uniquely identifiers parcels; polygon-level metadata include dominant class, pixel breakdown (Pix_dist), and per-polygon mean probability (unc).

## Data access, citation, and provenance

- Data access:
  - 1 km raster products available via CEH Environmental Information Platform.
  - Full vector and 25 m raster available on request under licence from CEH.
- DOIs exist for all LCM2015 products (GB and NI) to support citation and reproducibility.
- Projections:
  - GB data: British National Grid (EPSG 27700)
  - NI data: TM75 Irish Grid (EPSG 29903)
- The dataset emphasizes data provenance and metadata richness: per-polygon attributes include dominant class, pixel counts per class, mean probability, and composite image provenance.

## Uncertainty and metadata

- Uncertainty quantification is provided via per-pixel probabilities from the Random Forest classifier; summarized as a mean probability per polygon (and standard deviation where provided).
- The 25 m raster band 2 stores the mean per-polygon probability; 1 km products do not include per-polygon uncertainty.
- Rich metadata accompany the vector: polygon-level attributes, pixel-class distributions, and processing history.

## Citing and documentation

- Citing LCM2015 products requires their DOIs; documentation and further information available via CEH websites and the Environmental Information Centre.
- The dataset is stable/archived with DOIs to support repeatability and traceability in publications.

## Practical notes and cautions for users

- LCM2015 is not recommended for current-state change mapping in its present form; differences between maps arise from real change and classification error, compounded by evolving methods and data.
- Users should consult the methodological changes and class definitions (Appendices) to ensure consistent interpretation across versions and datasets.