# Final Report for LCM2007 - the new UK land cover map

- An evidence-base for environmental monitoring and policy evaluation across the UK, delivering the first continuous parcel-based land cover map (LCM2007) aligned with Biodiversity Action Plan Broad Habitats.
- Provides a suite of products (vector parcels, 25 m raster, and 1 km data products) covering Great Britain and Northern Ireland, designed to support habitat monitoring, biodiversity policy, landscape planning, ecosystem services assessment, and catchment management.
- Emphasises transparency, provenance, and open data access to inform monitoring frameworks and policy decisions.

## What LCM2007 is and what it provides

- LCM2007 classifies land cover (not land use) using a 23-class system, mapped across the UK with a 0.5 ha minimum mappable unit (MMU) and 20 m raster resolution for the main products.
- Product range:
  - Vector: land parcels with 10 processing attributes, including provenance, KBE history, and a ProbList of top spectral class candidates.
  - Raster: 25 m resolution with 23 LCM2007 classes.
  - 1 km data: percentage cover and dominant class for each 1 km grid, for both 23 classes and 10 Broad Habitat aggregates.
- Data access:
  - 1 km rasters via the CEH Information Gateway.
  - Full vector and 25 m rasters available on request under licence from CEH (fees may apply).

## Data sources and spatial framework

- Satellite imagery: Landsat TM5, IRS LISS3, SPOT-4/5; backup data from AWIFS; two-date summer-winter composites used to maximise class separability; 91% mapped from composites in 2007.
- Ancillary data: Ordnance Survey MasterMap (Great Britain), NI LPS, agricultural boundaries, NEXTMap DEM, soils, urban boundaries, coastline context, and additional national layers.
- Ground reference and validation: CEH ground reference points (2006–2008) plus Countryside Survey (CS) Broad Habitats (2007) for comparison.
- Spatial frameworks:
  - Great Britain: generalised OS MasterMap cartography refined with agricultural boundaries and image segments to produce UK-wide continuous coverage.
  - Northern Ireland: LPS Large-scale Vector data generalised and integrated with image segments; agricultural boundaries not added for marginal gains.

## Processing, segmentation, classification, and knowledge-based enhancements

- Pre-processing: cloud/cloud-shadow masking, atmospheric correction (FLAASH), geo-registration (target RMSE < 0.3 px), and topographic correction using NEXTMap DEM.
- Segmentation: three-band segmentation using winter NIR, summer red, and summer MIR, integrated with cartography and agricultural boundaries; applied to 60 composites.
- Classification: parcel-based supervised maximum likelihood classification using 37 composite and 21 single-date images; iterative ground-truth training; 23 LCM2007 classes mapped.
- Knowledge-based enhancements (KBE): seven rules addressing spectral confusion (e.g., arable vs urban/grassland), using terrain, soils, coastal proximity, urban context, etc.; approximately 20% of parcels reclassified via KBEs; KBEs can be reversed to the original spectral class if needed.
- Post-processing: hole-filling and manual edits; Landsat-7 ETM+ used to fill problematic holes in some scenes.
- ProbList and transparency: ProbList shows the five closest spectral variants to each parcel’s signature; CorePixels used for training statistics; KBE history recorded in the vector attributes to enable traceability and validation.

## Validation, accuracy, and comparisons

- Validation dataset: 9,127 CEH ground reference points; overall accuracy around 83%, with class-level variation.
  - Notable examples: Bog (Producer ~93%), Improved Grassland (User ~83%), other woodland, arable, and water classes showing varying performance; semi-natural grassland types (Neutral, Calcareous, Montane) often more challenging due to spectral ambiguity and KBE limitations.
- Countryside Survey (CS) comparison:
  - Broad Habitat agreement varies by class; grassland categories show notable discrepancies due to one-to-many relationships between field observations and remote sensing classifications.
  - Arable and Horticulture: LCM2007 matches CS 1 km square proportions well, but CS UK-wide estimates are lower for Arable/Horticulture than LCM2007, partly due to differences in class definitions, spectral confusion, and inclusion of boundary/linear features in LCM2007.
  - Fen, Marsh and Swamp: large discrepancies; CS often records mosaic patches that LCM2007 maps as Rough Grassland or Acid Grassland; CS patch size distributions below LCM/MMU influence observed comparisons.
- UK-wide and country-level patterns:
  - UK-wide: more than 50% of land is intensive (Arable and Horticulture + Improved Grassland) or Built-up Areas and Gardens; woodlands ~12% (broadleaved and coniferous); remaining is semi-natural with varying regional distributions.
  - England/northern Ireland/wales/scotland differences reflect climate, management, and habitat composition (e.g., Scotland with more coniferous woodland and mountainous habitats).
- 4.5 Summary and discussion:
  - Agreement between LCM2007 and CS varies by Broad Habitat; grassland is particularly problematic due to classification mapping and mosaic complexities.
  - LCM2007 provides coast-to-coast UK coverage with a robust thematic framework, enabling change detection and policy-relevant analyses, albeit with class-level uncertainties in specific habitats.

## Data access, governance, and provenance

- Vector data includes full provenance (Construct, ProbList, KBE, etc.) and field notes, enabling traceability and auditability for monitoring workflows.
- The 25 m raster and vector products carry detailed metadata; the 1 km rasters provide scalable outputs for national-scale monitoring and integration with other datasets.
- Data governance considerations:
  - Some datasets require licensing for full access; KBEs and ProbList offer transparency but require user validation for sub-class use.
  - Metadata gaps and data accessibility barriers noted; users should plan data governance and data-management at the source, and consider aggregating classes to mitigate uncertainties.

## Relevance to monitoring frameworks and policy evaluation

- Strengths for policy and monitoring decision-makers:
  - Provides a rigorous, policy-relevant UK-wide baseline aligned with Broad Habitats and BAPs.
  - Multi-resolution products (1 km to 25 m) enable scalable analyses across policy scopes and integration with other datasets (e.g., biodiversity, ecosystem services, climate, hydrology).
  - Ground-truth validated accuracy metrics and cross-validation with CS support interpretation of habitat extents and trends.
  - Clear provenance and a reproducible workflow facilitate monitoring program continuity and inter-country comparisons.
  - Open access to core outputs (via CEH gateway) supports policy analysis, habitat connectivity studies, and landscape planning.
- Practical considerations for monitoring design:
  - Be mindful of habitat-specific uncertainties, especially for grasslands and upland semi-natural habitats; consider aggregating grassland classes where appropriate to improve comparability with field data.
  Continuous spatial structure and reuse-friendly boundaries enable efficient future monitoring and change detection; however, change mapping across time requires careful methodological alignment due to evolving spatial frameworks and class definitions.

## Strengths and limitations for monitoring and policy use

- Strengths:
  - First continuous UK-wide parcel-based map aligned with Broad Habitats and Biodiversity Action Plan needs.
  - 20 m spectral resolution with a 0.5 ha MMU provides stable, consistent spatial units suitable for change detection and long-term monitoring.
  - KBEs enhance thematic resolution and help correct challenging classifications; open data access supports policy analytics.
  - Transparent provenance enables traceable analyses and reproducible monitoring workflows.
- Limitations:
  - Spectral confusion remains for several grassland and semi-natural habitats; certain upland and fen/marsh classes remain difficult to separate spectrally.
  - Coastal/inland water separation and some coastal class consistency issues; patch sizes of certain habitats can be smaller than the MMU, affecting mapping quality.
  - Change mapping across successive LCMs is complex due to differences in spatial structure and class definitions; requires careful methodological alignment or reprocessing to ensure comparability.
  - Metadata completeness and data-access barriers may hinder some users; governance and data-management strategies are essential.

## Key takeaways for monitoring framework decision-makers

- LCM2007 offers a policy-relevant, UK-wide land cover baseline with explicit links to Broad Habitats and Biodiversity Action Plans, enabling routine monitoring of habitat extent, landscape change, and ecosystem-service considerations.
- The integrated workflow (satellite imagery, national cartography, ground truth, and KBEs) provides a reproducible, provenance-rich framework suitable for long-term monitoring and cross-sector analyses.
- For policy planning and evaluation:
  - Use the 1 km and 25 m products for multi-scale analyses and integration with other policy datasets.
  - Leverage the vector provenance and ProbList to assess confidence in habitat classifications at locations of interest.
  - Consider aggregating grassland classes or using Broad Habitat associations to improve correspondence with field data and CS benchmarks.
- Be aware of habitat-level uncertainties, especially for grassland and upland habitats, and plan validation steps accordingly to ensure robust monitoring outcomes.