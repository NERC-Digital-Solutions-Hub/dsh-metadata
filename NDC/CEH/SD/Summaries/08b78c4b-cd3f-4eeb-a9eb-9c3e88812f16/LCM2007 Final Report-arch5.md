# Final Report for LCM2007 - the new UK land cover map

## Executive summary for Data Stewards
- LCM2007 provides a UK-wide, parcel-based land cover map with 23 land cover classes (mapped to Broad Habitats) and two raster products (25 m and 1 km) plus a detailed vector dataset with rich provenance.
- The dataset is derived from multiple sources (satellite imagery, national cartography, soils, DEMs, urban and agricultural boundaries) and is accompanied by extensive metadata, processing logs, and knowledge-based enhancements (KBEs) to improve classification accuracy.
- Access to data is tiered: 1 km rasters openly via the CEH Information Gateway; full vector and 25 m products on request under licence (fees may apply). Comprehensive provenance and KBE histories support governance, auditing, and re-use.
- Change detection is complex due to differences in spatial structure and classification schemes across CEH maps (LCM1990, LCM2000, LCM2007); robust change analysis requires specialized methods that account for these structural differences.

## What LCM2007 is and why it matters to data governance
- First continuous parcel-based land cover map for the UK, integrating detailed national cartography with multi-temporal imagery, enabling repeatable, reusable monitoring and policy support.
- Supports habitat monitoring, biodiversity policy, ecosystem services, landscape planning, climate and carbon accounting, and catchment management.
- Provides a common spatial framework to aid country comparisons and long-term change detection, while acknowledging limitations in comparing to Countryside Survey (CS) outputs.

## Data products and provenance
- Vector product: 23 LCM2007 land cover classes with 10+ attributes documenting processing, provenance, and KBEs; includes Broad Habitat Sub-classes (BHSub) and FieldCode, plus KBE histories (manual corrections, soil adjustments, coastal/offshore masks, etc.). Not all sub-classes are validated for accuracy.
- Raster products: 
  - 25 m resolution, 23 LCM2007 classes.
  - 1 km resolution rasters providing either (A) percentage cover per class or (B) dominant class per pixel.
- Minimum mapping unit and metadata: 0.5 ha MMU; outputs come with extensive metadata and processing provenance for reproducibility and auditing.
- KBEs: seven automated algorithms that resolve spectral confusion using contextual data (urban boundaries, soils, terrain, coastal proximity, etc.); about 20% of parcels are modified by KBEs; all KBEs are traceable and reversible if needed.

## Data sources, spatial framework, and governance considerations
- Data sources: Landsat TM/ETM+, SPOT-4/5, IRS AWIFS/LISS-III; ground reference points; Countryside Survey (CS) data; national cartography (OS MasterMap), agricultural boundaries, urban outlines, soils, and DEMs.
- Spatial framework:
  - Great Britain: boundary-aligned MMU with 0.5 ha minimum; segmentation integrates Landsat/image segments with cartography and boundaries.
  - Northern Ireland: LPS Large-scale Vector polygons; generalised similarly; agricultural boundaries largely excluded in NI context.
  - UK is produced as a continuous vector product (GB and NI databases) to avoid boundary inconsistencies seen in tile-based approaches.
- Pre-processing and alignment: cloud masking, atmospheric correction, geo-registration, topographic correction; three-band segmentation using winter NIR, summer red, and summer MIR composites.
- Validation and QA: knowledge that accuracy varies by habitat type; field validation used (_CS 2007, GB ground references), with an overall class accuracy around 83% for LCM2007; grassland and fen-type classes show notable classification challenges and require KBEs or auxiliary data for better discrimination.

## Classification approach and interpretability
- Approach: parcel-based supervised classification (maximum likelihood) of 23 LCM2007 classes, mapped to 17 Broad Habitats.
- KBEs enhance thematic resolution by incorporating non-spectral data (soil type, altitude, proximity to coast, urban boundaries, etc.); about 20% of parcels are altered by KBEs.
- Some Broad Habitats cannot be uniquely determined from optical imagery alone; KBEs help disambiguate grassland types (e.g., Neutral, Calcareous, Acid) through contextual rules.
- The Broad Habitat Association (BHA) rules provide structured correspondences between LCM2007 classes and CS classes, describing where mappings are straightforward vs. where caution is needed.

## Data quality, validation, and interpretation guidance
- Validation outcomes:
  - Overall producer/user accuracy varies by class; examples show high accuracy for some habitats (e.g., Bog) and more ambiguity for grasslands.
  - UK-wide CS comparison shows substantial variation by habitat; Arable and Horticulture tends to be overestimated by LCM2007 relative to CS upper limits, influenced by class definitions and inclusion of boundaries, as well as temporal image requirements.
  - Fen, Marsh and Swamp shows large discrepancies due to mosaic nature and small patch sizes, with many CS maps reflecting finer-scale components that LCM2007 cannot always detect consistently.
- Important caveats:
  - Change mapping is difficult because LCM2007’s spatial structure differs from LCM1990/2000; robust detection of genuine land cover change requires reorganising earlier maps into a common spatial framework.
  - Temporal consistency and spectral variability (e.g., arable crops with seasonal signatures) can drive misclassification.
  - Some habitat areas are below the MMU, potentially biasing area estimates for certain habitats in comparisons with CS.
- Bespoke validation methodology (Appendix 4) emphasizes fit-for-purpose accuracy assessment, and proposes parcel-level validation leveraging the LCM2007 parcel metadata and a Bayesian-like fuzzy validation approach using high-resolution imagery.

## Access, licensing, and governance implications
- Access levels:
  - 1 km rasters: open via CEH Information Gateway.
  - Full vector and 25 m rasters: available on request under licence; fees may apply.
- Governance tools:
  - Comprehensive provenance for each parcel (source images, processing steps, and KBEs) allows auditability and potential reversion of enhancements.
  - KBEs and processing logs facilitate reproducibility and governance of data processing histories.
- Data stewardship recommendations:
  - Maintain and provide clear licensing terms, data provenance, and KBEs history for re-use.
  - Offer guidance on selecting appropriate products (vector vs raster) given processing overhead, analytical needs, and scale.
  - Provide robust change-detection guidelines that account for structural differences across LCM generations.

## Practical applications and integration with other data
- Applications include habitat monitoring, biodiversity assessment, landscape planning, climate and carbon accounting, catchment management, and ecosystem service evaluation.
- The dataset serves as a coherent UK-wide reference frame compatible with CS outputs while acknowledging structural differences; can be used alongside field surveys, LiDAR, soil and climate data for enhanced policy-relevant analyses.
- European links: LCM2007 data support Corine Land Cover translation and European-scale land cover assessments (e.g., LUCAS, Corine), enabling cross-border environmental reporting.

## Key challenges and caveats for data stewards
- Spectral confusion, particularly within grassland and fen-related habitats; KBEs and auxiliary data (soil, altitude) are essential for improving separation of similar classes.
- Coastal, offshore, and montane zones introduce complexity in classification and validation.
- Change detection remains challenging due to differing spatial structures across LCM generations; aggregated class trajectories and consistent framework are recommended for robust change analyses.
- Data volumes are large; governance should include clear metadata standards, licensing terms, and data-use guidance.

## Enduring context and future-sense
- LCM2007 builds on LCM1990 and LCM2000, moving toward a reusable, Europe-aligned, parcel-based framework with a generalised but interoperable spatial structure anchored to real-world land units.
- The framework supports ongoing national monitoring and future re-mapping efforts by preserving boundary-based structure while enabling scalable, repeatable analyses.

## Appendix highlights relevant to Data Stewards
- Appendix 4 Bespoke validation: proposes a two-part validation approach (high vs moderate probability parcels) and a Python-based tool for informal validation using high-resolution imagery.
- Appendix 5 Broad Habitat Association: documents the rationale and rules linking LCM2007 classes to CS classes, including handling of Bog, Dwarf Shrub Heath, Montane habitats, Built-up areas, Fen, Rough grassland, and Water classes.
- Chapter 6 discusses change detection, CS integration, and European data connections (Corine/LUCAS), emphasizing the need for a common spatial framework to enable robust national change monitoring.