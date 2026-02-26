# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- UKCEH releases three national land cover maps (LCMs): LCM2017, LCM2018, and LCM2019, built from a common data framework and 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats references.
- Purpose: provide rapidly produced, automatically classified, UK-wide land cover maps with documented production methods, validation, and plans for ongoing annual updates.

## Data products and structure

- 21 UKCEH Land Cover Classes (not a 1:1 match to BAP in all cases; classes are aligned for comparability and change detection).
- Dataset suite (per year, GB and NI):
  - 20m Classified Pixels: 2-band, 8-bit rasters; class label and per-pixel confidence (0–100). Provides the finest detail and preserves narrow features.
  - Land Parcels: attributes derived from intersecting 20m pixels with the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha). Includes cadence-related attributes and a history of changes.
  - 25m Rasterised Land Parcels: 3-band rasters (dominant class, confidence, purity).
  - 1km Raster datasets:
    - 1km Percent Cover (21-band, 8-bit)
    - 1km Percent Aggregate Cover (10-band, 8-bit)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- Geographic scope and formats:
  - Great Britain (GB) and Northern Ireland (NI) have separate coordinate systems: GB = EPSG:27700 (British National Grid), NI = EPSG:29903 (TM75 Irish Grid).
  - Datasets are duplicated for each year, resulting in 42 primary datasets (plus metadata and appendices).

## Production workflow, methodology, and data lineage

- Bootstrap Training: automatic generation of training data from historic LCMs (starting with LCM2015), enabling rapid production without fresh field data.
  - Bootstrapped training uses majority signal across years to train Random Forest (RF) classifiers.
  - For 2017–2019, training data derived from LCM2015 parcels with high purity (≥99%).
  - Plans indicate evolving bootstrap strategies for future maps (e.g., 2020, 2021).
- Random Forest classification:
  - RF classifier trained on balanced samples (10,000 samples per class) from 36-band Seasonal Composite Images plus 20m Context Rasters.
  - Separate classifications per 100x100 km GB tile; NI uses a single 43-band scene per year.
- Data inputs:
  - Seasonal Composite Images from Sentinel-2 (TOA reflectance; no full SR processing applied in production for these years).
  - 20m Context Rasters (terrain, proximity to buildings/roads/seawater, foreshore, tidal water, woodlands) to improve spectral separability.
  - Classification Scenes and tile-based processing designed to ensure spectral/phenological variation is captured.
- UKCEH Land Parcel Spatial Framework:
  - Framework unchanged in footprint since LCM2015 but with storage/index adjustments; gid identifiers differ from LCM2015 for most parcels.
  - Framework emphasizes MMU ~0.5 ha and aims to facilitate time-series comparisons via spatial overlap.
- Data structure and evolution:
  - 20m Classified Pixels preserve detail; Land Parcels summarize through the Spatial Framework; 25m Rasterised Parcels generalize parcel data for broader-scale analyses.
  - Some attribute name changes align with production software conventions; text descriptions linked to dominant class via lookups.
- Validation and quality control:
  - UK-scale validation against GB countryside survey data (2019), National Forest Inventory, IACS, and bespoke validation points (n ≈ 22,325).
  - Reported accuracies: LCM2017 ≈ 78.6%, LCM2018 ≈ 79.6%, LCM2019 ≈ 79.4% (relative to the validation points; currency varies by product year).
  - Validation acknowledges potential mismatches in class mappings and notes the 80% correspondence as a strong indicator given automatic production.

## Data governance, metadata, and update cycle

- Update cycle: intended to release a new LCM annually (as a strategic objective to monitor land cover change more effectively).
- Metadata and documentation:
  - Appendix 4 provides detailed validation statistics and class-level confusion matrices.
  - Appendix 5 lists the full datasets per year and per geographic region (GB/NI) with naming conventions and storage descriptions.
  - Appendix 1 and 2 provide notes on UKCEH Land Cover Classes and their relation to UK BAP Broad Habitats.
  - Appendix 3 provides recommended RGB color mappings for visualization.
- Access considerations:
  - GB and NI datasets are provided at the 20m, 25m, and 1km scales, with detailed parcel-level attributes and per-pixel confidence measures.
  - Land Parcel Spatial Framework identifiers (gid) are stable within the LCM2017–LCM2019 set for cross-year comparisons using gid, though gid values do not correspond to LCM2015 parcels.
- Limitations and caveats for governance:
  - No deliberate manual corrections were applied in these maps; classification is fully automated.
  - Some spectral ambiguities remain, particularly among upland peatlands and coastal/intertidal zones.
  - Context rasters and the helper layers introduce improvements but may still cause cross-class confusions (e.g., Saltwater vs Freshwater near coasts).
  - Validation data come from sources with different class definitions; caution is advised when interpreting absolute accuracy figures.

## Practical implications for data stewards

- Data provenance and reproducibility:
  - Clear, documented production workflow: Bootstrap Training, RF classification, and use of Seasonal Composite Images with Context Layers.
  - Versioning and yearly updates enable longitudinal studies; gid-based parcel tracking supports change detection analyses within the same parcel framework (except for gid continuity with LCM2015).
- Data schema and interoperability:
  - Consistent class scheme (21 UKCEH Land Cover Classes) across years enhances comparability; 10 UKCEH Aggregate Classes available for broader analyses.
  - Multiple spatial resolutions and corresponding metadata support diverse use cases (fine-grained analysis with 20m pixels, aggregate assessments at 1km, and parcel-based summaries).
- Documentation and governance alignment:
  - Comprehensive appendices (habitat definitions, data recipes, validation matrices) facilitate harmonization with other datasets and governance standards.
  - Clear notes on data limitations, classification rationale, and future plans aid data stewards in risk assessment and policy alignment.

## Endnotes and additional context

- The document includes detailed tables, figures, and appendices:
  - Table 1–5: class mappings, parcel attributes, and dataset metadata (GB and NI counterparts).
  - Figure 2–3: visual explanations of dataset types and generalization effects.
  - Appendix 1–2: in-depth notes on UKCEH Land Cover Classes and BAP Broad Habitats.
  - Appendix 4: confusion matrices and accuracy metrics at the class level.
  - Appendix 5: full datasets listing for LCM2017, LCM2018, and LCM2019.
- References and acknowledgments point to foundational methods (Bootstrap Training, RF, and prior LCM production work) and related methodological papers.