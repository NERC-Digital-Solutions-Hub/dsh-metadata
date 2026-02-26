# Broad Habitat area estimates of change for Great Britain, summarized by ITE Land Class 1

- Overview
  - National estimates of Broad Habitat change (Habitats 1–17) for Great Britain between 1990, 1998, and 2007.
  - Calculated using the 2007 ITE Land Classification; estimates are summarized by Land Class.
  - Mapping methodology described in Maskell et al. 2008; Barr 1998; Barr 1990; with foundational classification references (Bunce et al. 1996, 2007; Scott 2007).
  - Data come from Countryside Survey (CS) 1990–2007 and are produced by NERC – Centre for Ecology & Hydrology (CEH).

- Data structure and key fields (CSV CS1990_98_07_Broad_Habitat_Change.csv)
  - YEAR_FROM: Survey start year
  - YEAR_TO: Survey end year
  - LAND_CLASS: ITE Land Class (Bunce et al. series)
  - BROAD_HABITAT: Broad Habitat code (1–17)
  - BROAD_HABITAT_NAME: Broad Habitat description (e.g., Broad Habitat 1 = Broadleaved, Mixed and Yew Woodland)
  - MEAN_CHANGE: Mean change in Broad Habitat area (000s ha) between the two years
  - LOWER_95PCT_LIMIT: Lower bound of 95% confidence interval for the change (000s ha)
  - UPPER_95PCT_LIMIT: Upper bound of 95% confidence interval for the change (000s ha)
  - SIG_5PCT: Significance at 5% level (Yes/No)

- Broad Habitat categories (codes and names)
  - 1 = Broadleaved, Mixed and Yew Woodland
  - 2 = Coniferous Woodland
  - 3 = Boundary and Linear Features
  - 4 = Arable and Horticulture
  - 5 = Improved Grassland
  - 6 = Neutral Grassland
  - 7 = Calcareous Grassland
  - 8 = Acid Grassland
  - 9 = Bracken
  - 10 = Dwarf Shrub Heath
  - 11 = Fen, Marsh, Swamp
  - 12 = Bog
  - 13 = Standing Open Waters and Canals
  - 14 = Rivers and Streams
  - 15 = Montane (1998–2007 only)
  - 16 = Inland Rock
  - 17 = Urban

- Data usage, attribution, and rights
  - All use of Countryside Survey data must be acknowledged.
  - Acknowledgement language:
    - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
    - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
  - Data are CS-derived; refer to Countryside Survey website and accompanying publications for full methodologies and maps.

- Methodology and references (context for analysts)
  - National estimates generated from the 1 km CS survey squares; methodology described in Scott 2007 (Statistical Report) and related CS technical reports.
  - Land Classification framework: ITE Land Classification of Great Britain 2007 (Bunce et al., 2007) with foundational Merlewood classifications (Bunce et al., 1996; 1981).
  - Mapping and classification method references:
    - Maskell et al., 2008 (CS Technical Report No. 1/07)
    - Barr et al. (1990s–2000s) Countryside Survey habitat mapping handbooks and field methods
    - Jackson, D.L. (2000) guidance on Biodiversity Habitat Classification
  - Additional sources for broader context and data usage are listed in the publication references and CS website.

- Practical notes for analysts
  - Outputs are suitable for time-series assessment of environmental health and policy performance at a national scale.
  - Data quality and uncertainty are explicit via 95% CIs and significance flag per habitat by land class.
  - Access and integration considerations: combine with other datasets to increase utility beyond single-use applications; ensure underlying CS data are accessible and properly licensed. Consider storing and sharing alongside related CS outputs in appropriate data portals with proper attribution.