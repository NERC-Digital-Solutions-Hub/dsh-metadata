# Dataset documentation

- LCM2015 is a parcel-based UK land cover map with 21 classes based on UK Biodiversity Action Plan Broad Habitats, produced from two-date Landsat-8 (30 m) composites (plus AWIFS as needed). It updates the 2007 map (LCM2007) and uses a per-polygon (gid) approach aligned to real-world boundaries for easier interpretation and compatibility with other geospatial data.
- The dataset is designed to support diverse environmental monitoring needs, including informing policy scrutiny, evaluation, and future decision-making.

## Data products and contents

- Core vector product: polygons with rich attributes for each parcel, including dominant class, detailed pixel breakdown within the polygon, and uncertainty metrics.
- Raster products: 25 m two-band raster (band 1: dominant class, band 2: mean per-polygon RF probability) and 1 km raster products (dominant class, dominant aggregate class, and percentage cover for both 21 classes and 10 aggregates).
- Spatial coverage and projections:
  - Great Britain: British National Grid (BNG)
  - Northern Ireland: Irish National Grid (TM75 Irish Grid)
- Data scale and mapping:
  - Minimum mappable unit: >0.5 ha
  - Parcels smaller than 0.5 ha or line features <20 m dissolved into surrounding area
- Class structure:
  - 21 LCM2015 target classes, tied to Broad Habitats; some classes are further subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban)
  - Aggregate classes (for 1 km rasters) provide simpler, policy-relevant groupings
- Unique identifiers and metadata:
  - Each vector parcel has a unique gid; metadata-rich polygons include dominant class, pixel distribution (Pix_dist), and mean polygon uncertainty
  - DOIs are provided for each product to support citation and reproducibility

## Methodology and key differences from LCM2007

- Classification algorithm:
  - LCM2015 uses Random Forest instead of Maximum Likelihood, enabling multi-modal training data handling and often improved performance.
- Training data and approach:
  - Training areas derived from stable data between 2000 and 2007, then expanded (including coastal and poorly mapped classes); ancillary data are integrated as input features rather than post-classification rules.
- Spatial framework and segmentation:
  - No segmentation-based spatial framework in LCM2015 (removes the segmentation approach used in LCM2007) to avoid mismatch with classification and improve change mapping flexibility.
- Data products and outputs:
  - Removal of Montane and Rough Grassland classes; grassland types re-aligned with JNCC Broad Habitats
  - 25 m raster now two bands; per-polygon and band-2 probabilities provide uncertainty; spectral sub-classes are deprecated due to RF classifier
  - Mixed woodland training moved to per-pixel classification with polygon-level summarisation
- Land cover mapping scope:
  - LCM2015 maps land cover (not strictly land use); certain land uses (e.g., arable vs. grassland) may be ambiguous without field data

## Data quality, uncertainty, and cautions

- Uncertainty:
  - RF provides per-pixel probability; polygon-level mean probability is included in vector data and band 2 of the 25 m raster
- Important cautions:
  - Do not rely on LCM2015 in its current state for change mapping without considering methodological differences and potential classification changes over time
  - Differences in output data between LCM2007 and LCM2015 may affect longitudinal analyses; users should review methodological notes before applying scripts from LCM2007

## Data access, licensing, and citation

- Data access:
  - 1 km raster products available via CEH Environmental Information Platform (EIP)
  - Full vector and 25 m raster products available on request under licence from CEH (fees may apply)
- Citation and DOIs:
  - All LCM2015 products have DOIs for proper citation (GB vector, GB 25 m raster, GB 1 km percentage/dominant target classes, GB 1 km aggregate classes; NI vector, NI 25 m raster, NI 1 km percentage/dominant classes, NI 1 km aggregate classes)
  - Example citation guidance provided; include author names, year, and full DOI in references
- Metadata and documentation:
  - LCM2015 provides rich polygon metadata (dominant class, pixel distribution, mean probability, etc.)
  - Documentation explains class definitions, colour mapping, and the relationship between LCM2015 classes and Broad Habitats
- Data paper and contact:
  - Data paper in preparation; for more information contact spatialdata@ceh.ac.uk

## Appendices and classification references

- Appendix content offers detailed definitions of Broad Habitat classes (per JNCC/Biodiversity Broad Habitat framework) and how LCM2015 maps these categories
- Class mapping and colour legend are specified to enable consistent visualization and interpretation

## Practical notes for policy monitoring and evaluation

- LCM2015 provides a robust, repeatable framework for monitoring UK land cover at multiple resolutions (vector, 25 m, 1 km) with explicit uncertainty information
- The per-polygon gid and detailed attribute sets support auditing, provenance tracking, and governance requirements for data used in environmental health monitoring
- The integration of ancillary data into the classification process enhances transparency and objectivity, aiding data governance and reproducibility in policy assessments
- Users should plan for data access requirements, potential licensing fees, and the need to align LCM2015 outputs with current monitoring frameworks and change-mapping objectives, given known differences from prior maps and cautions about change-mapping suitability.