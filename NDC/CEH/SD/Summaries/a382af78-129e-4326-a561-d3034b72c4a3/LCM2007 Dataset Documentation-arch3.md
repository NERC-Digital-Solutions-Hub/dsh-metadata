# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Purpose and scope
- Provides a parcel-based land cover classification (UK-wide) to support environmental monitoring, policy scrutiny, and future decision-making.
- Maps land cover (not land use) using 23 classes based on UK Biodiversity Action Plan Broad Habitats.
- Built from summer-winter satellite composites at 20–30 m, upgrading LCM2000 with a new spatial framework and image-segmentation.

## Data products and how they support monitoring
- Vector data set
  - Contains ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Each polygon has 10 attributes, including Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE (class code for display), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, and Construct method (OSMM-derived or segmented).
  - Features a unique Parcel_ID per polygon to support unambiguous communication and linking with other datasets.
  - Includes Broad Habitat sub-classes (BHSub) for enhanced interpretation, though these are not QA-validated at the same level as LCM2007 classes and should be validated by users for specific applications.
- Raster data sets
  - 25 m raster: 23 LCM2007 classes; derived from the vector dataset; supports detailed mapping at higher resolution.
  - 1 km raster: summary products derived from the 25 m data; includes dominant cover and percentage cover for both 23 LCM2007 classes and Aggregate classes (for national-scale analyses).
  - Separate products available for Great Britain and Northern Ireland with corresponding projections.
- Data formats, resolutions, and scales
  - Supports a range of thematic/spatial resolutions to accommodate diverse applications (local to national).
  - MMU: minimum mappable unit >0.5 ha; parcels smaller than 0.5 ha or linear features <20 m dissolved into surrounding landscape.

## Classes and interpretation
- 23 LCM2007 classes based on Broad Habitats (with some subdivisions):
  - Broadleaved woodland; Coniferous woodland; Arable and Horticulture; Improved Grassland; Semi-natural grassland (Rough grassland; Neutral grassland; Calcareous grassland; Acid grassland); Fen, Marsh and Swamp; Bog; Montane Habitats; Inland Rock; Saltwater; Freshwater; Supra-littoral Rock; Supra-littoral Sediment; Littoral Rock; Littoral Sediment; Saltmarsh; Built-up Areas and Gardens (Urban; Suburban).
- Some Broad Habitats are subdivided in LCM2007 (e.g., Built-up Areas and Gardens into Urban and Suburban; Heather vs Heather grassland; Littoral sediment vs Saltmarsh; Dwarf Shrub Heath into Heather and Heather grassland).
- Appendix 1 (class descriptions) and Appendix 2 (relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes) provide detailed mappings; Appendix 3 provides the colour mapping used in outputs.

## Metadata, data quality, and validation
- Rich metadata accompanying vector polygons, including processing history (KBE), source images, and spectral classification details.
- Validation against ground reference data: average accuracy ~83% across 9,127 polygons; local discrepancies may occur, as expected in remote sensing classifications.
- Knowledge-based enhancements (KBE) applied to improve classification where possible; ProbList lists top spectral matches to aid user validation.
- Caution on Broad Habitat sub-classes: not all sub-classes have QA-validated status; users should validate at the subclass level for specific analyses.

## Data access and licensing
- Data access:
  - 1 km raster data (dominant/percentage covers) available via the CEH Information Gateway.
  - Full vector product and 25 m raster product available on request under licence from CEH (applications via CEH data portal or contacting spatialdata@ceh.ac.uk).
- Licensing and fees may apply for some users and applications.
- Northern Ireland data use Irish National Grid; GB data use British National Grid. NI is transitioning to ITM projection.

## File sizes and data characteristics
- Vector data: extensive (nearly 10 million polygons) with 10 attributes each; substantial file sizes; shapefile example for 100 km x 100 km tiles.
  - GB vector: ~4.13 GB; NI vector: ~0.43 GB.
- Raster data:
  - GB 25 m: ~1.36 GB; NI 25 m: ~46 MB.
  - GB 1 km: ~21 MB to ~49 KB (depending on product).
- Data is designed to support a wide range of monitoring needs, from national trend assessment to finer-scale habitat mapping.

## Map projections and geographic coverage
- Great Britain vector and raster data: British National Grid (OSGB 1936).
- Northern Ireland vector and raster data: Irish National Grid (and ITM in transition).
- Outputs include both GB and NI datasets to accommodate jurisdictional requirements.

## Practical usage notes for policy monitoring
- Align outputs with Broad Habitat classifications to track policy-relevant habitats and changes over time.
- Use 1 km raster products for national-scale monitoring and trend analysis; use 25 m vector/raster products for finer-scale assessments or bespoke analysis requiring detailed polygon attributes.
- Retain Parcel_ID for clear communication and data linkage; be mindful that Broad Habitat sub-classes require independent validation for rigorous analysis.
- Reference Final Report for LCM2007 (Morton et al., 2011) and related Broad Habitat guidance (Jackson, 2000) for methodological context and nuances in habitat definitions.

## Access to further information
- Final Report for LCM2007: Morton, D. et al. 2011. Countryside Survey Technical Report No. 11/07.
- Broad Habitat interpretation guide: Jackson, D.L. 2000 (JNCC Report 307).
- Countryside Survey project: www.countrysidesurvey.org.uk
- Data access and contact: CEH Information Gateway; data@ceh.ac.uk; www.ceh.ac.uk/data

## Acknowledgements
- Acknowledges data sources and licensing from Landsat-TM5, SPOT, AWIFS, Ordnance Survey, and various government and research institutions; CEH and Countryside Survey partnership with contributions from multiple agencies.