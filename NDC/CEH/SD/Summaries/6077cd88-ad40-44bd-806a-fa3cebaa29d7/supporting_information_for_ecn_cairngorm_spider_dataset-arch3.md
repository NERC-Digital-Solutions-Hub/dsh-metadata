# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2021 Andrews, C., Sanzell, R., Dick, J. Dec. 2022

## Purpose and scope
- Provides supporting documentation for the ECN Cairngorm spider dataset (2004–2021).
- Documents sampling design, habitats, protocols, data structure, and quality controls to enable scrutiny, reuse, and interpretation for monitoring and policy-informed decision making.

## Location and study sites
- Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (57° 6' 28"N, 3° 50' 6"W).
- Elevation range 320–1111 m above sea level; ~10 km² area including part of Invereshie and Inchriach NNR.
- Focused transect sampling on west-facing slopes north of the catchment at 460–690 m a.s.l, across three habitats.

## Habitats studied
- Woodland transect: mature Scots Pine forest (Pinus sylvestris) with Vaccinium myrtillus in the shrub layer (at 460 m a.s.l.).
- Heath transect: wind-clipped dry heath (Calluna-Cladonia) with patches of bare ground (at 690 m a.s.l.).
- Bog habitat: blanket mire with Eriophorum vaginatum and Molinia caerulea (at 690 m a.s.l.).

## Sampling protocol
- Each habitat: 100 m transect with 10 pitfall traps spaced 10 m apart.
- Pitfall design: polypropylene pot buried flush with ground; ethylene glycol to 30 mm depth; 20 mm mesh to deter small vertebrates; 140 mm rain cover with ~30 mm gap to ground.
- Sampling frequency: fortnightly from approximately April to end October; start date depends on snow-free ground.
- Specimen processing: spiders identified to species and sex (from 2006 onwards) by a single expert araneologist for consistency; samples aggregated by habitat per collection period; specimens stored at UKCEH Edinburgh.
- Data are provided in long-format CSV; collected specimens include year, date, month, week, habitat, transect, transect_age (Old = pre-2007, New = post-2007), family, species, male/female counts, and total counts.

## Data structure and units
- Year, Date, Month, Week: temporal metadata with standard formats.
- Habitat: Bog, Heath, or Wood.
- Transect and Transect_age: location and pre/post-2007 status; two sets of transects were used post-2007 relocation.
- Taxonomic details: Family and Species.
- Counts: Male, Female, Total (per species per habitat/transect/year).

## Quality control and caveats
- Transect relocation after 2007; overlap years (2007–2008) to ensure continuity, with clear labeling of old vs. new transects.
- Year-to-year standardization should use the interval between first and last trapping dates rather than effort-based counts due to variable sampling days.
- Trapping effort is still informative since traps remained in place; even with missed collection dates, trap deployment duration can be used as a standardizing metric.
- 2020 Covid-19 adjustments: May–July sampling became monthly rather than fortnightly; overall duration for cross-year analysis remained unaffected.

## Usage for monitoring and policy
- Enables assessment of temporal trends in spider communities within a defined upland Cairngorms site.
- Supports analyses of habitat-specific responses and effects of transect relocation on long-term trends.
- Data can inform broader biodiversity monitoring, ecosystem health assessments, and policy decisions related to upland habitat management.

## References
- Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007–2019: data analysis report. UK Centre for Ecology & Hydrology; available at Nora/NEuri (URL: http://nora.nerc.ac.uk/id/eprint/528208).
- Protocols: ECN protocols (IA) available at https://ecn.ac.uk/sites/default/files/ECN/Protocols/IA.pdf.