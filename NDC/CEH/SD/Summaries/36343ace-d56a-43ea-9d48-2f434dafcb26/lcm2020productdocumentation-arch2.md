# The UKCEH Land Cover Map for 2020

- Purpose: A user guide for LCM2020, the UKCEH land cover map produced annually to enable consistent monitoring of environmental condition and change using standardised datasets and validation procedures.

## Data Products (GB and Northern Ireland)

- Six datasets in total:
  - 10m Classified Pixel datasets (GB & NI): classification results with two bands per location (land cover class and associated classification probability).
  - Land Parcel datasets (GB & NI): attributes derived by intersecting 10m classified pixels with the UKCEH Land Parcel Spatial Framework.
  - 25m Rasterised Land Parcel datasets (GB & NI): per-parcel raster products with three attributes (mode, conf, purity) per 25m pixel.
  - Note: Appendix 5 also lists a GB 20m Classified Raster Product; NI datasets are 10m classification and 25m parcels. MMU is ~0.5 ha for land parcels.
- Each geography’s product names and extents are defined, with spatial references aligned to British National Grid (GB) or Irish Grid (NI).

## Data Structure and Content

- 10m Classified Pixel datasets: mosaic of Classification Scenes; first band = most likely UKCEH Land Cover Class, second band = class probability (confidence). These pixels are not generalised by parcel framework to preserve fine landscape detail.
- 25m Rasterised Land Parcel datasets: derived by rasterising parcel-framework attributes; three-band rasters capturing dominant class, probability, and purity per parcel.
- 21 UKCEH Land Cover Classes: defined from Biodiversity Action Plan (BAP) Broad Habitats; however, mappings are not exact equivalents to BAP categories, with italicised references and capitalised class names for clarity. Appendices provide detailed correspondences and notes.

## Classification Approach and Data Production

- Base inputs: Sentinel-2 Seasonal Composite Images (winter, spring, summer, autumn) combined with 10 Context Rasters to reduce spectral confusion.
- Seasonal Composite Images: derived via Google Earth Engine; spectral bands from Sentinel-2 (10–60 m bands across 4 seasons).
- Classification Scenes: GB uses 100x100 km tiles, producing 36-band Seasonal Composite Images per tile; NI uses a single 43-band scene for the year.
- Bootstrap Training: automated training using historic LCM data (LCM2017–2019) filtered to >99% purity; creates large training sets (GB ~941,027; NI ~214,833). This enables the classifier to learn from abundant, wall-to-wall data without new field campaigns.
- Random Forest: Balanced sampling (10,000 samples per class per bag) to prevent dominance by common classes; classification yields 10m pixel product.
- Pipeline: Overlapping Classification Scenes are classified independently; final cut uses visual precedence in overlaps to resolve results.
- UKCEH Land Parcel Spatial Framework: parcels approx. 0.5 ha MMU; designed to reduce noise and support change detection. Some identifiers do not match LCM2015 for cross-year comparisons.

## Validation and Accuracy

- Validation approach: comparison with GB countryside survey (2019–2020), open-source National Forest Inventory data, IACS data, and bespoke validation points (total of 34,715 points).
- Overall accuracy: 79.2% (0.792) at full thematic detail (Appendix 4).
- Confusion matrices and producer’s/user accuracy statistics are provided to indicate class-specific performance and reliability.

## Relationship to Biodiversity Action Plan (BAP) Broad Habitats

- 21 UKCEH Land Cover Classes are aligned with BAP Broad Habitats but are not exact equivalents; BAP classes were designed for field botanists, not satellite detection.
- Appendices outline the mapping, with notes on where classes diverge (e.g., Freshwater vs. Rivers/Canals; Saltwater handling; peatland mappings) and guidance on interpreting overlaps and ambiguities.
- For users needing a simplified view, UKCEH Aggregate Classes can be derived from Land Parcel products.

## Practical Guidance for Analysts Monitoring the Environment

- Use in monitoring: annual maps enable differentiation of random classification errors from persistent real-world change; random errors are expected to flicker year-to-year, while real change persists.
- Data selection: 10m Classified Pixel datasets preserve fine-scale features (narrow habitats, small patches) but are not generalised; for robust temporal comparisons, the Land Parcel datasets provide consistent units for change analysis.
- Multi-dataset integration: combine LCM2020 with other environmental data sources to enhance monitoring (e.g., habitat extent, land use, biodiversity indicators), as encouraged by the Bootstrap Training and standardised outputs.
- Temporal context: annual production improves temporal consistency and supports change detection and policy assessment over time.
- Access and provenance: datasets are stored and served through appropriate data portals; Bootstrap Training uses historic maps as a training backbone, ensuring repeatable, extensible classification.

## Limitations and Considerations

- No manual region-wide corrections were performed to maintain annual production efficiency; significant improvements would require manual steps, which are currently avoided.
- Classification errors are largely random; some persistent misclassifications occur in spectrally similar or spectrally challenging classes (e.g., certain heath, bog, peatland, upland vegetation types).
- Spectral similarity challenges (e.g., Saltwater vs. Freshwater near coasts) and MMU-related fragmentation can affect certain classes.
- Some upland peatland/habitat classes are difficult to resolve spectrally; ongoing research and training data development are anticipated to improve accuracy in future releases.

## Data Access and Management

- Datasets are structured for use by monitoring teams, with explicit documentation on data production, validation, and class definitions.
- Datasets should be uploaded to and accessed from designated portals; users should reference the version (LCM2020) and consider whether to analyze at 10m pixel, 25m parcel, or aggregated class levels depending on the monitoring objective.