# Land Cover Map 2015

## Overview
- UK-wide, parcel-based land cover map providing 21 classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- Created from two-date Landsat-8 composites (30m) with AWIFS data as needed; later updates align with the LCM2007 framework.
- Produces multiple data products to support diverse monitoring needs: a core vector dataset, a 25m raster, and 1km aggregate products.
- Intended to support environmental health monitoring, policy scrutiny, and future decision-making; emphasizes data provenance, metadata, and uncertainty.

## Data Products and Structure
- Vector data set
  - 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Nine attributes per polygon, including dominant class (Modal_class), pixel counts per class (Pix_dist), uncertainty, and geometry identifier (gid).
  - Provides rich metadata and per-polygon uncertainty (mean probability from classification).
- 25m raster
  - Two-band raster: Band 1 = dominant LCM2015 class per polygon; Band 2 = mean per-polygon probability from Random Forest.
- 1km raster
  - Summary products derived from 25m data: dominant class at 1km, percentage cover per class (21 bands), and dominant/percentage products for 10 aggregate classes.
  - Coarse-resolution products suitable for national-scale modelling.
- Class mappings
  - 21 target classes mapped to Broad Habitats; some Broad Habitats are further subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban).
- Provenance and citations
  - Each product has a Digital Object Identifier (DOI) for citation and reproducibility.
- Spatial reference
  - Great Britain: British National Grid; Northern Ireland: Irish Grid.
- Size and format notes
  - 1km products provide aggregated information; 25m and vector products contain full detail and metadata.
- Access
  - 1km raster via CEH Environmental Information Platform (EIP).
  - Full vector and 25m products available under licence on request (licensing fees may apply).

## Methodology and Technical Changes
- Classification approach
  - New Random Forest classifier replaces previous Maximum Likelihood classification; handles multi-model training data without spectral sub-class grouping.
- Training data and ancillary data
  - Training areas constructed from a stable set classified similarly in 2000 and 2007, then augmented for coastal areas and classes requiring better representation.
  - Ancillary data (e.g., altitude, soil, distance to rivers) are integrated as inputs rather than post-classification refinements.
- Spatial framework
  - No segmentation-based polygons in LCM2015; per-pixel classification with a per-polygon aggregation to produce vector and raster outputs.
- Output and data structure differences
  - Montane class removed to enable robust change mapping; areas previously mapped as Montane now reclassified as Inland Rock or other upland habitats.
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitats without soil-data-based sub-classing.
  - 25m raster now two bands; probability data reorganized (vector: mean polygon probability; 25m raster: band 2).
  - Spectral sub-classes eliminated; no need for spectral sub-class training data.
  - Spatial segmentation removed from the 2015 spatial framework; reduced segmentation in upland areas.
- Woodland classification
  - Mixed woodland defined by >20% deciduous cover; training uses pure stands for convolution; polygon labels derived from modal_class after pixel-level classification.
- Output scope
  - LCM2015 maps land cover (not land use); includes per-polygon probabilities and detailed metadata for analyses and reproducibility.

## Classifications and Metadata
- 21 LCM2015 target classes (based on JNCC Broad Habitats) with mappings to aggregate 1km classes where applicable.
- Some classes offer finer splits (e.g., within Broad Habitat groups) to support diverse analyses.
- Unique labeling
  - Each parcel has a gid (geometry id) for unambiguous communication and cross-referencing.
- Metadata richness
  - Each polygon includes dominant class, per-class pixel counts, mean probability, and other descriptive attributes.
- Uncertainty
  - Per-polygon probability provided (uncertainty metric) from the Random Forest classifier.
- Colour mapping and documentation
  - Appendix materials describe colour mappings and class definitions; Table 1 and Tables in the documentation outline the 21 classes and their relationships to Broad Habitats.
- Citing and reproducibility
  - Each product has a DOI; users are encouraged to cite DOIs when publishing or modelling with LCM2015 data.

## Data Quality, Limitations, and Considerations for Monitoring
- Change mapping caveat
  - Differences between LCM versions reflect real changes and classification errors; the LCM2015 document cautions users that the LCM series can exhibit inconsistencies over time.
- Data quality and metadata gaps
  - Some data shortcomings exist (metadata gaps; data sharing issues; “silos” between organisations can hinder access).
- Data timeliness and updates
  - While LCM2015 is positioned as a stable, archived dataset, the users should be aware of its historical nature and review changes when comparing across years.
- Technical details affecting use
  - Minimum mapping unit: parcels >0.5 ha; linear features <20 m dissolve into surrounding landscape.
  - 1km products employ rounding; sums of percentages may not equal exactly 100% due to rounding and coastal extents.
  - Intertidal and coastal complexities addressed through stable training data selections; some tidal-state issues remain considerations for coastal analyses.
- Practical implications
  - For policy monitoring, use vector metadata and per-polygon probabilities to quantify confidence; use 1km products for large-scale modelling, and 25m products for detailed site-level assessments.
  - The removal of segmentation and introduction of a per-pixel framework enhances change-detection capabilities but requires careful handling of class definitions and aggregation rules.

## Data Access, Citation, and Governance
- Data access and licensing
  - CEH EIP hosts 1km raster data; full vector and 25m products available on request under licence; fees may apply.
- Projections and geographic scope
  - GB in British National Grid; NI in Irish Grid; separate datasets for GB and NI.
- DOIs and citation guidance
  - Each product set (vector, 25m raster, 1km rasters for GB and NI) has dedicated DOIs; publications should cite the DOIs and include authorship and date.
- Documentation and support
  - Detailed documentation, including Appendix 1–4 (class definitions, colour mapping, composite images), provided to support proper use and interpretation.
- Contact
  - Spatialdata@ceh.ac.uk for queries and data requests.

## Implications for Monitoring Framework Authors
- LCM2015 provides a robust, well-documented land-cover baseline with explicit uncertainty metrics, enabling transparent policy evaluation and trend analysis.
- The integration of ancillary data into the classifier improves objectivity and reproducibility, aligning with data governance requirements.
- Comprehensive metadata and DOIs support reproducible monitoring, bibliographic citation, and data provenance tracking.
- For policy monitoring, prefer:
  - 1km aggregate products for nationwide modelling and trend analysis.
  - 25m raster for change detection and local-scale assessments (understanding the accompanying metadata and probability information).
  - Vector data when detailed parcel-level attributes and per-polygon uncertainty are required.
- Be mindful of caveats around change detection across versions and the need to align class definitions with monitoring objectives and habitat classifications.