# UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2021

## Overview
- Supporting documentation for the ECN spider dataset collected 2004–2021 at the Cairngorm field station.
- Spiders were collected from pitfall traps across three habitats and identified by a single expert araneologist for consistency.
- The dataset has been used to analyse temporal trends in spider diversity (Andrews et al., 2020) and follows ECN standard protocols (IA Protocol).

## Location and Habitats
- Site: Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (57° 6' 28"N, 3° 50' 6"W).
- Elevation: 320–1111 m above sea level; area ~10 km²; includes part of Invereshie and Inchriach NNR.
- Transects (west-facing slopes, 460–690 m a.s.l.) across three habitats:
  - Woodland transect: mature Scots Pine woodland with Vaccinium myrtillus.
  - Heath transect: wind-clipped dry heath (Calluna-Cladonia) with bare ground patches.
  - Bog transect: blanket mire dominated by Eriophorum vaginatum and Molinia caerulea.

## Sampling Design and Protocol
- Each habitat: 100 m transect with 10 pitfall traps (75 mm × 105 mm) spaced 10 m apart.
- Traps buried flush with ground; filled with ethylene glycol to ~30 mm depth.
- Protective mesh (~20 mm) to prevent small vertebrate capture; rain covers to reduce washout; ~30 mm gap between cover and ground.
- Sampling frequency: fortnightly from about April to end October (weather/snow conditions may alter timing).
- Specimens from the full sampling period identified to species and sex (from 2006 onward) by the same araneologist.
- Specimens stored at UKCEH Edinburgh for future research.

## Data Structure and Variables
- Format: long-format CSV with fields including:
  - Year (YYYY), Date (DD/MM/YYYY), Month (MMM), Week (2-digit numeric)
  - Habitat (Bog, Heath, Wood), Transect (e.g., T1)
  - Transect_age (Old = pre-2007, New = post-2007)
  - Family, Species (e.g., Linyphiidae; Hilaira frigida)
  - Male, Female counts (from 2006), Total (Male + Female)
- Data organization supports aggregation by habitat, transect, species, and yearly trends.

## Quality Control and Considerations
- Transects were relocated in 2007; overlapping years (2007–2008) to ensure continuity, with clear labeling to distinguish old vs. new transects.
- Yearly sampling effort varies due to weather; standardization recommended using the interval between first and last trapping dates rather than counting sampling events.
- Pitfall traps remain in place despite incomplete sampling days; trapping duration remains informative for cross-year comparisons.
- 2020 Covid-19 period: sampling between 01 May and 31 July conducted monthly rather than fortnightly; overall duration for between-year analysis unaffected.

## References and Protocols
- Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019: data analysis report.
- ECN Protocols: IA (Interim Agreement) Protocols available at ECN website.

## Access and Utilisation Notes for Analysts
- Data stored at UKCEH Edinburgh; dataset underpinning regional spider diversity analyses and temporal trend assessments.
- Useful for cross-year standardisation exercises, habitat-based biodiversity monitoring, and evaluating environmental health over time.
- See Andrews et al. (2020) for methods details and temporal analyses; protocols available for methodological replication.