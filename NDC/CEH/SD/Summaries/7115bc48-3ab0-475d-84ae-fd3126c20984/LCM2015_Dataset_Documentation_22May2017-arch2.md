# Dataset documentation

- LCM2015 (Land Cover Map 2015) is a parcel-based UK land cover map produced from satellite data (Landsat-8 mainly, plus AWIFS) classified into 21 Broad Habitat classes aligned with JNCC Broad Habitat definitions.
- Purpose: provide multiple data products to support diverse user needs, with rich metadata and uncertainty information to aid analysis and interpretation.

## Important cautions for users

- LCM2015 is complex and not recommended for change mapping in its current state.
- Differences between LCM products over time mean changes reflect real changes plus classification and methodology differences; users should treat cross-year comparisons with care.
- Differences in data format and class definitions from previous LCM versions can affect script compatibility and outputs.

## What LCM2015 is and how it was produced

- Classifies two-date composite images into 21 land cover classes, based on UK Biodiversity Action Plan Broad Habitat definitions.
- Data sources: Landsat-8 (30 m) primarily, supplemented by AWIFS (60 m) as needed.
- Output framework: per-polygon polygons reflecting real-world boundaries; similar to LCM2007 but with methodological upgrades.
- Spatial framework: GB and NI use OS-based and regional base maps; GB typically in British National Grid, NI in Irish Grid.

## Key differences from LCM2007 (output, methodology, framework)

- Output data
  - Montane class removed; upland areas reclassified using spectral data (now as Inland Rock or other upland habitats).
  - Rough grassland class removed; grassland types now match JNCC Broad Habitats without relying on soil data.
  - 25 m raster becomes a two-band image: band 1 is class, band 2 is mean per-polygon probability.
  - Probability data: simplified, with mean per-polygon probability in vector and band 2; not provided for 1 km products.
  - No spectral sub-classes; sub-classes deprecated due to Random Forest classifier.
  - Spatial framework: segmentation-based polygons removed; per-pixel classification with per-polygon modal class for outputs.
  - Mixed woodland training relies on pure stands and pixel-based classification with modal class at polygon level.
- Methodology
  - New classifier: Random Forest (versus Maximum Likelihood in 2007).
  - Stable training areas used as a starting point, expanded with coastal and difficult classes.
  - Ancillary data (slope, distance to rivers, etc.) are input data for classification, integrated rather than applied post-classification.
- Output and mapping philosophy
  - LCM2015 maps land cover (not land use) and uses per-pixel classifications summarized to polygons.
  - Minimum mappable unit: >0.5 ha; dissolves smaller parcels and very small linear features.

## LCM2015 data products and structure

- Vector data set
  - Core vector product with 6.7 million GB polygons and 0.9 million NI polygons.
  - Attributes include: gid (unique parcel ID), BHAB (dominant Broad Habitat class), pix_dist (counts of pixels per class), uncertainty (mean per polygon probability), npix, modal_class (dominant class code), modal_prop, Composite (source composite image number), among others.
- 25 m raster
  - Two-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from Random Forest.
- 1 km raster (dominant and percentage cover)
  - Dominant class per 1 km pixel (both for 21 classes and 10 aggregate classes).
  - Percentage cover per 1 km pixel for each class (21 bands for GB; aggregated 10 bands for aggregates).
  - Rounding can mean sums differ from 100; coastal pixels sum to less than 100 due to mapping extents.
- Spatial coverage and projection
  - Great Britain and Northern Ireland provided separately with respective projections (GB: British National Grid; NI: TM75 Irish Grid).
  - Parceled data ensure compatibility with other geospatial datasets; per-polygon gid facilitates unambiguous communication.
- Resolution and data limits
  - Minimum mapping unit >0.5 ha; features smaller are dissolved into surrounding landscape.
  - Some coastal and intertidal areas removed from stable training data; inter-tidal areas excluded from coastal training.

## Data access and citation

- 1 km raster data are accessible via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector and 25 m raster products are available under license on request from CEH (spatialdata@ceh.ac.uk); license fees may apply.
- Each LCM2015 product has its own DOI for citation; GB and NI datasets have separate DOIs.
  - DOIs should be cited in publications, with full DOI references provided in the dataset documentation.
- Data usage notes and DOIs are provided to promote repeatability and proper attribution.

## Products in detail

- Core vector product
  - Contains per-polygon attributes: gid, BHAB (dominant Broad Habitat), pix_dist (detailed pixel counts), unc (probability), unc_stdev, npix, modal_class, modal_prop, composite.
- 25 m raster
  - Two bands: band 1 = dominant class code; band 2 = mean per-polygon probability.
- 1 km products
  - Dominant cover by class (1 km, 1 band) and by aggregate class (1 km, 1 band).
  - Percentage cover by class (21 bands) and by aggregate class (10 bands).
  - GB and NI have separate product sets and projections (see metadata tables for specifics).
- Mapping and labeling
  - 21 LCM2015 target classes aligned to JNCC Broad Habitat equivalents; some classes are further subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral Sediment and Saltmarsh).

## Metadata, uncertainty, and colour mapping

- Rich metadata accompanies the vector: dominant class, pixel breakdown, and mean polygon probability.
- Uncertainty is quantified via per-polygon probability from the Random Forest classifier; available for vector and 25 m raster (not for 1 km products).
- Standard color mapping is provided (Appendix 3) to ensure consistent visualization across platforms.

## Additional information and references

- Background and definitions align with Jackson (2000) Broad Habitat framework.
- Methodological context and historical evolution described with references to Morton et al. (2011) and related LCM reports.
- Acronyms and definitions explained in the appendices, along with guidance for class interpretation and potential caveats.

## Access, contact, and further information

- Data access details and contact: spatialdata@ceh.ac.uk; CEH websites for LCM2015 and data access.
- Project and data paper status: LCM2015 data papers prepared; DOIs and citation guidance provided for reuse and reporting.