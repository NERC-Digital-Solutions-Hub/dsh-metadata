Final Report for LCM2007 - the new UK land cover map

## Overview
- LCM2007 is the UK’s continuous parcel-based land cover map produced for Countryside Survey 2007, with supporting 25m raster and 1km aggregated data.
- Provides cross-UK coverage of Broad Habitats, with a pathway to policy-relevant analyses and habitat monitoring.
- Data are grounded in national cartography (Ordnance Survey MasterMap and LPS Large-Scale Vector), multi-temporal satellite imagery, ground reference data, and knowledge-based enhancements to improve thematic accuracy.

## Data sources and spatial framework
- Data sources:
  - Satellite imagery (e.g., Landsat, SPOT, LISS-3) and ancillary data (national cartography, boundaries, soils, DEMs, urban datasets).
  - Ground reference points and Countryside Survey validation data.
- Spatial framework and MMU:
  - Minimum mappable unit of 0.5 ha; 20 m minimum feature width; parcels created by integrating cartography with image segments.
  - 25 m raster product (23 LCM2007 classes) and 1 km raster products (two summaries per location).
  - Vector products include polygon-level metadata and processing history; segmentation aligns with OSMM and agricultural boundaries to improve parcel coherence.
- Data organization:
  - Parcel-based classification into 23 LCM2007 classes aligned to Broad Habitats, plus 10 aggregated classes for 1km rasters.

## Data products and access
- Outputs:
  - Vector product: parcels with attributes such as area, Broad Habitat, processing history, KBE history.
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two formats per location (percentage cover per class; dominant class).
- Access and licensing:
  - 1 km raster data available via the CEH Information Gateway.
  - Full vector and 25 m raster data available on request under licence; fees may apply.
  - Detailed provenance and metadata support traceability and re-analysis.

## Methodology, knowledge-based enhancements, and validation
- Classification and enhancements:
  - Parcel-based supervised classification (maximum likelihood) across multi-date composites, mapped to 23 LCM2007 classes.
  - Knowledge-Based Enhancements (KBEs): seven automated rule-based enhancements to improve thematic resolution and resolve spectral ambiguities; some KBEs are reversible for access to original classifications.
- Validation framework:
  - Ground-reference polygons underpin accuracy assessment; appendix discusses bespoke validation approaches and the potential for an informal Bayesian-style validation using parcel-level metadata (KBE history and probability lists).
  - KBEs and metadata enable end users to assess and refine classifications for their location and purpose.

## Key findings: similarities, differences, and interpretation
- Similar area estimates (UK-wide CS 95% confidence limits):
  - Similar for Broadleaved woodland, Acid Grassland, Inland Rock.
- Dissimilar area estimates (UK-wide CS 95% confidence limits):
  - Dissimilar for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats.
- Main drivers of differences (detailed in the report):
  - Definitions and scope differences in how Arable/Horticulture and other grassland classes are mapped; spectral variability and temporal mismatch across multi-year image ranges.
  - Inclusion of Boundary and Linear Features in LCM2007’s Arable and Horticulture category, inflating its area relative to Countryside Survey maps.
  - Grassland classification disagreements (Improved vs Neutral Grassland) due to species composition and soil data limitations.
  - Dwarf Shrub Heath vs Acid Grassland and Montane habitats reflect upland mosaic and altitude-based reclassification in LCM2007.
  - Fen, Marsh and Swamp: large mosaic nature and small patch sizes cause substantial differences; CS often records fen as Rough Grassland or Acid Grassland in LCM2007 mappings; small CS parcels below the MMU affect comparisons.
- UK land cover composition (summary):
  - Across the UK, over 50% of land is intensive agriculture or built-up; woodlands ~12%; semi-natural areas prominent in Scotland (mountain/peatland) with regional variation.
  - Comparisons with LCM2000 show shifts in Arable and Semi-natural Grassland proportions and conifer woodland changes.
- Change detection and interpretation:
  - Real change detection is confounded by mismatched spatial/thematic structures across LCM iterations; robust change analysis requires aggregated or trajectory-based approaches.

## Validation, accuracy, and cross-dataset comparisons
- CS 2007 vs LCM2007 comparisons reveal varying levels of agreement by habitat type; Grassland remains the most challenging category due to the one-to-many mapping between observed land cover and Broad Habitats.
- For 1 km CS squares, LCM2007 shows high correspondence with the CS 2007 Arable and Horticulture extent, but broader BH extents are over- or under-estimated in places due to classification and boundary mapping differences.
- Fen/Marsh/Swamp shows the greatest discrepancy in UK-wide estimates, driven by mosaic complexity and small patch sizes.
- The report discusses that re-organising prior CEH maps into a common spatial framework based on real-world land-use units would aid future change detection and comparability.

## Governance, provenance, and contextual insights
- The LCM2007 dataset includes detailed polygon-level provenance and KBE histories, enabling users to audit the basis of each classification and to apply validation tailored to their location.
- The documentation emphasizes fit-for-purpose validation, acknowledging that no single accuracy figure fully captures suitability across all potential uses.
- The KBEs and metadata provide a framework to interpret and perhaps reclassify parcels with higher confidence for user-specific analyses.

## European links and context
- LCM2007 contributes to European-level assessments (e.g., Corine Land Cover) by providing vector-derived translation of Broad Habitats; data underpin pan-European land cover initiatives and cross-border analyses.
- The project aligns with European datasets (e.g., IMAGE2006), and provides a robust UK-centric framework to support national and European environmental monitoring.

## Challenges and limitations
- Persistent spectral confusion for several habitat types (e.g., various grasslands, fen-related mosaics) despite KBEs and soil data integration.
- Differences in field survey granularity (CS) versus parcel-level outputs (LCM2007) complicate direct comparisons; many CS features lie below the MMU or are too fine-scale to map.
- NI/Scotland pose specific spatial-framework integration and data-availability challenges.
- Change detection remains sensitive to differences in spatial structure, local mosaics, and temporal image ranges.

## Next steps and recommendations
- Ongoing refinement to improve discrimination of grassland types and to enhance change-detection capabilities.
- Expanded validation to support national estimates of Broad Habitats and to better quantify uncertainties in contentious classes.
- Use of the parcel-level KBEs and probability metadata to create location-specific, user-driven accuracy assessments and potential reclassification where appropriate.
- Encouragement for users to consult the CEH gateway for data access and to review accompanying metadata and KBEs for bespoke analyses.

## Endnotes and context
- LCM2007 is presented as the first UK-wide, high-resolution, parcel-based land cover map with strong provenance and governance-ready metadata, designed to support policy, planning, and environmental monitoring.
- The report situates LCM2007 within a broader landscape of land cover mapping, ground surveys (Countryside Survey), and European data initiatives, highlighting the value of integrating multiple information sources to inform evidence-based policy.