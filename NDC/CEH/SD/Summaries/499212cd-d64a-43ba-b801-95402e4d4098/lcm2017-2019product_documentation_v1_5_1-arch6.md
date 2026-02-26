# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- Presents three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map provides land cover across the UK using 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with aims to enable broader data use and change detection.
- Production relies on Bootstrap Training plus Random Forest classification to produce annual, automatically generated maps (no manual corrections in this release).
- Outputs are designed to enable self-service data exploration and cross-year comparisons.

## Data products and formats
- 20m Classified Pixels (GB and NI): 2-band raster per year; Band 1 = most likely UKCEH Land Cover Class, Band 2 = class membership probability (0–100).
- Land Parcels (GB and NI): parcel-level attributes including gid, _hist (histogram of class counts per parcel), _mode, _purity, _conf, _stdev, _n.
- 25m Rasterised Land Parcels (GB and NI): 3-band raster per year; Band 1 = _mode, Band 2 = _conf, Band 3 = _purity.
- 1km Raster datasets:
  - 1km Percent Cover (21-band, 8-bit)
  - 1km Percent Aggregate Cover (10-band, 8-bit)
  - 1km Dominant Cover (1-band)
  - 1km Dominant Aggregate Cover (noted in metadata)
- Coordinate systems and extents:
  - GB: British National Grid, EPSG 27700; extents 0–700,000 East, 0–1,300,000 North
  - NI: Irish Grid, EPSG 29903; extents provided per dataset
- Output structure replicated for GB and NI; datasets exist as 20m classified pixels, land parcels, 25m rasterised parcels, and 1km summary rasters.

## Production pipeline and data sources
- Seasonal imagery: Sentinel-2 Seasonal Composite Images (TOA reflectance; 20m) for winter, spring, summer, autumn; median reflectance per season.
- Context rasters (20m): include height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, tidal water, woodland.
- Classification Scenes: GB classified in 100x100 km tiles (36-band seasonal composites + 10 context rasters → 46-band scenes); NI uses a single 43-band scene per year.
- Bootstrap Training: uses historical UKCEH LCM2015 parcels with ≥99% purity to bootstrap the training set; aims to capture majority signal over time.
- Random Forest: trained with balanced sampling (10,000 samples per class); produces the 20m Classified Pixels product.
- Software: bespoke UKCEH workflow integrating WEKA, PostGIS, and GDAL.

## Spatial framework and data structure
- UKCEH Land Parcel Spatial Framework: unchanged geometry from LCM2015; 0.5 ha minimum mapping unit (MMU); parcels are designed to represent discrete land units.
- gid (parcel identifier): remains stable for 2017–2019 comparisons, but may not align with LCM2015 identifiers.
- Class relationships: 21 UKCEH Land Cover Classes, with additional generalised 10 UKCEH Aggregate Classes; Appendix 1–2 provide mapping to Biodiversity Broad Habitats (BAP).
- Colour and naming conventions: detailed in Appendix 3; text notes clarify distinctions between UKCEH and BAP nomenclature.

## Classification approach and validation
- Bootstrap Training and Random Forest classification underpin automatic map production; no manual region-wide corrections.
- Validation data: 22,325 points derived from GB countryside survey (2019), National Forest Inventory, IACS, and bespoke interpretation points.
- Reported overall accuracy (GB-wide): LCM2017 = 78.6%, LCM2018 = 79.6%, LCM2019 = 79.4%.
- Validation caveats: points are not absolute truth; currency of validation data varies; class conversions between sources can affect accuracy.
- Full validation details and confusion matrices provided in Appendix 4.

## Data quality, limitations, and caveats
- No manual accuracy corrections were performed this release; full automation prioritised for annual updates.
- Seasonal data gaps due to cloud cover are handled by the RF classifier, but future products may explore gap-filling with Sentinel-1 SAR or alternative optical data.
- Some spectral confusions persist (e.g., upland peatland vegetation, certain grassland vs. arable distinctions) despite context layers.
- MMU constraints and parcel-based summarisation can obscure small or fragmented patches; 20m Classified Pixels preserve detail that is lost in parcel-aggregated outputs.

## Data access, usage, and interoperability
- 20m Classified Pixels preserve landscape detail; 25m Land Parcels and 1km rasters enable aggregated analyses and change detection at multiple scales.
- Parcel-level attributes (_hist, _mode, _purity, _conf, _stdev, _n) support detailed summarisation and uncertainty assessment.
- Cross-year comparability is supported via Bootstrap Training, though parcel identifiers (gid) and underlying spatial framework changes mean users should anchor comparisons with gid where possible.
- Appendix 5 provides a full list of datasets per year and per product.

## Appendices and additional notes
- Appendix 1–2 provide detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats, including detection considerations and potential confusions.
- Appendix 3 offers recommended RGB color recipes for display of each UKCEH Land Cover Class.
- Appendix 4 contains the per-class confusion matrices used for validation (producer’s and user’s accuracies by class).
- Appendix 5 lists the full datasets per year and per product.

## Future plans and ongoing development
- UKCEH aims to release a new LCM annually (as stated for LCM2020 and beyond), with planned enhancements to training data and possibly new data sources.
- Ongoing exploration of improved gap-filling strategies (e.g., Sentinel-1 SAR) and refinements to the Land Parcel Spatial Framework to better reflect higher-resolution data and changing landscapes.