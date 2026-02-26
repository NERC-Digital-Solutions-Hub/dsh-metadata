# Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous UK land cover map at parcel level (land parcels as the spatial framework).
- Maps 23 land cover classes linked to 17 Broad Habitats; minimum mapping unit 0.5 ha; 25 m raster; provides 1 km summaries and a comprehensive vector product.
- UK-wide coverage (GB and NI); designed for change detection and policy-relevant environmental monitoring.
- Rigorous QA including field validation; knowledge-based enhancements (KBEs) improve thematic resolution and contextual classification; data hosted via CEH portals with licensing options.

## Data framework and sources
- Spatial framework built from national cartography (OS MasterMap and LPS Large Vector) with multiple generalisation stages to MMU 0.5 ha and MFW ~20 m.
- GB framework uses generalised OSMM/topography and agricultural boundaries; NI framework uses NI sector maps with agricultural boundaries largely omitted.
- Result: a reusable, parcel-based UK-wide framework suitable for change detection and integration with other datasets.

## Data processing and segmentation
- Pre-processing includes cloud/shadow masking, atmospheric and topographic correction, and image-to-geo-registration.
- Segmentation uses spectral bands (winter NIR, summer red, summer MIR) integrated with OSMM boundaries and agricultural data to improve homogeneity.
- 60 composites processed; manual hole filling where needed; segments linked to parcels for classification.

## Classification and knowledge-based enhancements (KBE)
- Parcel-based supervised maximum likelihood classification using multi-date composites and ground truth data.
- Iterative refinement with ground truth corrections; KBEs resolve spectral confusion using contextual data (urban context, proximity to water, terrain, soils).
- Approximately 20% of parcels undergo reclassification or refinement via KBEs; KBEs enable habitat-level differentiation (e.g., acid/calcareous/neutral grasslands) and support auditability by allowing reversibility to spectral classifications.

## UK coverage and products
- Outputs: UK-wide continuous vector of land parcels and a 25 m raster; 1 km summaries for quick analyses.
- Spatial resolution: imagery ~20–30 m; MMU 0.5 ha; MFW ~20 m.
- Main outputs: vector with 10 polygon-processing attributes, 25 m raster with 23 classes, and 1 km summaries; crosswalks to Broad Habitats and aggregation relationships provided.

## Validation and quality assurance
- Ground truth: 9127 points collected 2006–2008; overall accuracy ~83% across LCM2007 classes; class-level accuracy varies.
- Countryside Survey (CS) 2007 comparison: CS 1 km squares provide broad-habitat correspondence with LCM2007; overall CS vs LCM2007 alignment shows notable differences by habitat type.
- CS national estimates and 95% confidence limits used to assess UK-wide performance; differences highlighted for several habitats (e.g., Arable, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane, coastal habitats, Fen, Marsh and Swamp).
- Discrepancies attributed to: differences in class definitions, spectral confusion, boundary/linear feature mapping, multi-year imagery effects, and the MMU affecting CS vs LCM comparison.

## Dissimilar area estimates (4.3.2)
- Dissimilar areas identified where CS 95% confidence limits do not contain the UK LCM2007 area for certain classes:
  - Arable and Horticulture: CS upper vs LCM2007 higher; explanations include differing definitions, spectral variability, and inclusion of boundaries/linear features in LCM2007.
  - Improved Grassland and Neutral Grassland: differences likely due to how neutral vs improved grassland are spectrally represented and soil data limitations.
  - Dwarf Shrub Heath and Bog: allocation differences between habitats; Montane and coastal habitats poorly represented in CS contributing to discrepancies.
  - Fen, Marsh and Swamp: large variability due to mosaic nature and small patch sizes; some CS mapped areas may be recorded as Rough Grassland or Acid Grassland in LCM2007.
- Additional discussion notes temporal range of imagery and patch sizes relative to MMU influence habitat area estimates.

## UK Land Cover distribution (4.4)
- UK-wide distribution: just over half of land is intensive (Arable + Improved Grassland) or Built-up Areas and Gardens; about 12% woodland; roughly 30% semi-natural; remaining areas include coastal and montane habitats.
- Country-level contrasts:
  - England: highest intensive land use (~76%).
  - Scotland: largest share of Coniferous Woodland and the most extensive semi-natural grassland and montane habitats.
  - Northern Ireland and Wales: intermediate intensive land use with notable grassland and woodland components.
- Comparison with LCM2000 shows shifts in Arable and Semi-natural Grassland proportions and slight changes in woodland and urban area extents; spatial framework changes contribute to some of these differences.

## Access, usage and applications (4.5)
- Access: 1 km raster data via CEH Information Gateway; full vector and 25 m raster data on request; licensing may apply.
- Primary applications: habitat monitoring, biodiversity assessments, ecosystem services, landscape planning, habitat connectivity, catchment management; designed to integrate with other environmental datasets for policy evaluation.
- KBEs and parcel-level metadata enable tailored analyses, reclassification exercises, and audit/validation efforts.

## Key figures and outputs
- 10 million land parcels UK-wide (GB ~8.6 million; NI ~0.9 million).
- 23 land cover classes mapped to 17 Broad Habitats; 0.5 ha MMU; 25 m raster; 1 km summaries available.
- Outputs include vector with 10 processing attributes, 25 m raster, and 1 km summary layers; crosswalks to Broad Habitats and aggregation relationships provided.

## Core takeaways for Environment Analysts
- LCM2007 provides a standardized, UK-wide, parcel-based land cover dataset aligned to Broad Habitats, enabling consistent, time-series monitoring.
- The generalised spatial framework (OSMM/LPS) improves spatial accuracy and change-detection capabilities; KBEs are crucial for resolving spectral confusion and extracting higher-level habitat information, with reversibility for auditability.
- Validation shows robust overall accuracy but underscores uncertainties in upland and grassland classes; users should consider both producer’s and user’s accuracies and leverage Broad Habitat Associations for robust interpretation.
- Comparison with Countryside Survey highlights where spectral-based products and field surveys diverge; suggests potential for integrating KBEs to better represent certain habitats (e.g., Fen, Marsh and Swamp).
- For policy-relevant use, combine LCM2007 with ground-truth data (CS-like), other environmental layers, and be mindful of scale and spatial-structure differences when performing change detection or landscape-level analyses.

## Example areas and data formats
- Example areas illustrate performance across uplands, calcareous grasslands, urban zones, arable and fenlands.
- Data formats: vector land parcels with rich metadata; 25 m raster; 1 km summaries; KBEs recorded for traceability; ProbList and KBE history available for audit.

## Data access and datasets
- 1 km raster data via CEH Information Gateway.
- Full vector and 25 m raster data available under license on request from CEH.
- The dataset supports cross-country comparisons, policy evaluation (biodiversity targets, Natura, habitat connectivity), and integration with meteorological, hydrological, and ecological models.