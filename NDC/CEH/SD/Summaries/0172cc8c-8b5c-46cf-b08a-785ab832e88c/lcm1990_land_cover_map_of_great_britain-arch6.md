# Land Cover Map of Great Britain

## Overview
- Digital land cover dataset produced from Landsat Thematic Mapper imagery (1990) at 25m resolution.
- Represents 25 land cover classes (plus Unclassified) and provides a comprehensive national map of land cover for Great Britain.
- First complete, satellite-derived digital national land cover map for Britain; used for planning, management, ecology, conservation, forestry, water, urban planning, transport, telecommunications, recreation, and mineral extraction.
- Available via licence; can be provided for specific areas and in 25m or 1km aggregated forms; multiple licensing options available.

## Data content and products
- 25m data: 25 target cover-types numbered 1–25; plus UNCLASSIFIED (0).
- 1km data: 17 key cover-types (A–Q) represented as proportion percentages within each 1km cell for summary datasets.
- Stand-alone datasets: geographic-area data orders at 25m resolution; 1km summary data as proportion bands per 1km cell.
- Data can be customised (e.g., deliver 25m data as 17 key types) if required.
- Applications illustrated include detection of changing land cover, landscape management, bracken mapping for health studies, motorway/environmental impact assessments, and telecom planning.

## Spatial resolution and accuracy
- Resolution: 25m grid; 0.125 ha minimum mapped size (with practical limits up to around 1–5 ha for reliable subdivision).
- Coverage: most features 1 ha or larger are clearly detectable; very small features may be omitted depending on spectral signature.
- Registration: Landsat-derived maps aligned to 1 km field-squares with average positional error around 20 m (0.8 pixels).
- Classifications created by supervised maximum likelihood using combined summer and winter imagery to improve accuracy; cloud coverage minimal (0.4% obscured on both dates); offshore islands largely unaffected (0.1% missing).
- Classification accuracy: overall correspondence with ground data around 67–71% when considering class definitions and time differences; after excluding boundary pixels, correspondence rises to about 71%; including boundary pixels, ~76% overall. Realistic, practical accuracy estimated at 80–85% when accounting for definitional and temporal differences.
- Key caveat: most map errors arise from mixed boundary pixels (pixels on boundaries between classes) and from differences in class definitions between surveys. Ground-truth data are rarely perfect; accuracy figures reflect cross-method comparisons and generalization effects.

## Classification scheme and usage
- Two levels of data:
  - 25 target classes (25m resolution): detailed classification with 25 labeled classes.
  1. Sea/Estuary to 25. Inland Water to 25. In coastal categories, extent is defined to first bridge/estuarine boundary or barrier.
  - 17 key classes (1km resolution): aggregated data suitable for higher-level analyses.
- A–Q correspond to key classes in 1km data; each 1km cell stores the proportion (as an integer percent) of that cell classified as the corresponding key class.
- A–Q class descriptions provide detailed definitions (e.g., A Sea/Estuary; B Inland Water; C Coastal Bare Ground; D Saltmarsh; E Rough Pasture/Dune Grass/Grass Moor; F Pasture/Meadow/Amenity Grass; G Marsh/Rough Grass; H Grass/Shrub Heath; I Shrub Heath; J Bracken; K Deciduous/Mixed Wood; L Coniferous/Evergreen Wood; M Bog (Herbaceous); N Tilled Land; O Suburban/Rural Development; P Urban Development; Q Inland Bare Ground; plus UNCLASSIFIED 0).
- Some 25-class items are aggregated in the 17-class summary (e.g., Open Shrub Heath and Open Shrub Moor are combined in certain contexts).
- Notes emphasize flexibility: users can tailor aggregation to their objectives within GIS, acknowledging potential inconsistencies across subtypes.

## Data access, licensing, and cost
- Availability: data can be ordered for specific geographic areas; licences must be signed by a responsible person (or supervisor for students).
- Licence types: from single-user research to corporate multi-user/multi-site licences; new licensing forms can be developed to ease access.
- Charges: three bands (commercial, non-commercial, and research); UK academics may receive additional reductions under NERC arrangements.
- Contact: CEH Wallingford data team for licensing and orders (phone and email provided).

## Practical use and caveats for data users
- Land cover is a reflection of dominant cover at imaging times; land use and cover can differ.
- Accuracy reflects map-model limitations, resolution, class definitions, and temporal changes; avoid treating accuracy as a single measure of error.
- Boundary and mixed-pixel issues can affect classification; consider excluding boundary areas for certain analyses to improve accuracy.
- Temporal changes between the two imaging dates can affect comparisons (e.g., pasture ploughed or re-seeded between seasons/years).
- The dataset is suitable for monitoring landscape change, environmental impact assessments, ecological planning, and integration into GIS for policy and planning support.

## Related datasets and updates
- Land Cover Map 2000 is available, with additional information on its creation and potential; sample 1km data and download access via Countryside 2000 resources.
- Data and licensing inquiries overall directed to Land Cover Map Sales, CEH Wallingford.

## Appendices and technical details
- Appendix 2 provides a colour mapping "recipe" for LCM1990, detailing RGB values for each of the 26 LCM subclass descriptions (0 = Unclassified; 1–25 = A–Q), useful for visualisation and map production.
- References to methodological sources and prior studies on accuracy assessment, classification approaches, and remote sensing applications are listed.