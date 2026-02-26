# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

- Overview
  - Data supplement to the 2018 Environmental Pollution paper on long-term increase in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain.
  - Provides column heading explanations for PolecatRodenticidesFINAL1990-2016 (EIDC.csv), detailing data structure used across multiple survey periods and years.
  - Supports monitoring and evaluation of environmental health risks and policy relevance by enabling traceable analysis of rodenticide exposure in wildlife.

- Data structure and key variables
  - record: unique animal identifier issued by Vincent Wildlife Trust.
  - data: origin of chemical analyses data (OLD = Shore et al. 2003; NEW = Sainsbury et al. 2016).
  - year: carcass collection year (1990–2016).
  - time: time since first animal collection (in years).
  - survey: which analysis survey (ONE: 1990–1995; TWO: 1995–1998; THREE: 2013–2016).
  - season: season of carcass collection (Spring, Summer, Fall, Winter).
  - halfYear: division of year (FIRST: Dec–May; SECOND: Jun–Nov).
  - x, y: OSGB36 coordinates (eastings, northings) for collection locations.
  - region: North, South, East, West GB.
  - expansion: inside or outside the 1990s range.
  - sex: male or female (where known).
  - landClass: predominant land use at collection location, derived from CEH Land Cover map 2007 with a 1 km buffer; mainly arable vs pastoral.
  - hBrom, hDifm, hBrod: concentrations of bromadiolone, difenacoum, brodifacoum in liver (µg/g); LOD values from Shore et al. 2003 applied to NEW dataset (2018).
  - hBBrom, hBDifm, hBBrod: binary indicators of detection (0 = none detected; 1 = detected).
  - hBRods: number of different rodenticides detected (0, 1, 2, or 3).
  - hCRods: total number of rodenticide compounds detected (0, 1/2/3; 1 = one; 2 = two; 3 = three).
  - hConcT: total concentration of detected rodenticides (µg/g); LOD applied from Shore 2003 to 2018 dataset.
  - Notes: NA indicates missing data for the particular field.

- Data provenance, harmonisation, and methods
  - Combines legacy data (Shore et al. 2003) with newer data (Sainsbury et al. 2018) to enable long-term analyses.
  - LOD values from Shore et al. 2003 applied to the 2018 dataset to maintain comparability.
  - Spatial and land-cover harmonisation:
    - Coordinates stored in OSGB36.
    - Land cover classifications based on CEH Land Cover map 2007; 1 km buffers around carcass locations to assign predominant land class.
  - Analyses focus on liver residues to identify exposure to second-generation anticoagulant rodenticides.

- Temporal and spatial scope
  - Time frame: carcass collections from 1990 to 2016.
  - Geographic scope: Great Britain with regional categorisation (North, South, East, West).

- Relevance for monitoring and policy evaluation
  - Establishes an environmental health indicator: secondary exposure to anticoagulant rodenticides in polecats.
  - Enables assessment of:
    - Temporal trends (e.g., long-term increases in exposure).
    - Spatial patterns by region and land cover.
    - Variation by survey period and season.
    - Exposure intensity through concentrations, number of compounds, and detection status.
  - Supports decision-making on pesticide stewardship, wildlife protection, and monitoring program design.
  - Facilitates data-driven reporting through clear metadata, and potential for data governance by sharing underlying data (subject to restrictions).

- Data quality, governance, and practical considerations
  - Metadata gaps and NA values indicate incomplete data in some fields, consistent with observational monitoring datasets.
  - Challenges align with monitoring-framework archetype: data gaps, access constraints, and need for robust metadata, data harmonisation, and governance to ensure data quality, openness, and comparability.
  - Requires data cleaning, transformation, quality assurance, and careful handling of detection limits (LOD) and cross-study harmonisation.
  - Underlying data sharing may be constrained by policy or permissions, despite value for transparency and policy appraisal.

- References
  - Shore RF, Birks JDS, Afsar A, Wienburg CL, Kitchener AC (2003). Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats (Mustela putorius) from throughout their range in Britain, 1992-1999. Environmental Pollution, 122, 183-193.
  - Sainsbury KA, Shore RF, Schofield H, et al. (2018). Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain. Environmental Pollution, 236, 689-698.