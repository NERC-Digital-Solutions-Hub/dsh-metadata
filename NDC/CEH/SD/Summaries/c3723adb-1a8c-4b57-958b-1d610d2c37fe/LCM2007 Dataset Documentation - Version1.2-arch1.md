LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- Land Cover Map 2007 (LCM2007) is a parcel-based classification of UK land cover using 23 classes aligned with UK Broad Habitats.
- It maps land cover (not land use) from summer-winter satellite composites at 20–30 m pixels.
- MMU: minimum mappable area > 0.5 ha; parcels smaller than 0.5 ha or lines < 20 m are dissolved into surroundings.

## Data Products and Formats
- Vector Data Set
  - 8.6 million polygons (GB) and 0.9 million polygons (NI).
  - 10 attributes per polygon (Table 1): Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels.
  - Unique Parcel_ID for each polygon; BHSub provides Broad Habitat sub-class descriptions; ProbList shows top 5 spectral class probabilities.
  - Rich metadata for each polygon, including processing history and spectral class probabilities.
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes (GB and NI separate).
  - 1 km raster: aggregate products (dominant class and percentage cover for both LCM2007 classes and aggregates).
  - 25 m raster data can be converted to per-class percentages at 1 km resolution.
- Data Access
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence from CEH (fees may apply).

## Class System and Metadata
- 23 LCM2007 classes based on Broad Habitats (with some subdivisions):
  - Built-up Areas and Gardens subdivided into Urban and Suburban.
  - Dwarf Shrub Heath subdivided into Heather and Heather grassland.
  - Littoral Sediment subdivided into Littoral sediment and Saltmarsh (Priority Habitat).
- Appendix 1 details each class; Appendix 2 describes relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 provides colour mappings for display.
- The vector dataset includes attributes such as INTCODE (class code for display), KBE (processing history), and ProbList (top spectral class probabilities).

## Validation and Accuracy
- Ground reference validation: 9,127 polygons; average accuracy about 83% (note this is an average across tests; local accuracies may vary).
- Change mapping across LCM1990, LCM2000, and LCM2007 is complex due to class/spatial differences and typical image classification errors (~20%), so LCM2007 is not well suited for change detection.

## Data Quality and Limitations
- LCM2007 maps land cover, not land use; some lands (e.g., grass for recreation vs grazing) may be spectrally similar and not distinguishable by class alone.
- Broad Habitat sub-classes (BHSub) exist primarily for information in ProbList and may require user validation for sub-class use.
- Certain grassland distinctions (Neutral, Calcareous, Acid) may be misclassified relative to ground reference data; aggregates may be preferred for some analyses.
- Montane, Inland Rock, and other specialized classes rely on altitude or soil data and may have caveats regarding accuracy.

## Data Projections and Size
- Vector and raster data have distinct projections:
  - Great Britain: British National Grid (OSGB 1936).
  - Northern Ireland: Irish National Grid (Ireland 1965), with NI transitioning towards ITM.
- File sizes (approximate):
  - Vector (GB): ~4.13 GB; Vector (NI): ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: GB up to ~49 KB–21 MB range (depending on product).

## Usage Guidance for Analysts
- Use 23-class data for detailed thematic analyses; use 1 km aggregates when modelling at national scales or combining with other datasets (e.g., meteorological, species distribution).
- Retain Parcel_ID and proceed with user-driven validation when exploring Broad Habitat sub-classes.
- For change analyses, prefer other datasets or multiple-LCM integrations due to cross-class differences and classification errors between LCM generations.
- Leverage the rich vector metadata for reproducibility, data provenance, and integration with other GIS datasets.

## Updates and History
- Version History:
  - Originally published in July 2011 (vector GB and 25 m raster GB; 1 km products introduced later).
  - Version 1.2 updated May 2012 to include dataset updates and enhanced change detection commentary.
- Appendix 4 lists updates (May 2014): tile additions (Fair Isle, Stranraer), water class addition for 1 km products, and other product updates.

## Appendices at a Glance
- Appendix 1: LCM2007 Classes – detailed descriptions and definitions for each of the 23 classes.
- Appendix 2: Mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: LCM2007 colour mapping for visualization (also available as ArcGIS .lyr).
- Appendix 4: Product updates and version changes (e.g., 1.2 updates).

## Further Information and References
- Final Report for LCM2007: Morton et al., 2011 (Countryside Survey Technical Report No. 11/07).
- Broad Habitat classification guidance: Jackson, 2000 (JNCC Report 307).
- Data access portals and contact: CEH Information Gateway; spacialdata@ceh.ac.uk; Countryside Survey project at www.countrysidesurvey.org.uk.