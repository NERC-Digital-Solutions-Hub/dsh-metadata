# Dataset documentation

- Purpose and scope
  - Land Cover Map 2015 (LCM2015) provides parcel-based UK land cover maps in 21 classes, aligned with UK Biodiversity Action Plan Broad Habitats.
  - Built from two-date composite satellite images (mainly Landsat-8 at 30 m, supplemented by AWIFS at 60 m) to support environmental monitoring and policy performance over time.
  - Notes: not recommended to use LCM2015 in its current form for change mapping; differences between LCM products reflect real change and classification differences over time.

- Key data outputs and formats
  - Vector data set (core product): polygons with rich attributes (gid, dominant class, pixel counts per class, uncertainty, modal_class, etc.); approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - 25 m raster: two-band raster (band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from the Random Forest classifier).
  - 1 km raster products: dominant class and percentage cover for both 21 target classes and 10 aggregate classes; derived from the 25 m raster.
  - Minimum mapping unit: >0.5 ha; parcels smaller than 0.5 ha or linear features <20 m are dissolved into surrounding landscape.
  - Spatial detail ranges from per-polygon vector to 25 m raster to 1 km aggregated products.

- Classification and methodology
  - New classifier: Random Forest (RF) replaces previous Maximum Likelihood Classifier; RF handles multi-model training data and reduces need for spectral sub-classes.
  - Training data and stable areas: training areas built from areas consistently classified in 2000 and 2007, with additional coastal and challenging classes; ancillary data integrated as inputs rather than post-classification rules.
  - Ancillary data and knowledge-based enhancements: moved into the input data for objective classification, reducing manual rule-crafting.
  - No spectral sub-classes: sub-classes deemed redundant; classification outputs are the 21 target classes presented at polygon level.
  - Spatial framework: no segmentation-based polygons in LCM2015; per-pixel classification, designed to simplify change mapping across time.
  - Mixed woodland handling: pixels summarized to polygons; training uses pure stands for coniferous and broadleaf classifications; pix_dist attribute provides per-pixel detail.
  - Data products are designed to support multiple applications, including modelling at various resolutions.

- LCM2015 classes and labelling
  - 21 target classes tied to broad habitats; some classes are further subdivided in the raster datasets (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral habitats subdivided into Littoral Rock, Littoral Sediment, Saltmarsh, etc.).
  - Unique gid attribute for unambiguous feature communication; rich metadata for each polygon, including dominant class and pixel-level breakdown.

- Uncertainty and data provenance
  - RF provides per-pixel probability; expressed as mean per-polygon probability in vector and as band 2 in the 25 m raster.
  - Per-polygon uncertainty (unc) and standard deviation (unc_stdev) included in vector attributes.
  - DOI-based citation system for each product; per-product DOIs supplied for GB and NI outputs.

- Data access and projections
  - Great Britain vector and 25 m raster; Northern Ireland vector and rasters; separate projections for GB (British National Grid) and NI (TM75 Irish Grid).
  - Data access:
    - 1 km raster products: available via CEH Environmental Information Platform (eip.ceh.ac.uk).
    - Full vector and 25 m raster products: available on request under licence from CEH; licensing may apply.
  - Citations: each product has a DOI; guidance provided for citing in publications.

- Differences from previous LCM versions (LCM2007)
  - Change in output data handling (montane and rough grassland classes removed; re-classified using spectral data in 2015).
  - 25 m raster now two-band; probability data recorded differently.
  - Transition from Maximum Likelihood to Random Forest classifier.
  - Ancillary data used as inputs rather than separate post-classification rules.
  - Segmentation-based spatial framework removed; per-pixel approach adopted.
  - Mixed woodland training approach updated; polygon labeling uses modal class.

- Data product overview and documentation
  - Core vector product, 25 m raster, and 1 km dominant/percentage products cover GB and NI with a range of resolutions and formats.
  - Appendices provide detailed mappings between LCM2015 classes and Broad Habitat definitions, colour mapping, and composite image information.
  - Each product has dedicated DOIs to support reproducibility and traceability.

- Usage guidance and cautions
  - LCM2015 maps land cover (not always directly interchangeable with land use).
  - Some grassland and peat-related habitats can be spectrally similar; caution advised when aggregating classes or interpreting specific categories.
  - Change mapping should consider differences in methodology and class definitions between LCM2015 and earlier maps.

- Updates and version history
  - Version 1.0: Original release (April 6, 2017).
  - Version 1.1: Publication year corrected in Tables 4 and 5 (May 4, 2017).
  - Version 1.2: Updated vector attribute “composite” in Table 2 (May 22, 2017).

- Contact and additional information
  - Contact: CEH Spatial Data, plus informational links for further details and access:
    - www.ceh.ac.uk
    - https://www.ceh.ac.uk/services/land-cover-map-2015
    - https://eip.ceh.ac.uk/lcm
  - Data citation references and data-provision procedures outlined within the document.