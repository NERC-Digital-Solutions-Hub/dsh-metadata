# The UKCEH Land Cover Map for 2023

- A user guide for LCM2023, the UKCEH land cover product for 2023, describing seven datasets (three per region for GB and NI) plus a 1 km summary raster.
- Purpose: explain data production, validation, and accuracy to help users apply LCM2023 appropriately and understand its limitations.
- Aim for Data Leaders: understand the end-to-end data system, governance, and how to manage, discover, and use these assets for monitoring land cover state and change.

## Data content and structure

- Datasets included
  - 10 m Classified Pixel datasets (GB and NI): pixel-level land cover class with a second band for class membership probability/confidence.
  - 25 m Rasterised Land Parcel datasets (GB and NI): land parcels derived by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework; three raster bands per parcel (mode, conf, purity).
  - 1 km raster products (GB and NI): summary rasters with dominant class and percentage cover per 1 km cell (two summary bands for dominant/aggregate, plus 21 bands for class percentage).
  - 1 km Dominant and Percentage cover products are designed to enable change detection and coarse-scale summaries.
- Spatial details
  - 10 m classified pixels preserve fine landscape features; no generalisation by Land Parcel framework at this resolution.
  - Coordinate systems: Great Britain = British National Grid (EPSG:27700); Northern Ireland = Irish Grid (TM75, EPSG:29903).
  - Parcel framework MMU ~ 0.5 ha; parcels are designed to represent discrete land units (fields, parks, urban areas, etc.).

- Production-scale attributes
  - 10 m pixels: two-band product per region (class, class confidence).
  - 25 m parcels: three attributes per parcel (dominant class, confidence, purity).
  - 1 km rasters: dominant class, aggregate, and class percentage bands (for both GB and NI).

- Data sources and components
  - Seasonal Composite Images: Sentinel-2 multispectral data (ten bands) resampled to 10 m, with four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
  - Context Rasters: 10 m auxiliary layers to reduce spectral confusion (e.g., terrain, distance to buildings/roads/coast, land/water masks, etc.).
  - Classification Scenes: GB classified in 32 tiles (~100 x 100 km) with a single Scene for NI (49-band scene combining Sentinel-2 with NI Context Rasters).
  - UKCEH Land Parcel Spatial Framework: 0.5 ha MMU framework used to structure 10 m pixels into parcels; parcels provide stable units for time-series comparison.

## Data production and methodology

- Bootstrap Training
  - Automatic training data generation from historical LCM maps (LCM2020–2022) with >80% probability and consistent class across three years.
  - Enables training without fresh field data, leveraging wall-to-wall historical coverage.
- Random Forest classification
  - Balanced training across classes via bagging (10000 samples per bag) to prevent dominance by more common classes.
  - Produces the 10 m Classified Pixel product; probability/confidence is linked to the class assignment.
- Seasonal and context data fusion
  - Classification Scenes are built from Seasonal Composites plus Context Rasters to improve discrimination, particularly where spectral signals are similar.
- UKCEH Land Parcel Spatial Framework
  - Land parcels are derived by generalising national cartography and aligning them to the 10 m pixel results; the framework supports change detection and time-series analyses.
- Validation and accuracy
  - Formal validation with 33,107 points across 21 classes.
  - Overall accuracy reported at 83%.
- Software and tooling
  - Custom UKCEH software integrating Weka (RF), PostGIS, and GDAL; uses open-source components.

## Data quality, validation, and known issues

- Validation
  - Overall accuracy: 83% against a comprehensive reference dataset from countryside surveys, National Forest Inventory, Rural Payments, and bespoke validation points.
- Known issues
  - A small number of land parcel vectors are missing, causing nodata areas in the 25 m rasterised parcel dataset (negligible impact on 1 km products; 10 m classified pixels unaffected).
- Accuracy details
  - Validation includes detailed producer’s and user’s accuracy matrices across all classes; spatial patterns show typical confusions (e.g., between grassland types, bog/peat-related classes) common in satellite-based land cover mapping.
- Known caveat
  - Slight methodological differences across years can yield small changes not tied to real land cover change; annual updates aim to minimize non-dynamic discrepancies.

## Access, citation, and governance

- Data citations and DOIs
  - Each LCM2023 dataset has a DOI; examples include:
    - 10 m Classified Pixels GB: https://doi.org/10.5285/7727ce7d-531e-4d77-b756-5cc59ff016bd
    - 10 m Classified Pixels NI: https://doi.org/10.5285/17223091-ca33-41f8-bd5b-bdd2a222cdae
    - 25 m Rasterised Land Parcels GB: https://doi.org/10.5285/ab10ea4a-1788-4d25-a6df-f1aff829dfff
    - 25 m Rasterised Land Parcels NI: https://doi.org/10.5285/becb5f16-948f-407b-8fa3-f7762ba6efb6
    - 1 km Summary Rasters (GB/NI): https://doi.org/10.5285/96bc980a-31b4-4d1b-87e9-007d4932a56b
  - Full citations and dataset-specific references are provided in the accompanying table (Table 5) and the Marston et al. papers for historical methods.
- Usage guidance
  - Formal validation and uncertainty guidance are provided; users should interpret 10 m pixel classifications with caution in fine-scale analyses and rely on 25 m parcel or 1 km summary products for stable aggregations.
- Distribution and disclaimers
  - The data are intended for annual production; differences year-to-year reflect both real change and methodological evolution; users should align analyses with the temporal resolution and update cadence.

## Practical implications for Data Leaders

- Data system view
  - LCM2023 provides a multi-resolution, audited data stack (10 m pixels, 25 m parcels, and 1 km summaries) with explicit metadata, lineage, and validation metrics.
  - The land parcel framework adds stability for time-series analysis while preserving high-resolution detail at the pixel level.
- Governance and data management
  - Annual production enhances temporal consistency, enabling clearer separation of change from random classification noise; useful for continuous monitoring and KPI tracking.
  - Bootstrap Training enables near-wall-to-wall coverage without bespoke field campaigns, but acknowledges potential limitations for transition-sensitive classes (e.g., arable vs. grassland).
- Discoverability and integration
  - Clear DOI-based citations and data provenance support reproducibility and integration with other UKCEH datasets; harmonised coordinate systems facilitate cross-border integration (GB and NI).
  - Complementary context rasters and Seasonal Composites improve data usability across policy, planning, and research use cases.
- Limitations and planning
  - Be mindful of known issues (missing vector parcels, potential class confusion in spectral-near-neighbor habitats, and coastal salt/freshwater delineation near tidal areas).
  - For precise boundary work, rely on 25 m parcel data or higher-level 1 km summaries; for detailed habitat mapping, balance 10 m detail with validation status.