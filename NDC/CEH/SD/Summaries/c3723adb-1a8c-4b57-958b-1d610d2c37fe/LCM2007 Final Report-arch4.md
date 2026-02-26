# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Presents the Land Cover Map 2007 (LCM2007), the first continuous parcel-based UK land cover map, derived from multi-temporal remote sensing and knowledge-based enhancements.
  - Maps Broad Habitats (BH) and Broad Habitat Associations (BHA) to support biodiversity policy, landscape planning, and ecosystem assessments.
  - Delivers a robust data platform (vector parcels and raster products) across UK, GB, England, Scotland, Wales, and Northern Ireland, enabling monitoring and change detection.

- Data products and specifications
  - 23 LCM2007 classes, aggregated into 10 Broad Habitats (BH) and 10 Broad Habitat Associations (BHA); 17 terrestrial BHs when aggregated.
  - Spatial units: minimum mappable unit around 0.5 ha; 20 m satellite data basis; 25 m raster product; vector product includes detailed attributes; 1 km raster products summarize coverage.
  - Data products:
    - Primary vector product with polygon attributes, knowledge-based enhancements (KBE) history.
    - 25 m raster product (23 classes).
    - 1 km raster products (23 classes and 10 aggregates) providing percent cover or dominant class per square.
  - Metadata: comprehensive processing history retained with each polygon for traceability and reuse.

- Data sources and spatial frameworks
  - Satellite imagery (primary): Landsat-TM5, IRS-LISS3, SPOT-4/5; AWIFS as backup; 20–30 m pixels; multi-date composites used where possible.
  - Ground truth and validation: CEH ground reference points (2006–2008); Countryside Survey (CS) BHs for independent comparison.
  - External spatial data: OS MasterMap (GB), LPS Large-scale Vector (NI), agricultural boundaries, urban areas, soils, elevations, and other ancillary data.
  - Spatial framework: nine UK “chunks” with rules for continuous coverage; segmentation enhanced by image data and agricultural boundaries to improve spectral cohesion and boundary detail.

- Classification framework and knowledge-based enhancements (KBE)
  - Method: parcel-based supervised maximum likelihood classification with iterative training refinement.
  - KBEs address spectral confusion and improve thematic resolution by incorporating contextual data (urban boundaries, coastal proximity, terrain, soils).
  - A sequence of seven automated KBEs applied; terrain/soil components and urban/rural context refine parcel classifications; KBEs modify about 20% of parcels with documented adjustments.

- Validation, accuracy, and comparisons
  - Overall accuracy around 83% for LCM2007 classes; class-specific accuracies vary.
  - Countryside Survey (CS) comparison indicates:
    - Similar area estimates for Broadleaved woodland, Acid Grassland, and Inland Rock.
    - Dissimilar estimates for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
  - Key factors driving differences with CS:
    - Differences in class definitions and temporal alignment (images from multiple years).
    - Spectral confusion, especially for Arable and Horticulture due to high spectral variability and field changes.
    - Inclusion of Boundary/Linear Features in LCM2007 vs CS mapping approaches, affecting field-area estimates.
    - Grassland categories: challenges separating Improved vs Neutral/Calcareous/Acid grasslands; Rough Grassland inclusion in LCM2007; soil data limitations for grassland typing.
    - Fen, Marsh and Swamp areas are particularly variable and often underrepresented in LCM2007 due to small patch size and spectral mixing.
  - UK-wide and country-level patterns: LCM2007 generally aligns with CS for some broad categories but shows substantial variation for others; CS patch-size and stratification affect comparability.

- UK Land Cover distribution and temporal context
  - UK-wide: more than 50% of land is intensive use (Arable and Horticulture plus Improved Grassland) or built-up; woodlands occupy ~12%; remaining area is semi-natural.
  - Country differences: England shows the highest intensive land use; Scotland has the largest share of Coniferous Woodland and substantial semi-natural mountain/grassland areas; CS comparisons across countries reveal varying levels of agreement.
  - Comparison with LCM2000 indicates shifts in Arable and Semi-natural Grassland proportions; spatial framework changes complicate direct comparisons.

- Access, licensing, and data availability
  - 1 km raster data sets available via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under licence; fees may apply.
  - Documentation and metadata provided to enable traceability and reuse.
  - Data formats include vector parcels with rich attributes and KBEs; 25 m and 1 km raster products for broad-scale analyses; cross-referencing with CS possible through BH/BHA frameworks.

- Applications and relevance for Data Leaders
  - Provides a robust, scalable data platform for monitoring habitat extent, connectivity, and ecosystem services.
  - Supports evidence-based policy across biodiversity, landscape planning, catchment management, climate assessments, carbon accounting, and urban planning.
  - Delivers a reusable spatial framework (coast-to-coast UK) to underpin future land surface mapping, change detection, and policy evaluation.
  - Demonstrates the value of integrating multiple data sources (cartography, soils, elevation, urban/agricultural boundaries) and knowledge-based rules to improve data quality and user trust.
  - Highlights the need for ongoing data standards, rich metadata, and accessible data to enable co-ownership and collaboration across policy, planning, and scientific communities.

- End notes and key takeaways
  - LCM2007 marks a major advancement, balancing automated classification with knowledge-based refinements while aligning with BH/BHA frameworks.
  - Grassland and upland classifications remain challenging; the KBEs help in many cases but cannot fully resolve all ambiguities.
  - The project emphasizes the value of a common, static spatial framework for efficient future monitoring and change detection.

- Related validations and governance
  - Bespoke validation approach enables parcel-level assessment with KBE history; users can apply image-–based plausibility checks to assess fit-for-purpose accuracy.
  - Appendix materials outline Broad Habitat Association (BHA) rules to improve cross-product correspondences and to guide interpretation of land cover across datasets.
  - The report advocates integrating ground surveys (CS) with satellite-derived maps to enhance understanding of habitat quality and change over time.

- Broader context and European links
  - UK component contributes to Corine Land Cover 2006 via transformation from LCM2007 vector, supporting pan-European environmental assessment.
  - LCM2007 builds on European data initiatives (IMAGE2006) and aligns with broader European land cover monitoring efforts to facilitate cross-border analyses.