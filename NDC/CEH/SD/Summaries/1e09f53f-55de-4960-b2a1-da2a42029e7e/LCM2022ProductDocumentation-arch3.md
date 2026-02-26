# The UKCEH Land Cover Map for 2022

- Purpose: User guide for LCM2022, detailing data production, validation, and accuracy to help users apply UKCEH LCM data in current and future work.
- Scope: Seven datasets across Great Britain and Northern Ireland (GB & NI) plus a 1 km summary raster product.
  - 10 m classified pixel dataset (GB and NI)
  - Classified land parcel dataset (GB and NI)
  - 25 m pixel rasterised land parcel dataset (GB and NI)
  - 1 km summary raster products (GB & NI)
- Outputs align with 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats, with careful notes on relationships and distinctions.

## Data products and structure

- LCM2022 product suite details:
  - 10 m Classified Pixels (GB and NI)
  - Land Parcel Dataset (GB and NI)
  - 25 m Rasterised Land Parcels (GB and NI)
  - 1 km Summary Rasters (GB and NI)
- Dataset specifics:
  - GB coordinate system: British National Grid (EPSG 27700)
  - NI coordinate system: Irish Grid TM75 (EPSG 29903)
  - Pixel resolutions: 10 m (pixels) and 25 m (rasters)
  - Land parcel MMU: approximately 0.5 hectares
  - Number of parcels: GB ~ 6,741,294; NI ~ 902,252
- Outputs include a second band per 10 m pixel giving the classification probability/confidence.
- 1 km products provide dominant class and percentage cover (with sums that may differ slightly from 100% due to rounding and coastal effects).

## Methods and production

- Classification approach:
  - Automatic classification of Classification Scenes using Bootstrap Training with a Random Forest (RF) classifier.
  - Bootstrap Training draws training data from historic LCM maps (LCM2019–LCM2021) with >80% probability, ensuring consistency and large training samples.
  - RF training uses 10,000 samples per class per bag with replacement to balance class representation.
- Data inputs:
  - Seasonal Composite Images derived from Sentinel-2 (four seasonal periods) with 10 bands; contextual seasonality improves discrimination.
  - Context Rasters (GB: 10 rasters including height, aspect, slope, distance to features; NI: 9 rasters including urban mask, coast, freshwater, roads, etc.).
- Classification Scenes and coverage:
  - GB: 32 Classification Scenes created on a modified OS 100 x 100 km tile grid for full GB coverage.
  - NI: Single 49-band Classification Scene using minimum bounding rectangle of NI land mass.
- Data framework:
  - UKCEH Land Parcel Spatial Framework used to generate land parcels; parcels roughly 0.5 ha MMU and designed to represent discrete real-world units.
  - 10 m Classified Pixels are not generalised by the Land Parcel Framework to preserve fine features; 25 m rasters are created by rasterising the parcel framework.
- Validation:
  - Formal validation with 33,107 reference points across all 21 classes, yielding an overall accuracy of 86.1%.
- Software and provenance:
  - Custom UKCEH software integrates Weka RF with PostGIS and GDAL (all open source).

## Validation and accuracy

- Overall accuracy: 86.1% across all 21 classes (based on 33,107 validation points).
- Validation data sources include GB countryside survey, National Forest Inventory, Rural Payments Agency, and bespoke validation points.
- Accuracy metrics provided per class include producer’s and user’s accuracy, with confusion matrices illustrating inter-class misclassifications (noting some known spectral/semantic confusions among habitat types).

## Relation to policy, monitoring, and metadata

- 21 UKCEH Land Cover Classes are related to but not identical with UK BAP Broad Habitats; the guide preserves class definitions for historical consistency.
- Appendix 1–2 provide detailed notes on UKCEH classes and BAP Broad Habitats to aid interpretation and cross-walks with environmental reporting.
- The annual production aims to maximize temporal consistency, enable change detection, and differentiate real change from classification error (random errors expected to flicker over time).

## Known issues and caveats

- Minor data gaps: a small number of polygons missing from vector land parcel products, causing nodata in derived 25 m rasters; effects are negligible for 1 km products and the 10 m dataset is unaffected.
- Method changes: differences in methods across years may produce subtle discrepancies in year-to-year comparisons.
- Classification challenges: spectral confusion among some habitat types (e.g., bog, heath, various grasslands) due to overlapping spectral signatures; context rasters and training data mitigate but do not eliminate misclassifications.
- Special note on NI: classification scene is a single 49-band composite; GB uses multiple tiles to cover large area.

## Data accessibility, governance, and citation

- DOIs and formal citations are provided for each dataset; users should cite the applicable DOI when using LCM2022 data.
- Acknowledgement of the production method and related literature (e.g., Marston et al., 2024; related earlier LCM reports) is encouraged for reproducibility.
- Output products are produced with open-source tools; data sharing and metadata practices are emphasized to support governance and reuse.

## Appendices and supplementary information (highlights)

- Appendix 1–2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats, including definitions, potential confusions, and class-specific considerations for remote sensing.
- Appendix 3: Full list of LCM2022 datasets with DOIs and citations.
- Appendix 4: Correspondence matrices (confusion matrices) for each class, detailing misclassifications and accuracy metrics.
- Appendix 5–6: Colour recipes for displaying land cover classes (standard and color-blind-friendly) with accompanying QGIS symbology files.
- Appendix 7: References and methodological notes.

Key takeaways for monitoring framework authors

- Data quality and usefulness:
  - LCM2022 provides a robust, annually produced land cover data framework with explicit validation, enabling change detection and trend analysis.
  - The combination of 10 m classified pixels, land parcels, and 1 km summaries supports both fine-scale analysis and broad landscape assessments.
- Metadata and governance:
  - Clear metadata, DOIs for datasets, and open-source tooling enhance transparency, reproducibility, and governance.
  - Bootstrap Training leverages historical maps to minimize field data needs while maintaining quality; provenance and training data limitations are documented.
- Accessibility and barriers:
  - While data sharing is pursued, some metadata gaps and methodological changes over time can complicate cross-year comparisons; users should account for potential consistency issues.
  - Complex classifications and potential spectral confusion require careful interpretation, especially when aggregating to broader habitat categories or comparing to BAP Broad Habitats.
- Practical guidance for monitoring:
  - Use 10 m classified pixels for detailed landscape features; use 25 m parcel rasters and 1 km summaries for change detection and regional assessments.
  - Interpret class results with awareness of known issues (spectral confusion, coastal rounding in percentages, and coastal/estuarine edge effects).
  - Leverage contextual rasters and seasonal composites to improve classification reliability, particularly in spectrally similar landscapes.