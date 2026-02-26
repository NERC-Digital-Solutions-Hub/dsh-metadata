# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover map classifying satellite data into 21 classes, based on UK Biodiversity Action Plan Broad Habitat definitions.
- Built mainly from Landsat-8 (30 m) and supplementary AWIFS data (60 m); updates the 2007 LCM and aligns with the LCM2007 spatial framework.
- LCM2015 is designed to support a broad user community with a repeatable method suitable for change mapping, but the document cautions that differences between LCM products mean LCM2015 should not be used for current state change mapping without awareness of limitations.

## Data products
- Core vector dataset: 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland, each with rich attributes.
- 25 m raster product: two-band raster (band 1 = dominant class per polygon; band 2 = mean per-polygon probability).
- 1 km raster products: dominant cover (for 21 target classes and 10 aggregate classes) and percentage cover (21 bands for GB; 10 aggregated bands for GB; NI equivalents exist).
- All products are exchangeable through a range of formats; each dataset has a Digital Object Identifier (DOI) for citation.
- Spatial coverage and projections: GB in British National Grid; NI in Irish National Grid; GB and NI 1 km and 25 m rasters have separate metadata and coordinate details.

## Classification and methodology
- Algorithm: Random Forest classifier (replacing previous Maximum Likelihood Classifier used in LCM2007).
- Training and inputs: Stable initial training areas derived from 2000 and 2007 classifications, augmented for coastal/intertidal areas and hard-to-map classes; ancillary data (e.g., slope, proximity to rivers) integrated as needed within the input data rather than post-classification rules.
- Output data handling: Per-pixel classification with no spectral sub-classes; consistent labels at polygon level by modal_class; uncertainty captured as mean per-polygon probability and standard deviation.
- Spatial framework: LCM2015 does not use segmentation-based polygons; aims for per-pixel classification to ease future change mapping and inter-comparison.
- Data products relationship: Vector core informs 25 m raster; 1 km products are derived to support modeling and cross-dataset analyses.

## Data structure and metadata
- Vector data: 21 target land cover classes with 23-pixel-level breakdown per polygon, plus dominant class, gid (unique geometry ID), uncertainty metrics, and composition details.
- 25 m raster: band 1 = dominant class; band 2 = mean per-polygon probability.
- 1 km rasters: dominant class and aggregates with percentage cover (rounded integers; coastal areas may sum to less than 100% due to MMU and mapping limits).
- Unique labels and gid are recommended for maintaining unambiguous communication of features.
- Metadata: Rich metadata for each polygon; DOIs for all products; clear provenance and processing history included where possible.
- Uncertainty: Random Forest provides per-pixel probability estimates, summarized per polygon and available in corresponding products.

## Access, citation, and licensing
- Data access: 1 km raster data available via CEH Environmental Information Platform; full vector and 25 m raster available on request under licence.
- Licensing: Some users may incur licence fees; licensing terms available via CEH portals.
- Citation: All LC M2015 products have DOIs; recommended citation includes author list, date, and DOI (formats provided in the dataset documentation).
- Projections: GB data in British National Grid; NI data in TM75 Irish Grid.
- Contact: spatialdata@ceh.ac.uk; CEH website for additional information and access instructions.

## Cautionary notes and differences from LCM2007
- The montane class is removed in favor of reclassification based on spectral data; Montane areas mapped as Inland Rock or other upland habitats in LCM2015.
- Rough grassland class removed to align grassland types with JNCC Broad Habitat definitions; no soil data used in LCM2015 classifications.
- 25 m raster is two-band (classification band and mean probability) vs. single-band in older products.
- Probability data no longer provided as a separate ProbList per polygon in the vector; now available as mean polygon probability and in band 2 of the 25 m raster.
- Spectral sub-classes are no longer used; Random Forest handles multi-model data, reducing the need for spectral sub-class training.
- The segmentation-based spatial framework of LCM2007 is removed in LCM2015 to improve consistency and reduce segmentation-related errors; this primarily affects GB vector and 25 m raster products.
- Mixed woodland is handled using pixel-level classification with modal_class assignment for polygons; users can examine pix_dist for detailed composition.
- LCM2015 focuses on land cover rather than land use; some land uses may not be distinguishable spectrally (e.g., recreational grass vs. grazed grass).

## Governance and data stewardship implications
- LCM2015 provides a stable, archived dataset with clear DOIs and rich metadata to support reproducibility, attribution, and long-term data stewardship.
- The gid attribute and comprehensive polygon-level metadata support data provenance and traceability across datasets and analyses.
- Data stewards should plan for updates and versioning, maintain linkage to DOIs, and ensure proper citation in publications.
- Access controls and licensing considerations should be managed per the CEH information products policy; vector and 25 m data may require licensing or permission.
- Given differences from earlier products, data stewards should document methodological changes when integrating LCM2015 with prior datasets or during change mapping efforts.

## Contacts and further information
- CEH contact: spatialdata@ceh.ac.uk
- Data and documentation: https://www.ceh.ac.uk/services/land-cover-map-2015 and https://eip.ceh.ac.uk/lcm
- Data paper and DOIs: provided within the dataset documentation; guidance on data citation and DOI usage available via the CEH and eidc portals.