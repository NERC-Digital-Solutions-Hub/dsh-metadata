# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- UKCEH releases three new national land cover maps (LCMs): LCM2017, LCM2018 and LCM2019, extending the historical sequence (LCMs from 1990, 2000, 2007, 2015).
- Each map set uses a consistent 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats, with terminology and class relationships carefully defined to support cross-year comparisons.
- The product suite comprises multiple data layers, with Great Britain (GB) and Northern Ireland (NI) versions, totaling 42 datasets (per year) across 20m, 25m, and 1km scales, plus ancillary datasets.
- Production emphasizes automated, repeatable processes to enable annual updates, while validation provides quality checks to inform users about reliability and limitations.

## Data content and structure

- Classes and aggregation
  - 21 UKCEH Land Cover Classes (mapped from UKCEH LCM2015 framework; aligned for cross-year comparability).
  - An accompanying UKCEH Aggregate Classes set (10 classes) for generalized analyses.
  - Appendices explain class derivations and relationships to UK BAP Broad Habitats.
- Datasets and extents
  - 20m Classified Pixels (GB and NI): new 20m resolution RF-classified pixel data with per-pixel class and confidence (probability) score.
  -  Land Parcels: attributes summarizing 20m pixel classifications within land parcel units using the UKCEH Land Parcel Spatial Framework.
  - 25m Rasterised Land Parcels: 3-band rasters (dominant class, confidence, purity) derived from Land Parcels.
  - 1km Raster datasets: 1km percent cover (21 bands), 1km percent aggregate cover (10 bands), 1km dominant cover (1 band), 1km dominant aggregate cover (1 band).
- Coordinate systems and extents
  - GB: British National Grid (EPSG: 27700).
  - NI: Irish Grid (TM75; EPSG: 29903).
  - GB extent: 0–700 km Easting, 0–1,300 km Northing (GB); NI extent defined by its own grid.
- Dataset metadata and structure
  - 42 datasets per year (GB and NI variants for each product).
  - 20m Classified Pixels preserve detailed features; 25m and 1km products provide generalized summaries suitable for broader analyses.
  - GID identifiers for Land Parcels are stable within the UKCEH framework but do not match LCM2015 identifiers; parcel-level comparisons across years should use gid rather than spatial overlap alone.
- Seasonal and contextual inputs
  - Seasonal Composite Images: four seasons created from Sentinel-2 TOA reflectance (resampled to 20m) and combined with 20m Context Rasters to form Classification Scenes.
  - Context Rasters (GB and NI): height, aspect, slope, distances to buildings/roads/coast/freshwater, urban/foreshore masks, etc., to improve classification in spectrally similar areas.
- Data sources and processing approach
  - Sentinel-2 seasonal composites generated via Google Earth Engine.
  - Context layers derived from a mix of open data sources (Ordnance Survey, NEXTMap terrain, etc.).
  - No manual corrections were applied in this release to support rapid annual updates; visual checks and formal validation were still performed.

## Production methodology and data lineage

- Bootstrap Training
  - Fully automatic training approach that relies on historic UKCEH LCMs to sample spectral training observations (Bootstrap Training).
  - For LCM2017–2019, training samples were drawn from LCM2015 land parcels with purity ≥ 99%, enabling rapid bootstrap of current-classification models.
  - Future maps (LCM2020, LCM2021) planned to use majority signals across multiple years (e.g., 2017–2019; 2018–2020) to bootstrap training.
- Random Forest classification
  - RF classifier trained with balanced sampling (10,000 samples per class, with replacement) to ensure rarer classes are well represented.
  - Production software integrates WEKA, PostGIS, and GDAL (all open source).
  - Classification Scenes for GB use 36 spectral bands plus 10 context layers (46-band dataset); 74 overlapping GB Scenes were processed to cover the GB land surface, with manual precedence during overlaps to select the best outcomes.
- UK Land Parcel Spatial Framework
  - Land parcels are the fixed spatial units (~0.5 ha MMU) used to summarise 20m pixel data.
  - The framework was updated for processing efficiency; gid values change across years, affecting direct parcel-to-parcel comparability; cross-year comparison should rely on gid rather than spatial overlap.
- Validation and quality
  - UK-scale validation used 22,325 points from GB countryside survey 2019 data, National Forest Inventory data, IACS, and manual interpretation.
  - Reported overall accuracy: LCM2017 = 78.6%, LCM2018 = 79.6%, LCM2019 = 79.4%.
  - Validation acknowledges that observations are not perfect truth, and class mappings/transformations introduce uncertainties; Appendix 4 provides detailed confusion matrices and accuracy metrics.
- Automation and reproducibility
  - Emphasis on automated workflows to support annual updates with transparent documentation and reproducible results.
  - Some manual steps remain in overlapping region selection and final cut decisions to ensure quality control.

## Data governance, quality, and accessibility considerations for Data Stewards

- Standards and interoperability
  - Clear documentation of class definitions and crosswalks to BAP Broad Habitats (Appendices 1–2) to facilitate interpretability and cross-study comparisons.
  - Consistent naming conventions and explicit notes on capitalisation to distinguish defined UKCEH classes from generic terms.
- Provenance and lineage
  - Detailed description of data origins (Sentinel-2 seasonal composites, 20m context rasters, Land Parcel Framework) and processing chain (Bootstrap Training → RF classification → parcel summarisation → raster products).
  - GID-based parcel identifiers enable temporal alignment across LCM2017–LCM2019, with caveats about non-match to LCM2015 IDs.
- Update cadence and future plans
  - Aims to release a new LCM annually; planned enhancements include expanding input data (potentially Sentinel-1 SAR for gaps in cloudy periods) and expanding thematic detail as training data improve.
  - Future bootstrap strategies: increasing reliance on majority signals across multiple years to stabilise training data.
- Validation transparency
  - Validation results provided with accompanying caveats; Appendix 4 includes full confusion matrices and per-class producer/user accuracies and sample counts.
  - Users are encouraged to interpret accuracy in light of class definitions and conversion between BAP and UKCEH classes.
- Access and dissemination
  - Data are described for dissemination through UKCEH portals and catalogues; the document outlines dataset extents, coordinate systems, pixel sizes, and band structures to support discovery and reuse.

## Practical implications and guidance for users

- Use-case suitability
  - Suitable for land cover change detection, large-area habitat assessments, and integration with other UKCEH datasets, with awareness of annual changes in parcel identifiers and potential misclassification for certain classes.
- About the 21-class scheme
  - The 21-class system reconciles legacy UKCEH maps with current remote-sensing capabilities; for some land cover types spectral separability is challenging, but context layers help mitigate confusion (e.g., Neutral Grassland, Saltmarsh, Urban/Suburban distinctions).
- Data quality and limitations
  - Expect around 79% overall accuracy at the national scale; higher accuracy achievable for some dominant classes (e.g., Urban, Freshwater) and lower for spectrally similar classes (e.g., various grasslands with mixed spectral signals).
  - No manual corridor-wide corrections were applied in this cycle to enable annual production speed; manual checks ensure overall quality before release.
- Reproducibility and comparison
  - Cross-year comparisons should rely on gid-based parcel alignment and be mindful of changes in the Land Parcel Spatial Framework identifiers.
  - When comparing with LCM2015, use the provided crosswalks and be cautious about class definition changes and calibration differences.

## Future directions and closing notes

- Annual updates and potential data enhancements
  - Continuation of annual LCM releases with improved training data and potentially expanded input data (including SAR) to improve robustness under cloud cover.
  - Ongoing evaluation of training data strategies (Bootstrap Training) and calibration against new validation resources.
- Appendices and references
  - Appendices provide in-depth class definitions (Appendix 1–2), biodiversity habitat mappings (Appendix 2), recommended color schemes (Appendix 3), detailed validation results (Appendix 4), and full dataset listings (Appendix 5).