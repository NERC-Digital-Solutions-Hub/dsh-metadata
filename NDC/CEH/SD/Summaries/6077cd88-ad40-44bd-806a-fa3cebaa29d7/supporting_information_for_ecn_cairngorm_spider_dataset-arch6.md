# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2021 Andrews, C., Sanzell, R., Dick, J. Dec. 2022

## Overview
- This document provides supporting information for the ECN Cairngorm spider dataset (2004–2021).
- Spiders were collected using pitfall traps across three habitats within the Allt a'Mharcaidh catchment in the Cairngorms National Park, Scotland.
- All specimens were identified by a single expert araneologist to ensure consistency.
- A related methods and temporal trends report (Andrews et al., 2020) is available online, with protocols referenced here.

## Location and habitats
- Location: Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (57°6'28"N, 3°50'6"W).
- Elevation: 320–1111 m above sea level; area ~10 km²; includes part of Invereshie and Inchriach NNR.
- Transect focus: west-facing slopes north of the catchment (460–690 m a.s.l.).
- Habitats:
  - I. Woodland transect: mature Scots Pine woodland with Vaccinium myrtillus in the shrub layer (460 m a.s.l.).
  - II. Heath transect: wind-clipped Calluna-Cladonia dry heath with bare ground patches (690 m a.s.l.).
  - III. Bog habitat: blanket mire with Eriophorum vaginatum and Molinia caerulea (690 m a.s.l.).

## Sampling protocol
- Each habitat: a 100 m transect with 10 pitfall traps spaced 10 m apart.
- Pitfall trap details: polypropylene pots (75 mm × 105 mm) buried flush with ground, filled with ethylene glycol to 30 mm depth; galvanized wire mesh (~20 mm²) to exclude small fauna; rain cover (140 mm) with ~30 mm ground-gap.
- Sampling frequency: fortnightly from roughly April to end October; start date depends on snow-free conditions.
- Specimen handling: spiders from the duration of sampling aggregated into a single habitat sample; identified to species and sex (from 2006 onwards) by the same araneologist; stored at UKCEH Edinburgh for future research.

## Data structure and units
- Data format: long-format CSV with the following fields:
  - Year: sampling year (YYYY)
  - Date: collection date (DD/MM/YYYY)
  - Month: month name (MMM)
  - Week: week number (2-digit)
  - Habitat: Bog, Heath, or Wood
  - Transect: transect name (e.g., T1)
  - Transect_age: Old (pre-2007) or New (post-2007)
  - Family: taxonomic family (e.g., Linyphiidae)
  - Species: full species name (e.g., Hilaira frigida)
  - Male: count of male specimens (from 2006 onwards)
  - Female: count of female specimens (from 2006 onwards)
  - Total: total count (Male + Female)
  
## Quality Control and limitations
- Transect relocation occurred in 2007; use caution when compiling long-term trends across pre- and post-2007 data.
- Overlap period: 2007 and 2008 included both old and new transects to aid calibration.
- Data alongside variable sampling periods: standardize counts using the time between first and last trapping dates rather than raw sampling effort.
- Traps remained in place even when collection dates were missed; this allows calculation of trapping effort as time across the year.
- COVID-19 (2020): 01 May–31 July period was sampled monthly rather than fortnightly; overall between-year duration for analysis remained unaffected.

## References
- Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019: data analysis report. UK Centre for Ecology & Hydrology. http://nora.nerc.ac.uk/id/eprint/528208