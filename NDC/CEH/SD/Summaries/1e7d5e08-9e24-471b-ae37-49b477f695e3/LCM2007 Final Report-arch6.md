# Final Report for LCM2007 - the new UK land cover map

## Overview
- LCM2007 delivers the first UK land cover map as continuous parcels (10 million+ land parcels GB and NI included) with 23 land cover classes that map to 17 Broad Habitats.
- Outputs include a vector parcel dataset, a 25 m raster, and 1 km summary products for broad-scale analysis.
- The project provides rich metadata and a knowledge-based enhancement framework to support flexible re-analysis and user-specific reclassification.

## Data sources and spatial framework
- Spatial framework built from national cartography:
  - GB: OS MasterMap topography layer; NI: LPS Large-scale Vector.
  - Parcels generalised to a minimum mappable unit of 0.5 ha (MMU) and minimum feature width of 20 m (MFW).
  - Image segments integrated with cartography-derived parcels; agricultural boundaries added where useful.
- Data inputs:
  - Satellite imagery (composites mainly 91% of mapping; 9% single-date) from Landsat, SPOT, LISS-3, AWIFS; cloud and atmospheric corrections applied; terrain corrections using NEXTMap DEM.
  - Ground reference data for training/validation; cross-method comparison datasets.
- Processing chain:
  - Pre-processing, segmentation, parcel-based supervised classification (maximum likelihood), and post-class knowledge-based enhancements (KBEs).

## Data products and accessibility
- Vector product
  - UK-wide 23 land cover classes mapped to 17 Broad Habitats.
  - Parcel-level attributes include area, source images, Broad Habitat, processing lineage, ProbList (top five spectral-class probabilities), and KBE history.
- Raster products
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: class percentages and dominant class per 1 km pixel.
- Metadata and provenance
  - Detailed provenance for each parcel; KBEs and spectral probabilities are traceable.
- Access
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster data available on request (licensing may apply) via CEH data portal or spatialsdata@ceh.ac.uk.

## Quality assurance and validation
- Validation dataset: 9,127 ground reference polygons used.
- Overall accuracy: 83% (class-level accuracy varies; some classes high in producer’s quality but lower user accuracy in certain contexts).
- Validation framework includes separate testing data and class-specific as well as aggregate reliability indicators.
- Knowledge-based enhancements (KBEs) are documented with logs, enabling reversion or inspection of applied rules.

## Comparison with Countryside Survey (CS) 2007: Similarities and diffs
- Similar area estimates defined as within CS 95% confidence limits; similar examples include Broadleaved woodland, Acid Grassland, and Inland Rock.
- Dissimilar area estimates occur for Arable and Horticulture, Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
- Key reasons for differences
  - Differences in what CS vs LCM2007 classifies as Arable/Horticulture (including boundary/linear features in LCM2007).
  - Spectral confusion, especially for arable with phenology and multi-year imagery.
  - MMU and boundary feature treatment causing field-level discrepancies.
  - Grassland subtypes often mapped differently due to field vs spectral signatures; Broad Habitat Association rules extended cross-walk between classes.
  - Fen/Mash/Swamp differences largely due to mosaic land cover and small-scale patches, plus CS’s field-based data vs spectral-based mapping.
- Implications
  - LCM2007 provides independent, map-based area estimates and strengthens cross-validation with CS but differences should be considered when comparing to field survey data.

## Extent and area estimates of Broad Habitats
- UK-wide patterns show notable similarities for some habitats (e.g., Coniferous Woodland, Freshwater, Calcareous Grassland) within CS 95% limits.
- Other habitats show marked disparities (e.g., Fen, Marsh and Swamp) due to complex mosaics and scale effects.
- CS-based estimates offer field-derived context and uncertainty bounds; LCM2007 offers map-based estimates suitable for cross-validation and scenario analysis.
- Implications for users: select thematic level (BH, BHA, Aggregate) carefully when comparing datasets.

## Change mapping and temporal dynamics
- Change detection is complex due to:
  - Differing spatial structures across LCM1990, LCM2000, and LCM2007.
  - Boundary changes and spectral classification inconsistencies.
- No robust, stand-alone method yet to separate real change from methodological/spatial differences; aggregation or trajectory-based approaches may help.

## Key statistics and scale
- LCM2007 covers roughly 10 million land parcels (GB ~8.6 million; NI ~0.9 million).
- 23 land cover classes map to 17 Broad Habitats; minimum mapping unit 0.5 ha.
- Raster products at 25 m and 1 km resolutions; composite imagery accounts for the majority of mapping (about 91%).

## Applications and practical implications for data support
- Supports habitat monitoring, biodiversity policy, ecosystem services, landscape planning, and catchment management.
- Rich parcel-level metadata and KBEs enable users to:
  - Re-run analyses with alternative KBEs or threshold settings.
  - Reclassify certain KBEs to explore different thematic outcomes.
  - Use ProbList to assess classification plausibility and perform bespoke validation.
- Data access via CEH portals with licensing options; suitable for self-service use by researchers, policymakers, and practitioners.
- QA and CS cross-validation provide users with reliability context and help interpret differences.

## Practical considerations for data support (for the archetype)
- When enabling data use for others, emphasize:
  - The 0.5 ha MMU and MFW constraints that affect small features.
  - The knowledge-based enhancements affecting ~20% of parcels and the audit trail available for re-analysis.
  - The differences to expect when comparing LCM2007 outputs with Countryside Survey results, especially for grasslands and fen-like habitats.
  - The availability of unit-level metadata to verify class decisions against high-resolution imagery.

## Summary: Why this matters for data support
- LCM2007 provides a comprehensive, parcel-based UK land cover map aligned to Broad Habitats with rich provenance, enabling transparent data fusion, reuse, and method-driven reclassification.
- It offers coast-to-coast coverage at multiple spatial scales (vector, 25 m, 1 km) and supports policy-relevant analyses while highlighting areas of uncertainty and methodological differences with field surveys.
- The combination of KBEs, ProbList, and detailed metadata makes LCM2007 a strong backbone for evidence-based decision support, with clear pathways for validation and tailored reuse.