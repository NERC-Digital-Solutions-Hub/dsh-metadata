# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- A user guide accompanying the release of three UKCEH national land cover maps: LCM2017, LCM2018, and LCM2019.
- Purpose: provide 21 UKCEH Land Cover Classes (aligned with BAP Broad Habitats) derived automatically; explain content, production decisions, validation, and future plans to help users apply the data appropriately.

## Production overview and aims

- Maps produced automatically using Bootstrap Training combined with a Random Forest (RF) classifier to enable near-real-time, annual updates.
- Sentinel-2 Seasonal Composite Images (median reflectance per season) are classified after being combined with 20m Context Rasters to form Classification Scenes.
- Goal: rapid, coast-to-coast UK-wide land-cover maps with documented production choices and validation to aid decision-making and monitoring.
- Validation shows maps are of similar quality to the immediate predecessor (LCM2015) with formal checks performed.

## Data, structure, and metadata

- Datasets and products (42 datasets total, GB and NI each year):
  - 20m Classified Pixels (new in this release): per-pixel RF classification with a confidence score.
  - Land Parcels: derived attributes summarising 20m pixel classifications within a UKCEH Land Parcel Spatial Framework.
  - 25m Rasterised Land Parcels: rasterised representation with 3 bands (dominant class, confidence, purity).
  - 1km Raster datasets: 1km Percent Cover (21-band), 1km Percent Aggregate Cover (10-band), 1km Dominant Cover (single band), 1km Dominant Aggregate Cover.
- Geographic scope: Great Britain and Northern Ireland; GB uses British National Grid, NI uses Irish Grid.
- MMU and comparability:
  - Minimum Mapping Unit (MMU) ~0.5 ha for land parcels.
  - Gids (gid) for parcels do not match LCM2015, affecting direct parcel-to-parcel comparisons; use gid for cross-year comparisons (LCM2017–2019).
- Dataset evolution:
  - Attribute naming updated to align with production software (e.g., hist, mode, purity, conf, stdev); values adapted (purity as percentage, etc.).
  - Composite attribute removed; training and classification rely on 20m pixels and Google Earth Engine-derived data.

## Classification methodology and workflow

- Bootstrap Training:
  - Uses majority signal from UKCEH LCM2015 to bootstrap training data for 2017–2019.
  - Aims to avoid costly field data; historic maps supply broad, coast-to-coast coverage.
- Random Forest classification:
  - Balanced training: 10,000 samples per class from each training bag.
  - Self-contained workflow integrating Weka, PostGIS, and GDAL (open-source tools).
- Seasonal and contextual inputs:
  - Seasonal Composite Images from Sentinel-2 (TOA reflectance; SR not significantly improving results in this study) with 9 spectral bands.
  - 20m Context Rasters: terrain (height, aspect, slope), proximity to buildings/roads/coast/freshwater, foreshore and tidal masks, woodland mask.
- Classification Scenes:
  - GB: 100x100 km tiles, 36-band Seasonal Composite Images plus 10 context bands → 46-band Classification Scenes.
  - NI: single 43-band (36 spectral + 7 context) Classification Scene per year.
- UK Land Parcel Spatial Framework:
  - Maintains ~0.5 ha MMU; designed to group 20m classified pixels into real-world units for change detection.
  - Spatial framework kept consistent with LCM2015, with internal indexing changes; parcel identifiers (gid) differ from LCM2015 but can be used for cross-year matching via gid.

## Validation and accuracy

- Validation dataset: 22,325 points drawn from GB countryside survey data, National Forest Inventory, IACS, and interpretation points.
- Reported overall accuracy (UK scale):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes:
  - Used the same validation points for all three products; accuracy indicators relative to each product vary.
  - Some validation observations may be incorrect; some class definitions required subjective conversion to UKCEH classes.
  - Approximately 80% correspondence is considered impressive for an automatic, yearly 21-class map; improvements expected as methods mature.

## Data products in detail

- 20m Classified Pixels:
  - New addition; provides per-pixel class with a probability-based second band indicating confidence (0–100).
  - Maintains detailed landscape features not present in coarser rasters.
- Land Parcels:
  - Attributes per parcel: gid, _hist (class frequency per parcel as tuples), _mode (dominant class), _purity (percentage of modal class), _conf (mean class membership probability), _stdev (std dev of confidence), _n (number of pixels).
  - Note: some attribute names differ from LCM2015; a straightforward lookup suffices for mapping.
- 25m Rasterised Land Parcels:
  - 3-band rasters: band 1 = modal class, band 2 = parcel-averaged membership probability (_conf), band 3 = parcel purity (_purity).
- 1km Raster datasets:
  - 1km Percent Cover: 21-band, 8-bit; per-1km cell percentage per class.
  - 1km Percent Aggregate Cover: 10-band, 8-bit; per-1km cell aggregate cover.
  - 1km Dominant Cover: single-band; dominant class per 1km cell.
  - 1km Dominant Aggregate Cover: single-band; dominant aggregate class per 1km cell.

## Seasonal data and satellite input notes

- Sentinel-2 bands and resolutions are documented (bands 2–12 with varying 10–60 m resolutions).
- Google Earth Engine provides Sentinel-2 surface reflectance, but the production used TOA reflectance after evaluating potential gains from SR.

## Practical notes for users and governance considerations

- Data governance and openness:
  - Datasets include a clear lineage from 20m Classified Pixels to parcel-based summaries; transparency around the Bootstrap Training approach and validation.
  - Metadata changes exist due to production workflow alignment; users should map new attribute names to previous versions when comparing.
- Use-case guidance:
  - Suitable for annual land-cover monitoring and change detection at parcel and grid scales.
  - Acknowledge potential cross-year parcel-id differences; use gid for cross-year comparisons rather than relying on fixed parcel IDs.
- Limitations and caveats:
  - No manual corrections were applied this year; classification errors are randomly distributed over time, but persistent changes may be detected over multiple years.
  - Some upland and peatland classifications remain challenging; authors acknowledge potential confusion between closely related classes and the value of additional training data.

## Appendices and key concepts

- Appendix 1 and 2: UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats; detailed class definitions and practical notes on detection challenges.
- Appendix 3: Recommended RGB color recipe for displaying UKCEH Land Cover Classes.
- Appendix 5: Full list of datasets per year (LCM2017, LCM2018, LCM2019) and their GB/NI distinctions.

## Future directions and closing notes

- Annual release plan for 2020 (LCM2020) and beyond; bootstrap training strategy may evolve to use multi-year majority signals (e.g., 2017–2019 for 2020; 2018–2020 for 2021).
- The production team plans to continuously review input satellite data choices and consider expanding water-related and upland vegetation mappings with new training data in future LCM releases.