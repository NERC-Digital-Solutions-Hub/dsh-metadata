Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Supplement to the 2018 Environmental Pollution study documenting long-term increases in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain.
- Provides a detailed dataset description to support monitoring, interpretation, and policy decisions about wildlife exposure to SGARs.

## Data content and structure
- Batch and sample identifiers for chemical analysis.
- Record identifiers linking each carcass to the database (Vincent Wildlife Trust) and to the collector (National Museums Scotland).
- Cause of death (CoD) and date components: month, year, season, halfYear.
- Spatial data: x (easting) and y (northing) coordinates using OSGB36, region (North/South/East/West).
- Land use context: landClas s derived from CEH Land Cover map (1 km buffers around carcass), with predominant classification between arable and pastoral.
- SGAR exposure indicators:
  - brom, difm, floc, brod, dife: concentrations of individual rodenticides in liver (µg/g).
  - bRods: whether one or more rodenticides detected.
  - bBrom, bDifm, bFloc, bBrod, bDife: detection flags for each compound.
  - cRods: number of rodenticides detected in the liver.
  - sumALL: total concentration of rodenticide compounds detected (µg/g).
- Biological and isotopic data:
  - meanN and sdN for δ15N in whiskers; meanC and sdC for δ13C.
  - dN15Max: maximum δ15N value across whisker segments for the animal.
  - age, sex, alive, fat: demographic and physiological descriptors where available; NA indicates missing data.
- Data quality notes:
  - NA entries indicate no data available for that individual.
  - Measurements and units are specified (e.g., µg/g for residues; Metres for coordinates; ‰ for isotopes).

## Data processing and metadata
- Carcass collection locations overlaid onto the CEH Land Cover map (2007); 1 km buffers applied.
- Predominant land class computed as the larger of arable or pastoral within the 1 km buffer.
- Location and context data prepared to enable spatial analyses of SGAR exposure.
- Units and data types explicitly described in the header explanations to support data interpretation and reuse.

## Data limitations and quality considerations
- Missing data (NA) for several fields, which may limit certain analyses.
- Metadata completeness and consistency are critical; the dataset includes explicit header explanations to aid verifiability.
- The data reflect exposure detected in liver residues at time of carcass collection and may not capture historical exposure dynamics for individuals.

## Implications for monitoring and policy
- Enables assessment of temporal and spatial trends in secondary SGAR exposure in polecats across Great Britain.
- Facilitates linkage between exposure data and environmental/contextual variables (region, land cover, SGAR usage pressure areas).
- Supports evidence-based decisions on rodenticide regulation, wildlife protection, and post-market monitoring strategies.
- Demonstrates an approach for integrating chemical, spatial, and isotopic data to monitor environmental health indicators in wildlife populations.

## Governance, data sharing, and framework considerations
- The dataset exemplifies the need for robust metadata, clear data provenance, and standardized measures to support monitoring frameworks.
- Highlights potential barriers to data sharing, including metadata completeness, data management standards, and open access of underlying data.
- Emphasizes the importance of publicly sharing underlying data where possible, along with transparent data governance to ensure datasets meet quality and reuse standards.

## References
- McDonald, R.A., Harris, S., Turnbull, G., Brown, P., Fletcher, M., 1998. Anticoagulant rodenticides in stoats (Mustela erminea) and weasels (Mustela nivalis) in England. Environmental Pollution 103, 17-23.