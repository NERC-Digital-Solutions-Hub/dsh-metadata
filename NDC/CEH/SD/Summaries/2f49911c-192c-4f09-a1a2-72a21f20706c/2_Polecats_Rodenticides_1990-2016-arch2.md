# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Dataset supplement to the 2018 Environmental Pollution paper on long-term increases in secondary exposure to anticoagulant rodenticides in British polecats.
- Documents chemical analyses data from polecat liver tissues collected across Great Britain from 1990 to 2016.
- Aimed at standardised, inspectable environmental health indicators suitable for monitoring trends and policy performance.

## Data content and structure
- Core identifiers and metadata
  - record: unique animal identifier (issued by Vincent Wildlife Trust)
  - data: origin of chemical analyses data (NEW = Sainsbury et al. 2016; OLD = Shore et al. 2003)
  - year: carcass collection year (1990–2016)
  - time: years since first animal collection
  - survey: which rodenticide analysis survey (ONE: 1990–1995; TWO: 1995–1998; THREE: 2013–2016)
  - season: season of carcass collection (Spring, Summer, Fall, Winter)
  - halfYear: halves of the year (FIRST Dec–May; SECOND Jun–Nov)
- Spatial and geographical data
  - x, y: OSGB36 coordinates (metres)
  - region: North, South, East, West
  - expansio n: inside or outside the 1990s range (IN/OUT)
  - landClass: dominant land cover at carcass location (derived from CEH Land Cover Map 2007; majority class within 1 km buffer, focusing on arable vs pastoral)
- Biological metadata
  - sex: male or female (where known)
- Analytical results (concentrations and detections)
  - hBrom, hDifm, hBrod: concentrations of bromadiolone, difenacoum, brodifacoum in liver (µg/g); LOD applied from Shore et al. 2003 to 2018 dataset
  - hBBrom, hBDifm, hBBrod: detection status for each compound (0 = none detected; 1 = detected)
  - hBRods: number of rodenticides detected (0 = none; 1 = one or more)
  - hCRods: number of rodenticide compounds detected (0–3; 0 = none)
  - hConcT: total concentration of rodenticide compounds detected (µg/g; LOD applied)
- Notes
  - NA indicates missing data
  - 1–3 coding aligns with counts of detected compounds
  - Data processing and mapping steps described (see below)

## Provenance and data sources
- Primary literature:
  - Shore RF et al. 2003: spatial and temporal analysis of second-generation anticoagulant residues in polecats (1992–1999)
  - Sainsbury KA et al. 2018: long-term increase in secondary exposure in Great Britain
- Data origin and curation
  - Records compiled from analyses of polecat liver tissues; stored with a unique record identifier by Vincent Wildlife Trust
  - 1990s baseline data and later 2013–2016 data incorporated into a unified dataset (NEW vs OLD data sources noted)

## Spatial and temporal scope
- Temporal: carcass collection and analysis spanning 1990–2016
- Spatial: Great Britain (regional breakdown into North, South, East, West; coordinates in OSGB36; land-cover context via CEH map)
- Location processing: point coordinates overlaid on land-cover map; 1 km buffers used to assign dominant land class (arable vs pastoral)

## Data processing and standardisation
- Land cover classification
  - Overlay of carcass locations on CEH Land Cover Map 2007
  - 1 km buffers applied around each coordinate
  - Majority land class determined (arable vs pastoral)
- Measurement handling
  - Concentrations in µg/g
  - LODs from Shore et al. 2003 applied to Sainsbury et al. 2018 dataset
- Data integrity and QA
  - Standardised fields and coding to enable cross-study comparisons
  - Clear notes on data origin (NEW vs OLD) and survey periods
- Output format
  - Data prepared as a dataset supplement to the 2018 Environmental Pollution paper
  - Designed for inclusion in standard environmental health monitoring workflows

## Outputs and usage for monitoring
- Enables time-series assessments of secondary anticoagulant exposure in polecats
- Supports spatial analyses of exposure in relation to land use and region
- Facilitates standard reporting formats (maps, charts) for environmental health monitoring
- Can be stored in appropriate data portals and linked to other rodenticide exposure datasets

## Data access, reuse, and barriers
- Data are designed to be shareable and reusable to enable others to access underlying data used for outputs
- Emphasis on transparent provenance, standardized fields, and linkage to primary publications
- Encourages combining with other environmental datasets to enhance value beyond single-use analyses

## References
- Shore RF, Birks JDS, Afsar A, Wienburg CL, Kitchener AC (2003). Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats (Mustela putorius) from throughout their range in Britain, 1992-1999. Environmental Pollution, 122, 183-193.
- Sainsbury KA, Shore RF, Schofield H, Croose E, Pereira MG, Sleep D, Kitchener AC, Hantke G, McDonald RA (2018). Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain. Environmental Pollution, 236, 689-698.