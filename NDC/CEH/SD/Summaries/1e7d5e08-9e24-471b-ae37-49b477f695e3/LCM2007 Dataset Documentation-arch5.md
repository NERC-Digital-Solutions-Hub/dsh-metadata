# Land Cover Map 2007 Dataset Documentation

- An official documentation for the Land Cover Map 2007 (LCM2007) data products, describing purpose, production, data formats, metadata, validation, and access.
- LCM2007 provides parcel-based UK land cover classifications across 23 classes derived from satellite imagery (20–30 m) and aligned with UK Broad Habitats; exists in vector and raster formats; built to support a wide range of GIS applications.

## Data products and structure

- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland
  - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, TotPixels, Construct)
  - Parcel_ID uniquely identifies each parcel; includes source image
  - BH (Broad Habitat) and BHSub (Broad Habitat sub-class) used in classification; FieldCode provides sub-class codes; INTCODE is display-ready numeric class
  - KBE records knowledge-based enhancements; ProbList shows top 5 spectral class probabilities
  - Construct records initial data sources and segmentation basis
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes
  - 1 km raster: aggregates for UK-wide modeling; includes dominant class and percentage cover for both LCM2007 classes and aggregates
  - GB and NI provided in separate projections
- Data Volume
  - Vector: large files (example sizes provided, e.g., GB shapefile ~4.13 GB)
  - Raster: substantial but smaller than vector; 1 km products more compact
- Access
  - 1 km raster data accessible via CEH Information Gateway
  - Full vector and 25 m raster data available on request under licence; online application process and possible licence fees

## Classification and methodology

- Purpose: map land cover (not land use); 23 classes based on UK Broad Habitats
- Minimum mapping unit: >0.5 ha; parcels smaller than 0.5 ha or linear features <20 m dissolved into surrounding landscape
- Sub-class expansions: some Broad Habitats subdivided (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh)
- Validation
  - Ground reference data collected to compare against LC M2007 resolution
  - Average accuracy around 83% across 9127 ground reference polygons; local variations expected
- Metadata and processing history
  - Rich metadata for each polygon, including processing steps and spectral classification history
  - Probability-based characterization (ProbList) informs uncertainty

## Data access, formats, and standards

- Vector and raster data compiled with detailed attributes and provenance
- Coordinate systems and projections
  - Great Britain: British National Grid
  - Northern Ireland: Irish National Grid (with NI gradually transitioning to ITM in some contexts)
- Documentation emphasizes production methodology and limitations to guard against misuse

## Quality, limitations, and guidance

- LCM2007 maps land cover, not always a direct proxy for land use
- Sub-classes (Broad Habitat sub-classes) are informative but not always as rigorously QA-validated as the primary 23 LCM2007 classes
- Some habitat classes (e.g., Neutral/Calcareous Grassland) can be misclassified as Improved Grassland; users should perform their own validation for sub-class analyses
- Small patches and mosaic landscapes (e.g., Fen, Marsh and Swamp; Montane classifications) can be challenging to map consistently
- MMU-driven exclusion means very small features (<0.5 ha or <20 m) are dissolved into surrounding classes

## Appendices and colour mappings

- Appendix 1: LCM2007 Classes – definitions and brief reviews for each of the 23 classes
- Appendix 2: Relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes
- Appendix 3: Colour mapping for display (standard RGB values per class)
- Acknowledgements and data sources ( Landsat, SPOT, AWIFS, OS, and other data providers)

## Further information and references

- Final Report for LCM2007 – Morton et al., 2011 (Countryside Survey Technical Report No. 11/07)
- Guidance on Broad Habitat interpretation – Jackson, 2000 (JNCC Report 307)
- Licensing and contact: CEH spatialdata@ceh.ac.uk; data portal at www.ceh.ac.uk/data
- Acknowledges multiple data providers and licensing bodies; detailed copyright notices and data rights apply