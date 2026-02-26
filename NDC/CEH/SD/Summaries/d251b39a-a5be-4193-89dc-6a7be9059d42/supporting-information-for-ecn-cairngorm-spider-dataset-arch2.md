# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2019 Andrews, C. and Dick, J. Sept. 2021

## Overview
- Provides supporting documentation for the ECN Cairngorm spider dataset (2004–2019).
- Spiders collected from pitfall traps across three habitats in the Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland.
- All specimens identified by a single expert araneologist to ensure consistency.
- Related methods and temporal trends report available in Andrews et al. (2020).

## Location and Habitats
- Allt a'Mharcaidh catchment (57° 6' 28"N, 3° 50' 6"W), Cairngorms National Park.
- Elevation rises from 320 m to 1111 m a.s.l.; ~10 km2; includes part of Invereshie and Inchriach NNR.
- Sampling focused on west-facing slopes north of the catchment across three habitats:
  - I. Woodland transect at 460 m a.s.l. in mature Scots Pine with Vaccinium myrtillus dominating shrub layer.
  - II. Heath transect at 690 m a.s.l. in wind-clipped Calluna-Cladonia dry heath.
  - III. Bog habitat at 690 m a.s.l. in blanket mire with Eriophorum vaginatum and Molinia caerulea.

## Sampling Protocol
- In each habitat: 100 m transect with 10 pitfall traps spaced 10 m apart.
- Trap specs: polypropylene pot (75 mm × 105 mm), buried flush with ground, filled with ethylene glycol to 30 mm; topped with mesh (~20 mm2) to deter small vertebrates; rain cover 140 mm with ~30 mm gap to ground.
- Fortnightly sampling from around April to end October; start date depends on snow-free ground.
- Collected spiders aggregated into a single sample per habitat; specimens identified to species and sex by the same expert; stored at UKCEH Edinburgh.

## Data Structure and Units
- Data provided in long-format CSV with fields:
  - Year (YYYY), Date (DD/MM/YYYY), Month (MMM), Week (2-digit), Habitat (Bog/Heath/Wood), Transect (e.g., T1), Transect age (Old for pre-2007, New for post-2007), Family, Species, Male, Female, Total.
- Descriptions specify data types and formats for each field.

## Quality Control and Considerations
- Transects relocated from 2007 onward; note potential long-term comparability issues.
- Two years (2007–2008) of overlap where old and new transects operated concurrently to aid continuity.
- Variation in yearly sampling periods due to weather and snow; standardization recommended using the interval between first and last trapping dates rather than raw sampling effort.
- Even when collections are missed, traps remain in situ and can contribute to effort calculations.

## Data Use and References
- Data storage: specimens stored at UKCEH Edinburgh for future research.
- Key reference: Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019: data analysis report. UK Centre for Ecology & Hydrology.