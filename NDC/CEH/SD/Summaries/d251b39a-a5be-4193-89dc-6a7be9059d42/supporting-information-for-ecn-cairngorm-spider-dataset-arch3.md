# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2019 Andrews, C. and Dick, J. Sept. 2021

## Overview
- Provides supporting documentation for the ECN spider dataset, including site, habitats, sampling methods, and data structure.
- Data underpin a 2020 report on temporal trends in spider communities at the ECN Cairngorm field station.
- Data collected using standardized ECN protocols and identified by a single expert for consistency.

## Location and study design
- Site: Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (57°6'28"N, 3°50'6"W).
- Catchment details: ~10 km², elevation 320–1111 m a.s.l., includes part of Invereshie and Inchriach NNR.
- Habitats studied (sampling focused on west-facing slopes, 460–690 m a.s.l.): 
  - I. Woodland transect (mature Scots Pine with Vaccinium myrtillus)
  - II. Heath transect (wind-clipped dry heath)
  - III. Bog habitat (blanket mire with Eriophorum vaginatum and Molinia caerulea)

## Sampling protocol
- Transects: 100 m length with 10 pitfall traps placed 10 m apart.
- Trap design: polypropylene pots (75 mm × 105 mm) buried flush; filled with ethylene glycol to 30 mm; galvanized mesh top (~20 mm²) to deter small vertebrates; 140 mm rain cover; ~30 mm gap to ground.
- Frequency: fortnightly from ~April to end October (start date snow-dependent).
- Specimen handling: spiders collected per habitat, identified to species and sex by a single expert araneologist; all specimens stored at UKCEH Edinburgh.
- Data format: long-format CSV with Year, Date, Month, Week, Habitat, Transect, Transect age (Old for pre-2007; New for post-2007), Family, Species, Male, Female, Total.

## Data structure and units
- File format: long-format CSV.
- Key fields and meanings:
  - Year, Date, Month, Week: sampling timeline and timing.
  - Habitat: Bog, Heath, or Wood.
  - Transect, Transect age: transect identity and whether pre- or post-2007 relocation.
  - Family, Species: taxonomic details.
  - Male, Female, Total: counts by sex and total for each species.

## Quality control and comparability
- Transect relocation occurred in 2007; two-year overlap (2007–2008) to bridge old and new transects; data labelled accordingly to maintain clarity.
- Variable sampling periods annually due to weather or technical issues; typical sampling April–November on a two-weekly basis, not always achieved.
- Recommendation for standardising counts: use the time span between first and last trapping date rather than raw sampling effort; traps remain in place even when collection dates are missed, so trapping effort can still be quantified over the season.

## Usage and references
- Primary data usage documented in Andrews, C., Snazell, R., Dick, J. (2020): Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019: data analysis report.
- Further methodological details available in ECN protocols (Terrestrial I/IA) and related project materials.
- Data accessibility: dataset and associated reports are available via UKCEH/NORA repositories and linked references.