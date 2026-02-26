# Spatial masks for calcareous, coastal, upland and lowland heath habitats [Key Habitats 1992-93] (2017)

## Overview
- National-scale GIS-derived masks defining areas likely to contain four key habitats in England: calcareous grassland, coastal habitats, upland landscapes, and lowland heath.
- Based on a multi-source, stratified-sampling approach commissioned in the early 1990s to support assessment of habitats perceived as under threat.
- Data underpin population definitions for subsequent ecological field surveys (1992–1993) and are linked to Countryside Survey activities.

## Geographic and temporal scope
- Geography: England (with some methods referencing broader GB data; borders defined with Bartholomew 1:250,000 map).
- Time period of data collection: 1992–1993; Mask validation and documentation published in 2017.
- Related data: Countryside Survey data from 1990 used to supplement reporting for lowland areas.

## Habitat masks and their definitions
- Calcareous mask
  - Based on 1 km squares containing existing or potential calcareous grassland.
  - Derived by GIS using geology and drift deposits; includes areas with potential for future restoration or creation.
  - Final coverage: 26,555 1 km squares in England.
  - Distinguishes limestone types (e.g., oolitic, chalk, massive limestone) and coastal variants within the dataset.
- Coastal mask
  - Defined as land within 500 m inland from the high water mark plus contiguous coastal features (saltmarsh, dunes, coastal bare land).
  - Inland coastline delineated using Land Cover Map 1990 and Landsat-based classification; coast validated against HWM data where available.
  - Final coverage: 7,341 usable 1 km squares (out of 8,870 initially identified) after removing highly urban and purely maritime squares.
- Lowland heath mask
  - Built from soils and altitude data to identify 1 km squares with potential for heathland at landscape scale (not focused on small patches).
  - Utilizes Soil Survey and Land Research Centre soil typology; includes peat soils and mixes of dominant/sub-dominant soils to reflect regional variation.
  - Excludes areas unlikely to contain lowland heath based on ITE Land Classification 1990 classes; acknowledges coastal heathlands are reported separately due to classification challenges.
  - Final coverage: 8,538 1 km squares in lowland England.
- Upland mask
  - Derived from ITE Land Classification 1990, grouping 1 km squares into predominantly upland vs. lowland classes.
  - Excludes urban squares (>75% built-up) and those not occurring in England; final coverage: 15,616 km squares.
  - Notes regional variation in what constitutes “upland” across England.

## Dataset structure and content
- Format: Vector dataset comprising 1 km square polygons.
- Each square includes indicators for the applicable masks; calcareous mask further differentiates limestone and coastal types.
- Key columns:
  - DOMGEOL, Type/Description: Calcareous mask details (e.g., limestone types).
  - COAST, Type/Description: Coastal mask presence.
  - CALC, Type/Description: Calcareous mask presence.
  - LOHEATH, Type/Description: Lowland heath mask presence.
  - UPHEATH, Type/Description: Upland mask presence.
  - STRATA, Description: Coastal mask strata (H = hard coast, S = soft coast, E = estuarine).

## Methodology and survey design
- Survey framework
  - Stratified sampling across the entire study area; survey points were randomly selected from within the defined masks.
  - Field surveys conducted in 1992–1993 to characterize ecological attributes of the landscape and key habitats.
- Mask derivation steps
  - Calcareous mask: combines geology and drift deposits, excludes >75% urban areas, expands to escarpments, includes potential future restoration areas.
  - Coastal mask: uses Landsat-derived land cover, refines coastline with inland coastal buffer, and validates against HWM where possible.
  - Lowland heath mask: uses soil typology to identify potential heath areas, with regional adjustments to differentiate upland vs. lowland vegetation.
  - Upland mask: relies on ITE Land Classification 1990 to separate upland from lowland squares, excluding predominantly urban squares.

## Validation and quality
- Masks were validated through comparisons with other information sources.
- Overall fit judged to be acceptable for the purposes of the Key Habitat project, though some mismatches with other datasets were noted.

## Data provenance and access
- Primary publication documenting habitat data: Barr et al. (2017) Habitat and vegetation data from an ecological survey of terrestrial key habitats in England, 1992-1993. NERC Environmental Information Data Centre. DOI: 10.5285/7aefe6aa-0760-4b6d-9473-fad8b960abd4.
- Foundational methodology and mask construction described in earlier reports and field handbooks (Barr et al. 1993; Barr 1997; Bunce & Barr series; Bunce et al. 1990).
- Data management responsibilities: Institute of Terrestrial Ecology/Centre for Ecology & Hydrology; GIS analysis, data management, and metadata handling documented in associated publications.

## Practical notes for analysts
- Designed to support identifying population areas for 1 km sampling sites and to guide habitat assessments across England.
- Acknowledge potential data gaps or mis-matches when integrating with other habitat datasets; consider regional context when applying upland vs. lowland distinctions.
- Useful as a historical baseline for calcareous, coastal, upland, and lowland heath habitat distribution and for planning targeted ecological surveys.