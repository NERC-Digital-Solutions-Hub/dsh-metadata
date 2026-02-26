# Supporting information for the dataset: UK Environmental Change Network (ECN Cairngorm Spider Data 2004-2019 Andrews, C. and Dick, J. Sept. 2021

- Overview
  - This document provides supporting information for the ECN Cairngorm spider dataset (2004–2019).
  - Spiders were collected using standard ECN protocols; all specimens were identified by a single expert for consistency.
  - A related data-analysis report (Andrews et al., 2020) detailing methods and temporal trends is available.

- Location and study habitats
  - Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (coordinates and elevation range provided).
  - Focused transects on west-facing slopes north of the catchment across three habitats:
    - I. Woodland transect (mature Scots Pine with Vaccinium myrtillus shrub layer)
    - II. Heath transect (wind-clipped Calluna-Cladonia dry heath)
    - III. Bog habitat (blanket mire with Eriophorum vaginatum and Molinia caerulea)
  - Transects sampled at elevations between ~460–690 m above sea level.

- Sampling protocol
  - Per habitat: 100 m transect with 10 pitfall traps spaced 10 m apart.
  - Trap design: polypropylene pots (75 mm × 105 mm) buried flush with ground; filled with ethylene glycol to 30 mm depth.
  - Preventive measures: galvanized mesh to deter small vertebrates; rain covers to reduce washout; ~30 mm gap between cover and ground.
  - Sampling frequency: fortnightly from ~April to end of October, start date weather-dependent.
  - Specimen handling: samples aggregated per habitat; all specimens identified to species and sex by the same araneologist; stored at UKCEH Edinburgh for future research.

- Data structure and units
  - Data provided in long-format CSV with fields:
    - Year (YYYY)
    - Date (DD/MM/YYYY)
    - Month (MMM)
    - Week (two-digit)
    - Habitat (Bog, Heath, Wood)
    - Transect (e.g., T1)
    - Transect age (Old before 2007, New after 2007)
    - Family (taxonomic family)
    - Species (full species name)
    - Male (count)
    - Female (count)
    - Total (male + female)

- Quality control and caveats
  - Transect relocation occurred in 2007; data across pre- and post-2007 periods may not be strictly comparable.
  - An overlap in 2007–2008 involved both old and new transects operating simultaneously to aid continuity.
  - Data are labeled to indicate transect origin (old vs. new).
  - Sampling periods vary due to snow, weather, or technical issues; standardisation of counts should use the time span from first to last trapping date rather than raw sampling effort.
  - Even if collection dates are missed, traps remained in place to preserve continuous trapping effort.

- References and access
  - Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019: data analysis report. UK Centre for Ecology & Hydrology.
  - Protocols referenced: ECN terrestrial measurements (I/IA). 
  - Related data availability: data and methods description available via the cited sources and ECN/NORA repositories.