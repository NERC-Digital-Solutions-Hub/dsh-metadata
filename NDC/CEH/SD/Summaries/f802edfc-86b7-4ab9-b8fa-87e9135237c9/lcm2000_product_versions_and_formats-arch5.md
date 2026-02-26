# LCM2000

- LCM2000 is a parcel-based thematic land cover map of the United Kingdom, updating and extending the Land Cover Map of Great Britain (LCMGB) 1990 to provide an all-UK dataset (including Northern Ireland). It is derived from satellite imagery (mainly Landsat) with additional ancillary data and is classified against the Joint Nature Conservation Committee (JNCC) Broad Habitats. Produced in both vector and raster formats, it supports multiple detail levels and resolutions.

## Data structure and formats

- Vector data: parcels (polygons) with attached attributes; standard Level 2 (26 Subclasses) and Level 3 (72 Variant level) detail; Level 3 available by special arrangement.
- Raster data: 25m resolution (26 Subclasses) and 1km resolution (derived from 25m, with Subclass-level data, Dominant values, and Percentage values; 1km also provides Aggregate class level).
- Primary data formats: ESRI shapefile (vector); GeoTIFF (raster); ArcGIS users may require Spatial Analyst extension.
- Minimum mappable unit: parcels larger than 0.5 ha; smaller parcels are dissolved into surrounding land.
- Raster is not directly comparable with LCM1990 due to different production methods; not suitable for long-term change estimation.

## Coverage and classification scope

- Dataset compiled on a 100km tile basis; parcels are classified per tile and tiles may be merged to form the full country dataset.
- Hierarchical classification aligned with Broad Habitats; includes broader use extensions and possible Level 3 detail where applicable.
- Contextual and sensor- and date-dependent limitations may affect subclass/variant distinctions (dominant land cover at imaging time).

## Hierarchical nomenclature and class detail

- Subclass and Variant coding supports Level 2 (26 subclasses) and Level 3 (72 variants, where available).
- Variant detail (Level 3) depends on dominant cover at acquisition; not all regions will have Level 3 detail.
- Table-based coding links: Subclass codes and Variant codes correspond to land cover types, with descriptive names provided in accompanying material.

## Vector polygon attributes and provenance

- SegID: unique parcel identifier (stable for communication and provenance).
- BHSub: dominant land cover type (Level 2) code.
- BHSubVar: dominant land cover at Level 3 (when present).
- PerPixList: top-five spectral subclass percentages per parcel (Level 3 only).
- OpHistory: processing history descriptor for each parcel (input data, dates, KBC rules, etc.) with a structured six-field history plus an additional field for other information.
- TotPixels and CorePixels: total pixels in the parcel and pixels in the core area used for maximum likelihood classification.
- The dataset is designed to retain full lineage and processing history to support data governance and traceability.

## Processing history, quality controls, and accuracy

- OpHistory (PHD) records input scene, sensor (e.g., TM, IRS), acquisition dates, cloud-hole patches, and knowledge-based corrections (KBC) applied in phases 1 and 2.
- Phase 1 KBC rules capture scene-dependent corrections; Phase 2 KBC rules capture UK-wide adjustments.
- The data philosophy emphasizes retaining as much information as possible; users are encouraged to preserve parcel-level metadata and, when modifying data, to store changes in new attributes to maintain lineage.
- The document cautions about inherent inaccuracies due to data model, scale, resolution, interpretation, and target definitions; not all differences reflect errors.

## Edge overlaps, mosaicking, and artefacts (Appendix 1)

- Edges between overlapping 100km tiles may contain artefacts due to mosaic construction and patching with different imagery.
- Artefacts are uncommon and typically affect less than ~0.1% of parcels; users are advised to visually tidy edge areas by dissolving boundaries between adjacent parcels of the same class, without altering the underlying attribute data globally.
- Methods for dealing with edge artefacts include clipping to tile edges, unioning tiles, and dissolving boundaries—each with trade-offs:
  - Clipping may invalidate parcel-level attributes derived from source data.
  - Union can duplicate attribute handling; dissolving can lose some source metadata.
  - For Level 3 data, preserve bhsubvar during dissolve to avoid losing Level 3 information.
- Slivers and very small parcels can be managed by visual removal, dissolving into adjacent parcels, or “intelligent” dissolution based on boundary length with surrounding parcels.

## Customisation, governance, and data stewardship

- LCM2000 is designed as both a map and a data storage/analysis framework; users are encouraged to customize and extend the database, while maintaining provenance.
- Unique Segid labeling should be retained to enable unambiguous communication with the data management team and other users.
- Production philosophy prioritises preserving information; when altering data, record lineage in parcel metadata and retain original attributes or capture them in new attributes.
- Documenting changes is essential for data management, security, and user feedback.

## Production context, documentation, and references

- Production methods and full methodology are documented in external sources (FullER et al., Smith et al., Jackson et al.), with further guidance on Broad Habitat interpretation.
- For additional information and data access, contact the Land Cover Map team via the CEH Data portal or email, including references to related literature.

## Limitations and guidance for data stewards

- LCM2000 is not designed for estimating change over the 10-year period with the 1990 baseline; dataset versions differ in methods and are not directly comparable for change detection.
- Accuracy varies by region and land cover type; users should interpret results within the context of data model, acquisition conditions, and classification rules.
- When sharing or integrating LCM2000 data with other datasets, preserve Segid and key attribute fields to maintain traceability and data integrity; be aware of potential edge artefacts and the implications of tile merging on attribute data.