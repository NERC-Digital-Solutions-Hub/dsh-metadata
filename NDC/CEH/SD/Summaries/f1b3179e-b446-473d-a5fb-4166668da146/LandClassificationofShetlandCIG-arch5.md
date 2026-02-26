# Land Classification of Shetland (1974)

## Overview
- Stratification-based framework for sampling across Shetland, created for a 1974 terrestrial habitat survey using standardized methods (Bunce & Shaw, 1973).
- Aims to classify landforms and environmental characteristics into strata to support ecological assessment and subsequent studies.
- Stratification relied on maps and aerial photographs; 1 km grid cells used as the sampling unit; initial aerial data were not available, later used to refine vegetation maps and validate map-based predictions.
- Core output is a land-classification layer with 16 strata, intended to guide sampling and interpretation of terrestrial habitats.

## Content and scope
- Geographic coverage: Shetland Isles, Scotland.
- Time period: 1974 (background sampling and surveys conducted during that year).
- Data categories: 16 environmental strata representing areas with similar environmental characteristics; strata described in terms of coastal vs inland groupings and associated landscape features.
- Data format and projection: ESRI Shapefile; OSGB 1936 projection; resolution equivalent to 1 km grid squares.
- Dataset structure: features include OBJECTID, Shape, STRATA (values 1–16).
- Related datasets: Shetland Freshwater Survey 1974; Shetland Coastal Survey 1974; Shetland Vegetation Survey 1974; ITE Land Classification of Great Britain (2007).
- Key documents and publications: foundational methods papers (Bunce & Shaw 1973; Bunce 1974; Milner 1975), plus methodological and classification references (Hill 1973; Hill, Bunce & Shaw 1975; Metzger et al. 2005; Bunce et al. 1996/2007).

## Methodology and data lineage
- Stratification approach:
  - Initial stratification by landform using maps and aerial photographs; later integration of aerial data for detailed vegetation mapping and validation against map-derived predictions.
  - 1 km grid cells used as fixed sampling units across the 2046 land-containing squares in Shetland.
  - Two types of geographical attributes: continuous (e.g., altitude, slope) and presence/absence features (e.g., cliffs, hilltops).
- Attribute framework:
  - Table of 150 attributes used to produce stratification (geology, coast, hydrology, topography, etc.), including both physical attributes and landscape features.
  - Full attribute list and coding are described in the dataset documentation (Table 1 in the source).
- Data collection and analysis:
  - Nearly 1000 vegetation plots (200 m²) collected across the islands using standardized survey methods.
  - Stratified random sampling complemented by specialist surveys for bryophytes and lichens, and key habitat types (cliffs, salt-marshes, shingle banks).
  - Analysis employed indicator species methods (indicator species analysis) to delineate strata and relationships between geology and geography (Hill et al., 1973; 1975).

## Provenance and documentation
- Originator: R.G.H. Bunce, Institute of Terrestrial Ecology, Merlewood Research Station.
- Context: part of a broader project to assess status and value of Shetland’s plant and animal communities.
- Key publications and references:
  - Bunce, Shaw, and colleagues (various 1973–1996) on standardized ecological survey procedures and land classification frameworks.
  - Hill (1973) and Hill, Bunce & Shaw (1975) on reciprocal averaging and indicator-species analysis.
  - Metzger et al. (2005) and Bunce et al. (2007) related to wider climatic stratifications and land classification work.
- Strata overview (high-level grouping):
  - Strata 1–4: Coastal with minimal river influence; large land area; relatively gentle terrain.
  - Strata 5–8: Coastal with higher sea influence and steeper slopes; more headlands and sea cliffs; higher river inflow potential.
  - Strata 9–12: Inland, higher altitude with 600–900 ft hills; limited water bodies; major rock type often gneiss.
  - Strata 13–16: Inland, lower, more undulating with peat; hills around ~300 ft; rocks more often Old Red Sandstone.

## Practical considerations for Data Stewards
- Metadata and documentation needs:
  - Clear definition of each of the 16 strata, sampling unit (1 km grid), and the 150 attributes used for stratification.
  - Documentation of the map and aerial-photograph basis, data gaps (e.g., initial lack of aerial data), and methods for integrating later imagery.
  - Provenance trail linking to related Shetland surveys and ITE Great Britain land-classification work.
- Data quality, interoperability, and governance:
  - Ensure compatibility with modern coordinate reference systems if reprojecting (currently OSGB 1936).
  - Maintain linkage to original publications and method notes for reproducibility of the stratification and analysis approach (indicator species analysis).
  - Plan for long-term preservation of the shapefile and associated attribute definitions; guard against loss of the 150-attribute schema.
- Access and reuse:
  - Related datasets provide opportunities for integrated analyses across freshwater, coastal, and vegetation surveys; consider cross-dataset metadata mapping to support discoverability.
  - When sharing, include governance notes on methodological context, data lineage, and any embargo or usage constraints identified in the original documentation.