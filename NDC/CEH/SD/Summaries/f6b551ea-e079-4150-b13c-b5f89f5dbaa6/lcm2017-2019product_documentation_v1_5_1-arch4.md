# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map suite provides a set of geospatial data capturing land cover across the UK, built from 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and designed to match prior LCMs for comparability.
- Emphasises how data were produced, validated, and the reasoning behind production decisions to help users apply the data responsibly.

## Data structure and datasets
- Total dataset suite per year: 42 datasets (GB and Northern Ireland copies).
- Core dataset families:
  - 20m Classified Pixels (new): 2-band rasters; band 1 = most likely UKCEH Land Cover Class, band 2 = confidence (0–100). Preserves fine landscape features below MMU (~0.5 ha).
  - Land Parcels: 21-class attributes with per-parcel history histogram, mode, purity, confidence, standard deviation, and count.
  - 25m Rasterised Land Parcels: 3-band rasters (mode, confidence, purity).
  - 1km Derived rasters: 
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
- Spatial coverage and grid:
  - Great Britain: GB National Grid (EPSG: 27700)
  - Northern Ireland: NI Irish Grid (EPSG: 29903)
  - Pixel origins aligned with respective national grids; GB and NI products provided separately.

## Production methodology
- Bootstrap Training: automatic, self-starting training using historic LCM observations (primarily from LCM2015) to generate spectral training data for current imagery.
- Random Forest classification: balanced sampling from Bootstrap Training data; 10,000 samples per training bag; aimed at equal class representation to improve rarer class accuracy.
- Satellite inputs:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance per season) used to create Classification Scenes.
  - Seasonal data: winter, spring, summer, autumn; four-season mosaics per year.
- Context rasters: 20m rasters providing terrain, proximity to buildings/roads/sea/freshwater, foreshore and tidal masks, and other context to reduce spectral confusion.
- Classification Scenes:
  - GB uses 100x100 km tiles, producing 36-band Seasonal Composite Images combined with Context Rasters into 46-band GB Classification Scenes, with 74 overlapping scenes classified and then reconciled.
  - NI uses a single 43-band Classification Scene per year (36 spectral bands + 7 context layers) determined by NI’s extent.
- UK Land Parcel Spatial Framework:
  - Existing framework (adjusted for efficiency) used to summarize 20m Classified Pixels into Land Parcels.
  - gid identifiers differ from LCM2015; parcel structures are stable for cross-year comparisons via gid, but direct parcel-id matching across years is not possible.
- Validation and quality control:
  - Visual checks and formal validation performed; no manual corrections applied to the classification outputs this time.
  - Validation against multiple sources (GB countryside survey 2019, National Forest Inventory, IACS, bespoke validation points) yielding around 78.6–79.6% overall accuracy across 2017–2019.
  - Acknowledges limitations in validation data and class mapping; results are indicative of reality and improving over time.

## UKCEH Land Cover Classes and BAP Broad Habitats
- 21 UKCEH Land Cover Classes, aligned with BAP Broad Habitats but not exact BAP classifications for remote sensing.
- Appendix notes on how classes relate to BAP Broad Habitats and how some classes were refined (e.g., splitting dwarf shrub/heath into Heather and Heather Grassland, urban vs suburban distinctions).
- Emphasis on maintaining consistency for change-detection while allowing updates to reflect newer habitat descriptions.

## Data standards, metadata and presentation
- Detailed metadata for datasets, including coordinate systems, extents, pixel sizes, and band counts (as described in Tables and Appendices).
- RGB color recipe provided to visualize the 21 classes (Appendix 3).
- 20m Classified Pixels retain fine landscape detail; 25m Rasterised and 1km products show generalisation effects for broader analyses.

## Temporal and data governance notes
- Bootstrap Training lineage traces back to LCM2015 and earlier; future maps (LCM2020, LCM2021) planned to use progressively longer majority-based bootstraps.
- Provides a scalable approach to annual land cover mapping with minimal manual intervention, enabling near real-time change understanding while maintaining cross-year comparability.
- Important caveats for users:
  - gid values differ from LCM2015 for cross-year parcel comparisons.
  - Validation data and class mappings involve some subjectivity; treated as best available indicators.
  - Some coastal and upland classes have inherent detection challenges; context layers help but limitations remain.

## Future plans and maintenance
- Annual release trajectory anticipated (with LCM2020 planned for 2021) to support timely tracking of land cover change.
- Exploration of gap-filling approaches (e.g., Sentinel-1 SAR) and expanded input data to improve completeness under cloud cover and in challenging environments.
- Ongoing refinement of Bootstrap Training strategies and potential enhancements to the Land Parcel Framework as data and technology evolve.

## Practical takeaways for data-driven leadership
- Efficient, low-cost data refresh: Bootstrap Training plus RF enables annual LCM updates with minimal manual intervention, supporting timely decision-making.
- Data quality and traceability: Clear provenance from historic maps through Bootstrap Training and RF classification; gid-based parcel continuity supports change detection, with explicit notes on cross-year comparability limits.
- Rich data product suite: The combination of 20m Classified Pixels, Land Parcels, 25m parcels, and 1km thematic rasters provides multiple scales for analysis, modeling, and reporting.
- User-focused design and governance: 21 classes tied to widely understood habitat concepts, with robust validation and explicit metadata to facilitate discoverability, reuse, and integration with partner datasets.
- Limitations and planning: Acknowledges potential data access and standardization challenges (e.g., paywalls, metadata gaps, cross-year comparisons) and outlines intended improvements to address them.