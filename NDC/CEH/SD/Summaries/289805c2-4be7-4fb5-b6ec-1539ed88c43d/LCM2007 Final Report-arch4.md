# Final Report for LCM2007 - the new UK land cover map

- Overview
  - Presents the first continuous parcel-based UK land cover map (LCM2007) with 23 Broad Habitat-based classes, produced across GB and Northern Ireland.
  - Provides vector (parcels) and raster products (25 m and 1 km) to support national-scale habitat monitoring, landscape planning, biodiversity policy, and ecosystem service assessments.
  - Builds on Countryside Survey lineage, integrating multi-sensor imagery with national cartography and extensive ancillary data; emphasizes metadata-rich outputs and knowledge-based enhancements.

- Data framework and inputs
  - Multi-source imagery: Landsat TM5, LISS-3, SPOT-4/5; 20–30 m resolution; 60 composites used for UK-wide segmentation; 91% mapped from composites.
  - Ancillary data and references: CEH ground reference points, Countryside Survey Broad Habitats, OS MasterMap GB, NI LPS, soils, DEM, urban and land boundaries; segmentation extended with agricultural boundaries.
  - Spatial framework: UK-wide segment-based vector framework with NI-specific segments; integration with OS and agricultural boundaries to improve spectral delineation.
  - Outputs and metadata: vector product (23 classes) with 10+ attributes per parcel; 25 m raster (23 classes) and 1 km summaries; metadata includes processing steps, ProbList (top spectral variants), and KBEs history.
  - Data access: 1 km raster via CEH gateway; full vector and 25 m raster available on request under licence; licensing details through CEH.

- Classification approach and knowledge-based enhancements
  - Method: parcel-based supervised maximum likelihood classification using ground-reference training areas; iterative training and reclassification; manual edits for challenging scenes.
  - Knowledge-based enhancements (KBE): seven automated context rules (e.g., urban proximity, terrain, hydrology) plus seven additional algorithms; KBEs reassign around 20% of parcels to improve thematic resolution; KBEs are traceable via ProbList and can be reversed if needed.
  - Change considerations: cross-era change mapping is complicated by differing spatial structures, class definitions, and error profiles; separating real change from sensor/classification error remains challenging.

- Comparison with Countryside Survey (CS)
  - Similar area estimates: UK-wide similarity for Broadleaved woodland, Acid Grassland, and Inland Rock.
  - Dissimilar area estimates: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats show substantial differences.
  - Key factors driving differences:
    - Classification definitions and what constitutes each class (e.g., temporary grassland inclusion in Arable and Horticulture).
    - Spectral variability and spectral confusion, especially for Arable and Horticulture.
    - Differences in mapping of Boundary and Linear Features (CS versus LCM MMU handling).
    - Grassland intricacies: Improved vs Neutral Grassland allocation; spectral similarity complicates accurate sub-classing.
    - Fen, Marsh and Swamp is highly mosaic and small-scale; CS vs LCM7 differs in how these areas are represented and validated.
    - Montane and coastal habitats are underrepresented in CS, contributing to divergence.
  - Implications: large-scale grassland classification uncertainties; potential to use KBEs to better allocate mosaic habitats (e.g., Fen, Marsh and Swamp) in future work.

- UK Land Cover distribution (4.4)
  - National picture: over 50% of the UK in intensive land use (Arable and Horticulture + Improved Grassland) with 12% Broadleaved/Mixed/Yew woodland and 6% Coniferous woodland; ~30% semi-natural or natural, including coastal, semi-natural grasslands, and mountain/hill habitats.
  - Country-level variation: England ~76% intensive land use; Scotland ~36% intensive with large Coniferous Woodland and substantial Montane habitats; Northern Ireland and Wales show intermediate values; freshwater and coastal distributions vary by region.
  - Historical comparison: LCM2007 tends to differ from LCM2000 in Arable and Grassland shares; spatial framework changes contribute to some of these shifts.
  - Implications: habitat composition and landscape governance differ by country; cross-country comparability benefits from aggregated classes and standardized spatial frameworks.

- Summary and discussion (4.5)
  - Agreement between LCM2007 and CS varies by Broad Habitat; grassland sub-types present fundamental interpretive challenges.
  - Broad Habitat Association (BHA) rules were developed to improve correspondences across different mapping schemes, particularly for grassland and mosaics.
  - LCM2007 shows high correspondence with CS 1 km squares for Arable and Horticulture, but larger overall Arable estimates reflect classification and boundary-feature differences.
  - Fen, Marsh and Swamp exhibits substantial UK-wide discrepancies due to habitat mosaic and small patch size; consideration of additional data layers and KBEs could improve allocation to Fen, Marsh and Swamp in future updates.
  - Recommendations for users: consider aggregated grassland categories to improve cross-dataset comparability; interpret semi-natural habitats with caution due to classification ambiguity.
  - Data governance angle: demonstrates feasibility of a continuous UK-wide land cover product, but highlights the need for ongoing harmonization, validation, and inter-agency collaboration to refine spatial frameworks and KBEs for future monitoring.

- Example areas and products (5)
  - Demonstrates LCM2007 in upland, calcareous, urban, arable, and fenland contexts; illustrates the interaction of habitat types, urban interfaces, and landscape mosaics.
  - Vector and raster products explained: 25 m and 1 km resolutions; vector provides parcel-level metadata; 1 km products suitable for national-scale modeling and integration with climate and species distribution datasets.

- Change detection and governance implications for Data Leaders
  - The project emphasizes a repeatable, UK-wide, parcel-based data framework linked to static boundaries (e.g., MasterMap), facilitating future change detection.
  - Highlights the complexity of cross-era comparisons; stress on developing robust methodologies to distinguish real land cover change from methodological differences.
  - Data Leaders should promote:
    - Metadata-rich, queryable datasets with clear provenance and KBEs history.
    - Interoperability with national cartographic products and other data layers ( soils, hydrology, urban) to support governance and policy.
    - Access governance and licensing structures that balance open research use with licensing constraints.
    - Standardized validation pipelines and crosswalks with longitudinal datasets (e.g., Countryside Survey) to support policy evaluation and reporting.
  - Encourages collaboration to refine spatial frameworks, KBEs, and validation datasets for future updates and to improve cross-dataset comparability.

- Access, licensing, and outputs for decision-making
  - Outputs: vector (23 classes), 25 m raster, 1 km summaries; detailed metadata per parcel to support traceability and independent validation.
  - Access: 1 km raster openly via CEH gateway; full vector and 25 m raster available by licence on request; potential fees apply.
  Applications: biodiversity assessments, ecosystem service analysis, landscape connectivity, catchment and resource planning; useful as a contextual base map for higher-resolution habitat mapping and policy evaluation.

- Key takeaways for Data Leaders
  - A robust, repeatable, UK-wide data framework with metadata-rich outputs (including KBEs and ProbList) enables better governance, comparability, and policy support.
  - Integrating multi-sensor imagery with national cartography delivers a scalable baseline for monitoring change, but requires careful handling of class definitions, spatial structure, and validation across datasets.
  - The LCM2007 experience underlines the value of cross-partner collaboration, standardized validation approaches, and a staged data access model to balance openness with licensing and governance needs.
  - Future progress hinges on refining knowledge-based rules, developing crosswalks with field surveys (e.g., Countryside Survey), and adopting a common spatial framework to improve change detection and comparability across datasets.