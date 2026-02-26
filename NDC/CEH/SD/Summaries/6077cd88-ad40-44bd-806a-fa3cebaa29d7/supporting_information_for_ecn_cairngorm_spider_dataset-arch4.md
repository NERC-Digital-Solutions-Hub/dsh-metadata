# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2021 Andrews, C., Sanzell, R., Dick, J. Dec. 2022

## Overview
- Provides supporting documentation for the ECN spider dataset collected 2004-2021.
- Spiders were collected from pitfall traps across three habitats in the Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland.
- Data collected using standard ECN protocols; all specimens identified by a single expert araneologist for consistency.
- Related methods and temporal trend analyses are described in Andrews et al. (2020); full protocols available via ECN links.

## Location and study design
- Study area: Allt a'Mharcaidh catchment (57° 6' 28"N, 3° 50' 6"W) in the Cairngorms National Park; elevation 320–1111 m a.s.l.; area ~10 km²; includes part of Invereshie and Inchriach NNR.
- Transects focused on west-facing slopes north of the catchment; sampling across three habitats between 460 m and 690 m a.s.l.
- Habitats:
  - I. Woodland transect: mature Scots Pine with Vaccinium myrtillus dominating understory (460 m.a.s.l.).
  - II. Heath transect: wind-clipped dry heath with patches of bare ground (690 m.a.s.l.).
  - III. Bog habitat: blanket mire dominated by Eriophorum vaginatum and Molinia caerulea (690 m.a.s.l.).

## Sampling protocol
- Each habitat: 100 m transect with 10 pitfall traps spaced 10 m apart.
- Trap specifications: polypropylene pot (75 mm × 105 mm), buried flush with ground, ~30 mm depth of ethylene glycol; galvanized wire mesh (~20 mm²) to exclude small vertebrates; 140 mm rain cover with ~30 mm ground gap.
- Sampling frequency: fortnightly from spring to autumn (approx. April–October); start date aligned with snow-free ground.
- Specimen processing: samples aggregated by habitat; all specimens identified to species and sex (from 2006 onwards) by the same expert araneologist; specimens stored at UKCEH Edinburgh for future research.

## Data structure and units
- Data format: long-format CSV with fields including:
  - Year (YYYY), Date (DD/MM/YYYY), Month (MMM), Week (two-digit numeric)
  - Habitat (Bog, Heath, Wood), Transect (e.g., T1), Transect_age (Old pre-2007, New post-2007)
  - Family, Species (e.g., Linyphiidae; Hilaira frigida)
  - Male, Female counts (from 2006 onwards), Total (male + female)
  
## Quality control and caveats
- Transects relocated in 2007; pre- and post-2007 data may not be directly comparable. Two years (2007–2008) included overlap where both old and new transects ran simultaneously to aid continuity.
- Data labelling clarifies which transect data belongs to which configuration.
- Annual sampling effort varies due to weather, snow, and technical factors; standardization for multi-year analyses should use the interval between first and last trapping dates rather than raw sampling effort.
- Covid-19 (2020) adjustments: 01 May–31 July sampling was monthly rather than fortnightly; overall duration remained suitable for year-to-year comparisons.

## Uses and references
- Reference dataset and methods discussed in Andrews, C., Snazell, R., Dick, J. (2020): Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019.
- Protocols and data accessibility linked through ECN resources and associated reports.