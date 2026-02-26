# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Dataset supplement to the 2018 Environmental Pollution paper on long-term increase in exposure.
- Provides column explanations and data structure for polecat liver analyses across Great Britain from 1990–2016.
- Designed to support GIS-based analysis and map visualisations of spatial and temporal trends in rodenticide exposure.

## Data content and variables
- Core identifiers and provenance:
  - record: unique animal identifier (Vincent Wildlife Trust).
  - data: origin of chemical analyses (NEW = Sainsbury et al. 2016; OLD = Shore et al. 2003).
  - year: carcass collection year (1990–2016).
  - time: years since first collection.
  - survey: analysis survey (ONE = 1990–1995; TWO = 1995–1998; THREE = 2013–2016).
  - season: season of collection (Spring, Summer, Fall, Winter).
  - halfYear: period within year (FIRST = Dec–May; SECOND = Jun–Nov).
  - x, y: OSGB36 coordinates (metres).
  - region: North, South, East, West.
  - expansio n (expansion): inside or outside 1990s range (IN/OUT).
  - sex: Male/Female (when known).
- GIS and location processing:
  - landClas s: predominant land cover at carcass location (derived from overlay with CEH Land Cover 2007; 1 km buffers used; majority land class between arable and pastoral).
  - hBrom, hDifm, hBrod: concentrations of bromadiolone, difenacoum, brodifacoum (µg/g); LODs from Shore et al. 2003 applied to Sainsbury et al. 2018 dataset.
  - hBBrom, hBDifm, hBBrod: detection status (0 = none detected; 1 = detected; LOD-based).
  - hBRods: number of rodenticides detected (0 or more).
  - hCRods: number of rodenticide compounds detected (0–3).
  - hConcT: total concentration of rodenticide compounds (µg/g) for 2018 dataset.
- Data quality notes:
  - NA indicates missing data.
  - LAND cover and processing details include use of Quantum GIS 2.12.3 and CEH Land Cover map 2007.

## Spatial and temporal scope
- Spatial: Great Britain; coordinates in OSGB36; land-cover context via 1 km buffers and CEH Land Cover 2007.
- Temporal: carcass collections from 1990 to 2016; three survey periods spanning 1990–1995, 1995–1998, and 2013–2016.

## GIS methods and data processing
- Location data overlaid onto CEH Land Cover 2007; 1 km buffers created around carcass points.
- Majority land class determined for each point (between arable and pastoral).
- Land class classified using Quantum GIS (version 2.12.3).
- LOD values and detection indicators applied from Shore et al. 2003 to the Sainsbury et al. 2018 dataset.

## Data provenance and references
- Primary sources:
  - Shore RF et al. 2003. Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats in Britain.
  - Sainsbury KA et al. 2018. Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain.
- This dataset serves as a supplement to the 2018 Environmental Pollution paper and provides detailed column explanations and GIS-ready attributes.

## Practical use for GIS Specialists
- Create map visualisations of exposure patterns across regions, seasons, and time periods.
- Combine with land-cover and regional data to identify spatial trends and potential hotspots.
- Use as a data source for temporal trend analyses and spatial risk mapping of rodenticide residues.
- Leverage OSGB36 coordinates and standardized LOD/detection fields for consistent GIS analyses across datasets.

## Limitations and considerations
- Data originate from multiple sources with evolving data standards (NEW vs OLD), requiring careful harmonisation.
- Missing data (NA) present in several fields; careful handling needed for analyses.
- Complex, multi-source dataset with varying resolutions and scopes; appropriate data cleaning and quality checks are essential.

## References
- Shore RF, Birks JDS, Afsar A, et al. (2003). Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats from Britain, 1992–1999. Environmental Pollution, 122, 183-193.
- Sainsbury KA, Shore RF, Schofield H, et al. (2018). Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain. Environmental Pollution, 236, 689-698.