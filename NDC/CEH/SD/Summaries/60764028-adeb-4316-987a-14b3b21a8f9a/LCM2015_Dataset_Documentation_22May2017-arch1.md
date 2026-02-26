# Dataset documentation

- UK-wide Land Cover Map 2015 (LCM2015) is a parcel-based land cover map created from two-date satellite composites, classifying into 21 Broad Habitat (BH) classes based on UK Biodiversity Action Plan definitions.
- Primary data sources: Landsat-8 (30 m) with AWIFS (60 m) as needed; outputs include a core vector dataset, a 25 m raster, and 1 km aggregated products.
- Purpose and cautions: designed to support diverse user needs; differences between maps reflect real change and classification differences, so users should avoid treating LCM2015 as a direct change-metection product without careful validation.

## What LCM2015 is and what it contains

- Lands and scope: UK parcel-based map with polygons reflecting real-world boundaries; created from two-date composites and aligned to a stable spatial framework.
- Classes: 21 target classes based on JNCC Broad Habitats; some classes split or merged for mapping and analysis (e.g., subdivisions within Broad Habitat types; urban/suburban distinctions).
- Products (data tiers):
  - Core vector data set: per-polygon attributes plus metadata.
  - 25 m raster: two-band product (band 1 = dominant class per polygon; band 2 = mean per-polygon probability from classifier).
  - 1 km raster: dominant class and percentage cover products for both 21-class and 10-aggregate schemes.
- Uncertainty and metadata: includes per-polygon mean probability, standard deviation, and pixel-level probabilities; rich metadata and documented uncertainty information.
- Identifiers: each parcel has a unique gid; vector product includes extensive attributes per polygon.

## Data products and structure

- Vector data set
  - Polygons: GB ~6.7 million; NI ~0.9 million.
  - Key attributes: gid, BHAB (dominant BH), Pix_dist (counts per class within polygon), unc (mean probability 0–255), unc_stdev, npix, Modal_class (1–21), Modal_prop, Composite.
- 25 m raster
  - Band 1: dominant LCM2015 class per polygon.
  - Band 2: mean per-polygon probability from Random Forest classifier.
- 1 km raster
  - Products: 1 km dominant cover (21-class and aggregate), 1 km percentage cover (21-band and 10-band aggregate).
  - Note: percentage values are integers; sums may slightly deviate from 100 due to rounding; coastal pixels may sum to less than 100.
- Data formats and projections
  - GB vector and GB 25 m raster: British National Grid (EPSG 27700).
  - NI 25 m and NI 1 km rasters: TM75 Irish Grid (EPSG 29903).
- DOIs and citation
  - Each LCM2015 product (vector, 25 m, 1 km GB and NI variants) has a DOI; guidance provided for citing in publications.

## Methodology and classification

- Classifier: Random Forest (RF) used for per-pixel classification; avoids spectral-subclass grouping required by previous methods.
- Training data and stability
  - Initial training areas derived from areas consistently classified the same in 2000 and 2007; augmented with coastal areas and hard-to-map classes.
  - Ancillary data (e.g., slope, distance to rivers) are integrated as inputs, not post-classification corrections.
- Use of ancillary data
  - Unlike earlier methods, ancillary data are part of the input and influence classification during model training.
- Output design
  - Per-polygon probabilities are provided via the 25 m raster band and vector attributes; per-polygon uncertainty measures accompany the dominant class.
  - No segmentation-based spatial framework in LCM2015; per-pixel (per-polygon) approach emphasizes a per-pixel classification with subsequent aggregation for 1 km products.

## Differences from LCM2007 (and implications)

- Montane class removed: mapped as Inland Rock or other upland habitats based on spectral data; Montane distribution from LCM2007 should be used if required.
- Rough grassland removed: grassland types now align with JNCC Broad Habitats; no soil data used in LCM2015 classification.
- 25 m raster changes: now a two-band raster (classification band + probability band).
- Probability data: simplified in 2015 (mean per-polygon probability in vector; mean probability in band 2 of 25 m raster; no probability data for 1 km products).
- Subclasses: spectral sub-classes removed; RF handles multi-modal classes without needing spectral sub-classes.
- Spatial framework: segmentation removed; per-pixel classification without image-segmentation-based polygons; affects mainly GB vector and 25 m raster.
- Mixed woodland labeling: training now uses pure stands; modal_class assigned at polygon level; users may inspect pix_dist for detailed composition.

## Classes and mapping details

- 21 target LCM2015 classes (mapped to broader BH types); some groups have sub-divisions (e.g., Suburban vs Urban; Dwarf Shrub Heath split into Heather and Heather grassland; Littoral classifications split into multiple coastal habitats).
- Aggregate classes: 10 aggregates used for 1 km products to simplify applications requiring fewer classes.
- Relationship notes: table mapping between LCM2015 target classes, their Broad Habitat counterparts, and aggregate classes; detailed color mapping and labeling conventions provided in appendices.

## Data quality, uncertainty, and cautions

- Uncertainty: RF provides per-pixel probability; vector includes mean polygon probability; standard deviation captured as unc_stdev.
- Change mapping cautions: LCM2015 differences reflect both real change and methodological changes; LCM2015 is designed as a stable, archive-quality product rather than a strict time-series change detector.
- Minimum mapping unit: parcels smaller than 0.5 ha or linear features less than 20 m are dissolved into surrounding landscape.
- No direct inference of land use in all cases; arable/pasture distinctions may not always map cleanly to land use.

## Access, licensing, and usage guidance

- Access
  - 1 km raster data: available via CEH Environmental Information Platform (EIP).
  - Full vector and 25 m raster products: available on request under license; fees may apply.
- Usage notes
  - Data should be cited with DOIs; include authors and dates in text and full DOI in references.
  The dataset is intended for broad usage across land cover mapping, modelling, and ecological applications, with attention to the differences from prior LCM versions when combining with historical data.

## Projections, extents, and technical details

- Projections and extents: GB and NI datasets provided in their respective national grid systems; necessary metadata included for precise georeferencing.
- MMU and dataset structure: stable training areas; per-polygon labels; comprehensive polygon attributes; file-level metadata intended to support discoverability and reuse.

## Appendices and supporting information

- Appendix 1 and 2: definitions and mapping guidance for Broad Habitats and corresponding LCM2015 classes.
- Appendix 3: standard colour mapping recipe for LCM2015 classes.
- Appendix 4: composite image metadata used in LCM2015 production.
- References: foundational documents for Broad Habitat definitions and LCM2007 methodology.