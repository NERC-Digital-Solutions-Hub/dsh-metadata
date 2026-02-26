# Dataset documentation

- Purpose and scope
  - LCM2015 (Land Cover Map 2015) provides a UK parcel-based land cover map classified into 21 classes, based on UK Broad Habitat definitions.
  - It supports a wide user community with data products in multiple formats and resolutions, including vector, 25m raster, and 1km summaries.
  - It is a stable, archived dataset with DOIs for citation; CI caution: not recommended for change mapping in its current state due to real changes vs. classification errors.

- Data sources and method
  - Derived from two-date composite satellite imagery, mainly Landsat-8 (30m) with AWIFS (60m) as needed.
  - Uses ancillary data as part of the input, not post-classification rules.
  - Classifier: Random Forest (instead of previous Maximum Likelihood) to handle multi-modal training and reduce need for spectral sub-classes.
  - Training areas built from stable data (areas consistently classified across 2000 and 2007) supplemented for coastal and challenging classes.

- Spatial framework and outputs
  - Output data are polygonal (vector) with per-polygon metadata, reflecting real-world boundaries; no segmentation in the final framework to improve change mapping consistency.
  - Minimum mapped unit: >0.5 ha; very small parcels and very short lines dissolved into surrounding landscape.
  - Core products:
    - Vector data set (6.7 million polygons GB, 0.9 million NI) with rich attributes.
    - 25m raster (two-band: band 1 = dominant class, band 2 = mean per-polygon probability).
    - 1km raster products: dominant class, dominant aggregate class, and 21-band/10-band percentage covers.
  - 21 target classes align with JNCC Broad Habitats; certain broadly mapped habitats are further subdivided in the 21-class system.
  - Special labeling: each parcel receives a unique geometry id (gid) for unambiguous referencing; polygon attributes include dominant class (Modal_class) and a detailed breakdown of pixel counts per class (Pix_dist).

- Class definitions and data details
  - 21 LCM2015 classes based on UK Broad Habitats; examples include Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Bracken, Dwarf Shrub Heath, Fen/Marsh/Swamp, Bog, Standing Open Water, Rivers/Streams, Montane, Inland Rock, Built-Up Areas and Gardens (split into Urban and Suburban), Supralittoral/Littoral/Coastal variations, and more.
  - Some Broad Habitats are split or regrouped to support detection and mapping; e.g., Built-up Areas and Gardens are divided into Urban and Suburban; Littoral/Coastal classes provide finer coastal distinctions.
  - The dataset provides uncertainty information: per-polygon mean probability (from Random Forest) and standard deviation; per-polygon composite indicator for the source imagery.

- Data products and formats
  - Vector: polygon features with 9 core attributes (including gid, BHAB/dominant class, Pix_dist, unc, npix, Modal_class, Modal_prop, and Composite).
  - 25m raster: two-band product (classification in band 1, per-polygon mean probability in band 2).
  - 1km raster: dominant cover per class and percentage cover per class (both for 21 target classes and 10 aggregate classes).
  - Spatial references: Great Britain uses British National Grid; Northern Ireland uses TM75 Irish Grid; separate datasets and projections for GB and NI.

- Access, licensing and citation
  - 1km raster data are accessible via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25m products are available on request under licence from CEH (pricing may apply).
  - Each product has its own DOI for citation, facilitating reproducibility (GB vector and raster DOIs; NI vector and raster DOIs; 1km percentage/dominant products DOIs).
  - Projections and metadata are documented; include full DOIs in publications.

- Practical guidance and cautions for data use
  - LCM2015 is complex; users should consult the dataset documentation to understand methodological changes and data interpretation.
  - Avoid using LCM series for change mapping in its current state due to a mixture of real change and classification error; differences between maps reflect both real change and classification alterations.
  - Changes from previous LCM versions (notably LCM2007) include removal of the Montane and Rough Grassland classes, a shift to Random Forest classification, integrated use of ancillary data, elimination of segmentation in the spatial framework, and revised training data strategies.
  - Spectral sub-classes are largely deprecated with Random Forest; users should rely on the 21 target classes and the uncertainty information for interpretation.
  - For Northern Ireland, data structures and coordinates differ from Great Britain; always use the correct NI/Gb datasets and projections when analyzing cross-region data.

- Documentation and further information
  - The dataset comes with extensive appendices describing class mappings and colour legends; detailed instructions on colour coding and composite images are provided.
  - Additional information and updates are available via the CEH pages and the dataset’s DOI entries.