# Final Report for LCM2007 - the new UK land cover map

- Aims and scope
  - Delivers a continuous parcel-based land cover map for the UK (LCM2007) with 23 Broad Habitat (BH) classes and 10 aggregate classes, plus vector and raster products at 25 m and 1 km resolutions.
  - Designed to support habitat monitoring, policy, landscape planning, and change detection across the UK.
  - Spatial framework built from national cartography (OS MasterMap and LPS Large-scale Vector) with image-based classification and knowledge-based enhancements (KBEs).

- Outputs and data formats
  - Vector product: land parcels with 23 LCM2007 classes, BHSub, FieldCode, PROBList, KBE history, and other provenance attributes; 10 attributes per parcel detailing processing history and results.
  - Raster products:
    - 25 m: 23 LCM2007 classes.
    - 1 km: two products per location — (A) percentage cover for each class, and (B) dominant class.
  - Metadata: detailed processing steps (Construct, ProbList, KBE, etc.) enabling traceability and reproducibility.
  - Access: 1 km raster data via CEH Information Gateway; full vector and 25 m data available on request under licence (fees may apply).

- Spatial framework, data sources, and validation
  - Core framework combines OS MasterMap polygons with agricultural boundaries and image segmentation to create stable land parcels suitable for change analysis.
  - Minimum feature width/0.5 ha minimum mapping unit (MMU) and 20 m minimum feature width (MFW) chosen to align with 20 m satellite data.
  - Data sources include Landsat, LISS-3, SPOT, AWIFS composites, ground reference points (9127 points), Countryside Survey Broad Habitats (CS BH) for cross-validation.
  - Northern Ireland and GB spatial frameworks differ slightly due to boundary data and segmentation approaches; integration aimed at a coherent UK-wide product.

- Knowledge-based enhancements (KBEs) and thematic resolution
  - KBEs applied post-classification to resolve spectral confusion and improve thematic resolution (e.g., urban vs arable, coastal vs inland).
  - Regionally adaptive rules use terrain, soils, urban proximity, coastal proximity, and other contextual data; KBEs modify about 20% of parcels.
  - Grassland distinctions rely on KBEs plus ancillary data (soil, altitude); spectral separation alone is limited for some grassland types.
  - KBEs and BH associations improve alignment with field surveys when aggregating classes (e.g., grassland groups) for validation.

- Dissimilar area estimates and Countryside Survey (CS) comparison (4.3.2)
  - Dissimilar areas (LCM2007 outside CS 95% confidence limits UK-wide) observed for:
    - Arable and Horticulture
    - Improved Grassland
    - Neutral Grassland
    - Dwarf Shrub Heath
    - Bog
    - Montane Habitats
    - Coastal habitats
  - Key causes for discrepancies (CS vs LCM2007):
    - Differences in classification definitions (what constitutes Arable/Horticulture, boundaries included in LCM2007).
    - Spectral confusion and spectral variability of Arable/Grasslands across multi-year imagery; temporary grass and uncropped land may be included in Arable in LCM2007.
    - Boundaries and linear features mapped differently; LCM2007 boundaries often dissolve into field polygons, affecting area extent.
    - Grassland misclassification between Improved/Neutral/Calcareous/Acid, with soil data of limited use for distinguishing some grassland types.
    - Fen, Marsh and Swamp complexities due to mosaics and small patch sizes; CS often records Fen differently from LCM2007.
  - Specific notes:
    - Arable and Horticulture: LCM2007 ~63,005 km² vs CS upper limit ~51,276 km²; temporal range and boundary inclusion contribute to differences.
    - Improved/Neutral Grassland: substantial differences likely due to grassland classification and soil context; neutral vs improved distinctions are challenging spectrally.
    - Dwarf Shrub Heath and Bog: differences reflect allocation between habitats and the spectral/soil-context rules in KBEs.
    - Fen, Marsh and Swamp: CS often records Fen as larger patches; LCM2007 tends to classify mosaics into Rough Grassland or Acid Grassland; future refinements could use additional KBEs for Fen allocation.
  - Overall, CS comparisons show varying levels of agreement by BH, with grasslands being particularly challenging; Broader BH associations and aggregation improve comparability.

- UK-wide land cover patterns (4.4)
  - UK distribution: over half of UK land cover is intensive (Arable and Horticulture + Improved Grassland) or Built-up Areas and Gardens; remaining is semi-natural, with ~12% in Broadleaved and Coniferous woodlands, ~30% semi-natural (including Mountain, Heath and Bog, Semi-natural Grassland).
  - Country variations:
    - England: highest intensive land use (~64%–76% depending on stratification), with substantial built-up areas.
    - Scotland: lower intensive land use overall but higher Coniferous Woodland; larger semi-natural and upland mosaics (montane habitats).
    - NI and Wales: intermediate patterns with significant grassland and woodland components.
  - Comparison to LCM2000:
    - LCM2007 shows higher Arable area and differences in Grassland proportions compared with LCM2000, reflecting updated spatial framework and KBEs.

- Summary and discussion (4.5)
  - LCM2007 provides high-resolution, continuous UK-wide land cover mapped to BH levels with extensive metadata and multiple data products.
  - Agreement with Countryside Survey varies by habitat type; grassland remains a key challenge due to one-to-many relationships and boundary issues.
  - The spatial framework and KBEs enable improved change detection and habitat assessments, but cross-map change remains complex due to differing spatial and thematic structures among CEH maps (LCM1990, LCM2000, LCM2007).
  - Recommendations for users:
    - Consider aggregating grassland types to improve CS-BH correspondence for policy and monitoring.
    - Use the BH Association approach for assessing correspondences across field surveys.
    - Be mindful of patch size and MMU effects, particularly for Fen, Marsh and Swamp and small habitat patches.
  - The report advocates re-organizing earlier CEH maps into a common real-world spatial framework to facilitate robust change detection.

- Practical implications for GIS specialists
  - LCM2007 offers a detailed, reusable spatial framework with parcellated land cover units suitable for national and cross-border analyses.
  - KBEs provide a structured approach to resolve spectral confusion, but some habitat distinctions rely on ancillary data (soil, altitude) and may require user validation.
  - Vector data with rich provenance and KBE history supports reproducible workflows; 25 m raster provides a balance between detail and processing efficiency; 1 km rasters are suitable for nationwide modeling and integration with other datasets.
  - When comparing to field surveys or national inventories, aggregating classes (e.g., all grasslands) or using Broad Habitat Associations can improve alignment and interpretation.
  - For long-term monitoring and change detection, the stable, reusable spatial framework of LCM2007 is intended to streamline future mapping and analysis.

- Access, licensing and application guidance
  - CEH Information Gateway provides 1 km raster data; full vector and 25 m data available on request under licence (fees may apply).
  - Data support habitat monitoring, biodiversity policy, landscape planning, ecosystem services, carbon accounting, flood risk modeling, urban studies, and other GIS applications.
  - The parcel-level metadata enables reproducibility and traceability in GIS workflows.

- Context within the wider CEH Countryside Survey program
  - LCM2007 is part of Countryside Survey 2007, designed to complement ground-based field surveys (591 CS 1 km squares) with nationwide, wall-to-wall spatial data.
  - Emphasizes the value of integrating in situ and satellite-derived data, as well as linking to European datasets (Corine, LUCAS) and other national/international land cover resources.
  - Highlights the importance of a common spatial structure for effective change detection and policy-relevant analyses across the UK.