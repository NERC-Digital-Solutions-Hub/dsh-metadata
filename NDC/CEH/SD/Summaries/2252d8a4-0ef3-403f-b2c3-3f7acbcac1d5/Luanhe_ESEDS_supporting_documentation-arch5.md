# disservices (EDS) in the Luanhe River Basin, China

## Overview
- Geodatabase describing ecosystem types and their ecosystem services (ES) and disservices (EDS) in the Luanhe River Basin (LRB).
- Includes study area details, generation methods, units and structure of recorded values, quality control, and data structure.
- Funded under UKRI/NERC TaSE program; dataset underpinning the project on river basins as living laboratories.

## Study Area
- Location: Luanhe River Basin across parts of Hebei, Liaoning, and Inner Mongolia (39°10'–42°30' N, 115°30'–119°15' E).
- Environment: semiarid North China; ~45,775 km²; population ~5.4 million; important ecological barrier and water resource for the Beijing–Tianjin–Hebei region.
- Land use context: dominant pasture in the northeast, major reservoirs mid-reach, cropland around urban areas; relevant for multiple ES and EDS.

## Generation Methods
- Land uses (ecosystem types, ET) derived from China's National Land Use and Cover Change (CNLUCC) dataset at 30 m resolution.
- Six major ETs identified, subdivided into 14 ET subcategories; mapping aligned with Millennium Ecosystem Assessment (MA) and CICES v5.1.
- ES and EDS coverage: 11 provisioning services (PS), 10 regulating services (RS), 5 cultural services (CS), 7 ecological integrity indicators (EI), and 11 EDS added to the matrix.
- Capacity matrix populated by expert panels (total of 25 experts across two rounds; 2019 in-person workshop; 2020 online due to Covid-19).
- Scoring: ES/EDS capacity per ET on a 0–5 scale; confidence per score on a 1–3 scale. Quorum rules applied (at least 10 experts).

## Data Structure and Content
- Data converted from raster to vector for easier calculation and sharing.
- Format: ArcGIS shapefile (readable by most GIS apps) with accompanying .dbf table.
- Core attributes:
  - FID: unique feature ID
  - Shape: polygon geometry
  - ES_Type: ecosystem types (14 ET categories, e.g., cropland, forest, grassland, waterbody, built-up, unused land, etc.)
  - PS: Provisioning services (example categories include crops, livestock, fodder, capture fisheries, aquaculture, wild foods, timber, wood fuel, energy biomass, biochemicals and medicine, freshwater)
  - RS: Regulating services (examples include local and global climate regulation, flood protection, pest/disease regulation, drought regulation, fire regulation, erosion control, nutrient leaching)
  - CS: Cultural services (examples align with MA/CICES conceptualizations)
  - EI: Ecological integrity indicators (example categories)
  - EDS: Ecosystem disservices (example categories)
- Coverage: 14 ETs; 11 PS; 10 RS; 5 CS; 7 EI; 11 EDS. Names reflect the dataset’s domain-specific nomenclature (e.g., Local_clim, Global_cli, Flood_prot, Droughts, Erosion_an, Human_dise, Allergens, Heat_islan).

## Quality Control and Confidence
- Overall confidence: majority of ES/EDS scores rated as comfortable or moderately comfortable.
- 616 ES/EDS capacity scores; only 5 ES and 11 EDS had low confidence.
- Higher uncertainty associated with:
  - ES/EDS linked to Bare land, rock or gravel (unutilized lands) which are often overlooked in ES assessments.
  - Some disservices (e.g., human diseases from pathogens, allergens) and certain land-use types linked to industrial or sandy areas.
- Rationale for uncertainty: limited familiarity with certain EDS concepts; transition of some land types into ES/EDS contexts; data interpretation challenges for non-interoperable land-use categories.
- Overall reliability: confidence analysis suggests the expert-derived scores are reasonably reliable.

## Data Provenance, Access, and Maintenance
- Data provenance:
  - Base land-use inputs from CNLUCC (Liu et al. 2014; Xu et al. 2018).
  - ES/EDS framework anchored in MA (2005) and CICES v5.1 (Haines-Young & Potschin, 2018).
  - Expert-elicited capacity scores with explicit confidence indices (2019 and 2020 rounds).
- Access and use:
  - Delivered as ArcGIS shapefile with readable tabular data (.dbf) for use in Excel or GIS.
  - Designed to be compatible with common GIS workflows and data portals; metadata implied by data structure and documentation.
- Updates and versioning:
  - Score matrices completed in two periods (October 2019 and August 2020); two scoring rounds reflect iterative refinement and pandemic-related adjustments (in-person vs online).

## Data Stewardship Considerations and Limitations
- Governance and standards:
  - Clear provenance and methodological documentation; explicit scoring methodology and confidence metrics aid auditability.
  - Vectorization approach supports interoperability but relies on raster-to-vector conversion decisions.
- Metadata and discoverability:
  - Dataset structure and attribute naming are self-describing but explicit, machine-readable metadata would enhance discoverability in data catalogs.
- Sharing and sustainability:
  - Shapefile format supports broad sharing but consider providing alternative formats (e.g., GeoJSON, GeoPackage) for long-term accessibility.
  - Regular updates would require documenting versioning and changelogs as land-use inputs or ES/EDS definitions evolve.
- Limitations to note for reuse:
  - Some ES/EDS scores carry low confidence, particularly for less familiar or non-standard land-use categories.
  - The inclusion of unused land categories (bare land/rock/gravel) yielded lower ES scores, indicating potential gaps in local knowledge or data coverage.
  - Some EDS concepts were new to the study area, suggesting ongoing refinement may be needed for broader application.

## References
- Wu, Y., Zhang, X., Fu, Y., Hao, F., & Yin, G. (2020). Response of Vegetation to Changes in Temperature and Precipitation at a Semi-Arid Area of Northern China Based on Multi-Statistical Methods. Forests, 11(3): 340.
- Xu, X., Liu, J., Zhang, S., Li, R., Yan, C., & Wu, S. (2018). China's Multi-Period Land Use Land Cover Remote Sensing Monitoring Data Set (CNLUCC). Resource and Environment Data Cloud Platform: Beijing, China.